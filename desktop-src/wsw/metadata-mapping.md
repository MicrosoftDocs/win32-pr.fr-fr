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
# <a name="metadata-mapping"></a><span data-ttu-id="8ef91-106">Mappage de métadonnées</span><span class="sxs-lookup"><span data-stu-id="8ef91-106">Metadata Mapping</span></span>

<span data-ttu-id="8ef91-107">Le contenu d’un document de métadonnées est mappé à l’API de métadonnées de la manière décrite dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="8ef91-107">The contents of a metadata document map to the metadata API in the ways explained in the following sections.</span></span>


<span data-ttu-id="8ef91-108">Les préfixes d’espaces de noms suivants sont utilisés dans cette documentation :</span><span class="sxs-lookup"><span data-stu-id="8ef91-108">The following namespace prefixes are used throughout this documentation:</span></span>

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

<span data-ttu-id="8ef91-109">Les sections suivantes décrivent les constructions d’API, ainsi que les constructions de métadonnées (WSDL ou stratégie) auxquelles elles correspondent.</span><span class="sxs-lookup"><span data-stu-id="8ef91-109">The subsequent sections describe API constructs along with what metadata constructs (WSDL or Policy) they correspond to.</span></span>

<span data-ttu-id="8ef91-110">Vous pouvez vous familiariser avec les spécifications de métadonnées telles que WSDL et la stratégie pour comprendre cette section.</span><span class="sxs-lookup"><span data-stu-id="8ef91-110">Familiarity with metadata specifications such as WSDL and Policy will aid in understanding this section.</span></span>

## <a name="endpoint-address"></a><span data-ttu-id="8ef91-111">Adresse du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="8ef91-111">Endpoint address</span></span>

<span data-ttu-id="8ef91-112">L’adresse d’un point de terminaison (voir [**\_ \_ adresse du point de terminaison WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)) est obtenue à partir d’un élément d’extensibilité dans l’élément wsdl : port du document WSDL.</span><span class="sxs-lookup"><span data-stu-id="8ef91-112">The address of an endpoint (see [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)) is obtained from an extensibility element within the wsdl:port element of the WSDL document.</span></span> <span data-ttu-id="8ef91-113">Les éléments d’extensibilité suivants sont pris en charge pour spécifier l’adresse :</span><span class="sxs-lookup"><span data-stu-id="8ef91-113">The following extensibility elements are supported for specifying the address:</span></span>

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

## <a name="ws_channel_binding"></a><span data-ttu-id="8ef91-114">\_liaison WS Channel \_</span><span class="sxs-lookup"><span data-stu-id="8ef91-114">WS\_CHANNEL\_BINDING</span></span>

<span data-ttu-id="8ef91-115">La liaison de canal ( [**voir \_ \_ liaison WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)) est déterminée par le transport que la liaison SOAP utilise, comme suit :</span><span class="sxs-lookup"><span data-stu-id="8ef91-115">The channel binding (see [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)) is determined by the transport the soap binding used, as follows:</span></span>

``` syntax
<soap:binding transport=&quot;http://schemas.microsoft.com/soap/tcp&quot;/> => WS_TCP_CHANNEL_BINDING
```

``` syntax
<soap:binding transport=&quot;http://schemas.xmlsoap.org/soap/http&quot;/> => WS_HTTP_CHANNEL_BINDING
```

## <a name="ws_channel_property_envelope_version"></a><span data-ttu-id="8ef91-116">VERSION de l’enveloppe de la \_ propriété du canal WS \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="8ef91-116">WS\_CHANNEL\_PROPERTY\_ENVELOPE\_VERSION</span></span>

