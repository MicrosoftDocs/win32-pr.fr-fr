---
description: Certains serveurs et proxys HTTP requièrent une authentification avant d’autoriser l’accès aux ressources sur Internet. Les fonctions des services HTTP Microsoft Windows (WinHTTP) prennent en charge l’authentification du serveur et du proxy pour les sessions HTTP.
ms.assetid: 077d6275-8600-4091-b78e-419a41a2101a
title: Authentification dans WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75c6703e9d28902c5705f0b8ab8433193c4d085
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380825"
---
# <a name="authentication-in-winhttp"></a><span data-ttu-id="ff716-104">Authentification dans WinHTTP</span><span class="sxs-lookup"><span data-stu-id="ff716-104">Authentication in WinHTTP</span></span>

<span data-ttu-id="ff716-105">Certains serveurs et proxys HTTP requièrent une authentification avant d’autoriser l’accès aux ressources sur Internet.</span><span class="sxs-lookup"><span data-stu-id="ff716-105">Some HTTP servers and proxies require authentication before allowing access to resources on the Internet.</span></span> <span data-ttu-id="ff716-106">Les fonctions des services HTTP Microsoft Windows (WinHTTP) prennent en charge l’authentification du serveur et du proxy pour les sessions HTTP.</span><span class="sxs-lookup"><span data-stu-id="ff716-106">The Microsoft Windows HTTP Services (WinHTTP) functions support server and proxy authentication for HTTP sessions.</span></span>

## <a name="about-http-authentication"></a><span data-ttu-id="ff716-107">À propos de l’authentification HTTP</span><span class="sxs-lookup"><span data-stu-id="ff716-107">About HTTP Authentication</span></span>

<span data-ttu-id="ff716-108">Si l’authentification est requise, l’application HTTP reçoit le code d’état 401 (le serveur nécessite une authentification) ou 407 (le proxy nécessite une authentification).</span><span class="sxs-lookup"><span data-stu-id="ff716-108">If authentication is required, the HTTP application receives a status code of 401 (server requires authentication) or 407 (proxy requires authentication).</span></span> <span data-ttu-id="ff716-109">Avec le code d’État, le proxy ou le serveur envoie un ou plusieurs en-têtes Authenticate : WWW-Authenticate (pour l’authentification du serveur) ou Proxy-Authenticate (pour l’authentification du proxy).</span><span class="sxs-lookup"><span data-stu-id="ff716-109">Along with the status code, the proxy or server sends one or more authenticate headers: WWW-Authenticate (for server authentication) or Proxy-Authenticate (for proxy authentication).</span></span>

<span data-ttu-id="ff716-110">Chaque en-tête Authenticate contient un schéma d’authentification pris en charge et, pour les schémas de base et les schémas synthétiques, un domaine.</span><span class="sxs-lookup"><span data-stu-id="ff716-110">Each authenticate header contains a supported authentication scheme and, for the Basic and Digest schemes, a realm.</span></span> <span data-ttu-id="ff716-111">Si plusieurs schémas d’authentification sont pris en charge, le serveur retourne plusieurs en-têtes Authenticate.</span><span class="sxs-lookup"><span data-stu-id="ff716-111">If multiple authentication schemes are supported, the server returns multiple authenticate headers.</span></span> <span data-ttu-id="ff716-112">La valeur de domaine est sensible à la casse et définit un ensemble de serveurs ou de proxys pour lesquels les mêmes informations d’identification sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="ff716-112">The realm value is case-sensitive and defines a set of servers or proxies for which the same credentials are accepted.</span></span> <span data-ttu-id="ff716-113">Par exemple, l’en-tête « WWW-Authenticate : Basic domaine = "example" » peut être retourné lorsque l’authentification du serveur est requise.</span><span class="sxs-lookup"><span data-stu-id="ff716-113">For example, the header "WWW-Authenticate: Basic Realm="example"" might be returned when server authentication is required.</span></span> <span data-ttu-id="ff716-114">Cet en-tête spécifie que les informations d’identification de l’utilisateur doivent être fournies pour le domaine « example ».</span><span class="sxs-lookup"><span data-stu-id="ff716-114">This header specifies that user credentials must be supplied for the "example" domain.</span></span>

<span data-ttu-id="ff716-115">Une application HTTP peut inclure un champ d’en-tête Authorization avec une demande qu’elle envoie au serveur.</span><span class="sxs-lookup"><span data-stu-id="ff716-115">An HTTP application can include an authorization header field with a request it sends to the server.</span></span> <span data-ttu-id="ff716-116">L’en-tête Authorization contient le schéma d’authentification et la réponse appropriée requise par ce schéma.</span><span class="sxs-lookup"><span data-stu-id="ff716-116">The authorization header contains the authentication scheme and the appropriate response required by that scheme.</span></span> <span data-ttu-id="ff716-117">Par exemple, l’en-tête « Authorization : Basic \<username:password> » est ajouté à la demande et envoyé au serveur si le client a reçu l’en-tête de réponse « www-Authenticate : Basic Realm = «example »».</span><span class="sxs-lookup"><span data-stu-id="ff716-117">For example, the header "Authorization: Basic \<username:password>" would be added to the request and sent to the server if the client received the response header "WWW-Authenticate: Basic Realm="example"".</span></span>

