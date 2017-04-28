FROM beli/ldap
LABEL org.freenas.interactive="false"                     \
      org.freenas.version="0.0.1"                         \
      org.freenas.upgradeable="false"                     \
	  org.freenas.command="" 							  \
      org.freenas.expose-ports-at-host="true"             \
      org.freenas.autostart="false"                       \
      org.freenas.port-mappings="389:389/tcp"             \
	  org.freenas.settings="[ 							  \
		{                                                 \
			\"name\": \"CONF_ROOTPW\",                    \
			\"desc\": \"admin password\"                  \
		},                                                \
		{                                                 \
			\"name\": \"CONF_BASEDN\",                    \
			\"desc\": \"base of the tree to be served\"   \
		},                                                \
	  ]"                                                  \
      org.freenas.volumes="[                              \
          {                                               \
              \"name\": \"/data\",                        \
              \"descr\": \"Data storage\"                 \
          },                                              \
          {                                               \
              \"name\": \"/config\",                      \
              \"descr\": \"Config storage\"               \
          }                                               \
      ]"


