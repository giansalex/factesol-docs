Endpoints
=========
Estas son las url a las que se debe enviar los archivos de texto.

Ventas
------
Incluye Facturas, Boletas, Notas de Crédito y Notas de Débito.

https://factesol.net.pe/api/v1/doc/ventas

Bajas
------
Comunicaciones de Bajas de las ventas emitidas.


https://factesol.net.pe/api/v1/doc/bajas

Retención
---------
Comprobante de Retenciones.


https://factesol.net.pe/api/v1/doc/retenciones

Percepción
----------
Comprobante de Percepciones.


https://factesol.net.pe/api/v1/doc/percepciones

Reversión
---------
Resumen de Reversiones.

https://factesol.net.pe/api/v1/doc/reversiones

.. http:post::  /api/reversion/status

    Retorna el estado del resumen asociado al id despues de haber sido enviado a Sunat.

    **Example request**:

    .. sourcecode:: js

        {
            "Ruc": "20123456789",
            "TipoDocumento": "20",
            "Serie": "R001",
            "Correlativo": "123"
        }

    :jsonparam string Ruc: Ruc del emisor del comprobante.
    :jsonparam string TipoDocumento: Tipo documento (20 - Retencion, 40 - Percepcion).
    :jsonparam string Serie: Serie del comprobante.
    :jsonparam string Correlativo: Correlativo del comprobante.

    **Example response**:

    .. sourcecode:: js

        {
            "Success": true,
            "Code": "03",
            "Description": "El Resumen de Reversion XXXX ha sido aceptado"
        }


Resumen Diario
--------------

.. http:post::  /api/resumen/create/(date:fecha)

    Crea el resumen para la fecha indicada.

    **Example request**:

    .. prompt:: bash $

        /api/resumen/create/2019-05-17

    **Example response**:

    Retorna un array de los identificadores de los resumenes creado para la fecha indicada.


    .. sourcecode:: js

        [ 12, 13]

    :statuscode 200: no error
    :statuscode 404: No hay comprobantes para esa fecha


.. http:post::  /api/resumen/send/(int: id)

    Envia el resumen asociado al id (retornado al crear el resumen).

    **Example request**:

    .. prompt:: bash $

        /api/resumen/send/12

    **Example response**:

    .. sourcecode:: js

        {
            "Success": true,
            "Code": "06",
            "Description": "Enviado a Sunat por procesar"
        }

    :statuscode 200: no error
    :statuscode 404: No se encontro el resumen

.. http:post::  /api/resumen/status/(int: id)

    Retorna el estado del resumen asociado al id despues de haber sido enviado a Sunat.

    **Example request**:

    .. prompt:: bash $

        /api/resumen/status/12

    **Example response**:

    .. sourcecode:: js

        {
            "Success": true,
            "Code": "03",
            "Description": "El Resumen diario XXXX ha sido aceptado"
        }

    :statuscode 200: no error
    :statuscode 404: No se encontro el resumen