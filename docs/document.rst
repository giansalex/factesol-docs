Archivos de Texto
=================

Ejemplos de archivos de texto para el envio comprobantes electronicos.

Factura
-------
Ejemplo de una factura con operaciones gravadas e inafectas.

**Cabecera**

========================================================== ================
                    Dato                                          Valor   
========================================================== ================
Identificador de Cabecera                                       CAB
Tipo de operación                                                     
Tipo de documento                                               01
Serie del documento                                             **F001**
Correlativo del documento                                       123
Fecha de emisión                                                2017-12-20
Tipo de documento de identidad del adquirente                   6
Número de documento de identidad del adquirente                 20480048359
Razón social del adquirente                                     EMPRESA SAC
Correo del adquiriente                                          admin@domain.pe
Tipo de moneda en la cual se emite la factura electrónica       PEN
Descuentos Globales
Sumatoria otros Cargos
Total descuentos
Total valor de venta - Operaciones gravadas                     50
Total valor de venta - Operaciones inafectas                    0
Total valor de venta - Operaciones exoneradas                   50
Total valor de venta - Operaciones gratuitas
Sumatoria IGV                                                   9
Sumatoria ISC
Sumatoria otros tributos
Importe total de la venta                                       109
Monto de la percepción
Monto total incluido la percepción
Código del tipo de Nota de Credito o Debito electrónica
Descripción de motivo o sustento
Tipo de documento del documento que modifica
Serie y número del documento que modifica
Tipo de documento relacionado
Número de documento relacionado
Tipo de documento guía
Número de documento de guía
Monto total anticipos
Anticipo - Tipo Documento Relacionado
Anticipo - Nro. Documento Relacionado
Anticipo - Monto Documento Relacionado
Anticipo - Emisor del Documento Relacionado
Gratuito
Tipo de Cambio
========================================================== ================

**Detalles**

===================================================== ================ ================
                    Dato                               DETALLE 1         DETALLE 2
===================================================== ================ ================
Identificador de Detalle                              DET               DET
Código de unidad de medida por ítem                   NIU               MTR
Cantidad de unidades por ítem                         5                 2
Código de producto                                    C0001             C0002
Codigo producto SUNAT
Descripción                                           PROD 1            PROD 2
Valor unitario por ítem                               10                25
Descuentos por item
Monto de IGV por ítem                                 1.8               0              
Afectación al IGV por ítem                            10                30
Monto de ISC por ítem
Tipo de sistema ISC
Precio de venta unitario por item                     10                25
Valor de venta por ítem                               50                50
Valor referencial unitario por ítem (gratuita)
===================================================== ================ ================

Contenido del archivo de texto.

.. code-block:: bash

    CAB||01|F001|123|2017-12-20|6|20480048359|EMPRESA SAC|admin@domain.pe|PEN|0|0|0|50|0|50||9|0|0|109|||||||||||||||||
    DET|NIU|5|C0001||PROD 1|10|0|1.8|10|||10|50||
    DET|MTR|4|C0002||PROD 2|25|0|0|30|||25|50||


Boleta
-------

Ejemplo de una Boleta con operaciones gravadas e inafectas.

**Cabecera**

========================================================== ================
                    Dato                                          Valor   