<span data-ttu-id="8ef91-117">La version d’enveloppe ( [**voir \_ \_ version d' \_ enveloppe \_ de la propriété WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) est déterminée par la liaison SOAP utilisée, comme suit :</span><span class="sxs-lookup"><span data-stu-id="8ef91-117">The envelope version (see [**WS\_CHANNEL\_PROPERTY\_ENVELOPE\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) is determined by which soap binding is used, as follows:</span></span>

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

## <a name="addressing-version"></a><span data-ttu-id="8ef91-118">Version d’adressage</span><span class="sxs-lookup"><span data-stu-id="8ef91-118">Addressing Version</span></span>

<span data-ttu-id="8ef91-119">La version d’adressage ( [**voir \_ \_ version d' \_ adressage \_ de la propriété WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) est déterminée par les assertions suivantes dans la stratégie de point de terminaison :</span><span class="sxs-lookup"><span data-stu-id="8ef91-119">The addressing version (see [**WS\_CHANNEL\_PROPERTY\_ADDRESSING\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) is determined by the following assertions in the endpoint policy:</span></span>

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

<span data-ttu-id="8ef91-120">Si une assertion d’adressage n’est pas présente, le transport de la [**\_ \_ version \_ WS Addressing**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) est pris par défaut.</span><span class="sxs-lookup"><span data-stu-id="8ef91-120">If an addressing assertion is not present, then [**WS\_ADDRESSING\_VERSION\_TRANSPORT**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) is assumed.</span></span>

## <a name="message-encoding"></a><span data-ttu-id="8ef91-121">Encodage de message</span><span class="sxs-lookup"><span data-stu-id="8ef91-121">Message Encoding</span></span>

<span data-ttu-id="8ef91-122">L’encodage du message (voir [**\_ \_ \_ encodage de la propriété WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) est déterminé par les assertions suivantes dans la stratégie de point de terminaison :</span><span class="sxs-lookup"><span data-stu-id="8ef91-122">The encoding of the message (see [**WS\_CHANNEL\_PROPERTY\_ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) is determined by the following assertions in the endpoint policy:</span></span>

``` syntax
<wsp:Policy...>
    <binp:BinaryEncoding.../> => WS_ENCODING_XML_BINARY_SESSION_1, WS_ENCODING_XML_BINARY_1
</wsp:Policy>
```

<span data-ttu-id="8ef91-123">Notez que l’assertion de stratégie d’encodage binaire n’inclut pas d’informations indiquant si l’encodage binaire est une session ou sans session.</span><span class="sxs-lookup"><span data-stu-id="8ef91-123">Note that the binary encoding policy assertion does not include information about whether the binary encoding is sessionful or sessionless.</span></span> <span data-ttu-id="8ef91-124">Cela est déterminé par la contrainte de propriété Encoding (qui doit être appropriée selon que le type de [**\_ canal WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) utilisé ou non est de type session ou non).</span><span class="sxs-lookup"><span data-stu-id="8ef91-124">This is determined by the encoding property constraint (which should be appropriate according to whether or not the [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) being used is sessionful or not).</span></span>

``` syntax
<wsp:Policy...>
    <mtomp:OptimizedMimeSerialization.../> => WS_ENCODING_XML_MTOM_UTF8, WS_ENCODING_XML_MTOM_UTF16LE, WS_ENCODING_XML_MTOM_UTF16BE
</wsp:Policy>
```

<span data-ttu-id="8ef91-125">Si aucune des assertions ci-dessus n’est présente, un encodage de texte est utilisé : [**WS \_ Encoding \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding), **WS \_ encodage \_ XML \_ utf16le**, **WS \_ Encoding \_ XML \_ utf16be**.</span><span class="sxs-lookup"><span data-stu-id="8ef91-125">If neither of the above assertions are present, then a text encoding is used: [**WS\_ENCODING\_XML\_UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding), **WS\_ENCODING\_XML\_UTF16LE**, **WS\_ENCODING\_XML\_UTF16BE**.</span></span>

<span data-ttu-id="8ef91-126">Notez que la stratégie n’inclut pas d’informations sur le jeu de caractères pour les encodages MTOM ou texte (qu’il s’agisse de UTF8, UTF16LE ou UTF16BE).</span><span class="sxs-lookup"><span data-stu-id="8ef91-126">Note that policy does not include information about the character set for MTOM or text encodings (whether it is UTF8, UTF16LE or UTF16BE).</span></span> <span data-ttu-id="8ef91-127">La valeur réelle du jeu de caractères utilisée est déterminée par la contrainte de propriété Encoding.</span><span class="sxs-lookup"><span data-stu-id="8ef91-127">The actual character set value used is determined by the encoding property constraint.</span></span>

## <a name="constraints-with-http-header-authentication"></a><span data-ttu-id="8ef91-128">Contraintes avec l’authentification d’en-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="8ef91-128">Constraints with HTTP Header Authentication</span></span>

<span data-ttu-id="8ef91-129">Cette section s’applique lorsque la contrainte de liaison de sécurité de la contrainte de liaison de sécurité d' [**\_ \_ en-tête \_ \_ \_ \_ http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint) est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8ef91-129">This section applies when the [**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint) security binding constraint is specified.</span></span>

<span data-ttu-id="8ef91-130">Cette liaison de sécurité est indiquée dans la stratégie par des assertions différentes qui déclarent que l’authentification d’en-tête HTTP doit être utilisée et qu’un schéma d’authentification particulier doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="8ef91-130">This security binding is indicated in the policy by different assertions that states both that HTTP header authentication should be used, and that a particular authentication scheme should be used.</span></span> <span data-ttu-id="8ef91-131">Les assertions de stratégie correspondent aux valeurs du [**schéma d’authentification de l' \_ \_ \_ \_ \_ en \_ \_ -tête http de la propriété de liaison WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) , comme suit :</span><span class="sxs-lookup"><span data-stu-id="8ef91-131">The policy assertions correspond to the values of the [**WS\_SECURITY\_BINDING\_PROPERTY\_HTTP\_HEADER\_AUTH\_SCHEME**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) as follows:</span></span>

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

## <a name="constraints-with-sll-transport-security"></a><span data-ttu-id="8ef91-132">Contraintes avec sécurité de transport SSL</span><span class="sxs-lookup"><span data-stu-id="8ef91-132">Constraints with SLL Transport Security</span></span>

<span data-ttu-id="8ef91-133">Cette section s’applique lorsque la contrainte de liaison de sécurité de la contrainte de sécurité de [**\_ \_ transport \_ \_ \_ WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint) est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8ef91-133">This section applies when the [**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="8ef91-134">Les assertions de stratégie suivantes sont utilisées dans ce cas :</span><span class="sxs-lookup"><span data-stu-id="8ef91-134">The following policy assertions are used in this case:</span></span>

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

## <a name="constraints-with-sspi-transport-security"></a><span data-ttu-id="8ef91-135">Contraintes avec sécurité de transport SSPI</span><span class="sxs-lookup"><span data-stu-id="8ef91-135">Constraints with SSPI Transport Security</span></span>

<span data-ttu-id="8ef91-136">Cette section s’applique lorsque la contrainte de liaison de sécurité de la contrainte de sécurité de [**\_ transport WS TCP \_ SSPI \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint) est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8ef91-136">This section applies when the [**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="8ef91-137">Les assertions de stratégie suivantes sont utilisées dans ce cas :</span><span class="sxs-lookup"><span data-stu-id="8ef91-137">The following policy assertions are used in this case:</span></span>

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

## <a name="constrains-with-transport-security"></a><span data-ttu-id="8ef91-138">Contractions avec la sécurité de transport</span><span class="sxs-lookup"><span data-stu-id="8ef91-138">Constrains with Transport Security</span></span>

<span data-ttu-id="8ef91-139">La contrainte de propriété du niveau de protection du transport de la [**\_ \_ propriété \_ \_ \_ WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) peut être spécifiée si l’une des contraintes de liaison de sécurité est spécifiée :</span><span class="sxs-lookup"><span data-stu-id="8ef91-139">The [**WS\_SECURITY\_PROPERTY\_TRANSPORT\_PROTECTION\_LEVEL**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) property constraint can be specified if any of the security binding constraints are specified:</span></span>

-   [<span data-ttu-id="8ef91-140">**\_contrainte de \_ liaison de sécurité de transport WS SSL \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8ef91-140">**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)

    <span data-ttu-id="8ef91-141">La valeur de la stratégie est [**toujours \_ \_ connexion au niveau de protection WS \_ \_ et \_ chiffrement**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).</span><span class="sxs-lookup"><span data-stu-id="8ef91-141">The value from policy is always [**WS\_PROTECTION\_LEVEL\_SIGN\_AND\_ENCRYPT**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).</span></span>

-   [<span data-ttu-id="8ef91-142">**contrainte de liaison de sécurité de transport de WS \_ TCP \_ SSPI \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8ef91-142">**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)

    <span data-ttu-id="8ef91-143">La valeur de la stratégie est spécifiée dans le cadre de l’assertion WindowsTransportSecurity, comme suit :</span><span class="sxs-lookup"><span data-stu-id="8ef91-143">The value from policy is specified as part of the WindowsTransportSecurity assertion, as follows:</span></span>

    ``` syntax
    <netf:WindowsTransportSecurity...>None</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_NONE
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>Sign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>EncryptAndSign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN_AND_ENCRYPT
    ```

-   [<span data-ttu-id="8ef91-144">**\_contrainte de \_ \_ liaison de \_ sécurité \_ d’en-tête \_ WS http**</span><span class="sxs-lookup"><span data-stu-id="8ef91-144">**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)

    <span data-ttu-id="8ef91-145">La valeur de la stratégie est toujours le [**\_ niveau de protection WS \_ \_ None**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).</span><span class="sxs-lookup"><span data-stu-id="8ef91-145">The value from policy is always [**WS\_PROTECTION\_LEVEL\_NONE**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).</span></span>

## <a name="constraints-with-kerberos-apreq-security-binding"></a><span data-ttu-id="8ef91-146">Contraintes avec la liaison de sécurité Kerberos APREQ</span><span class="sxs-lookup"><span data-stu-id="8ef91-146">Constraints with Kerberos APREQ Security Binding</span></span>

<span data-ttu-id="8ef91-147">Cette section s’applique lorsque la contrainte de liaison de sécurité de la contrainte de sécurité de [**\_ message WS Kerberos \_ APREQ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint) est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8ef91-147">This section applies when the [**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="8ef91-148">Les assertions de stratégie suivantes sont utilisées dans ce cas :</span><span class="sxs-lookup"><span data-stu-id="8ef91-148">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:KerberosToken>
            <WssGssKerberosV5ApReqToken11.../>
        </sp:KerberosToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="constraints-with-message-security-binding"></a><span data-ttu-id="8ef91-149">Contraintes avec liaison de sécurité de message</span><span class="sxs-lookup"><span data-stu-id="8ef91-149">Constraints with Message Security Binding</span></span>

<span data-ttu-id="8ef91-150">Cette section s’applique lorsque la contrainte de liaison de sécurité de la contrainte de liaison de sécurité de [**\_ \_ message \_ \_ \_ WS username**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint) est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8ef91-150">This section applies when the [**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="8ef91-151">Les assertions de stratégie suivantes sont utilisées dans ce cas :</span><span class="sxs-lookup"><span data-stu-id="8ef91-151">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:SignedSupportingTokens>
    <wsp:Policy>
        <sp:UsernameToken.../>
    </wsp:Policy>
</sp:SignedSupportingTokens>
```

## <a name="ws_cert_message_security_binding_constraint"></a><span data-ttu-id="8ef91-152">\_contrainte de \_ liaison de sécurité de message WS CERT \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="8ef91-152">WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT</span></span>

<span data-ttu-id="8ef91-153">Cette section s’applique lorsque la contrainte de liaison de sécurité de la contrainte de liaison de sécurité de [**\_ message du certificat \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint) est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8ef91-153">This section applies when the [**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="8ef91-154">Les assertions de stratégie suivantes sont utilisées dans ce cas :</span><span class="sxs-lookup"><span data-stu-id="8ef91-154">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:EndorsingSupportingTokens>
    <wsp:Policy>
        <sp:X509Token.../>
   </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="ws_issued_token_message_security_binding_constraint"></a><span data-ttu-id="8ef91-155">\_contrainte de \_ \_ liaison de sécurité de message de jeton \_ WS \_ émis \_</span><span class="sxs-lookup"><span data-stu-id="8ef91-155">WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT</span></span>

<span data-ttu-id="8ef91-156">Cette section s’applique lorsque la contrainte de liaison de sécurité de la contrainte de liaison de sécurité de [**\_ message de \_ jeton \_ \_ \_ \_ WS émis**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8ef91-156">This section applies when the [**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="8ef91-157">Les assertions de stratégie suivantes sont utilisées dans ce cas :</span><span class="sxs-lookup"><span data-stu-id="8ef91-157">The following policy assertions are used in this case:</span></span>

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

<span data-ttu-id="8ef91-158">Les éléments suivants décrivent le mappage des champs de la contrainte de liaison de [**sécurité de message de \_ \_ jeton \_ \_ \_ \_ WS émis**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) à la stratégie ci-dessus :</span><span class="sxs-lookup"><span data-stu-id="8ef91-158">The following describes the mapping of fields of the [**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) to the above policy:</span></span>

-   <span data-ttu-id="8ef91-159">Le champ claimConstraints permet de vérifier l’ensemble des URI de type de revendication qui apparaissent dans l’élément WSI : ClaimType ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="8ef91-159">The claimConstraints field is used to verify the set of claim type URIs that appear within the wsi:ClaimType element above.</span></span>

-   <span data-ttu-id="8ef91-160">Le champ issuerAddress correspond à l’élément d’émetteur wsp : ci-dessus, qui est l' [**\_ \_ adresse du point de terminaison WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) du service qui peut émettre le jeton.</span><span class="sxs-lookup"><span data-stu-id="8ef91-160">The issuerAddress field corresponds to the wsp:Issuer element above, which is the [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) of the service that can issue the token.</span></span>

-   <span data-ttu-id="8ef91-161">Le champ requestSecurityTokenTemplate correspond aux éléments enfants de l’élément wsp : RequestSecurityTokenTemplate.</span><span class="sxs-lookup"><span data-stu-id="8ef91-161">The requestSecurityTokenTemplate field corresponds to the child elements of the wsp:RequestSecurityTokenTemplate element.</span></span>

## <a name="ws_security_context_message_security_binding_constraint"></a><span data-ttu-id="8ef91-162">\_contrainte de \_ \_ liaison de sécurité de message de contexte \_ de \_ sécurité WS \_</span><span class="sxs-lookup"><span data-stu-id="8ef91-162">WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT</span></span>

<span data-ttu-id="8ef91-163">Cette section s’applique lorsque la contrainte de liaison de sécurité de la contrainte de sécurité de [**\_ message du contexte de sécurité \_ \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8ef91-163">This section applies when the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="8ef91-164">Les assertions de stratégie suivantes sont utilisées dans ce cas :</span><span class="sxs-lookup"><span data-stu-id="8ef91-164">The following policy assertions are used in this case:</span></span>

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

<span data-ttu-id="8ef91-165">Le mode d’entropie est déterminé par l’assertion <SP : Trust10>.</span><span class="sxs-lookup"><span data-stu-id="8ef91-165">The entropy mode is determined by the <sp:Trust10> assertion.</span></span> <span data-ttu-id="8ef91-166"><SP : RequireClientEntropy/> et <SP : RequireServerEntropy/> => [**\_ mode d' \_ entropie de clé de sécurité WS \_ \_ \_ combiné**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode) <SP : RequireClientEntropy/> => mode d’entropie de **clé de \_ sécurité WS \_ \_ \_ \_ client \_ uniquement** <SP : RequireServerEntropy/> => **\_ \_ \_ \_ serveur en mode entropie \_ \_ de clé de sécurité WS uniquement**</span><span class="sxs-lookup"><span data-stu-id="8ef91-166"><sp:RequireClientEntropy/> and <sp:RequireServerEntropy/> => [**WS\_SECURITY\_KEY\_ENTROPY\_MODE\_COMBINED**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode) <sp:RequireClientEntropy/> => **WS\_SECURITY\_KEY\_ENTROPY\_MODE\_CLIENT\_ONLY** <sp:RequireServerEntropy/> => **WS\_SECURITY\_KEY\_ENTROPY\_MODE\_SERVER\_ONLY**</span></span>

## <a name="ws_request_security_token_property_trust_version"></a><span data-ttu-id="8ef91-167">\_version d' \_ \_ approbation de propriété du jeton de sécurité \_ des \_ demandes WS \_</span><span class="sxs-lookup"><span data-stu-id="8ef91-167">WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_TRUST\_VERSION</span></span>

<span data-ttu-id="8ef91-168">Cette section s’applique lorsque la contrainte de liaison de sécurité de la contrainte de liaison de sécurité de [**\_ message de \_ jeton \_ \_ \_ \_ WS émis**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8ef91-168">This section applies when the [**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="8ef91-169">Les assertions de stratégie suivantes sont utilisées pour identifier la [**\_ \_ version de WS Trust**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version) et les options associées.</span><span class="sxs-lookup"><span data-stu-id="8ef91-169">The following policy assertions are used to identify the [**WS\_TRUST\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version) and associated options.</span></span>

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

<span data-ttu-id="8ef91-170">La version d’approbation peut être spécifiée à l’aide de la [**contrainte de propriété de jeton de \_ sécurité de demande \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint) avec un ID de propriété de la version de l’approbation de propriété de jeton de la [**\_ demande \_ \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id).</span><span class="sxs-lookup"><span data-stu-id="8ef91-170">The trust version can be specified using the [**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint) with a property id of [**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_TRUST\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id).</span></span>

## <a name="ws_security_property_security_header_version"></a><span data-ttu-id="8ef91-171">\_version de \_ l' \_ \_ en-tête de sécurité \_ de la propriété WS Security</span><span class="sxs-lookup"><span data-stu-id="8ef91-171">WS\_SECURITY\_PROPERTY\_SECURITY\_HEADER\_VERSION</span></span>

<span data-ttu-id="8ef91-172">Cette section s’applique lorsque l’une des contraintes de liaison suivantes est utilisée :</span><span class="sxs-lookup"><span data-stu-id="8ef91-172">This section applies when any of the following binding constraints are used:</span></span>

-   [<span data-ttu-id="8ef91-173">**\_contrainte de \_ \_ liaison de \_ sécurité de message \_ \_ WS Kerberos APREQ**</span><span class="sxs-lookup"><span data-stu-id="8ef91-173">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="8ef91-174">**\_contrainte de \_ liaison de sécurité de message WS username \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8ef91-174">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [<span data-ttu-id="8ef91-175">**\_contrainte de \_ liaison de sécurité de message WS CERT \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8ef91-175">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="8ef91-176">**\_contrainte de \_ \_ liaison de sécurité de message de jeton \_ WS \_ émis \_**</span><span class="sxs-lookup"><span data-stu-id="8ef91-176">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

<span data-ttu-id="8ef91-177">La version de sécurité d’en-tête (telle que spécifiée par la version de l' [**\_ \_ \_ \_ en- \_ tête de sécurité de la propriété WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) est déterminée par l’une des assertions de stratégie suivantes :</span><span class="sxs-lookup"><span data-stu-id="8ef91-177">The header security version (as specified by [**WS\_SECURITY\_PROPERTY\_SECURITY\_HEADER\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) is determined by one of the following policy assertions:</span></span>

``` syntax
<wsp:Wss10> ... </wsp:Wss10> => WS_SECURITY_HEADER_VERSION_1_0
```

``` syntax
<wsp:Wss11> ... </wsp:Wss11> => WS_SECURITY_HEADER_VERSION_1_1
```

## <a name="constraints-with-header-security-layout"></a><span data-ttu-id="8ef91-178">Contraintes avec disposition de sécurité d’en-tête</span><span class="sxs-lookup"><span data-stu-id="8ef91-178">Constraints with Header Security Layout</span></span>

<span data-ttu-id="8ef91-179">Cette section s’applique lorsque l’une des contraintes de liaison suivantes est utilisée :</span><span class="sxs-lookup"><span data-stu-id="8ef91-179">This section applies when any of the following binding constraints are used:</span></span>

-   [<span data-ttu-id="8ef91-180">**\_contrainte de \_ \_ liaison de \_ sécurité de message \_ \_ WS Kerberos APREQ**</span><span class="sxs-lookup"><span data-stu-id="8ef91-180">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="8ef91-181">**\_contrainte de \_ liaison de sécurité de message WS username \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8ef91-181">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [<span data-ttu-id="8ef91-182">**\_contrainte de \_ liaison de sécurité de message WS CERT \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8ef91-182">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="8ef91-183">**\_contrainte de \_ \_ liaison de sécurité de message de jeton \_ WS \_ émis \_**</span><span class="sxs-lookup"><span data-stu-id="8ef91-183">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

<span data-ttu-id="8ef91-184">La disposition d’en-tête de sécurité (telle que spécifiée par la disposition de l' [**\_ \_ \_ \_ en- \_ tête de sécurité de la propriété WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) est déterminée par l’une des assertions de stratégie suivantes :</span><span class="sxs-lookup"><span data-stu-id="8ef91-184">The security header layout (as specified by [**WS\_SECURITY\_PROPERTY\_SECURITY\_HEADER\_LAYOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) is determined by one of the following policy assertions:</span></span>

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

## <a name="constraints-with-timestamp-security"></a><span data-ttu-id="8ef91-185">Contraintes avec sécurité de l’horodateur</span><span class="sxs-lookup"><span data-stu-id="8ef91-185">Constraints with Timestamp Security</span></span>

<span data-ttu-id="8ef91-186">Cette section s’applique lorsque l’une des contraintes de liaison suivantes est utilisée :</span><span class="sxs-lookup"><span data-stu-id="8ef91-186">This section applies when any of the following binding constraints are used:</span></span>

-   [<span data-ttu-id="8ef91-187">**\_contrainte de \_ \_ liaison de \_ sécurité de message \_ \_ WS Kerberos APREQ**</span><span class="sxs-lookup"><span data-stu-id="8ef91-187">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="8ef91-188">**\_contrainte de \_ liaison de sécurité de message WS username \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8ef91-188">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [<span data-ttu-id="8ef91-189">**\_contrainte de \_ liaison de sécurité de message WS CERT \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8ef91-189">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="8ef91-190">**\_contrainte de \_ \_ liaison de sécurité de message de jeton \_ WS \_ émis \_**</span><span class="sxs-lookup"><span data-stu-id="8ef91-190">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

<span data-ttu-id="8ef91-191">Le fait qu’un horodateur soit inclus ou non dans l’en-tête de sécurité (tel que spécifié par l’utilisation de l’horodateur de la [**\_ propriété de sécurité \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) est déterminé par la présence de SP : IncludeTimestamp à l’emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="8ef91-191">Whether or not a timestamp is included in the security header (as specified by [**WS\_SECURITY\_PROPERTY\_TIMESTAMP\_USAGE**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) is determined by the presence of the sp:IncludeTimestamp in the following location:</span></span>

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:IncludeTimestamp.../>
    </wsp:Policy>
</sp:TransportBinding>
```

<span data-ttu-id="8ef91-192">Si l’assertion SP : IncludeTimestamp est présente, la valeur de la stratégie [**est \_ \_ \_ \_ toujours utilisation d’horodateur de sécurité WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).</span><span class="sxs-lookup"><span data-stu-id="8ef91-192">If the sp:IncludeTimestamp assertion is present, the value from policy is [**WS\_SECURITY\_TIMESTAMP\_USAGE\_ALWAYS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).</span></span>

<span data-ttu-id="8ef91-193">Si l’assertion SP : IncludeTimestamp n’est pas présente, la valeur de la stratégie est l’utilisation de l' [**\_ horodateur de sécurité WS \_ \_ \_ jamais**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).</span><span class="sxs-lookup"><span data-stu-id="8ef91-193">If the sp:IncludeTimestamp assertion is not present, the value from policy is [**WS\_SECURITY\_TIMESTAMP\_USAGE\_NEVER**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).</span></span>

 

 




