---
title: Mappage de métadonnées
description: Le contenu d’un document de métadonnées est mappé à l’API de métadonnées de la manière décrite dans les sections suivantes.
ms.assetid: 266f8319-b7ac-497f-8eb7-8e2c7bcede33
keywords:
- Services Web de mappage de métadonnées pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb9da067768569e78ba6bb98ee219e11917d3201
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "106512534"
---
# <a name="metadata-mapping"></a>Mappage de métadonnées

Le contenu d’un document de métadonnées est mappé à l’API de métadonnées de la manière décrite dans les sections suivantes.


Les préfixes d’espaces de noms suivants sont utilisés dans cette documentation :

``` syntax
wsdl   => http://schemas.xmlsoap.org/wsdl/
soap11 => http://schemas.xmlsoap.org/wsdl/soap/
soap12 => http://schemas.xmlsoap.org/wsdl/soap12/
wsa09  => http://schemas.xmlsoap.org/ws/2004/08/addressing
wsa10  => http://www.w3.org/2005/08/addressing
wsa09p => http://schemas.xmlsoap.org/ws/2004/08/addressing/policy
wsa10p => http://www.w3.org/2006/05/addressing/wsdl
binp   => http://schemas.microsoft.com/ws/06/2004/mspolicy/netbinary1
mtomp  => http://schemas.xmlsoap.org/ws/2004/09/policy/optimizedmimeserialization
sp     => http://schemas.xmlsoap.org/ws/2005/07/securitypolicy
wsp    => http://schemas.xmlsoap.org/ws/2004/09/policy
netf   => http://schemas.microsoft.com/ws/2006/05/framing/policy
httpp  => http://schemas.microsoft.com/ws/06/2004/policy/http
wst10  => http://schemas.xmlsoap.org/ws/2005/02/trust
wsi    => http://schemas.xmlsoap.org/ws/2005/05/identity
```

Les sections suivantes décrivent les constructions d’API, ainsi que les constructions de métadonnées (WSDL ou stratégie) auxquelles elles correspondent.

Vous pouvez vous familiariser avec les spécifications de métadonnées telles que WSDL et la stratégie pour comprendre cette section.

## <a name="endpoint-address"></a>Adresse du point de terminaison

L’adresse d’un point de terminaison (voir [**\_ \_ adresse du point de terminaison WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)) est obtenue à partir d’un élément d’extensibilité dans l’élément wsdl : port du document WSDL. Les éléments d’extensibilité suivants sont pris en charge pour spécifier l’adresse :

``` syntax
<wsdl:port...>
    <soap11:address.../>
</wsdl:port>
```

``` syntax
<wsdl:port...>
    <soap12:address.../>
</wsdl:port>
```

``` syntax
<wsdl:port...>
    <wsa09:EndpointReference.../>
</wsdl:port>
```

``` syntax
<wsdl:port...>
    <wsa10:EndpointReference.../>
</wsdl:port>
```

## <a name="ws_channel_binding"></a>\_liaison WS Channel \_

La liaison de canal ( [**voir \_ \_ liaison WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)) est déterminée par le transport que la liaison SOAP utilise, comme suit :

``` syntax
<soap:binding transport=&quot;http://schemas.microsoft.com/soap/tcp&quot;/> => WS_TCP_CHANNEL_BINDING
```

``` syntax
<soap:binding transport=&quot;http://schemas.xmlsoap.org/soap/http&quot;/> => WS_HTTP_CHANNEL_BINDING
```

## <a name="ws_channel_property_envelope_version"></a>VERSION de l’enveloppe de la \_ propriété du canal WS \_ \_ \_

