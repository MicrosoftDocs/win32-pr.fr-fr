---
title: Gestion de l’authentification
description: Certains proxys et serveurs requièrent une authentification avant d’accorder l’accès aux ressources sur Internet.
ms.assetid: f3752031-30d3-4e35-8eae-1d4971b66bc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e82d8cd93f1010c71560d856793ad06d8bc5d9d5
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380853"
---
# <a name="handling-authentication"></a><span data-ttu-id="3eae8-103">Gestion de l’authentification</span><span class="sxs-lookup"><span data-stu-id="3eae8-103">Handling Authentication</span></span>

<span data-ttu-id="3eae8-104">Certains proxys et serveurs requièrent une authentification avant d’accorder l’accès aux ressources sur Internet.</span><span class="sxs-lookup"><span data-stu-id="3eae8-104">Some proxies and servers require authentication before granting access to resources on the Internet.</span></span> <span data-ttu-id="3eae8-105">Les fonctions WinINet prennent en charge l’authentification du serveur et du proxy pour les sessions http.</span><span class="sxs-lookup"><span data-stu-id="3eae8-105">The WinINet functions support server and proxy authentication for http sessions.</span></span> <span data-ttu-id="3eae8-106">L’authentification des serveurs FTP doit être gérée par la fonction [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) .</span><span class="sxs-lookup"><span data-stu-id="3eae8-106">Authentication of ftp servers must be handled by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function.</span></span> <span data-ttu-id="3eae8-107">Actuellement, l’authentification de la passerelle FTP n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="3eae8-107">Currently, FTP gateway authentication is not supported.</span></span>

## <a name="about-http-authentication"></a><span data-ttu-id="3eae8-108">À propos de l’authentification HTTP</span><span class="sxs-lookup"><span data-stu-id="3eae8-108">About HTTP Authentication</span></span>

