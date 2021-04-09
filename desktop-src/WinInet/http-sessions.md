---
title: Sessions HTTP
description: Les ressources sur le Web sont accessibles à l’aide de http.
ms.assetid: 0f307e28-9c38-41e7-9795-7eef08e99a3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b0b4d30bc86c588495a55ed4867a4084c43a09
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101865"
---
# <a name="http-sessions"></a><span data-ttu-id="52ff8-103">Sessions HTTP</span><span class="sxs-lookup"><span data-stu-id="52ff8-103">HTTP Sessions</span></span>

<span data-ttu-id="52ff8-104">WinINet vous permet d’accéder aux ressources du World Wide Web (WWW).</span><span class="sxs-lookup"><span data-stu-id="52ff8-104">WinINet enables you to access resources on the World Wide Web (WWW).</span></span> <span data-ttu-id="52ff8-105">Vous pouvez accéder directement à ces ressources à l’aide de [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (pour plus d’informations, consultez [accès direct aux URL](handling-uniform-resource-locators.md)).</span><span class="sxs-lookup"><span data-stu-id="52ff8-105">These resources can be accessed directly by using [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for more information, see [Accessing URLs Directly](handling-uniform-resource-locators.md)).</span></span>

<span data-ttu-id="52ff8-106">Les ressources sur le Web sont accessibles à l’aide de http.</span><span class="sxs-lookup"><span data-stu-id="52ff8-106">Resources on the WWW are accessed by using http.</span></span> <span data-ttu-id="52ff8-107">Les fonctions HTTP gèrent les protocoles sous-jacents, tout en permettant à votre application d’accéder à des informations sur le Web.</span><span class="sxs-lookup"><span data-stu-id="52ff8-107">The HTTP functions handle the underlying protocols, while allowing your application to access information on the WWW.</span></span> <span data-ttu-id="52ff8-108">À mesure que le protocole HTTP évolue, les protocoles sous-jacents sont mis à jour pour maintenir le comportement de la fonction.</span><span class="sxs-lookup"><span data-stu-id="52ff8-108">As the HTTP protocol evolves, the underlying protocols are updated to maintain function behavior.</span></span>

<span data-ttu-id="52ff8-109">Le diagramme suivant montre les relations des fonctions utilisées avec le protocole HTTP.</span><span class="sxs-lookup"><span data-stu-id="52ff8-109">The following diagram shows the relationships of the functions that are used with the HTTP protocol.</span></span> <span data-ttu-id="52ff8-110">Les zones grisées représentent des fonctions qui retournent des handles [**HINTERNET**](appendix-a-hinternet-handles.md) , tandis que les zones simples représentent des fonctions qui utilisent le descripteur **HINTERNET** créé par la fonction sur laquelle ils dépendent.</span><span class="sxs-lookup"><span data-stu-id="52ff8-110">The shaded boxes represent functions that return [**HINTERNET**](appendix-a-hinternet-handles.md) handles, while the plain boxes represent functions that use the **HINTERNET** handle created by the function on which they depend.</span></span>

![fonctions WinInet utilisées pour http](images/ax-wnt05.png)

<span data-ttu-id="52ff8-112">Pour plus d’informations, consultez [Handles HINTERNET](appendix-a-hinternet-handles.md).</span><span class="sxs-lookup"><span data-stu-id="52ff8-112">For more information, see [HINTERNET Handles](appendix-a-hinternet-handles.md).</span></span>

## <a name="using-the-wininet-functions-to-access-the-www"></a><span data-ttu-id="52ff8-113">Utilisation des fonctions WinINet pour accéder au Web</span><span class="sxs-lookup"><span data-stu-id="52ff8-113">Using the WinINet Functions to Access the WWW</span></span>

-   [<span data-ttu-id="52ff8-114">Initiation d’une connexion au Web</span><span class="sxs-lookup"><span data-stu-id="52ff8-114">Initiating a Connection to the WWW</span></span>](#initiating-a-connection-to-the-www)
-   [<span data-ttu-id="52ff8-115">Ouverture d’une demande</span><span class="sxs-lookup"><span data-stu-id="52ff8-115">Opening a Request</span></span>](#opening-a-request)
-   [<span data-ttu-id="52ff8-116">Ajout d’en-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="52ff8-116">Adding Request Headers</span></span>](#adding-request-headers)
-   [<span data-ttu-id="52ff8-117">Envoi d’une demande</span><span class="sxs-lookup"><span data-stu-id="52ff8-117">Sending a Request</span></span>](#sending-a-request)
-   [<span data-ttu-id="52ff8-118">Publication des données sur le serveur</span><span class="sxs-lookup"><span data-stu-id="52ff8-118">Posting Data to the Server</span></span>](#posting-data-to-the-server)
-   [<span data-ttu-id="52ff8-119">Obtention d’informations sur une demande</span><span class="sxs-lookup"><span data-stu-id="52ff8-119">Getting Information About a Request</span></span>](#getting-information-about-a-request)
-   [<span data-ttu-id="52ff8-120">Téléchargement des ressources à partir du Web</span><span class="sxs-lookup"><span data-stu-id="52ff8-120">Downloading Resources from the WWW</span></span>](#downloading-resources-from-the-www)

<span data-ttu-id="52ff8-121">Les fonctions suivantes sont utilisées pendant les sessions HTTP pour accéder au Web.</span><span class="sxs-lookup"><span data-stu-id="52ff8-121">The following functions are used during HTTP sessions to access the WWW.</span></span>



| <span data-ttu-id="52ff8-122">Fonction</span><span class="sxs-lookup"><span data-stu-id="52ff8-122">Function</span></span>                                               | <span data-ttu-id="52ff8-123">Description</span><span class="sxs-lookup"><span data-stu-id="52ff8-123">Description</span></span>                                                                                                                                                                                  |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="52ff8-124">**HttpAddRequestHeaders**</span><span class="sxs-lookup"><span data-stu-id="52ff8-124">**HttpAddRequestHeaders**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) | <span data-ttu-id="52ff8-125">Ajoute des en-têtes de requête HTTP au descripteur de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="52ff8-125">Adds HTTP request headers to the HTTP request handle.</span></span> <span data-ttu-id="52ff8-126">Cette fonction requiert un handle créé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="52ff8-126">This function requires a handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>                                                 |
| [<span data-ttu-id="52ff8-127">**HttpOpenRequest**</span><span class="sxs-lookup"><span data-stu-id="52ff8-127">**HttpOpenRequest**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)             | <span data-ttu-id="52ff8-128">Ouvre un handle de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="52ff8-128">Opens an HTTP request handle.</span></span> <span data-ttu-id="52ff8-129">Cette fonction requiert un handle créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="52ff8-129">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                                                         |
| [<span data-ttu-id="52ff8-130">**HttpQueryInfo**</span><span class="sxs-lookup"><span data-stu-id="52ff8-130">**HttpQueryInfo**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)                 | <span data-ttu-id="52ff8-131">Interroge les informations relatives à une requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="52ff8-131">Queries information about an HTTP request.</span></span> <span data-ttu-id="52ff8-132">Cette fonction requiert un handle créé par la fonction [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) ou [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="52ff8-132">This function requires a handle created by the [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span> |
| [<span data-ttu-id="52ff8-133">**HttpSendRequest**</span><span class="sxs-lookup"><span data-stu-id="52ff8-133">**HttpSendRequest**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)             | <span data-ttu-id="52ff8-134">Envoie la requête HTTP spécifiée au serveur HTTP.</span><span class="sxs-lookup"><span data-stu-id="52ff8-134">Sends the specified HTTP request to the HTTP server.</span></span> <span data-ttu-id="52ff8-135">Cette fonction requiert un handle créé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="52ff8-135">This function requires a handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>                                                  |
| [<span data-ttu-id="52ff8-136">**InternetErrorDlg**</span><span class="sxs-lookup"><span data-stu-id="52ff8-136">**InternetErrorDlg**</span></span>](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)           | <span data-ttu-id="52ff8-137">Affiche des boîtes de dialogue prédéfinies pour les conditions d’erreur Internet courantes.</span><span class="sxs-lookup"><span data-stu-id="52ff8-137">Displays predefined dialog boxes for common Internet error conditions.</span></span> <span data-ttu-id="52ff8-138">Cette fonction requiert le handle utilisé dans l’appel à [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="52ff8-138">This function requires the handle used in the call to [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span>                     |



 

### <a name="initiating-a-connection-to-the-www"></a><span data-ttu-id="52ff8-139">Initiation d’une connexion au Web</span><span class="sxs-lookup"><span data-stu-id="52ff8-139">Initiating a Connection to the WWW</span></span>

<span data-ttu-id="52ff8-140">Pour démarrer une connexion au Web, l’application doit appeler la fonction [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) sur le [**HINTERNET**](appendix-a-hinternet-handles.md) racine retourné par [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="52ff8-140">To start a connection to the WWW, the application must call the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function on the root [**HINTERNET**](appendix-a-hinternet-handles.md) returned by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="52ff8-141">[**Internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) doit établir une session http en déclarant le type de \_ service http du service Internet \_ .</span><span class="sxs-lookup"><span data-stu-id="52ff8-141">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) must establish an HTTP session by declaring the INTERNET\_SERVICE\_HTTP service type.</span></span> <span data-ttu-id="52ff8-142">Pour plus d’informations sur l’utilisation de [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), consultez [utilisation de internetconnect](enabling-internet-functionality.md).</span><span class="sxs-lookup"><span data-stu-id="52ff8-142">For more information on using [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), see [Using InternetConnect](enabling-internet-functionality.md).</span></span>

### <a name="opening-a-request"></a><span data-ttu-id="52ff8-143">Ouverture d’une demande</span><span class="sxs-lookup"><span data-stu-id="52ff8-143">Opening a Request</span></span>

<span data-ttu-id="52ff8-144">La fonction [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) ouvre une requête HTTP et retourne un descripteur [**HINTERNET**](appendix-a-hinternet-handles.md) qui peut être utilisé par les autres fonctions http.</span><span class="sxs-lookup"><span data-stu-id="52ff8-144">The [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function opens an HTTP request and returns an [**HINTERNET**](appendix-a-hinternet-handles.md) handle that can be used by the other HTTP functions.</span></span> <span data-ttu-id="52ff8-145">Contrairement aux autres fonctions ouvertes (telles que [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) n’envoie pas la requête à Internet lorsqu’elle est appelée.</span><span class="sxs-lookup"><span data-stu-id="52ff8-145">Unlike the other open functions (such as [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) does not send the request to the Internet when called.</span></span> <span data-ttu-id="52ff8-146">La fonction [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) envoie la demande et établit une connexion sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="52ff8-146">The [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) function sends the request and establishes a connection over the network.</span></span>

<span data-ttu-id="52ff8-147">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) accepte un descripteur de session http créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) et un verbe http, un nom d’objet, une chaîne de version, un point d’interconnexion, des types d’acceptation, des indicateurs et une valeur de contexte.</span><span class="sxs-lookup"><span data-stu-id="52ff8-147">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) takes an HTTP session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) and an HTTP verb, object name, version string, referrer, accept types, flags, and context value.</span></span>

<span data-ttu-id="52ff8-148">Le verbe HTTP est une chaîne à utiliser dans la demande.</span><span class="sxs-lookup"><span data-stu-id="52ff8-148">The HTTP verb is a string to be used in the request.</span></span> <span data-ttu-id="52ff8-149">Les verbes HTTP courants utilisés dans les demandes sont les suivants : obtient, PUT et poster.</span><span class="sxs-lookup"><span data-stu-id="52ff8-149">Common HTTP verbs used in requests include GET, PUT, and POST.</span></span> <span data-ttu-id="52ff8-150">Si cette valeur est définie sur **null**, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) utilise la valeur par défaut obten.</span><span class="sxs-lookup"><span data-stu-id="52ff8-150">If this value is set to **NULL**, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) uses the default value GET.</span></span>

<span data-ttu-id="52ff8-151">Le nom de l’objet est une chaîne qui contient le nom de l’objet cible du verbe HTTP spécifié.</span><span class="sxs-lookup"><span data-stu-id="52ff8-151">The object name is a string that contains the name of the specified HTTP verb's target object.</span></span> <span data-ttu-id="52ff8-152">Il s’agit généralement d’un nom de fichier, d’un module exécutable ou d’un spécificateur de recherche.</span><span class="sxs-lookup"><span data-stu-id="52ff8-152">This is generally a file name, an executable module, or a search specifier.</span></span> <span data-ttu-id="52ff8-153">Si le nom d’objet fourni est une chaîne vide, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) recherche la page par défaut.</span><span class="sxs-lookup"><span data-stu-id="52ff8-153">If the object name supplied is an empty string, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) looks for the default page.</span></span>

<span data-ttu-id="52ff8-154">La chaîne de version doit contenir la version HTTP.</span><span class="sxs-lookup"><span data-stu-id="52ff8-154">The version string should contain the HTTP version.</span></span> <span data-ttu-id="52ff8-155">Si ce paramètre a la **valeur null**, la fonction utilise « http/1.1 ».</span><span class="sxs-lookup"><span data-stu-id="52ff8-155">If this parameter is **NULL**, the function uses ""HTTP/1.1"".</span></span>

<span data-ttu-id="52ff8-156">Le référent spécifie l’adresse du document à partir duquel le nom de l’objet a été obtenu.</span><span class="sxs-lookup"><span data-stu-id="52ff8-156">The referrer specifies the address of the document from which the object name was obtained.</span></span> <span data-ttu-id="52ff8-157">Si ce paramètre a la **valeur null**, aucun référent n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="52ff8-157">If this parameter is **NULL**, no referrer is specified.</span></span>

<span data-ttu-id="52ff8-158">La chaîne terminée par le caractère **null** qui contient les types Accept indique les types de contenu acceptés par l’application.</span><span class="sxs-lookup"><span data-stu-id="52ff8-158">The **null**-terminated string that contains the accept types indicates the content types accepted by the application.</span></span> <span data-ttu-id="52ff8-159">Si ce paramètre a la **valeur null** , cela signifie qu’aucun type de contenu n’est accepté par l’application.</span><span class="sxs-lookup"><span data-stu-id="52ff8-159">Setting this parameter to **NULL** indicates that no content types are accepted by the application.</span></span> <span data-ttu-id="52ff8-160">Si une chaîne vide est fournie, l’application indique qu’elle accepte uniquement les documents de type "" Text/ \* "".</span><span class="sxs-lookup"><span data-stu-id="52ff8-160">If an empty string is supplied, the application indicates it accepts only documents of type ""text/\*"".</span></span> <span data-ttu-id="52ff8-161">La valeur « "Text/ \* " » indique des documents texte uniquement, et non des images ou d’autres fichiers binaires.</span><span class="sxs-lookup"><span data-stu-id="52ff8-161">The value ""text/\*"" indicates text-only documents—not pictures or other binary files.</span></span>

<span data-ttu-id="52ff8-162">Les valeurs d’indicateur contrôlent la mise en cache, les cookies et les problèmes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="52ff8-162">The flag values control caching, cookies, and security issues.</span></span> <span data-ttu-id="52ff8-163">Pour Microsoft Network (MSN), NTLM et d’autres types d’authentification, définissez l’indicateur de maintien de la [ \_ \_ \_ connexion à l’indicateur Internet](api-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="52ff8-163">For Microsoft Network (MSN), NTLM, and other types of authentication, set the [INTERNET\_FLAG\_KEEP\_CONNECTION](api-flags.md) flag.</span></span>

<span data-ttu-id="52ff8-164">Si l' [indicateur \_ \_ Async de l’indicateur Internet](api-flags.md) a été défini dans l’appel à [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), une valeur de contexte différente de zéro doit être définie pour une opération asynchrone appropriée.</span><span class="sxs-lookup"><span data-stu-id="52ff8-164">If the [INTERNET\_FLAG\_ASYNC](api-flags.md) flag was set in the call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), a nonzero context value should be set for proper asynchronous operation.</span></span>

<span data-ttu-id="52ff8-165">L’exemple suivant est un exemple d’appel à [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="52ff8-165">The following example is a sample call to [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>

`hHttpRequest = HttpOpenRequest( hHttpSession, "GET", "", NULL, "", NULL, 0, 0);`

### <a name="adding-request-headers"></a><span data-ttu-id="52ff8-166">Ajout d’en-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="52ff8-166">Adding Request Headers</span></span>

<span data-ttu-id="52ff8-167">La fonction [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) permet aux applications d’ajouter un ou plusieurs en-têtes de demande à la requête initiale.</span><span class="sxs-lookup"><span data-stu-id="52ff8-167">The [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) function enables applications to add one or more request headers to the initial request.</span></span> <span data-ttu-id="52ff8-168">Cette fonction permet à une application d’ajouter des en-têtes de format libre supplémentaires au handle de requête HTTP. elle est destinée à être utilisée par des applications sophistiquées qui requièrent un contrôle précis sur la requête envoyée au serveur HTTP.</span><span class="sxs-lookup"><span data-stu-id="52ff8-168">This function allows an application to append additional free-format headers to the HTTP request handle; it is intended for use by sophisticated applications that require precise control over the request sent to the HTTP server.</span></span>

<span data-ttu-id="52ff8-169">[**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) a besoin d’un handle de requête http créé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), d’une chaîne qui contient les en-têtes, de la longueur des en-têtes et des modificateurs.</span><span class="sxs-lookup"><span data-stu-id="52ff8-169">[**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) needs an HTTP request handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), a string that contains the headers, the length of the headers, and modifiers.</span></span>

### <a name="sending-a-request"></a><span data-ttu-id="52ff8-170">Envoi d’une demande</span><span class="sxs-lookup"><span data-stu-id="52ff8-170">Sending a Request</span></span>

<span data-ttu-id="52ff8-171">[**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) établit une connexion à Internet et envoie la demande au site spécifié.</span><span class="sxs-lookup"><span data-stu-id="52ff8-171">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) establishes a connection to the Internet and sends the request to the specified site.</span></span> <span data-ttu-id="52ff8-172">Cette fonction requiert un handle [**HINTERNET**](appendix-a-hinternet-handles.md) créé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="52ff8-172">This function requires an [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="52ff8-173">[**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) peut également envoyer des en-têtes supplémentaires ou des informations facultatives.</span><span class="sxs-lookup"><span data-stu-id="52ff8-173">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) can also send additional headers or optional information.</span></span> <span data-ttu-id="52ff8-174">Les informations facultatives sont généralement utilisées pour les opérations qui écrivent des informations sur le serveur, telles que PUT et poster.</span><span class="sxs-lookup"><span data-stu-id="52ff8-174">The optional information is generally used for operations that write information to the server, such as PUT and POST.</span></span>

<span data-ttu-id="52ff8-175">Une fois que [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) a envoyé la demande, l’application peut utiliser les fonctions [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)et [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) sur le handle [**HINTERNET**](appendix-a-hinternet-handles.md) créé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) pour télécharger les ressources du serveur.</span><span class="sxs-lookup"><span data-stu-id="52ff8-175">After [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) sends the request, the application can use the [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) functions on the [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) to download the server's resources.</span></span>

### <a name="posting-data-to-the-server"></a><span data-ttu-id="52ff8-176">Publication des données sur le serveur</span><span class="sxs-lookup"><span data-stu-id="52ff8-176">Posting Data to the Server</span></span>

<span data-ttu-id="52ff8-177">Pour la publication de données sur un serveur, le verbe HTTP dans l’appel à [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) doit être de type « publication » ou « put ».</span><span class="sxs-lookup"><span data-stu-id="52ff8-177">To post data to a server, the HTTP verb in the call to [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) must be either POST or PUT.</span></span> <span data-ttu-id="52ff8-178">L’adresse de la mémoire tampon qui contient les données de publication doit ensuite être passée au paramètre *lpOptional* dans [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="52ff8-178">The address of the buffer that contains the POST data should then be passed to the *lpOptional* parameter in [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="52ff8-179">Le paramètre *dwOptionalLength* doit être défini sur la taille des données.</span><span class="sxs-lookup"><span data-stu-id="52ff8-179">The *dwOptionalLength* parameter should be set to the size of the data.</span></span>

<span data-ttu-id="52ff8-180">Vous pouvez également utiliser la fonction [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) pour envoyer des données sur un handle [**HINTERNET**](appendix-a-hinternet-handles.md) envoyé à l’aide de [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa).</span><span class="sxs-lookup"><span data-stu-id="52ff8-180">You can also use the [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) function to post data on an [**HINTERNET**](appendix-a-hinternet-handles.md) handle sent using [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa).</span></span>

### <a name="getting-information-about-a-request"></a><span data-ttu-id="52ff8-181">Obtention d’informations sur une demande</span><span class="sxs-lookup"><span data-stu-id="52ff8-181">Getting Information About a Request</span></span>

<span data-ttu-id="52ff8-182">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) permet à une application de récupérer des informations sur une requête http.</span><span class="sxs-lookup"><span data-stu-id="52ff8-182">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) allows an application to retrieve information about an HTTP request.</span></span> <span data-ttu-id="52ff8-183">La fonction requiert un handle [**HINTERNET**](appendix-a-hinternet-handles.md) créé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) ou [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), une valeur de niveau d’information et une longueur de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="52ff8-183">The function requires an [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), an information level value, and a buffer length.</span></span> <span data-ttu-id="52ff8-184">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) accepte également une mémoire tampon qui stocke les informations et un index d’en-tête de base zéro qui énumère plusieurs en-têtes portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="52ff8-184">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) also accepts a buffer that stores the information and a zero-based header index that enumerates multiple headers with the same name.</span></span>

### <a name="downloading-resources-from-the-www"></a><span data-ttu-id="52ff8-185">Téléchargement des ressources à partir du Web</span><span class="sxs-lookup"><span data-stu-id="52ff8-185">Downloading Resources from the WWW</span></span>

<span data-ttu-id="52ff8-186">Après avoir ouvert une demande avec [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) et l’avoir envoyée au serveur [**avec HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta), l’application peut utiliser les fonctions [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)et [**INTERNETSETFILEPOINTER**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) pour télécharger la ressource à partir du serveur http.</span><span class="sxs-lookup"><span data-stu-id="52ff8-186">After opening a request with [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and sending it to the server with [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta), the application can use the [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) functions to download the resource from the HTTP server.</span></span>

<span data-ttu-id="52ff8-187">L’exemple suivant télécharge une ressource.</span><span class="sxs-lookup"><span data-stu-id="52ff8-187">The following example downloads a resource.</span></span> <span data-ttu-id="52ff8-188">La fonction accepte le descripteur de la fenêtre active, le numéro d’identification d’une zone d’édition et un handle [**HINTERNET**](appendix-a-hinternet-handles.md) créé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) et envoyé par [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="52ff8-188">The function accepts the handle to the current window, the identification number of an edit box, and an [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and sent by [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="52ff8-189">Elle utilise [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) pour déterminer la taille de la ressource, puis la télécharge à l’aide de [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span><span class="sxs-lookup"><span data-stu-id="52ff8-189">It uses [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) to determine the size of the resource and then downloads it using [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span> <span data-ttu-id="52ff8-190">Le contenu est ensuite affiché dans la zone d’édition.</span><span class="sxs-lookup"><span data-stu-id="52ff8-190">The contents are then displayed in the edit box.</span></span>


```C++
int WINAPI Dumper(HWND hX, int intCtrlID, HINTERNET hResource)
{
    LPTSTR lpszData;    // buffer for the data
    DWORD  dwSize;       // size of the data available
    DWORD  dwDownloaded; // size of the downloaded data
    DWORD  dwSizeSum=0;  // size of the data in the textbox
    LPTSTR lpszHolding;  // buffer to merge the textbox data and buffer

    // Set the cursor to an hourglass.
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    // This loop handles reading the data.
    do
    {
        // The call to InternetQueryDataAvailable determines the
        // amount of data available to download.
        if (!InternetQueryDataAvailable(hResource,&dwSize,0,0))
        {
            printf("InternetQueryDataAvailable failed (%d)\n", GetLastError());
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
        {
            // Allocate a buffer of the size returned by
            // InternetQueryDataAvailable.
            lpszData = new TCHAR[dwSize+1];

            // Read the data from the HINTERNET handle.
            if(!InternetReadFile(hResource,
                                 (LPVOID)lpszData,
                                 dwSize,
                                 &dwDownloaded))
            {
                printf("InternetReadFile failed (%d)\n", GetLastError());
                delete[] lpszData;
                break;
            }
            else
            {
                // Add a null terminator to the end of the data buffer
                lpszData[dwDownloaded]='\0';

                // Allocate the holding buffer.
                lpszHolding = new TCHAR[dwSizeSum + dwDownloaded + 1];

                // Check if there has been any data written
                // to the textbox.
                if (dwSizeSum != 0)
                {
                    // Retrieve the data stored in the textbox if any
                    GetDlgItemText(hX,intCtrlID,
                                   (LPTSTR)lpszHolding,
                                   dwSizeSum);

                    // Add a null terminator at the end of the
                    // textbox data.
                    lpszHolding[dwSizeSum]='\0';
                }
                else
                {
                    // Make the holding buffer an empty string.
                    lpszHolding[0]='\0';
                }

                size_t cchDest = dwSizeSum + dwDownloaded + dwDownloaded + 1;
                LPTSTR* ppszDestEnd = 0;
                size_t* pcchRemaining = 0;

                // Add the new data to the holding buffer
                HRESULT hr = StringCchCatEx(lpszHolding,
                                            cchDest,
                                            lpszData,
                                            ppszDestEnd,
                                            pcchRemaining,
                                            STRSAFE_NO_TRUNCATION);

                if(SUCCEEDED(hr))
                {
                    // Write the holding buffer to the textbox.
                    SetDlgItemText(hX,intCtrlID,(LPTSTR)lpszHolding);

                    // Delete the two buffers.
                    delete[] lpszHolding;
                    delete[] lpszData;

                    // Add the size of the downloaded data to the
                    // textbox data size.
                    dwSizeSum = dwSizeSum + dwDownloaded + 1;

                    // Check the size of the remaining data.
                    // If it is zero, break.
                    if (dwDownloaded == 0)
                        break;
                    else
                    {
                    //  TODO: Insert error handling code here.
                    }
                }
            }
        }
    }
    while(TRUE);

    // Close the HINTERNET handle.
    InternetCloseHandle(hResource);

    // Set the cursor back to an arrow.
    SetCursor(LoadCursor(NULL,IDC_ARROW));

    return TRUE;
}
```



> [!Note]  
> <span data-ttu-id="52ff8-191">WinINet ne prend pas en charge les implémentations de serveur.</span><span class="sxs-lookup"><span data-stu-id="52ff8-191">WinINet does not support server implementations.</span></span> <span data-ttu-id="52ff8-192">En outre, il ne doit pas être utilisé à partir d’un service.</span><span class="sxs-lookup"><span data-stu-id="52ff8-192">In addition, it should not be used from a service.</span></span> <span data-ttu-id="52ff8-193">Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="52ff8-193">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 