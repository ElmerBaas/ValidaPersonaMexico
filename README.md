# ValidaPersonaMexico

2018-08-21 v0.1
-Cuenta con un método para validar los curp's
http://187.160.251.219/ws/index.php?wsdl

Ejemplo de petición:

Cabecera:
POST http://187.160.251.219/ws/index.php HTTP/1.1
Accept-Encoding: gzip,deflate
Content-Type: text/xml;charset=UTF-8
SOAPAction: "urn:ValidateMexico#Curp"
Content-Length: 631
Host: 187.160.251.219
Connection: Keep-Alive
User-Agent: Apache-HttpClient/4.1.1 (java 1.5)

Cuerpo:
<soapenv:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:urn="urn:ValidateMexico">
   <soapenv:Header/>
   <soapenv:Body>
      <urn:Curp soapenv:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/">
         <return xsi:type="urn:CurpReq">
            <user xsi:type="xsd:string">prueba</user>
            <password xsi:type="xsd:string">sC}9pW1Q]c</password>
            <Curp xsi:type="xsd:string">LOOA531113HTCPBN07</Curp>
         </return>
      </urn:Curp>
   </soapenv:Body>
</soapenv:Envelope>

Ejemplo de respuesta:

Cabecera:
HTTP/1.1 200 OK
Date: Tue, 21 Aug 2018 14:31:47 GMT
Content-Type: text/xml; charset=UTF-8
Content-Length: 555
Connection: keep-alive
X-Powered-By: PHP/5.6.19
Server: DVI-SERVER Server v0.0.1
X-SOAP-Server: DVI-SERVER/0.0.1 (1.0)
Content-Encoding: gzip

Cuerpo:
<SOAP-ENV:Envelope SOAP-ENV:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/" xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:SOAP-ENC="http://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="urn:ValidateMexico">
   <SOAP-ENV:Body>
      <ns1:CurpResponse xmlns:ns1="urn:ValidateMexico">
         <return xsi:type="tns:CurpRes">
            <Response xsi:type="xsd:string">correct</Response>
            <Curp xsi:type="xsd:string">LOOA531113HTCPBN07</Curp>
            <Paterno xsi:type="xsd:string">LOPEZ</Paterno>
            <Materno xsi:type="xsd:string">OBRADOR</Materno>
            <Nombre xsi:type="xsd:string">ANDRES MANUEL</Nombre>
            <Sexo xsi:type="xsd:string">H</Sexo>
            <FechaNacimiento xsi:type="xsd:string">1953-11-13</FechaNacimiento>
            <Nacionalidad xsi:type="xsd:string">MEX</Nacionalidad>
            <DocProbatorio xsi:type="xsd:string">1</DocProbatorio>
            <AnioReg xsi:type="xsd:string">1953</AnioReg>
            <Foja xsi:type="xsd:string"/>
            <Tomo xsi:type="xsd:string"/>
            <Libro xsi:type="xsd:string">0011</Libro>
            <NumActa xsi:type="xsd:string">01642</NumActa>
            <NumEntidadReg xsi:type="xsd:string">27</NumEntidadReg>
            <CRIP xsi:type="xsd:string"/>
            <CveMunicipioReg xsi:type="xsd:string">012</CveMunicipioReg>
            <NumRegExtranjeros xsi:type="xsd:string"/>
            <FolioCarta xsi:type="xsd:string"/>
            <CveEntidadEmisora xsi:type="xsd:string">04001</CveEntidadEmisora>
         </return>
      </ns1:CurpResponse>
   </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