<span data-ttu-id="3eae8-109">Si l’authentification est requise, l’application cliente reçoit un code d’état 401, si le serveur requiert une authentification, ou 407, si le proxy requiert une authentification.</span><span class="sxs-lookup"><span data-stu-id="3eae8-109">If authentication is required, the client application receives a status code 401, if the server requires authentication, or 407, if the proxy requires authentication.</span></span> <span data-ttu-id="3eae8-110">Avec le code d’État, le proxy ou le serveur envoie un ou plusieurs en-têtes de réponse d’authentification (Proxy-Authenticate (pour l’authentification du proxy) ou WWW-Authenticate (pour l’authentification du serveur).</span><span class="sxs-lookup"><span data-stu-id="3eae8-110">With the status code, the proxy or server sends one, or more, authenticate response headers—Proxy-Authenticate (for proxy authentication) or WWW-Authenticate (for server authentication).</span></span>

<span data-ttu-id="3eae8-111">Chaque en-tête de réponse Authenticate contient un schéma d’authentification disponible et un domaine.</span><span class="sxs-lookup"><span data-stu-id="3eae8-111">Each authenticate response header contains an available authentication scheme and a realm.</span></span> <span data-ttu-id="3eae8-112">Si plusieurs schémas d’authentification sont pris en charge, le serveur retourne plusieurs en-têtes de réponse d’authentification.</span><span class="sxs-lookup"><span data-stu-id="3eae8-112">If multiple authentication schemes are supported, the server returns multiple authenticate response headers.</span></span> <span data-ttu-id="3eae8-113">La valeur de domaine est sensible à la casse et définit un espace de protection sur le proxy ou le serveur.</span><span class="sxs-lookup"><span data-stu-id="3eae8-113">The realm value is case-sensitive and defines a protection space on the proxy or server.</span></span> <span data-ttu-id="3eae8-114">Par exemple, l’en-tête « WWW-Authenticate : Basic Realm = » exemple «» est un exemple d’en-tête retourné lorsque l’authentification du serveur est requise.</span><span class="sxs-lookup"><span data-stu-id="3eae8-114">For example, the header "WWW-Authenticate: Basic Realm="example"" would be an example of a header returned when server authentication is required.</span></span>

<span data-ttu-id="3eae8-115">L’application cliente qui a envoyé la demande peut s’authentifier en incluant un champ d’en-tête d’autorisation avec la requête.</span><span class="sxs-lookup"><span data-stu-id="3eae8-115">The client application that sent the request can authenticate itself by including an Authorization header field with the request.</span></span> <span data-ttu-id="3eae8-116">L’en-tête Authorization contient le schéma d’authentification et la réponse appropriée requis par ce schéma.</span><span class="sxs-lookup"><span data-stu-id="3eae8-116">The Authorization header would contain the authentication scheme and the appropriate response required by that scheme.</span></span> <span data-ttu-id="3eae8-117">Par exemple, l’en-tête « Authorization : Basic \<username:password> » est ajouté à la demande et renvoyé au serveur si le client a reçu l’en-tête de réponse d’authentification « www-Authenticate : Basic Realm = » example «».</span><span class="sxs-lookup"><span data-stu-id="3eae8-117">For example, the header "Authorization: Basic \<username:password>" would be added to the request and re-sent to the server if the client received the authenticate response header "WWW-Authenticate: Basic Realm="example"".</span></span>

<span data-ttu-id="3eae8-118">Il existe deux types généraux de schémas d’authentification :</span><span class="sxs-lookup"><span data-stu-id="3eae8-118">There are two general types of authentication schemes:</span></span>

-   <span data-ttu-id="3eae8-119">Schéma d’authentification de base, où le nom d’utilisateur et le mot de passe sont envoyés en texte clair au serveur.</span><span class="sxs-lookup"><span data-stu-id="3eae8-119">Basic authentication scheme, where the user name and password are sent in cleartext to the server.</span></span>
-   <span data-ttu-id="3eae8-120">Les schémas de stimulation-réponse, qui permettent un format de stimulation/réponse.</span><span class="sxs-lookup"><span data-stu-id="3eae8-120">Challenge-response schemes, which allow for a challenge-response format.</span></span>

<span data-ttu-id="3eae8-121">Le schéma d’authentification de base est basé sur le modèle qu’un client doit s’authentifier avec un nom d’utilisateur et un mot de passe pour chaque domaine.</span><span class="sxs-lookup"><span data-stu-id="3eae8-121">The Basic authentication scheme is based on the model that a client must authenticate itself with a user name and password for each realm.</span></span> <span data-ttu-id="3eae8-122">Le serveur traite la demande s’il est renvoyé avec un en-tête d’autorisation qui comprend un nom d’utilisateur et un mot de passe valides.</span><span class="sxs-lookup"><span data-stu-id="3eae8-122">The server services the request if it is resent with an Authorization header that includes a valid user name and password.</span></span>

<span data-ttu-id="3eae8-123">Les schémas de stimulation/réponse permettent une authentification plus sécurisée.</span><span class="sxs-lookup"><span data-stu-id="3eae8-123">Challenge-response schemes enable more secure authentication.</span></span> <span data-ttu-id="3eae8-124">Si une demande nécessite une authentification à l’aide d’un modèle de stimulation-réponse, le code d’État et les en-têtes d’authentification appropriés sont retournés au client.</span><span class="sxs-lookup"><span data-stu-id="3eae8-124">If a request requires authentication using a challenge-response scheme, the appropriate status code and Authenticate headers are returned to the client.</span></span> <span data-ttu-id="3eae8-125">Le client doit ensuite renvoyer la demande avec un Negotiate.</span><span class="sxs-lookup"><span data-stu-id="3eae8-125">The client must then to resend the request with a negotiate.</span></span> <span data-ttu-id="3eae8-126">Le serveur renvoie un code d’état approprié avec un défi, et le client a alors besoin de renvoyer la demande avec la réponse appropriée pour obtenir le service demandé.</span><span class="sxs-lookup"><span data-stu-id="3eae8-126">The server would return an appropriate status code with a challenge, and the client would then require to resend the request with the proper response to get the requested service.</span></span>

<span data-ttu-id="3eae8-127">Le tableau suivant répertorie les schémas d’authentification, le type d’authentification, la DLL qui les prend en charge et une description du schéma.</span><span class="sxs-lookup"><span data-stu-id="3eae8-127">The following table lists authentication schemes, the authentication type, the DLL that supports them, and a description of the scheme.</span></span>



| <span data-ttu-id="3eae8-128">Schéma</span><span class="sxs-lookup"><span data-stu-id="3eae8-128">Scheme</span></span>                                    | <span data-ttu-id="3eae8-129">Type</span><span class="sxs-lookup"><span data-stu-id="3eae8-129">Type</span></span>               | <span data-ttu-id="3eae8-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3eae8-130">DLL</span></span>                  | <span data-ttu-id="3eae8-131">Description</span><span class="sxs-lookup"><span data-stu-id="3eae8-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------|--------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3eae8-132">De base (texte en clair)</span><span class="sxs-lookup"><span data-stu-id="3eae8-132">Basic (cleartext)</span></span>                         | <span data-ttu-id="3eae8-133">basic</span><span class="sxs-lookup"><span data-stu-id="3eae8-133">basic</span></span>              | <span data-ttu-id="3eae8-134">Wininet.dll</span><span class="sxs-lookup"><span data-stu-id="3eae8-134">Wininet.dll</span></span>          | <span data-ttu-id="3eae8-135">Utilise une chaîne encodée en base64 qui contient le nom d’utilisateur et le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="3eae8-135">Uses a base64 encoded string that contains the user name and password.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="3eae8-136">Digest</span><span class="sxs-lookup"><span data-stu-id="3eae8-136">Digest</span></span>                                    | <span data-ttu-id="3eae8-137">stimulation-réponse</span><span class="sxs-lookup"><span data-stu-id="3eae8-137">challenge-response</span></span> | <span data-ttu-id="3eae8-138">Digest.dll</span><span class="sxs-lookup"><span data-stu-id="3eae8-138">Digest.dll</span></span>           | <span data-ttu-id="3eae8-139">Un schéma de stimulation/réponse qui est le défi de l’utilisation d’une valeur à usage unique (chaîne de données spécifiée par le serveur).</span><span class="sxs-lookup"><span data-stu-id="3eae8-139">A challenge-response scheme that challenges using a nonce (a server-specified data string) value.</span></span> <span data-ttu-id="3eae8-140">Une réponse valide contient une somme de contrôle du nom d’utilisateur, du mot de passe, de la valeur nonce donnée, de la méthode HTTP et de l’Uniform Resource Identifier (URI) demandé.</span><span class="sxs-lookup"><span data-stu-id="3eae8-140">A valid response contains a checksum of the user name, the password, the given nonce value, the HTTP method, and the requested Uniform Resource Identifier (URI).</span></span> <span data-ttu-id="3eae8-141">La prise en charge de l’authentification Digest a été introduite dans Microsoft Internet Explorer 5.</span><span class="sxs-lookup"><span data-stu-id="3eae8-141">Digest authentication support was introduced in Microsoft Internet Explorer 5.</span></span> |
| <span data-ttu-id="3eae8-142">NT LAN Manager (NTLM)</span><span class="sxs-lookup"><span data-stu-id="3eae8-142">NT LAN Manager (NTLM)</span></span>                     | <span data-ttu-id="3eae8-143">stimulation-réponse</span><span class="sxs-lookup"><span data-stu-id="3eae8-143">challenge-response</span></span> | <span data-ttu-id="3eae8-144">Winsspi.dll</span><span class="sxs-lookup"><span data-stu-id="3eae8-144">Winsspi.dll</span></span>          | <span data-ttu-id="3eae8-145">Un modèle de stimulation-réponse qui fonde le défi sur le nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3eae8-145">A challenge-response scheme that bases the challenge on the user name.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="3eae8-146">Réseau Microsoft (MSN)</span><span class="sxs-lookup"><span data-stu-id="3eae8-146">Microsoft Network (MSN)</span></span>                   | <span data-ttu-id="3eae8-147">stimulation-réponse</span><span class="sxs-lookup"><span data-stu-id="3eae8-147">challenge-response</span></span> | <span data-ttu-id="3eae8-148">Msnsspc.dll</span><span class="sxs-lookup"><span data-stu-id="3eae8-148">Msnsspc.dll</span></span>          | <span data-ttu-id="3eae8-149">Schéma d’authentification de The Microsoft Network.</span><span class="sxs-lookup"><span data-stu-id="3eae8-149">The Microsoft Network's authentication scheme.</span></span>                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="3eae8-150">Authentification par mot de passe distribué (DPA)</span><span class="sxs-lookup"><span data-stu-id="3eae8-150">Distributed Password Authentication (DPA)</span></span> | <span data-ttu-id="3eae8-151">stimulation-réponse</span><span class="sxs-lookup"><span data-stu-id="3eae8-151">challenge-response</span></span> | <span data-ttu-id="3eae8-152">Msapsspc.dll</span><span class="sxs-lookup"><span data-stu-id="3eae8-152">Msapsspc.dll</span></span>         | <span data-ttu-id="3eae8-153">Similaire à l’authentification MSN et est également utilisé par le réseau Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3eae8-153">Similar to MSN authentication and is also used by the Microsoft Network.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="3eae8-154">Authentification par mot de passe distant (RPA)</span><span class="sxs-lookup"><span data-stu-id="3eae8-154">Remote Passphrase Authentication (RPA)</span></span>    | <span data-ttu-id="3eae8-155">CompuServe</span><span class="sxs-lookup"><span data-stu-id="3eae8-155">CompuServe</span></span>         | <span data-ttu-id="3eae8-156">Rpawinet.dll, da.dll</span><span class="sxs-lookup"><span data-stu-id="3eae8-156">Rpawinet.dll, da.dll</span></span> | <span data-ttu-id="3eae8-157">Schéma d’authentification CompuServe.</span><span class="sxs-lookup"><span data-stu-id="3eae8-157">CompuServe authentication scheme.</span></span> <span data-ttu-id="3eae8-158">Pour plus d’informations, consultez les [spécifications du mécanisme RPA](https://www.compuserve.com/).</span><span class="sxs-lookup"><span data-stu-id="3eae8-158">For more information, see the [RPA Mechanism Specifications](https://www.compuserve.com/).</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="3eae8-159">Pour tout autre chose que l’authentification de base, les clés de Registre doivent être configurées en plus de l’installation de la DLL appropriée.</span><span class="sxs-lookup"><span data-stu-id="3eae8-159">For anything other than Basic authentication, the registry keys must be set up in addition to installing the appropriate DLL.</span></span>

<span data-ttu-id="3eae8-160">Si l’authentification est requise, l’indicateur de maintien de la [ \_ \_ \_ connexion à l’indicateur Internet](api-flags.md) doit être utilisé dans l’appel à [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="3eae8-160">If authentication is required, the [INTERNET\_FLAG\_KEEP\_CONNECTION](api-flags.md) flag should be used in the call to [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="3eae8-161">L’indicateur de maintien de la connexion à l' \_ indicateur Internet \_ \_ est requis pour NTLM et d’autres types d’authentification afin de maintenir la connexion lors de l’exécution du processus d’authentification.</span><span class="sxs-lookup"><span data-stu-id="3eae8-161">The INTERNET\_FLAG\_KEEP\_CONNECTION flag is required for NTLM and other types of authentication in order to maintain the connection while completing the authentication process.</span></span> <span data-ttu-id="3eae8-162">Si la connexion n’est pas maintenue, le processus d’authentification doit être redémarré avec le proxy ou le serveur.</span><span class="sxs-lookup"><span data-stu-id="3eae8-162">If the connection is not maintained, the authentication process must be restarted with the proxy or server.</span></span>

<span data-ttu-id="3eae8-163">Les fonctions [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) et [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) s’exécutent correctement, même lorsque l’authentification est requise.</span><span class="sxs-lookup"><span data-stu-id="3eae8-163">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) functions complete successfully even when authentication is required.</span></span> <span data-ttu-id="3eae8-164">La différence est que les données retournées dans les fichiers d’en-tête et [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) recevront une page HTML informant l’utilisateur du code d’État.</span><span class="sxs-lookup"><span data-stu-id="3eae8-164">The difference is, the data returned in the header files and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) would receive an HTML page informing the user of the status code.</span></span>

### <a name="registering-authentication-keys"></a><span data-ttu-id="3eae8-165">Inscription des clés d’authentification</span><span class="sxs-lookup"><span data-stu-id="3eae8-165">Registering Authentication Keys</span></span>

<span data-ttu-id="3eae8-166">\_ \_ La préconfiguration de type ouvert Internet \_ examine les valeurs de Registre **ProxyEnable**, **ProxyServer** et **ProxyOverride**.</span><span class="sxs-lookup"><span data-stu-id="3eae8-166">INTERNET\_OPEN\_TYPE\_PRECONFIG looks at the registry values **ProxyEnable**, **ProxyServer**, and **ProxyOverride**.</span></span> <span data-ttu-id="3eae8-167">Ces valeurs se trouvent sous **HKEY \_ Current \_ User** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Internet Settings**.</span><span class="sxs-lookup"><span data-stu-id="3eae8-167">These values are located under **HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Internet Settings**.</span></span>

<span data-ttu-id="3eae8-168">Pour les schémas d’authentification autres que Basic, une clé doit être ajoutée au Registre sous **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security**.</span><span class="sxs-lookup"><span data-stu-id="3eae8-168">For authentication schemes other than Basic, a key must be added to the registry under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**.</span></span> <span data-ttu-id="3eae8-169">Une valeur **DWORD** , **Flags**, doit être définie avec la valeur appropriée.</span><span class="sxs-lookup"><span data-stu-id="3eae8-169">A **DWORD** value, **Flags**, should be set with the appropriate value.</span></span> <span data-ttu-id="3eae8-170">La liste suivante affiche les valeurs possibles pour la valeur **Flags** .</span><span class="sxs-lookup"><span data-stu-id="3eae8-170">The following list shows the possible values for the **Flags** value.</span></span>

-   <span data-ttu-id="3eae8-171">Contexte unique des indicateurs d’authentification du plug-in \_ \_ \_ \_ \_ par \_ tcpip (valeur = 0x01)</span><span class="sxs-lookup"><span data-stu-id="3eae8-171">PLUGIN\_AUTH\_FLAGS\_UNIQUE\_CONTEXT\_PER\_TCPIP (value=0x01)</span></span>

    <span data-ttu-id="3eae8-172">Chaque socket TCP/IP (Transmission Control Protocol/Internet Protocol) contient un contexte différent.</span><span class="sxs-lookup"><span data-stu-id="3eae8-172">Each Transmission Control Protocol/Internet Protocol (TCP/IP) socket contains a different context.</span></span> <span data-ttu-id="3eae8-173">Dans le cas contraire, un nouveau contexte est passé pour chaque modèle d’URL de domaine ou de bloc.</span><span class="sxs-lookup"><span data-stu-id="3eae8-173">Otherwise, a new context is passed for each realm or block URL template.</span></span>

-   <span data-ttu-id="3eae8-174">Les \_ indicateurs d’authentification de plug-in \_ \_ peuvent \_ gérer \_ l’interface utilisateur (valeur = 0x02)</span><span class="sxs-lookup"><span data-stu-id="3eae8-174">PLUGIN\_AUTH\_FLAGS\_CAN\_HANDLE\_UI (value=0x02)</span></span>

    <span data-ttu-id="3eae8-175">Cette DLL peut gérer ses propres entrées utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3eae8-175">This DLL can handle its own user input.</span></span>

-   <span data-ttu-id="3eae8-176">Les \_ indicateurs d’authentification de plug-in \_ \_ \_ ne peuvent gérer \_ aucun \_ passwd (valeur = 0x04)</span><span class="sxs-lookup"><span data-stu-id="3eae8-176">PLUGIN\_AUTH\_FLAGS\_CAN\_HANDLE\_NO\_PASSWD (value=0x04)</span></span>

    <span data-ttu-id="3eae8-177">Cette DLL peut être en capacité d’effectuer une authentification sans inviter l’utilisateur à entrer un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="3eae8-177">This DLL might be capable of doing an authentication without prompting the user for a password.</span></span>

-   <span data-ttu-id="3eae8-178">Indicateurs d’authentification du plug-in \_ \_ \_ non \_ domaine (valeur = 0x08)</span><span class="sxs-lookup"><span data-stu-id="3eae8-178">PLUGIN\_AUTH\_FLAGS\_NO\_REALM (value=0x08)</span></span>

    <span data-ttu-id="3eae8-179">Cette DLL n’utilise pas de chaîne de domaine http standard.</span><span class="sxs-lookup"><span data-stu-id="3eae8-179">This DLL does not use a standard http realm string.</span></span> <span data-ttu-id="3eae8-180">Toutes les données qui semblent être un domaine sont des données spécifiques au schéma.</span><span class="sxs-lookup"><span data-stu-id="3eae8-180">Any data that appears to be a realm is scheme-specific data.</span></span>

-   <span data-ttu-id="3eae8-181">Indicateurs d’authentification du plug-in \_ \_ \_ Keep \_ Alive \_ non \_ requis (valeur = 0x10)</span><span class="sxs-lookup"><span data-stu-id="3eae8-181">PLUGIN\_AUTH\_FLAGS\_KEEP\_ALIVE\_NOT\_REQUIRED (value=0x10)</span></span>

    <span data-ttu-id="3eae8-182">Cette DLL ne requiert pas de connexion permanente pour sa séquence de stimulation/réponse.</span><span class="sxs-lookup"><span data-stu-id="3eae8-182">This DLL does not require a persistent connection for its challenge-response sequence.</span></span>

<span data-ttu-id="3eae8-183">Par exemple, pour ajouter l’authentification NTLM, vous devez ajouter la clé NTLM à la sécurité du logiciel de l' **\_ \_ ordinateur local** de la \\  \\ **sécurité Microsoft** \\ **Internet Explorer** \\ .</span><span class="sxs-lookup"><span data-stu-id="3eae8-183">For example, to add NTLM authentication, the key NTLM must be added to **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**.</span></span> <span data-ttu-id="3eae8-184">Sous **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security** \\ **NTLM**, la valeur de chaîne, **DLLFile** et une valeur **DWORD** , **Flags**, doit être ajoutée.</span><span class="sxs-lookup"><span data-stu-id="3eae8-184">Under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**\\**NTLM**, the string value, **DLLFile**, and a **DWORD** value, **Flags**, must be added.</span></span> <span data-ttu-id="3eae8-185">**DLLFile** doit avoir la valeur Winsspi.dll et les **indicateurs** doivent avoir la valeur 0x08.</span><span class="sxs-lookup"><span data-stu-id="3eae8-185">**DLLFile** must be set to Winsspi.dll, and **Flags** must be set to 0x08.</span></span>

### <a name="server-authentication"></a><span data-ttu-id="3eae8-186">Authentification du serveur</span><span class="sxs-lookup"><span data-stu-id="3eae8-186">Server Authentication</span></span>

<span data-ttu-id="3eae8-187">Lorsqu’un serveur reçoit une demande qui requiert une authentification, le serveur renvoie un message de code d’état 401.</span><span class="sxs-lookup"><span data-stu-id="3eae8-187">When a server receives a request that requires authentication, the server returns a 401 status code message.</span></span> <span data-ttu-id="3eae8-188">Dans ce message, le serveur doit inclure un ou plusieurs en-têtes de réponse WWW-Authenticate.</span><span class="sxs-lookup"><span data-stu-id="3eae8-188">In that message, the server should include one or more WWW-Authenticate response headers.</span></span> <span data-ttu-id="3eae8-189">Ces en-têtes incluent les méthodes d’authentification disponibles sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="3eae8-189">These headers include the authentication methods the server has available.</span></span> <span data-ttu-id="3eae8-190">WinINet choisit la première méthode qu’il reconnaît.</span><span class="sxs-lookup"><span data-stu-id="3eae8-190">WinINet chooses the first method it recognizes.</span></span>

<span data-ttu-id="3eae8-191">L’authentification de base offre une sécurité faible, sauf si le canal est tout d’abord chiffré avec SSL ou PCT.</span><span class="sxs-lookup"><span data-stu-id="3eae8-191">Basic authentication provides weak security unless the channel is first link-encrypted with SSL or PCT.</span></span>

<span data-ttu-id="3eae8-192">La fonction [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) peut être utilisée pour obtenir les données de nom d’utilisateur et de mot de passe de l’utilisateur, ou une interface utilisateur personnalisée peut être conçue pour obtenir les données.</span><span class="sxs-lookup"><span data-stu-id="3eae8-192">The [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) function can be used to obtain the user name and password data from the user, or a customized user interface can be designed to obtain the data.</span></span>

<span data-ttu-id="3eae8-193">Une interface personnalisée peut utiliser la fonction [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) pour définir les valeurs de [ \_ \_ mot de passe](option-flags.md) de l’option Internet et de l' [ \_ option \_ Internet](option-flags.md) , puis renvoyer la demande au serveur.</span><span class="sxs-lookup"><span data-stu-id="3eae8-193">A custom interface can use the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) function to set the [INTERNET\_OPTION\_PASSWORD](option-flags.md) and [INTERNET\_OPTION\_USERNAME](option-flags.md) values and then resend the request to the server.</span></span>

### <a name="proxy-authentication"></a><span data-ttu-id="3eae8-194">Authentification proxy</span><span class="sxs-lookup"><span data-stu-id="3eae8-194">Proxy Authentication</span></span>

<span data-ttu-id="3eae8-195">Lorsqu’un client tente d’utiliser un proxy qui requiert une authentification, le proxy renvoie un message de code d’État 407 au client.</span><span class="sxs-lookup"><span data-stu-id="3eae8-195">When a client attempts to use a proxy that requires authentication, the proxy returns a 407 status code message to the client.</span></span> <span data-ttu-id="3eae8-196">Dans ce message, le proxy doit inclure un ou plusieurs en-têtes de réponse Proxy-Authenticate.</span><span class="sxs-lookup"><span data-stu-id="3eae8-196">In that message, the proxy should include one or more Proxy-Authenticate response headers.</span></span> <span data-ttu-id="3eae8-197">Ces en-têtes incluent les méthodes d’authentification disponibles à partir du proxy.</span><span class="sxs-lookup"><span data-stu-id="3eae8-197">These headers include the authentication methods available from the proxy.</span></span> <span data-ttu-id="3eae8-198">WinINet choisit la première méthode qu’il reconnaît.</span><span class="sxs-lookup"><span data-stu-id="3eae8-198">WinINet chooses the first method it recognizes.</span></span>

<span data-ttu-id="3eae8-199">La fonction [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) peut être utilisée pour obtenir les données de nom d’utilisateur et de mot de passe de l’utilisateur, ou une interface utilisateur personnalisée peut être conçue.</span><span class="sxs-lookup"><span data-stu-id="3eae8-199">The [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) function can be used to obtain the user name and password data from the user, or a customized user interface can be designed.</span></span>

<span data-ttu-id="3eae8-200">Une interface personnalisée peut utiliser la fonction [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) pour définir le [ \_ \_ \_ mot de passe de l’option Internet](option-flags.md) et les valeurs du [ \_ \_ \_ nom d’utilisateur du proxy](option-flags.md) de l’option Internet, puis renvoyer la demande au proxy.</span><span class="sxs-lookup"><span data-stu-id="3eae8-200">A custom interface can use the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) function to set the [INTERNET\_OPTION\_PROXY\_PASSWORD](option-flags.md) and [INTERNET\_OPTION\_PROXY\_USERNAME](option-flags.md) values and then resend the request to the proxy.</span></span>

<span data-ttu-id="3eae8-201">Si aucun nom d’utilisateur et mot de passe de proxy n’est défini, WinINet tente d’utiliser le nom d’utilisateur et le mot de passe pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="3eae8-201">If no proxy user name and password are set, WinINet attempts to use the user name and password for the server.</span></span> <span data-ttu-id="3eae8-202">Ce comportement permet aux clients d’implémenter la même interface utilisateur personnalisée que celle utilisée pour gérer l’authentification du serveur.</span><span class="sxs-lookup"><span data-stu-id="3eae8-202">This behavior enables clients to implement the same customized user interface used to handle server authentication.</span></span>

## <a name="handling-http-authentication"></a><span data-ttu-id="3eae8-203">Gestion de l’authentification HTTP</span><span class="sxs-lookup"><span data-stu-id="3eae8-203">Handling HTTP Authentication</span></span>

<span data-ttu-id="3eae8-204">L’authentification HTTP peut être gérée à l’aide de [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) ou d’une fonction personnalisée qui utilise [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) ou qui ajoute ses propres en-têtes d’authentification.</span><span class="sxs-lookup"><span data-stu-id="3eae8-204">HTTP authentication can be handled with either [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) or a customized function that uses [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) or adds its own authentication headers.</span></span> <span data-ttu-id="3eae8-205">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) peut examiner les en-têtes associés à un handle [**HINTERNET**](appendix-a-hinternet-handles.md) pour rechercher les erreurs masquées, telles que les codes d’état d’un proxy ou d’un serveur.</span><span class="sxs-lookup"><span data-stu-id="3eae8-205">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) can examine the headers associated with an [**HINTERNET**](appendix-a-hinternet-handles.md) handle to find hidden errors, such as status codes from a proxy or server.</span></span> <span data-ttu-id="3eae8-206">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) peut être utilisée pour définir le nom d’utilisateur et le mot de passe du proxy et du serveur.</span><span class="sxs-lookup"><span data-stu-id="3eae8-206">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) can be used to set the user name and password for the proxy and server.</span></span> <span data-ttu-id="3eae8-207">Pour l’authentification MSN et DPA, [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) doit être utilisé pour définir le nom d’utilisateur et le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="3eae8-207">For MSN and DPA authentication, [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) must be used to set the user name and password.</span></span>

