Ejemplos
========
Se proveen algunos ejemplos para el envio de comprobantes al API.

.. note:: Para ejecuar los siguiente ejemplos necesita crear un token, vaya a la sección :doc:`tutorial` 

C#
---
Usar los espacios de nombres.

.. code-block:: csharp

    using System;
    using System.Net;

Emplear el siguiente codigo para el envio.

.. code-block:: csharp
    :emphasize-lines: 18

    var token = "UN-TOKEN-VALIDO";
    var txt = "CAB||01|F001|433|2017-12-01|6|20480048359...";

    var http = (HttpWebRequest)WebRequest.Create("https://factesol.net.pe/api/v1/doc/ventas");
    http.Method = "POST";
    http.ContentType = "application/json";
    http.Headers.Add("Authorization", "Bearer " + token);
    var content = Encoding.UTF8.GetBytes(txt);
    http.ContentLength = content.Length;
    using (var wr = http.GetRequestStream())
    {
        wr.Write(content, 0, content.Length);
    }

    var resp = (HttpWebResponse)http.GetResponse();
    if (resp.StatusCode == HttpStatusCode.OK)
    {
        Console.WriteLine("Enviado a Factesol");
    }

Java
-----

Realizar los siguientes import.

.. code-block:: java

    import java.io.IOException;
    import java.io.OutputStream;
    import java.net.HttpURLConnection;
    import java.net.URL;

Emplear el siguiente codigo para el envio.

.. code-block:: java
    :emphasize-lines: 17

    String endpoint = "https://factesol.net.pe/api/v1/doc/ventas";
    String token = "UN-TOKEN-VALIDO";
    String txtContent = "CAB||01|F001|433|2017-12-01|6|20480048359...";

    URL url = new URL(endpoint);
    HttpURLConnection conn = (HttpURLConnection) url.openConnection();
    conn.setDoOutput(true);
    conn.setRequestProperty("Authorization", "Bearer " + token);
    conn.setRequestMethod("POST");
    conn.setRequestProperty("Content-Type", "text/plain");

    OutputStream os = conn.getOutputStream();
    os.write(txtContent.getBytes());
    os.flush();

    if (conn.getResponseCode() == HttpURLConnection.HTTP_OK) {
        System.out.println("Success");
    }

    conn.disconnect();

PHP
-----
Para el siguiente ejemplo necesita tener activada la extension Curl.

.. code-block:: php
    :emphasize-lines: 22

    <?php

    $token = "UN-TOKEN-VALIDO";
    $txt = "CAB||01|F001|433|2017-12-01|6|20480048359...";

    $header = array();
    $header[] = 'Content-type: text/plain';
    $header[] = 'Authorization: Bearer ' . $token;

    $ch = curl_init();

    curl_setopt($ch, CURLOPT_URL, "https://factesol.net.pe/api/v1/doc/ventas");
    curl_setopt($ch, CURLOPT_POST, 1);
    curl_setopt($ch, CURLOPT_RETURNTRANSFER, 1 );
    curl_setopt($ch, CURLOPT_POSTFIELDS, $txt);
    curl_setopt($ch, CURLOPT_HTTPHEADER, $header); 

    $result = curl_exec ($ch);

    curl_close ($ch);

    var_dump($result);
    
Visual FoxPro
-----

.. code-block:: vb
    :emphasize-lines: 10

    token = "UN-TOKEN-VALIDO"
    txt = "CAB||01|F001|433|2017-12-01|6|20480048359..."
    //o También 
    //* txt = FILETOSTR(Ruta_de_archivo)

    oHTTP =  Createobject('MsXml2.XmlHttp');
    oHTTP.OPEN("POST", pURL_WSDL, .F.):
    oHTTP.setRequestHeader("Content-Type", "text/plain")
    oHTTP.setRequestHeader("Authorization", "Bearer " + ctoken)
    oHTTP.SEND( ALLTRIM(txt) )
    
    Do While oHTTP.ReadyState <> 4
       Doevents Force
    Enddo     

    RespuestaWS = oHTTP.responseText
    RespuestaEstado = oHTTP.status
 