La version d’enveloppe ( [**voir \_ \_ version d' \_ enveloppe \_ de la propriété WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) est déterminée par la liaison SOAP utilisée, comme suit :

``` syntax
<wsdl:binding...>
    <soap11:binding.../> => WS_ENVELOPE_VERSION_SOAP_1_1
</wsdl:binding>
```

``` syntax
<wsdl:binding...>
    <soap12:binding.../> => WS_ENVELOPE_VERSION_SOAP_1_2
</wsdl:binding>
```

## <a name="addressing-version"></a>Version d’adressage

La version d’adressage ( [**voir \_ \_ version d' \_ adressage \_ de la propriété WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) est déterminée par les assertions suivantes dans la stratégie de point de terminaison :

``` syntax
<wsp:Policy...>
    <wsa09p:UsingAddressing.../> => WS_ADDRESSING_VERSION_0_9
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <wsa10p:UsingAddressing.../> => WS_ADDRESSING_VERSION_1_0
</wsp:Policy>
```

Si une assertion d’adressage n’est pas présente, le transport de la [**\_ \_ version \_ WS Addressing**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) est pris par défaut.

## <a name="message-encoding"></a>Encodage de message

L’encodage du message (voir [**\_ \_ \_ encodage de la propriété WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) est déterminé par les assertions suivantes dans la stratégie de point de terminaison :

``` syntax
<wsp:Policy...>
    <binp:BinaryEncoding.../> => WS_ENCODING_XML_BINARY_SESSION_1, WS_ENCODING_XML_BINARY_1
</wsp:Policy>
```

Notez que l’assertion de stratégie d’encodage binaire n’inclut pas d’informations indiquant si l’encodage binaire est une session ou sans session. Cela est déterminé par la contrainte de propriété Encoding (qui doit être appropriée selon que le type de [**\_ canal WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) utilisé ou non est de type session ou non).

``` syntax
<wsp:Policy...>
    <mtomp:OptimizedMimeSerialization.../> => WS_ENCODING_XML_MTOM_UTF8, WS_ENCODING_XML_MTOM_UTF16LE, WS_ENCODING_XML_MTOM_UTF16BE
</wsp:Policy>
```

Si aucune des assertions ci-dessus n’est présente, un encodage de texte est utilisé : [**WS \_ Encoding \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding), **WS \_ encodage \_ XML \_ utf16le**, **WS \_ Encoding \_ XML \_ utf16be**.

Notez que la stratégie n’inclut pas d’informations sur le jeu de caractères pour les encodages MTOM ou texte (qu’il s’agisse de UTF8, UTF16LE ou UTF16BE). La valeur réelle du jeu de caractères utilisée est déterminée par la contrainte de propriété Encoding.

## <a name="constraints-with-http-header-authentication"></a>Contraintes avec l’authentification d’en-tête HTTP

Cette section s’applique lorsque la contrainte de liaison de sécurité de la contrainte de liaison de sécurité d' [**\_ \_ en-tête \_ \_ \_ \_ http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint) est spécifiée.

Cette liaison de sécurité est indiquée dans la stratégie par des assertions différentes qui déclarent que l’authentification d’en-tête HTTP doit être utilisée et qu’un schéma d’authentification particulier doit être utilisé. Les assertions de stratégie correspondent aux valeurs du [**schéma d’authentification de l' \_ \_ \_ \_ \_ en \_ \_ -tête http de la propriété de liaison WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) , comme suit :

``` syntax
<wsp:Policy...>
    <httpp:BasicAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_BASIC
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <httpp:NegotiateAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_NEGOTIATE
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <httpp:NtlmAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_NTLM
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <httpp:DigestAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_DIGEST
</wsp:Policy>
```

## <a name="constraints-with-sll-transport-security"></a>Contraintes avec sécurité de transport SSL

Cette section s’applique lorsque la contrainte de liaison de sécurité de la contrainte de sécurité de [**\_ \_ transport \_ \_ \_ WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint) est spécifiée. Les assertions de stratégie suivantes sont utilisées dans ce cas :

``` syntax
<wsp:Policy...>
    <sp:TransportBinding...>
        <wsp:Policy...>
            <sp:TransportToken...>
                <wsp:Policy...>
                    <sp:HttpsToken.../>
            </wsp:Policy...>
        </wsp:Policy>
    </sp:TransportBinding...>
</wsp:Policy>
```

## <a name="constraints-with-sspi-transport-security"></a>Contraintes avec sécurité de transport SSPI

Cette section s’applique lorsque la contrainte de liaison de sécurité de la contrainte de sécurité de [**\_ transport WS TCP \_ SSPI \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint) est spécifiée. Les assertions de stratégie suivantes sont utilisées dans ce cas :

``` syntax
<wsp:Policy...>
    <sp:TransportBinding...>
        <wsp:Policy...>
            <sp:TransportToken...>
                <wsp:Policy...>
                    <netf:WindowsTransportSecurity.../>
            </wsp:Policy...>
        </wsp:Policy>
    </sp:TransportBinding...>
</wsp:Policy>
```

## <a name="constrains-with-transport-security"></a>Contractions avec la sécurité de transport

La contrainte de propriété du niveau de protection du transport de la [**\_ \_ propriété \_ \_ \_ WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) peut être spécifiée si l’une des contraintes de liaison de sécurité est spécifiée :

-   [**\_contrainte de \_ liaison de sécurité de transport WS SSL \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)

    La valeur de la stratégie est [**toujours \_ \_ connexion au niveau de protection WS \_ \_ et \_ chiffrement**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).

-   [**contrainte de liaison de sécurité de transport de WS \_ TCP \_ SSPI \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)

    La valeur de la stratégie est spécifiée dans le cadre de l’assertion WindowsTransportSecurity, comme suit :

    ``` syntax
    <netf:WindowsTransportSecurity...>None</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_NONE
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>Sign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>EncryptAndSign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN_AND_ENCRYPT
    ```

-   [**\_contrainte de \_ \_ liaison de \_ sécurité \_ d’en-tête \_ WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)

    La valeur de la stratégie est toujours le [**\_ niveau de protection WS \_ \_ None**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).

## <a name="constraints-with-kerberos-apreq-security-binding"></a>Contraintes avec la liaison de sécurité Kerberos APREQ

Cette section s’applique lorsque la contrainte de liaison de sécurité de la contrainte de sécurité de [**\_ message WS Kerberos \_ APREQ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint) est spécifiée. Les assertions de stratégie suivantes sont utilisées dans ce cas :

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:KerberosToken>
            <WssGssKerberosV5ApReqToken11.../>
        </sp:KerberosToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="constraints-with-message-security-binding"></a>Contraintes avec liaison de sécurité de message

Cette section s’applique lorsque la contrainte de liaison de sécurité de la contrainte de liaison de sécurité de [**\_ \_ message \_ \_ \_ WS username**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint) est spécifiée. Les assertions de stratégie suivantes sont utilisées dans ce cas :

``` syntax
<sp:SignedSupportingTokens>
    <wsp:Policy>
        <sp:UsernameToken.../>
    </wsp:Policy>
</sp:SignedSupportingTokens>
```

## <a name="ws_cert_message_security_binding_constraint"></a>\_contrainte de \_ liaison de sécurité de message WS CERT \_ \_ \_

Cette section s’applique lorsque la contrainte de liaison de sécurité de la contrainte de liaison de sécurité de [**\_ message du certificat \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint) est spécifiée. Les assertions de stratégie suivantes sont utilisées dans ce cas :

``` syntax
<sp:EndorsingSupportingTokens>
    <wsp:Policy>
        <sp:X509Token.../>
   </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="ws_issued_token_message_security_binding_constraint"></a>\_contrainte de \_ \_ liaison de sécurité de message de jeton \_ WS \_ émis \_

Cette section s’applique lorsque la contrainte de liaison de sécurité de la contrainte de liaison de sécurité de [**\_ message de \_ jeton \_ \_ \_ \_ WS émis**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) est spécifiée. Les assertions de stratégie suivantes sont utilisées dans ce cas :

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:IssuedToken sp:IncludeToken=&quot;xs:anyURI&quot;? ...=&quot;&quot; >
            <wsp:Issuer>...</wsp:Issuer>?
            <wsp:RequestSecurityTokenTemplate TrustVersion='xs:anyURI&quot;?>
                ...
                <wst10:Claims>
                    <wsi:ClaimType Optional='xs:boolean'?>xs:anyURI<wt:ClaimType>*
                </wst10:Claims>
                ...
            </wsp:RequestSecurityTokenTemplate>
            <wsp:Policy>
                <sp:RequireDerivedKeys/> ?
                <sp:RequireExternalReference/> ?
                <sp:RequireInternalReference/> ?
            </wsp:Policy> ?
        </sp:IssuedToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

Les éléments suivants décrivent le mappage des champs de la contrainte de liaison de [**sécurité de message de \_ \_ jeton \_ \_ \_ \_ WS émis**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) à la stratégie ci-dessus :

-   Le champ claimConstraints permet de vérifier l’ensemble des URI de type de revendication qui apparaissent dans l’élément WSI : ClaimType ci-dessus.

-   Le champ issuerAddress correspond à l’élément d’émetteur wsp : ci-dessus, qui est l' [**\_ \_ adresse du point de terminaison WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) du service qui peut émettre le jeton.

-   Le champ requestSecurityTokenTemplate correspond aux éléments enfants de l’élément wsp : RequestSecurityTokenTemplate.

## <a name="ws_security_context_message_security_binding_constraint"></a>\_contrainte de \_ \_ liaison de sécurité de message de contexte \_ de \_ sécurité WS \_

Cette section s’applique lorsque la contrainte de liaison de sécurité de la contrainte de sécurité de [**\_ message du contexte de sécurité \_ \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) est spécifiée. Les assertions de stratégie suivantes sont utilisées dans ce cas :

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:SecureConversationToken sp:IncludeToken=&quot;xs:anyURI&quot;? ...=&quot;&quot; >
            <wsp:Issuer>...</wsp:Issuer>?
            <wsp:Policy>
                <sp:RequireDerivedKeys.../>?
                <sp:RequireExternalUriReference.../>?
                <sp:SC10SecurityContextToken.../>? => WS_SECURE_CONVERSATION_VERSION_FEBRUARY_2005
                <sp:BootstrapPolicy... >?
                   <wsp:Policy> ...  </wsp:Policy> => WS_SECURITY_CONSTRAINTS
                </sp:BootstrapPolicy>
            </wsp:Policy>
        </wsp:SecureConversationToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

Le mode d’entropie est déterminé par l’assertion <SP : Trust10>. <SP : RequireClientEntropy/> et <SP : RequireServerEntropy/> => [**\_ mode d' \_ entropie de clé de sécurité WS \_ \_ \_ combiné**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode) <SP : RequireClientEntropy/> => mode d’entropie de **clé de \_ sécurité WS \_ \_ \_ \_ client \_ uniquement** <SP : RequireServerEntropy/> => **\_ \_ \_ \_ serveur en mode entropie \_ \_ de clé de sécurité WS uniquement**

## <a name="ws_request_security_token_property_trust_version"></a>\_version d' \_ \_ approbation de propriété du jeton de sécurité \_ des \_ demandes WS \_

Cette section s’applique lorsque la contrainte de liaison de sécurité de la contrainte de liaison de sécurité de [**\_ message de \_ jeton \_ \_ \_ \_ WS émis**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) est spécifiée. Les assertions de stratégie suivantes sont utilisées pour identifier la [**\_ \_ version de WS Trust**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version) et les options associées.

``` syntax
<sp:Trust10> => WS_TRUST_VERSION_FEBRUARY_2005
    <sp:Policy>
        <sp:MustSupportClientChallenge/> ?
        <sp:MustSupportServerChallenge/> ?
        <sp:RequireClientEntropy/> ?
        <sp:RequireServerEntropy/> ?
        <sp:MustSupportIssuedTokens/> ?
    </sp:Policy>
</sp:Trust10>
```

La version d’approbation peut être spécifiée à l’aide de la [**contrainte de propriété de jeton de \_ sécurité de demande \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint) avec un ID de propriété de la version de l’approbation de propriété de jeton de la [**\_ demande \_ \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id).

## <a name="ws_security_property_security_header_version"></a>\_version de \_ l' \_ \_ en-tête de sécurité \_ de la propriété WS Security

Cette section s’applique lorsque l’une des contraintes de liaison suivantes est utilisée :

-   [**\_contrainte de \_ \_ liaison de \_ sécurité de message \_ \_ WS Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**\_contrainte de \_ liaison de sécurité de message WS username \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**\_contrainte de \_ liaison de sécurité de message WS CERT \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**\_contrainte de \_ \_ liaison de sécurité de message de jeton \_ WS \_ émis \_**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

La version de sécurité d’en-tête (telle que spécifiée par la version de l' [**\_ \_ \_ \_ en- \_ tête de sécurité de la propriété WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) est déterminée par l’une des assertions de stratégie suivantes :

``` syntax
<wsp:Wss10> ... </wsp:Wss10> => WS_SECURITY_HEADER_VERSION_1_0
```

``` syntax
<wsp:Wss11> ... </wsp:Wss11> => WS_SECURITY_HEADER_VERSION_1_1
```

## <a name="constraints-with-header-security-layout"></a>Contraintes avec disposition de sécurité d’en-tête

Cette section s’applique lorsque l’une des contraintes de liaison suivantes est utilisée :

-   [**\_contrainte de \_ \_ liaison de \_ sécurité de message \_ \_ WS Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**\_contrainte de \_ liaison de sécurité de message WS username \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**\_contrainte de \_ liaison de sécurité de message WS CERT \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**\_contrainte de \_ \_ liaison de sécurité de message de jeton \_ WS \_ émis \_**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

La disposition d’en-tête de sécurité (telle que spécifiée par la disposition de l' [**\_ \_ \_ \_ en- \_ tête de sécurité de la propriété WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) est déterminée par l’une des assertions de stratégie suivantes :

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:Lax.../> => WS_SECURITY_HEADER_LAYOUT_LAX
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:Strict.../> => WS_SECURITY_HEADER_LAYOUT_STRICT
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:LaxTsFirst.../> => WS_SECURITY_HEADER_LAYOUT_LAX_WITH_TIMESTAMP_FIRST
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:LaxTsLast.../> => WS_SECURITY_HEADER_LAYOUT_LAX_WITH_TIMESTAMP_LAST
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

## <a name="constraints-with-timestamp-security"></a>Contraintes avec sécurité de l’horodateur

Cette section s’applique lorsque l’une des contraintes de liaison suivantes est utilisée :

-   [**\_contrainte de \_ \_ liaison de \_ sécurité de message \_ \_ WS Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**\_contrainte de \_ liaison de sécurité de message WS username \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**\_contrainte de \_ liaison de sécurité de message WS CERT \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**\_contrainte de \_ \_ liaison de sécurité de message de jeton \_ WS \_ émis \_**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

Le fait qu’un horodateur soit inclus ou non dans l’en-tête de sécurité (tel que spécifié par l’utilisation de l’horodateur de la [**\_ propriété de sécurité \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) est déterminé par la présence de SP : IncludeTimestamp à l’emplacement suivant :

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:IncludeTimestamp.../>
    </wsp:Policy>
</sp:TransportBinding>
```

Si l’assertion SP : IncludeTimestamp est présente, la valeur de la stratégie [**est \_ \_ \_ \_ toujours utilisation d’horodateur de sécurité WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).

Si l’assertion SP : IncludeTimestamp n’est pas présente, la valeur de la stratégie est l’utilisation de l' [**\_ horodateur de sécurité WS \_ \_ \_ jamais**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).

 

 