<span data-ttu-id="3eae8-208">Pour toute fonction personnalisée qui ajoute ses propres WWW-Authenticate ou Proxy-Authenticate en-têtes, l’indicateur [Internet \_ Flag \_ no \_ auth](api-flags.md) doit être défini pour désactiver l’authentification.</span><span class="sxs-lookup"><span data-stu-id="3eae8-208">For any customized function that adds its own WWW-Authenticate or Proxy-Authenticate headers, the [INTERNET\_FLAG\_NO\_AUTH](api-flags.md) flag should be set to disable authentication.</span></span>

<span data-ttu-id="3eae8-209">L’exemple suivant montre comment [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) peut être utilisé pour gérer l’authentification http.</span><span class="sxs-lookup"><span data-stu-id="3eae8-209">The following example shows how [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) can be used to handle HTTP authentication.</span></span>


```C++
HINTERNET hOpenHandle,  hConnectHandle, hResourceHandle;
DWORD dwError, dwErrorCode;
HWND hwnd = GetConsoleWindow();

hOpenHandle = InternetOpen(TEXT("Example"),
                           INTERNET_OPEN_TYPE_PRECONFIG, 
                           NULL, NULL, 0);

hConnectHandle = InternetConnect(hOpenHandle,
                                 TEXT("www.server.com"), 
                                 INTERNET_INVALID_PORT_NUMBER,
                                 NULL,
                                 NULL, 
                                 INTERNET_SERVICE_HTTP,
                                 0,0);

hResourceHandle = HttpOpenRequest(hConnectHandle, TEXT("GET"),
                                  TEXT("/premium/default.htm"),
                                  NULL, NULL, NULL, 
                                  INTERNET_FLAG_KEEP_CONNECTION, 0);

resend:

HttpSendRequest(hResourceHandle, NULL, 0, NULL, 0);

// dwErrorCode stores the error code associated with the call to
// HttpSendRequest.  

dwErrorCode = hResourceHandle ? ERROR_SUCCESS : GetLastError();

dwError = InternetErrorDlg(hwnd, hResourceHandle, dwErrorCode, 
                           FLAGS_ERROR_UI_FILTER_FOR_ERRORS | 
                           FLAGS_ERROR_UI_FLAGS_CHANGE_OPTIONS |
                           FLAGS_ERROR_UI_FLAGS_GENERATE_DATA,
                           NULL);

if (dwError == ERROR_INTERNET_FORCE_RETRY)
    goto resend;

// Insert code to read the data from the hResourceHandle
// at this point.

```