========================================================== ================
Identificador de Cabecera                                       CAB
Tipo de operación                                                     
Tipo de documento                                               03
Serie del documento                                             **B001**
Correlativo del documento                                       123
Fecha de emisión                                                2017-12-20
Tipo de documento de identidad del adquirente                   1
Número de documento de identidad del adquirente                 22334455
Razón social del adquirente                                     PERSONA F
Correo del adquiriente                                          user@gmail.com
Tipo de moneda en la cual se emite la factura electrónica       USD
Descuentos Globales
Sumatoria otros Cargos
Total descuentos
Total valor de venta - Operaciones gravadas                     50
Total valor de venta - Operaciones inafectas                    0
Total valor de venta - Operaciones exoneradas                   50
Total valor de venta - Operaciones gratuitas
Sumatoria IGV                                                   9
Sumatoria ISC
Sumatoria otros tributos
Importe total de la venta                                       109
Monto de la percepción
Monto total incluido la percepción
Código del tipo de Nota de Credito o Debito electrónica
Descripción de motivo o sustento
Tipo de documento del documento que modifica
Serie y número del documento que modifica
Tipo de documento relacionado
Número de documento relacionado
Tipo de documento guía
Número de documento de guía
Monto total anticipos
Anticipo - Tipo Documento Relacionado
Anticipo - Nro. Documento Relacionado
Anticipo - Monto Documento Relacionado
Anticipo - Emisor del Documento Relacionado
Gratuito
Tipo de Cambio                                                  3.26
========================================================== ================

**Detalles**

===================================================== ================ ================
                    Dato                               DETALLE 1         DETALLE 2
===================================================== ================ ================
Identificador de Detalle                              DET               DET
Código de unidad de medida por ítem                   NIU               ZZ
Cantidad de unidades por ítem                         5                 2
Código de producto                                    C0001             C0002
Codigo producto SUNAT
Descripción                                           PROD 1            PROD 2
Valor unitario por ítem                               10                25
Descuentos por item
Monto de IGV por ítem                                 1.8               0              
Afectación al IGV por ítem                            10                30
Monto de ISC por ítem
Tipo de sistema ISC
Precio de venta unitario por item                     10                25
Valor de venta por ítem                               50                50
Valor referencial unitario por ítem (gratuita)
===================================================== ================ ================

Contenido del archivo de texto.

.. code-block:: bash

    CAB||03|B001|123|2017-12-20|1|22334455|PERSONA F|user@gmail.com|USD|0|0|0|50|0|50||9|0|0|109|||||||||||||||||3.26
    DET|NIU|5|C0001||PROD 1|10|0|1.8|10|||10|50||
    DET|ZZ|4|C0002||PROD 2|25|0|0|30|||25|50||


Nota de Crédito
----------------

Ejemplo de una Nota de Crédito relacionada a una factura.

**Cabecera**

========================================================== ================
                    Dato                                          Valor   
========================================================== ================
Identificador de Cabecera                                       CAB
Tipo de operación                                                     
Tipo de documento                                               07
Serie del documento                                             **F001**
Correlativo del documento                                       111
Fecha de emisión                                                2017-12-20
Tipo de documento de identidad del adquirente                   6
Número de documento de identidad del adquirente                 20480048359
Razón social del adquirente                                     EMPRESA SAC
Correo del adquiriente                                          admin@domain.pe
Tipo de moneda en la cual se emite la factura electrónica       PEN
Descuentos Globales
Sumatoria otros Cargos
Total descuentos
Total valor de venta - Operaciones gravadas                     50
Total valor de venta - Operaciones inafectas                    0
Total valor de venta - Operaciones exoneradas                   50
Total valor de venta - Operaciones gratuitas
Sumatoria IGV                                                   9
Sumatoria ISC
Sumatoria otros tributos
Importe total de la venta                                       109
Monto de la percepción
Monto total incluido la percepción
Código del tipo de Nota de Credito o Debito electrónica         02
Descripción de motivo o sustento                                Error en Ruc
Tipo de documento del documento que modifica                    01
Serie y número del documento que modifica                       **F001-123**
Tipo de documento relacionado
Número de documento relacionado
Tipo de documento guía
Número de documento de guía
Monto total anticipos
Anticipo - Tipo Documento Relacionado
Anticipo - Nro. Documento Relacionado
Anticipo - Monto Documento Relacionado
Anticipo - Emisor del Documento Relacionado
Gratuito
Tipo de Cambio
========================================================== ================

**Detalles**

===================================================== ================ ================
                    Dato                               DETALLE 1         DETALLE 2
