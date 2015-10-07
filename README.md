# ipacoop
Alfresco 5.0.d Customization


#Firma Digital

##1) Crear paquetes: mvn clean package -DskipTests
##2) Instalar archivos AMPS http://docs.alfresco.com/5.0/tasks/dev-extensions-tutorials-simple-module-install-amp.html
##3) Crear archivo .p12
	###3.1) Generar llave y certificado
			openssl req -x509 -nodes -sha1 -days 365 -config /etc/ssl/openssl.cnf  -newkey rsa:2048 -keyout NAME.key -out NAME.crt
	###3.2) Generar p12
			openssl pkcs12 -export -in CRTFILENAME.crt -inkey KEYFILENAME.key -name "ALIAS_NAME" -out  NAME.p12
	###3.3) Instalar archivo p12 en el almacen de llaves del SO o Navegador