<span data-ttu-id="3eae8-210">Dans l’exemple, dwErrorCode est utilisé pour stocker toutes les erreurs associées à l’appel à [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="3eae8-210">In the example, dwErrorCode is used to store any errors associated with the call to [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="3eae8-211">[**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) se termine correctement, même si le proxy ou le serveur requiert une authentification.</span><span class="sxs-lookup"><span data-stu-id="3eae8-211">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) completes successfully, even if the proxy or server requires authentication.</span></span> <span data-ttu-id="3eae8-212">Lorsque le \_ \_ filtre de l’interface utilisateur erreur \_ des indicateurs pour les \_ \_ Erreurs est passé à [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), la fonction vérifie les en-têtes pour les erreurs masquées.</span><span class="sxs-lookup"><span data-stu-id="3eae8-212">When the FLAGS\_ERROR\_UI\_FILTER\_FOR\_ERRORS flag is passed to [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), the function checks the headers for any hidden errors.</span></span> <span data-ttu-id="3eae8-213">Ces erreurs masquées incluent toutes les demandes d’authentification.</span><span class="sxs-lookup"><span data-stu-id="3eae8-213">These hidden errors would include any requests for authentication.</span></span> <span data-ttu-id="3eae8-214">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) affiche la boîte de dialogue appropriée pour inviter l’utilisateur à entrer les données nécessaires.</span><span class="sxs-lookup"><span data-stu-id="3eae8-214">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) displays the appropriate dialog box to prompt the user for the necessary data.</span></span> <span data-ttu-id="3eae8-215">Les indicateurs de l' \_ \_ interface utilisateur erreur indicateurs \_ \_ Générer \_ les données et indicateurs \_ erreur \_ de modification des indicateurs d’interface utilisateur \_ \_ \_ doivent également être passés à [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), de sorte que la fonction construit la structure de données appropriée pour l’erreur et stocke les résultats de la boîte de dialogue dans le handle [**HINTERNET**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="3eae8-215">The FLAGS\_ERROR\_UI\_FLAGS\_GENERATE\_DATA and FLAGS\_ERROR\_UI\_FLAGS\_CHANGE\_OPTIONS flags should also be passed to [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), so that the function constructs the appropriate data structure for the error and stores the results of the dialog box in the [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span>