===================================================== ================ ================
Identificador de Detalle                              DET               DET
Código de unidad de medida por ítem                   NIU               MTR
Cantidad de unidades por ítem                         5                 2
Código de producto                                    C0001             C0002
Codigo producto SUNAT
Descripción                                           PROD 1            PROD 2
Valor unitario por ítem                               10                25
Descuentos por item
Monto de IGV por ítem                                 1.8               0              
Afectación al IGV por ítem                            10                30
Monto de ISC por ítem
Tipo de sistema ISC
Precio de venta unitario por item                     10                25
Valor de venta por ítem                               50                50
Valor referencial unitario por ítem (gratuita)
===================================================== ================ ================

Contenido del archivo de texto.

.. code-block:: bash

    CAB||07|F001|111|2017-12-20|6|20480048359|EMPRESA SAC|admin@domain.pe|PEN|0|0|0|50|0|50||9|0|0|109|||02|ERROR EN RUC|01|F001-123|||||||||||
    DET|NIU|5|C0001||PROD 1|10|0|1.8|10|||10|50||
    DET|MTR|4|C0002||PROD 2|25|0|0|30|||25|50||


Nota de Débito
---------------

Ejemplo de una Nota de Débito relacionada a una factura.

**Cabecera**

========================================================== ================
                    Dato                                          Valor   
========================================================== ================
Identificador de Cabecera                                       CAB
Tipo de operación                                                     
Tipo de documento                                               08
Serie del documento                                             **F001**
Correlativo del documento                                       122
Fecha de emisión                                                2017-12-20
Tipo de documento de identidad del adquirente                   6
Número de documento de identidad del adquirente                 20480048359
Razón social del adquirente                                     EMPRESA SAC
Correo del adquiriente                                          admin@domain.pe
Tipo de moneda en la cual se emite la factura electrónica       PEN
Descuentos Globales
Sumatoria otros Cargos
Total descuentos
Total valor de venta - Operaciones gravadas                     50
Total valor de venta - Operaciones inafectas                    0
Total valor de venta - Operaciones exoneradas                   50
Total valor de venta - Operaciones gratuitas
Sumatoria IGV                                                   9
Sumatoria ISC
Sumatoria otros tributos
Importe total de la venta                                       109
Monto de la percepción
Monto total incluido la percepción
Código del tipo de Nota de Credito o Debito electrónica         01
Descripción de motivo o sustento                                Intereses
Tipo de documento del documento que modifica                    01
Serie y número del documento que modifica                       **F001-123**
Tipo de documento relacionado
Número de documento relacionado
Tipo de documento guía
Número de documento de guía
Monto total anticipos
Anticipo - Tipo Documento Relacionado
Anticipo - Nro. Documento Relacionado
Anticipo - Monto Documento Relacionado
Anticipo - Emisor del Documento Relacionado
Gratuito
Tipo de Cambio
========================================================== ================

**Detalles**

===================================================== ================ ================
                    Dato                               DETALLE 1         DETALLE 2
===================================================== ================ ================
Identificador de Detalle                              DET               DET
Código de unidad de medida por ítem                   NIU               MTR
Cantidad de unidades por ítem                         5                 2
Código de producto                                    C0001             C0002
Codigo producto SUNAT
Descripción                                           PROD 1            PROD 2
Valor unitario por ítem                               10                25
Descuentos por item
Monto de IGV por ítem                                 1.8               0              
Afectación al IGV por ítem                            10                30
Monto de ISC por ítem
Tipo de sistema ISC
Precio de venta unitario por item                     10                25
Valor de venta por ítem                               50                50
Valor referencial unitario por ítem (gratuita)
===================================================== ================ ================

Contenido del archivo de texto.

.. code-block:: bash

    CAB||07|F001|122|2017-12-20|6|20480048359|EMPRESA SAC|admin@domain.pe|PEN|0|0|0|50|0|50||9|0|0|109|||01|Intereses|01|F001-123|||||||||||
    DET|NIU|5|C0001||PROD 1|10|0|1.8|10|||10|50||
    DET|MTR|4|C0002||PROD 2|25|0|0|30|||25|50||