> [!Note]  
> <span data-ttu-id="ff716-118">Bien qu’elles soient affichées ici sous forme de texte brut, le nom d’utilisateur et le mot de passe sont en fait [*codés en base64*](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="ff716-118">Although they are shown here as plain text, the username and password are actually [*base64 encoded*](glossary.md).</span></span>

 

<span data-ttu-id="ff716-119">Il existe deux types généraux de schémas d’authentification :</span><span class="sxs-lookup"><span data-stu-id="ff716-119">There are two general types of authentication schemes:</span></span>

-   <span data-ttu-id="ff716-120">Schéma d’authentification de base, dans lequel le nom d’utilisateur et le mot de passe sont envoyés en texte clair au serveur.</span><span class="sxs-lookup"><span data-stu-id="ff716-120">Basic authentication scheme, in which the user name and password are sent in clear text to the server.</span></span>

    <span data-ttu-id="ff716-121">Le schéma d’authentification de base est basé sur le modèle qu’un client doit identifier lui-même à l’aide d’un nom d’utilisateur et d’un mot de passe pour chaque domaine.</span><span class="sxs-lookup"><span data-stu-id="ff716-121">The Basic authentication scheme is based on the model that a client must identify itself with a user name and password for each realm.</span></span> <span data-ttu-id="ff716-122">Le serveur traite la demande uniquement si la demande est envoyée avec un en-tête d’autorisation qui comprend un nom d’utilisateur et un mot de passe valides.</span><span class="sxs-lookup"><span data-stu-id="ff716-122">The server services the request only if the request is sent with an authorization header that includes a valid user name and password.</span></span>

-   <span data-ttu-id="ff716-123">Des schémas de stimulation-réponse, tels que Kerberos, dans lesquels le serveur conteste les [*données d’authentification*](glossary.md)du client.</span><span class="sxs-lookup"><span data-stu-id="ff716-123">Challenge-response schemes, such as Kerberos, in which the server challenges the client with [*authentication data*](glossary.md).</span></span> <span data-ttu-id="ff716-124">Le client transforme les données avec les informations d’identification de l’utilisateur et renvoie les données transformées au serveur à des fins d’authentification.</span><span class="sxs-lookup"><span data-stu-id="ff716-124">The client transforms the data with the user credentials and sends the transformed data back to the server for authentication.</span></span>

    <span data-ttu-id="ff716-125">Les schémas de stimulation/réponse permettent une authentification plus sécurisée.</span><span class="sxs-lookup"><span data-stu-id="ff716-125">Challenge-response schemes enable a more secure authentication.</span></span> <span data-ttu-id="ff716-126">Dans un schéma de stimulation/réponse, le nom d’utilisateur et le mot de passe ne sont jamais transmis sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="ff716-126">In a challenge-response scheme, the username and password are never transmitted over the network.</span></span> <span data-ttu-id="ff716-127">Une fois que le client a sélectionné un modèle de stimulation-réponse, le serveur renvoie un code d’état approprié avec un challenge contenant les [*données d’authentification*](glossary.md) de ce schéma.</span><span class="sxs-lookup"><span data-stu-id="ff716-127">After the client selects a challenge-response scheme, the server returns an appropriate status code with a challenge that contains the [*authentication data*](glossary.md) for that scheme.</span></span> <span data-ttu-id="ff716-128">Le client renvoie ensuite la demande avec la réponse appropriée pour obtenir le service demandé.</span><span class="sxs-lookup"><span data-stu-id="ff716-128">The client then resends the request with the proper response to obtain the requested service.</span></span> <span data-ttu-id="ff716-129">Les schémas de stimulation/réponse peuvent exécuter plusieurs échanges.</span><span class="sxs-lookup"><span data-stu-id="ff716-129">Challenge-response schemes can take multiple exchanges to complete.</span></span>

<span data-ttu-id="ff716-130">Le tableau suivant répertorie les schémas d’authentification pris en charge par WinHTTP, le type d’authentification et une description du schéma.</span><span class="sxs-lookup"><span data-stu-id="ff716-130">The following table contains the authentication schemes that are supported by WinHTTP, the authentication type, and a description of the scheme.</span></span>



| <span data-ttu-id="ff716-131">Schéma</span><span class="sxs-lookup"><span data-stu-id="ff716-131">Scheme</span></span>            | <span data-ttu-id="ff716-132">Type</span><span class="sxs-lookup"><span data-stu-id="ff716-132">Type</span></span>               | <span data-ttu-id="ff716-133">Description</span><span class="sxs-lookup"><span data-stu-id="ff716-133">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff716-134">De base (texte en clair)</span><span class="sxs-lookup"><span data-stu-id="ff716-134">Basic (plaintext)</span></span> | <span data-ttu-id="ff716-135">De base</span><span class="sxs-lookup"><span data-stu-id="ff716-135">Basic</span></span>              | <span data-ttu-id="ff716-136">Utilise une chaîne [*encodée en base64*](glossary.md) qui contient le nom d’utilisateur et le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="ff716-136">Uses a [*base64 encoded*](glossary.md) string that contains the user name and password.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="ff716-137">Digest</span><span class="sxs-lookup"><span data-stu-id="ff716-137">Digest</span></span>            | <span data-ttu-id="ff716-138">Stimulation-réponse</span><span class="sxs-lookup"><span data-stu-id="ff716-138">Challenge-response</span></span> | <span data-ttu-id="ff716-139">Défis liés à l’utilisation d’une valeur à usage unique (chaîne de données spécifiée par le serveur).</span><span class="sxs-lookup"><span data-stu-id="ff716-139">Challenges using a nonce (a server-specified data string) value.</span></span> <span data-ttu-id="ff716-140">Une réponse valide contient une somme de contrôle du nom d’utilisateur, du mot de passe, de la valeur de nonce donnée, du [*verbe http*](glossary.md)et de l’Uniform Resource Identifier (Uri) demandé.</span><span class="sxs-lookup"><span data-stu-id="ff716-140">A valid response contains a checksum of the user name, the password, the given nonce value, the [*HTTP verb*](glossary.md), and the requested Uniform Resource Identifier (URI).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="ff716-141">NTLM</span><span class="sxs-lookup"><span data-stu-id="ff716-141">NTLM</span></span>              | <span data-ttu-id="ff716-142">Stimulation-réponse</span><span class="sxs-lookup"><span data-stu-id="ff716-142">Challenge-response</span></span> | <span data-ttu-id="ff716-143">Requiert la transformation des [*données d’authentification*](glossary.md) avec les informations d’identification de l’utilisateur pour prouver l’identité.</span><span class="sxs-lookup"><span data-stu-id="ff716-143">Requires the [*authentication data*](glossary.md) to be transformed with the user credentials to prove identity.</span></span> <span data-ttu-id="ff716-144">Pour que l’authentification NTLM fonctionne correctement, plusieurs échanges doivent avoir lieu sur la même connexion.</span><span class="sxs-lookup"><span data-stu-id="ff716-144">For NTLM authentication to function correctly, several exchanges must take place on the same connection.</span></span> <span data-ttu-id="ff716-145">Par conséquent, l’authentification NTLM ne peut pas être utilisée si un proxy intermédiaire ne prend pas en charge les connexions persistantes.</span><span class="sxs-lookup"><span data-stu-id="ff716-145">Therefore, NTLM authentication cannot be used if an intervening proxy does not support keep-alive connections.</span></span> <span data-ttu-id="ff716-146">L’authentification NTLM échoue également si [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) est utilisé avec l’indicateur [**\_ Disable \_ Keep \_ Alive WinHTTP**](option-flags.md) qui désactive la sémantique Keep-Alive.</span><span class="sxs-lookup"><span data-stu-id="ff716-146">NTLM authentication also fails if [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) is used with the [**WINHTTP\_DISABLE\_KEEP\_ALIVE**](option-flags.md) flag that disables keep-alive semantics.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="ff716-147">Passport</span><span class="sxs-lookup"><span data-stu-id="ff716-147">Passport</span></span>          | <span data-ttu-id="ff716-148">Stimulation-réponse</span><span class="sxs-lookup"><span data-stu-id="ff716-148">Challenge-response</span></span> | <span data-ttu-id="ff716-149">Utilise [Microsoft Passport 1,4](passport-authentication-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="ff716-149">Uses [Microsoft Passport 1.4](passport-authentication-in-winhttp.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="ff716-150">Negotiate</span><span class="sxs-lookup"><span data-stu-id="ff716-150">Negotiate</span></span>         | <span data-ttu-id="ff716-151">Stimulation-réponse</span><span class="sxs-lookup"><span data-stu-id="ff716-151">Challenge-response</span></span> | <span data-ttu-id="ff716-152">Si le serveur et le client utilisent tous deux Windows 2000 ou une version ultérieure, l’authentification Kerberos est utilisée.</span><span class="sxs-lookup"><span data-stu-id="ff716-152">If both the server and client are using Windows 2000 or later, Kerberos authentication is used.</span></span> <span data-ttu-id="ff716-153">Sinon, l’authentification NTLM est utilisée.</span><span class="sxs-lookup"><span data-stu-id="ff716-153">Otherwise NTLM authentication is used.</span></span> <span data-ttu-id="ff716-154">Kerberos est disponible dans les systèmes d’exploitation Windows 2000 et versions ultérieures et est considéré comme plus sécurisé que l’authentification NTLM.</span><span class="sxs-lookup"><span data-stu-id="ff716-154">Kerberos is available in Windows 2000 and later operating systems and is considered to be more secure than NTLM authentication.</span></span> <span data-ttu-id="ff716-155">Pour que l’authentification par négociation fonctionne correctement, plusieurs échanges doivent avoir lieu sur la même connexion.</span><span class="sxs-lookup"><span data-stu-id="ff716-155">For Negotiate authentication to function correctly, several exchanges must take place on the same connection.</span></span> <span data-ttu-id="ff716-156">Par conséquent, l’authentification Negotiate ne peut pas être utilisée si un proxy intermédiaire ne prend pas en charge les connexions persistantes.</span><span class="sxs-lookup"><span data-stu-id="ff716-156">Therefore, Negotiate authentication cannot be used if an intervening proxy does not support keep-alive connections.</span></span> <span data-ttu-id="ff716-157">L’authentification par négociation échoue également si [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) est utilisé avec l’indicateur de [**désactivation de la fonction de \_ \_ maintien \_**](option-flags.md) de l’activité WinHTTP qui désactive la sémantique Keep-Alive.</span><span class="sxs-lookup"><span data-stu-id="ff716-157">Negotiate authentication also fails if [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) is used with the [**WINHTTP\_DISABLE\_KEEP\_ALIVE**](option-flags.md) flag that disables keep-alive semantics.</span></span> <span data-ttu-id="ff716-158">Le schéma d’authentification Negotiate est parfois appelé authentification Windows intégrée.</span><span class="sxs-lookup"><span data-stu-id="ff716-158">The Negotiate authentication scheme is sometimes called Integrated Windows authentication.</span></span> |



 

## <a name="authentication-in-winhttp-applications"></a><span data-ttu-id="ff716-159">Authentification dans les applications WinHTTP</span><span class="sxs-lookup"><span data-stu-id="ff716-159">Authentication in WinHTTP Applications</span></span>

<span data-ttu-id="ff716-160">L’interface de programmation d’applications (API) WinHTTP fournit deux fonctions utilisées pour accéder aux ressources Internet lorsque l’authentification est nécessaire : [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) et [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes).</span><span class="sxs-lookup"><span data-stu-id="ff716-160">The WinHTTP application programming interface (API) provides two functions used to access Internet resources in situations where authentication is required: [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) and [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes).</span></span>

<span data-ttu-id="ff716-161">Quand une réponse est reçue avec un code d’état 401 ou 407, [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) peut être utilisé pour analyser les en-têtes d’authentification afin de déterminer les schémas d’authentification pris en charge et la cible d’authentification.</span><span class="sxs-lookup"><span data-stu-id="ff716-161">When a response is received with a 401 or 407 status code, [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) can be used to parse the authentication headers to determine the supported authentication schemes and the authentication target.</span></span> <span data-ttu-id="ff716-162">La cible d’authentification est le serveur ou le proxy qui demande l’authentification.</span><span class="sxs-lookup"><span data-stu-id="ff716-162">The authentication target is the server or proxy that requests authentication.</span></span> <span data-ttu-id="ff716-163">**WinHttpQueryAuthSchemes** détermine également le premier schéma d’authentification, à partir des schémas disponibles, en fonction des préférences de schéma d’authentification suggérées par le serveur.</span><span class="sxs-lookup"><span data-stu-id="ff716-163">**WinHttpQueryAuthSchemes** also determines the first authentication scheme, from the available schemes, based on the authentication scheme preferences suggested by the server.</span></span> <span data-ttu-id="ff716-164">Cette méthode de choix d’un schéma d’authentification est le comportement suggéré par [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="ff716-164">This method for choosing an authentication scheme is the behavior suggested by [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

<span data-ttu-id="ff716-165">[**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) permet à une application de spécifier le schéma d’authentification utilisé avec un nom d’utilisateur et un mot de passe valides pour une utilisation sur le serveur ou le proxy cible.</span><span class="sxs-lookup"><span data-stu-id="ff716-165">[**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) enables an application to specify the authentication scheme that is used along with a valid username and password for use on the target server or proxy.</span></span> <span data-ttu-id="ff716-166">Après avoir défini les informations d’identification et renvoyé la demande, les en-têtes nécessaires sont générés et ajoutés automatiquement à la demande.</span><span class="sxs-lookup"><span data-stu-id="ff716-166">After setting the credentials and resending the request, the necessary headers are generated and added to the request automatically.</span></span> <span data-ttu-id="ff716-167">Étant donné que certains schémas d’authentification requièrent plusieurs transactions, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) peut renvoyer l’erreur, erreur WinHTTP de renvoi de \_ \_ \_ demande.</span><span class="sxs-lookup"><span data-stu-id="ff716-167">Because some authentication schemes require multiple transactions [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) could return the error, ERROR\_WINHTTP\_RESEND\_REQUEST.</span></span> <span data-ttu-id="ff716-168">Lorsque cette erreur se produit, l’application doit continuer à renvoyer la demande jusqu’à la réception d’une réponse qui ne contient pas de code d’état 401 ou 407.</span><span class="sxs-lookup"><span data-stu-id="ff716-168">When this error is encountered, the application should continue to resend the request until a response is received that does not contain a 401 or 407 status code.</span></span> <span data-ttu-id="ff716-169">Un code d’état 200 indique que la ressource est disponible et que la demande est réussie.</span><span class="sxs-lookup"><span data-stu-id="ff716-169">A 200 status code indicates that the resource is available and the request is successful.</span></span> <span data-ttu-id="ff716-170">Consultez [**codes d’État http**](http-status-codes.md) pour obtenir des codes d’État supplémentaires qui peuvent être retournés.</span><span class="sxs-lookup"><span data-stu-id="ff716-170">See [**HTTP Status Codes**](http-status-codes.md) for additional status codes that can be returned.</span></span>

<span data-ttu-id="ff716-171">Si un schéma d’authentification et des informations d’identification acceptables sont connus avant l’envoi d’une demande au serveur, une application peut appeler [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) avant d’appeler [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="ff716-171">If an acceptable authentication scheme and credentials are known before a request is sent to the server, an application can call [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) before calling [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="ff716-172">Dans ce cas, WinHTTP tente une pré-authentification avec le serveur en fournissant des informations d’identification ou des [*données d’authentification*](glossary.md) dans la demande initiale au serveur.</span><span class="sxs-lookup"><span data-stu-id="ff716-172">In this case, WinHTTP attempts pre-authentication with the server by providing credentials or [*authentication data*](glossary.md) in the initial request to the server.</span></span> <span data-ttu-id="ff716-173">La pré-authentification peut réduire le nombre d’échanges dans le processus d’authentification et, par conséquent, améliorer les performances de l’application.</span><span class="sxs-lookup"><span data-stu-id="ff716-173">Pre-authentication can decrease the number of exchanges in the authentication process and therefore improve application performance.</span></span>

<span data-ttu-id="ff716-174">La pré-authentification peut être utilisée avec les schémas d’authentification suivants :</span><span class="sxs-lookup"><span data-stu-id="ff716-174">Preauthentication can be used with the following authentication schemes:</span></span>

-   <span data-ttu-id="ff716-175">De base-toujours possible.</span><span class="sxs-lookup"><span data-stu-id="ff716-175">Basic - always possible.</span></span>
-   <span data-ttu-id="ff716-176">Négocier la résolution dans Kerberos-probablement possible ; la seule exception est lorsque les décalages de temps sont désactivés entre le client et le contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="ff716-176">Negotiate resolving into Kerberos - very likely possible; the only exception is when the time-skews are off between the client and the domain controller.</span></span>
-   <span data-ttu-id="ff716-177">(Négocier la résolution dans NTLM)-jamais possible.</span><span class="sxs-lookup"><span data-stu-id="ff716-177">(Negotiate resolving into NTLM) - never possible.</span></span>
-   <span data-ttu-id="ff716-178">NTLM-possible dans Windows Server 2008 R2 uniquement.</span><span class="sxs-lookup"><span data-stu-id="ff716-178">NTLM - possible in Windows Server 2008 R2 only.</span></span>
-   <span data-ttu-id="ff716-179">Digest-jamais possible.</span><span class="sxs-lookup"><span data-stu-id="ff716-179">Digest - never possible.</span></span>
-   <span data-ttu-id="ff716-180">Passport-jamais possible ; après la stimulation-réponse initiale, WinHTTP utilise des cookies pour se pré-authentifier auprès de Passport.</span><span class="sxs-lookup"><span data-stu-id="ff716-180">Passport - never possible; after the initial challenge-response, WinHTTP uses cookies to pre-authenticate to Passport.</span></span>

<span data-ttu-id="ff716-181">Une application WinHTTP standard effectue les étapes suivantes afin de gérer l’authentification.</span><span class="sxs-lookup"><span data-stu-id="ff716-181">A typical WinHTTP application completes the following steps in order to handle authentication.</span></span>

-   <span data-ttu-id="ff716-182">Demandez une ressource avec [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) et [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="ff716-182">Request a resource with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) and [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>
-   <span data-ttu-id="ff716-183">Vérifiez les en-têtes de réponse avec [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span><span class="sxs-lookup"><span data-stu-id="ff716-183">Check the response headers with [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>
-   <span data-ttu-id="ff716-184">Si un code d’état 401 ou 407 est retourné, indiquant que l’authentification est requise, appelez [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) pour trouver un schéma acceptable.</span><span class="sxs-lookup"><span data-stu-id="ff716-184">If a 401 or 407 status code is returned indicating that authentication is required, call [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) to find an acceptable scheme.</span></span>
-   <span data-ttu-id="ff716-185">Définissez le schéma d’authentification, le nom d’utilisateur et le mot de passe avec [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials).</span><span class="sxs-lookup"><span data-stu-id="ff716-185">Set the authentication scheme, username, and password with [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials).</span></span>
-   <span data-ttu-id="ff716-186">Renvoyez la requête avec le même handle de demande en appelant [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="ff716-186">Resend the request with the same request handle by calling [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

<span data-ttu-id="ff716-187">Les informations d’identification définies par [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) sont utilisées uniquement pour une demande.</span><span class="sxs-lookup"><span data-stu-id="ff716-187">The credentials set by [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) are only used for one request.</span></span> <span data-ttu-id="ff716-188">WinHTTP ne met pas en cache les informations d’identification à utiliser dans d’autres requêtes, ce qui signifie que les applications doivent être écrites pour répondre à plusieurs demandes.</span><span class="sxs-lookup"><span data-stu-id="ff716-188">WinHTTP does not cache the credentials to use in other requests, which means that applications must be written that can respond to multiple requests.</span></span> <span data-ttu-id="ff716-189">Si une connexion authentifiée est réutilisée, les autres demandes peuvent ne pas être renouvelées, mais votre code doit être en mesure de répondre à une demande à tout moment.</span><span class="sxs-lookup"><span data-stu-id="ff716-189">If an authenticated connection is re-used, other requests may not be challenged, but your code should be able to respond to a request at any time.</span></span>

### <a name="example-retrieving-a-document"></a><span data-ttu-id="ff716-190">Exemple : extraction d’un document</span><span class="sxs-lookup"><span data-stu-id="ff716-190">Example: Retrieving a Document</span></span>

<span data-ttu-id="ff716-191">L’exemple de code suivant tente de récupérer un document spécifié à partir d’un serveur HTTP.</span><span class="sxs-lookup"><span data-stu-id="ff716-191">The following sample code attempts to retrieve a specified document from an HTTP server.</span></span> <span data-ttu-id="ff716-192">Le code d’État est récupéré à partir de la réponse pour déterminer si l’authentification est requise.</span><span class="sxs-lookup"><span data-stu-id="ff716-192">The status code is retrieved from the response to determine if authentication is required.</span></span> <span data-ttu-id="ff716-193">Si un code d’état 200 est trouvé, le document est disponible.</span><span class="sxs-lookup"><span data-stu-id="ff716-193">If a 200 status code is found, the document is available.</span></span> <span data-ttu-id="ff716-194">Si le code d’état 401 ou 407 est trouvé, l’authentification est requise avant que le document puisse être récupéré.</span><span class="sxs-lookup"><span data-stu-id="ff716-194">If a status code of 401 or 407 is found, authentication is required before the document can be retrieved.</span></span> <span data-ttu-id="ff716-195">Pour tout autre code d’État, un message d’erreur s’affiche.</span><span class="sxs-lookup"><span data-stu-id="ff716-195">For any other status code, an error message is displayed.</span></span> <span data-ttu-id="ff716-196">Pour obtenir la liste des codes d’État possibles, consultez [**codes d’État http**](http-status-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="ff716-196">See [**HTTP Status Codes**](http-status-codes.md) for a list of possible status codes.</span></span>


```C++
#include <windows.h>
#include <winhttp.h>
#include <stdio.h>

#pragma comment(lib, "winhttp.lib")

DWORD ChooseAuthScheme( DWORD dwSupportedSchemes )
{
  //  It is the server's responsibility only to accept 
  //  authentication schemes that provide a sufficient
  //  level of security to protect the servers resources.
  //
  //  The client is also obligated only to use an authentication
  //  scheme that adequately protects its username and password.
  //
  //  Thus, this sample code does not use Basic authentication  
  //  becaus Basic authentication exposes the client's username
  //  and password to anyone monitoring the connection.
  
  if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_NEGOTIATE )
    return WINHTTP_AUTH_SCHEME_NEGOTIATE;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_NTLM )
    return WINHTTP_AUTH_SCHEME_NTLM;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_PASSPORT )
    return WINHTTP_AUTH_SCHEME_PASSPORT;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_DIGEST )
    return WINHTTP_AUTH_SCHEME_DIGEST;
  else
    return 0;
}

struct SWinHttpSampleGet
{
  LPCWSTR szServer;
  LPCWSTR szPath;
  BOOL fUseSSL;
  LPCWSTR szServerUsername;
  LPCWSTR szServerPassword;
  LPCWSTR szProxyUsername;
  LPCWSTR szProxyPassword;
};

void WinHttpAuthSample( IN SWinHttpSampleGet *pGetRequest )
{
  DWORD dwStatusCode = 0;
  DWORD dwSupportedSchemes;
  DWORD dwFirstScheme;
  DWORD dwSelectedScheme;
  DWORD dwTarget;
  DWORD dwLastStatus = 0;
  DWORD dwSize = sizeof(DWORD);
  BOOL  bResults = FALSE;
  BOOL  bDone = FALSE;

  DWORD dwProxyAuthScheme = 0;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  INTERNET_PORT nPort = ( pGetRequest->fUseSSL ) ? 
                        INTERNET_DEFAULT_HTTPS_PORT  :
                        INTERNET_DEFAULT_HTTP_PORT;

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, 
                               pGetRequest->szServer, 
                               nPort, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, 
                                   L"GET", 
                                   pGetRequest->szPath,
                                   NULL, 
                                   WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES,
                                   ( pGetRequest->fUseSSL ) ? 
                                       WINHTTP_FLAG_SECURE : 0 );

  // Continue to send a request until status code 
  // is not 401 or 407.
  if( hRequest == NULL )
    bDone = TRUE;

  while( !bDone )
  {
    //  If a proxy authentication challenge was responded to, reset
    //  those credentials before each SendRequest, because the proxy  
    //  may require re-authentication after responding to a 401 or  
    //  to a redirect. If you don't, you can get into a 
    //  407-401-407-401- loop.
    if( dwProxyAuthScheme != 0 )
      bResults = WinHttpSetCredentials( hRequest, 
                                        WINHTTP_AUTH_TARGET_PROXY, 
                                        dwProxyAuthScheme, 
                                        pGetRequest->szProxyUsername,
                                        pGetRequest->szProxyPassword,
                                        NULL );
    // Send a request.
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS,
                                   0,
                                   WINHTTP_NO_REQUEST_DATA,
                                   0, 
                                   0, 
                                   0 );

    // End the request.
    if( bResults )
      bResults = WinHttpReceiveResponse( hRequest, NULL );

    // Resend the request in case of 
    // ERROR_WINHTTP_RESEND_REQUEST error.
    if( !bResults && GetLastError( ) == ERROR_WINHTTP_RESEND_REQUEST)
        continue;

    // Check the status code.
    if( bResults ) 
      bResults = WinHttpQueryHeaders( hRequest, 
                                      WINHTTP_QUERY_STATUS_CODE |
                                      WINHTTP_QUERY_FLAG_NUMBER,
                                      NULL, 
                                      &dwStatusCode, 
                                      &dwSize, 
                                      NULL );

    if( bResults )
    {
      switch( dwStatusCode )
      {
        case 200: 
          // The resource was successfully retrieved.
          // You can use WinHttpReadData to read the 
          // contents of the server's response.
          printf( "The resource was successfully retrieved.\n" );
          bDone = TRUE;
          break;

        case 401:
          // The server requires authentication.
          printf(" The server requires authentication. Sending credentials...\n" );

          // Obtain the supported and preferred schemes.
          bResults = WinHttpQueryAuthSchemes( hRequest, 
                                              &dwSupportedSchemes, 
                                              &dwFirstScheme, 
                                              &dwTarget );

          // Set the credentials before resending the request.
          if( bResults )
          {
            dwSelectedScheme = ChooseAuthScheme( dwSupportedSchemes);

            if( dwSelectedScheme == 0 )
              bDone = TRUE;
            else
              bResults = WinHttpSetCredentials( hRequest, 
                                        dwTarget, 
                                        dwSelectedScheme,
                                        pGetRequest->szServerUsername,
                                        pGetRequest->szServerPassword,
                                        NULL );
          }

          // If the same credentials are requested twice, abort the
          // request.  For simplicity, this sample does not check
          // for a repeated sequence of status codes.
          if( dwLastStatus == 401 )
            bDone = TRUE;

          break;

        case 407:
          // The proxy requires authentication.
          printf( "The proxy requires authentication.  Sending credentials...\n" );

          // Obtain the supported and preferred schemes.
          bResults = WinHttpQueryAuthSchemes( hRequest, 
                                              &dwSupportedSchemes, 
                                              &dwFirstScheme, 
                                              &dwTarget );

          // Set the credentials before resending the request.
          if( bResults )
            dwProxyAuthScheme = ChooseAuthScheme(dwSupportedSchemes);

          // If the same credentials are requested twice, abort the
          // request.  For simplicity, this sample does not check 
          // for a repeated sequence of status codes.
          if( dwLastStatus == 407 )
            bDone = TRUE;
          break;

        default:
          // The status code does not indicate success.
          printf("Error. Status code %d returned.\n", dwStatusCode);
          bDone = TRUE;
      }
    }

    // Keep track of the last status code.
    dwLastStatus = dwStatusCode;

    // If there are any errors, break out of the loop.
    if( !bResults ) 
        bDone = TRUE;
  }

  // Report any errors.
  if( !bResults )
  {
    DWORD dwLastError = GetLastError( );
    printf( "Error %d has occurred.\n", dwLastError );
  }

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
}

```



## <a name="automatic-logon-policy"></a><span data-ttu-id="ff716-197">Stratégie d’ouverture de session automatique</span><span class="sxs-lookup"><span data-stu-id="ff716-197">Automatic Logon Policy</span></span>

<span data-ttu-id="ff716-198">La stratégie de connexion automatique (ouverture de session automatique) détermine le moment où il est acceptable pour WinHTTP d’inclure les informations d’identification par défaut dans une demande.</span><span class="sxs-lookup"><span data-stu-id="ff716-198">The automatic logon (auto-logon) policy determines when it is acceptable for WinHTTP to include the default credentials in a request.</span></span> <span data-ttu-id="ff716-199">Les informations d’identification par défaut sont le jeton de thread actuel ou le jeton de session, selon que WinHTTP est utilisé en mode synchrone ou asynchrone.</span><span class="sxs-lookup"><span data-stu-id="ff716-199">The default credentials are either the current thread token or the session token depending on whether WinHTTP is used in synchronous or asynchronous mode.</span></span> <span data-ttu-id="ff716-200">Le jeton de thread est utilisé en mode synchrone, et le jeton de session est utilisé en mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="ff716-200">The thread token is used in synchronous mode, and the session token is used in asynchronous mode.</span></span> <span data-ttu-id="ff716-201">Ces informations d’identification par défaut sont souvent le nom d’utilisateur et le mot de passe utilisés pour se connecter à Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ff716-201">These default credentials are often the username and password used to log on to Microsoft Windows.</span></span>

<span data-ttu-id="ff716-202">La stratégie d’ouverture de session automatique a été implémentée pour éviter que ces informations d’identification ne soient utilisées de façon illégale pour l’authentification auprès d’un serveur non approuvé.</span><span class="sxs-lookup"><span data-stu-id="ff716-202">The auto-logon policy was implemented to prevent these credentials from being casually used to authenticate against an untrusted server.</span></span> <span data-ttu-id="ff716-203">Par défaut, le niveau de sécurité est défini sur le \_ niveau de sécurité WinHTTP AUTOlogon \_ \_ \_ , ce qui permet d’utiliser les informations d’identification par défaut uniquement pour les requêtes intranet.</span><span class="sxs-lookup"><span data-stu-id="ff716-203">By default, the security level is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM, which allows the default credentials to be used only for Intranet requests.</span></span> <span data-ttu-id="ff716-204">La stratégie d’ouverture de session automatique s’applique uniquement aux schémas d’authentification NTLM et Negotiate.</span><span class="sxs-lookup"><span data-stu-id="ff716-204">The auto-logon policy only applies to the NTLM and Negotiate authentication schemes.</span></span> <span data-ttu-id="ff716-205">Les informations d’identification ne sont jamais transmises automatiquement avec d’autres schémas.</span><span class="sxs-lookup"><span data-stu-id="ff716-205">Credentials are never automatically transmitted with other schemes.</span></span>

<span data-ttu-id="ff716-206">La stratégie d’ouverture de session automatique peut être définie à l’aide de la fonction [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) avec l’option WinHTTP de l’indicateur de [**\_ \_ \_ stratégie AutoLogon**](option-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="ff716-206">The auto-logon policy can be set using the [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) function with the [**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**](option-flags.md) flag.</span></span> <span data-ttu-id="ff716-207">Cet indicateur s’applique uniquement au handle de demande.</span><span class="sxs-lookup"><span data-stu-id="ff716-207">This flag applies only to the request handle.</span></span> <span data-ttu-id="ff716-208">Lorsque la stratégie est définie sur le niveau de sécurité WINHTTP ouverture de la stratégie \_ \_ \_ \_ faible, les informations d’identification par défaut peuvent être envoyées à tous les serveurs.</span><span class="sxs-lookup"><span data-stu-id="ff716-208">When the policy is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW, default credentials can be sent to all servers.</span></span> <span data-ttu-id="ff716-209">Lorsque la stratégie est définie sur le \_ niveau de sécurité WinHTTP AUTOlogon \_ \_ \_ élevé, les informations d’identification par défaut ne peuvent pas être utilisées pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="ff716-209">When the policy is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH, default credentials cannot be used for authentication.</span></span> <span data-ttu-id="ff716-210">Il est fortement recommandé d’utiliser l’ouverture de session automatique au niveau du support.</span><span class="sxs-lookup"><span data-stu-id="ff716-210">It is strongly recommended that you use the auto-logon at the MEDIUM level.</span></span>

## <a name="stored-user-names-and-passwords"></a><span data-ttu-id="ff716-211">Noms d’utilisateur et mots de passe stockés</span><span class="sxs-lookup"><span data-stu-id="ff716-211">Stored User Names and Passwords</span></span>

<span data-ttu-id="ff716-212">Windows XP a introduit le concept de noms d’utilisateurs et de mots de passe stockés.</span><span class="sxs-lookup"><span data-stu-id="ff716-212">Windows XP introduced the concept of Stored User Names and Passwords.</span></span> <span data-ttu-id="ff716-213">Si les informations d’identification Passport d’un utilisateur sont enregistrées via l' **Assistant Inscription Passport** ou la **boîte de dialogue informations d’identification** standard, elles sont enregistrées dans les noms d’utilisateur et mots de passe stockés.</span><span class="sxs-lookup"><span data-stu-id="ff716-213">If a user's Passport credentials are saved through the **Passport Registration Wizard** or the standard **Credential Dialog**, it is saved in the Stored User Names and Passwords.</span></span> <span data-ttu-id="ff716-214">Quand vous utilisez WinHTTP sur Windows XP ou version ultérieure, WinHTTP utilise automatiquement les informations d’identification dans les noms d’utilisateurs et les mots de passe stockés si les informations d’identification ne sont pas définies explicitement.</span><span class="sxs-lookup"><span data-stu-id="ff716-214">When using WinHTTP on Windows XP or later, WinHTTP automatically uses the credentials in the Stored User Names and Passwords if credentials are not explicitly set.</span></span> <span data-ttu-id="ff716-215">Cela est similaire à la prise en charge des informations d’identification d’ouverture de session par défaut pour NTLM/Kerberos.</span><span class="sxs-lookup"><span data-stu-id="ff716-215">This is similar to the support of default logon credentials for NTLM/Kerberos.</span></span> <span data-ttu-id="ff716-216">Toutefois, l’utilisation des informations d’identification Passport par défaut n’est pas soumise aux paramètres de stratégie d’ouverture de session automatique.</span><span class="sxs-lookup"><span data-stu-id="ff716-216">However, use of default Passport credentials is not subject to the automatic logon policy settings.</span></span>

 

 