<span data-ttu-id="3eae8-216">L’exemple de code suivant montre comment l’authentification peut être gérée à l’aide de [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="3eae8-216">The following example code shows how authentication could be handled using [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


```C++
HINTERNET hOpenHandle,  hResourceHandle, hConnectHandle;
DWORD dwStatus;
DWORD dwStatusSize = sizeof(dwStatus);
char strUsername[64], strPassword[64];

// Normally, hOpenHandle, hResourceHandle,
// and hConnectHandle need to be properly assigned.

hOpenHandle = InternetOpen(TEXT("Example"),
                           INTERNET_OPEN_TYPE_PRECONFIG,
                           NULL, NULL, 0);
hConnectHandle = InternetConnect(hOpenHandle,
                                 TEXT("www.server.com"),
                                 INTERNET_INVALID_PORT_NUMBER,
                                 NULL,
                                 NULL,
                                 INTERNET_SERVICE_HTTP,
                                 0,0);

hResourceHandle = HttpOpenRequest(hConnectHandle, TEXT("GET"),
                                  TEXT("/premium/default.htm"),
                                  NULL, NULL, NULL,
                                  INTERNET_FLAG_KEEP_CONNECTION,
                                  0);

resend:

HttpSendRequest(hResourceHandle, NULL, 0, NULL, 0);

HttpQueryInfo(hResourceHandle, HTTP_QUERY_FLAG_NUMBER |
              HTTP_QUERY_STATUS_CODE, &dwStatus, &dwStatusSize, NULL);

switch (dwStatus)
{
    // cchUserLength is the length of strUsername and
    // cchPasswordLength is the length of strPassword.
    DWORD cchUserLength, cchPasswordLength;

    case HTTP_STATUS_PROXY_AUTH_REQ: // Proxy Authentication Required
        // Insert code to set strUsername and strPassword.

        // Insert code to safely determine cchUserLength and
        // cchPasswordLength. Insert appropriate error handling code.
        InternetSetOption(hResourceHandle,
                          INTERNET_OPTION_PROXY_USERNAME,
                          strUsername,
                          cchUserLength+1);

        InternetSetOption(hResourceHandle,
                          INTERNET_OPTION_PROXY_PASSWORD,
                          strPassword,
                          cchPasswordLength+1);
        goto resend;
        break;

    case HTTP_STATUS_DENIED:     // Server Authentication Required.
        // Insert code to set strUsername and strPassword.

        // Insert code to safely determine cchUserLength and
        // cchPasswordLength. Insert error handling code as
        // appropriate.
        InternetSetOption(hResourceHandle, INTERNET_OPTION_USERNAME,
                          strUsername, cchUserLength+1);
        InternetSetOption(hResourceHandle, INTERNET_OPTION_PASSWORD,
                          strPassword, cchPasswordLength+1);
        goto resend;
        break;
}

// Insert code to read the data from the hResourceHandle
// at this point.

```



> [!Note]  
> <span data-ttu-id="3eae8-217">WinINet ne prend pas en charge les implémentations de serveur.</span><span class="sxs-lookup"><span data-stu-id="3eae8-217">WinINet does not support server implementations.</span></span> <span data-ttu-id="3eae8-218">En outre, il ne doit pas être utilisé à partir d’un service.</span><span class="sxs-lookup"><span data-stu-id="3eae8-218">In addition, it should not be used from a service.</span></span> <span data-ttu-id="3eae8-219">Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="3eae8-219">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 