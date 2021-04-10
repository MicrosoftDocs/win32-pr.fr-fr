---
description: Les services HTTP Microsoft Windows (WinHTTP) exposent un ensemble de fonctions C/C++ qui permettent à votre application d’accéder aux ressources HTTP sur le Web. Cette rubrique fournit une vue d’ensemble de la façon dont ces fonctions sont utilisées pour interagir avec un serveur HTTP.
ms.assetid: 66a1616b-0cf3-45c7-880b-e36728b5a9c4
title: Vue d’ensemble des sessions WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98dc8116dff75f279b87cb5f5ee6af607034176f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113142"
---
# <a name="winhttp-sessions-overview"></a><span data-ttu-id="0912a-104">Vue d’ensemble des sessions WinHTTP</span><span class="sxs-lookup"><span data-stu-id="0912a-104">WinHTTP Sessions Overview</span></span>

<span data-ttu-id="0912a-105">Les services HTTP Microsoft Windows (WinHTTP) exposent un ensemble de fonctions C/C++ qui permettent à votre application d’accéder aux ressources HTTP sur le Web.</span><span class="sxs-lookup"><span data-stu-id="0912a-105">The Microsoft Windows HTTP Services (WinHTTP) exposes a set of C/C++ functions that enable your application to access HTTP resources on the Web.</span></span> <span data-ttu-id="0912a-106">Cette rubrique fournit une vue d’ensemble de la façon dont ces fonctions sont utilisées pour interagir avec un serveur HTTP.</span><span class="sxs-lookup"><span data-stu-id="0912a-106">This topic provides an overview of how these functions are used to interact with an HTTP server.</span></span>

-   [<span data-ttu-id="0912a-107">Utilisation de l’API WinHTTP pour accéder au Web</span><span class="sxs-lookup"><span data-stu-id="0912a-107">Using the WinHTTP API to Access the Web</span></span>](#using-the-winhttp-api-to-access-the-web)
-   [<span data-ttu-id="0912a-108">Initialisation de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="0912a-108">Initializing WinHTTP</span></span>](#initializing-winhttp)
-   [<span data-ttu-id="0912a-109">Ouverture d’une demande</span><span class="sxs-lookup"><span data-stu-id="0912a-109">Opening a Request</span></span>](#opening-a-request)
-   [<span data-ttu-id="0912a-110">Ajout d’en-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="0912a-110">Adding Request Headers</span></span>](#adding-request-headers)
-   [<span data-ttu-id="0912a-111">Envoi d’une demande</span><span class="sxs-lookup"><span data-stu-id="0912a-111">Sending a Request</span></span>](#sending-a-request)
-   [<span data-ttu-id="0912a-112">Publication des données sur le serveur</span><span class="sxs-lookup"><span data-stu-id="0912a-112">Posting Data to the Server</span></span>](#posting-data-to-the-server)
-   [<span data-ttu-id="0912a-113">Obtention d’informations sur une demande</span><span class="sxs-lookup"><span data-stu-id="0912a-113">Getting Information About a Request</span></span>](#getting-information-about-a-request)
-   [<span data-ttu-id="0912a-114">Téléchargement de ressources à partir du Web</span><span class="sxs-lookup"><span data-stu-id="0912a-114">Downloading Resources from the Web</span></span>](#downloading-resources-from-the-web)

## <a name="using-the-winhttp-api-to-access-the-web"></a><span data-ttu-id="0912a-115">Utilisation de l’API WinHTTP pour accéder au Web</span><span class="sxs-lookup"><span data-stu-id="0912a-115">Using the WinHTTP API to Access the Web</span></span>

<span data-ttu-id="0912a-116">Le diagramme suivant montre l’ordre dans lequel les fonctions WinHTTP sont généralement appelées lors de l’interaction avec un serveur HTTP.</span><span class="sxs-lookup"><span data-stu-id="0912a-116">The following diagram shows the order in which WinHTTP functions are typically called when interacting with an HTTP server.</span></span> <span data-ttu-id="0912a-117">Les zones grisées représentent des fonctions qui génèrent un descripteur [HINTERNET](hinternet-handles-in-winhttp.md) , tandis que les zones simples représentent des fonctions qui utilisent ces handles.</span><span class="sxs-lookup"><span data-stu-id="0912a-117">The shaded boxes represent functions that generate an [HINTERNET](hinternet-handles-in-winhttp.md) handle, while the plain boxes represent functions that use those handles.</span></span>

![fonctions qui créent des handles](images/art-winhttp3.png)

## <a name="initializing-winhttp"></a><span data-ttu-id="0912a-119">Initialisation de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="0912a-119">Initializing WinHTTP</span></span>

<span data-ttu-id="0912a-120">Avant d’interagir avec un serveur, WinHTTP doit être initialisé en appelant [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen).</span><span class="sxs-lookup"><span data-stu-id="0912a-120">Before interacting with a server, WinHTTP must be initialized by calling [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen).</span></span> <span data-ttu-id="0912a-121">[**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) crée un contexte de session pour conserver des détails sur la session http et retourne un descripteur de session.</span><span class="sxs-lookup"><span data-stu-id="0912a-121">[**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) creates a session context to maintain details about the HTTP session, and returns a session handle.</span></span> <span data-ttu-id="0912a-122">À l’aide de ce handle, la fonction [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) est alors en mesure de spécifier un serveur http ou HTTPS (Secure Hypertext Transfer Protocol) cible.</span><span class="sxs-lookup"><span data-stu-id="0912a-122">Using this handle, the [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) function is then able to specify a target HTTP or Secure Hypertext Transfer Protocol (HTTPS) server.</span></span>

> [!Note]  
> <span data-ttu-id="0912a-123">Un appel à [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) n’entraîne pas de connexion réelle au serveur http tant qu’une demande n’est pas effectuée pour une ressource spécifique.</span><span class="sxs-lookup"><span data-stu-id="0912a-123">A call to [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) does not result in an actual connection to the HTTP server until a request is made for a specific resource.</span></span>

 

## <a name="opening-a-request"></a><span data-ttu-id="0912a-124">Ouverture d’une demande</span><span class="sxs-lookup"><span data-stu-id="0912a-124">Opening a Request</span></span>

<span data-ttu-id="0912a-125">La fonction [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) ouvre une requête HTTP pour une ressource particulière et retourne un descripteur [HINTERNET](hinternet-handles-in-winhttp.md) qui peut être utilisé par les autres fonctions http.</span><span class="sxs-lookup"><span data-stu-id="0912a-125">The [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function opens an HTTP request for a particular resource and returns an [HINTERNET](hinternet-handles-in-winhttp.md) handle that can be used by the other HTTP functions.</span></span> <span data-ttu-id="0912a-126">[**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) n’envoie pas la requête au serveur lorsqu’il est appelé.</span><span class="sxs-lookup"><span data-stu-id="0912a-126">[**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) does not send the request to the server when called.</span></span> <span data-ttu-id="0912a-127">La fonction [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) établit en fait une connexion sur le réseau et envoie la demande.</span><span class="sxs-lookup"><span data-stu-id="0912a-127">The [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) function actually establishes a connection over the network and sends the request.</span></span>

<span data-ttu-id="0912a-128">L’exemple suivant montre un exemple d’appel à [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) qui utilise les options par défaut.</span><span class="sxs-lookup"><span data-stu-id="0912a-128">The following example shows a sample call to [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) that uses the default options.</span></span>

`HINTERNET hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL, NULL, NULL, NULL, 0);`

## <a name="adding-request-headers"></a><span data-ttu-id="0912a-129">Ajout d’en-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="0912a-129">Adding Request Headers</span></span>

<span data-ttu-id="0912a-130">La fonction [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) permet à une application d’ajouter des en-têtes de demande de format libre supplémentaires au descripteur de requête http.</span><span class="sxs-lookup"><span data-stu-id="0912a-130">The [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) function allows an application to append additional free-format request headers to the HTTP request handle.</span></span> <span data-ttu-id="0912a-131">Il est destiné à être utilisé par des applications sophistiquées qui requièrent un contrôle précis sur les demandes envoyées au serveur HTTP.</span><span class="sxs-lookup"><span data-stu-id="0912a-131">It is intended for use by sophisticated applications that require precise control over the requests sent to the HTTP server.</span></span>

<span data-ttu-id="0912a-132">La fonction [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) nécessite un handle de requête http créé par [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), une chaîne qui contient les en-têtes, la longueur des en-têtes et les modificateurs éventuels.</span><span class="sxs-lookup"><span data-stu-id="0912a-132">The [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) function requires an HTTP request handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), a string that contains the headers, the length of the headers, and any modifiers.</span></span>

<span data-ttu-id="0912a-133">Les modificateurs suivants peuvent être utilisés avec [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).</span><span class="sxs-lookup"><span data-stu-id="0912a-133">The following modifiers can be used with [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).</span></span>



| <span data-ttu-id="0912a-134">Modificateur</span><span class="sxs-lookup"><span data-stu-id="0912a-134">Modifier</span></span>                                                                                         | <span data-ttu-id="0912a-135">Description</span><span class="sxs-lookup"><span data-stu-id="0912a-135">Description</span></span>                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0912a-136">**ajout de l' \_ indicateur ADDREQ WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0912a-136">**WINHTTP\_ADDREQ\_FLAG\_ADD**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                       | <span data-ttu-id="0912a-137">Ajoute l’en-tête s’il n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="0912a-137">Adds the header if it does not exist.</span></span> <span data-ttu-id="0912a-138">Utilisé avec [**l' \_ indicateur ADDREQ WinHTTP \_ \_ Replace**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).</span><span class="sxs-lookup"><span data-stu-id="0912a-138">Used with [**WINHTTP\_ADDREQ\_FLAG\_REPLACE**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).</span></span>                                                                                                                                                                                                               |
| [<span data-ttu-id="0912a-139">**\_indicateur ADDREQ \_ WinHTTP \_ ajouter \_ si \_ nouveau**</span><span class="sxs-lookup"><span data-stu-id="0912a-139">**WINHTTP\_ADDREQ\_FLAG\_ADD\_IF\_NEW**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)              | <span data-ttu-id="0912a-140">Ajoute l’en-tête uniquement s’il n’existe pas déjà ; dans le cas contraire, une erreur est retournée.</span><span class="sxs-lookup"><span data-stu-id="0912a-140">Adds the header only if it does not already exist; otherwise, an error is returned.</span></span>                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="0912a-141">**ADDREQ de l' \_ \_ indicateur de \_ fusion WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="0912a-141">**WINHTTP\_ADDREQ\_FLAG\_COALESCE**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                  | <span data-ttu-id="0912a-142">Fusionne les en-têtes du même nom.</span><span class="sxs-lookup"><span data-stu-id="0912a-142">Merges headers of the same name.</span></span>                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="0912a-143">**\_ADDREQ \_ de l’indicateur \_ de fusion WinHTTP \_ avec \_ virgule**</span><span class="sxs-lookup"><span data-stu-id="0912a-143">**WINHTTP\_ADDREQ\_FLAG\_COALESCE\_WITH\_COMMA**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)     | <span data-ttu-id="0912a-144">Fusionne les en-têtes du même nom à l’aide d’une virgule.</span><span class="sxs-lookup"><span data-stu-id="0912a-144">Merges headers of the same name using a comma.</span></span> <span data-ttu-id="0912a-145">Par exemple, l’ajout de « Accept : Text/ \* » suivi de « Accept : audio/ \* » avec cet indicateur forme l’en-tête unique « Accept : Text/ \* , audio/ \* », ce qui a pour effet de fusionner le premier en-tête.</span><span class="sxs-lookup"><span data-stu-id="0912a-145">For example, adding "Accept: text/\*" followed by "Accept: audio/\*" with this flag forms the single header "Accept: text/\*, audio/\*", causing the first header found to be merged.</span></span> <span data-ttu-id="0912a-146">Il revient à l’application appelante de garantir un schéma cohésif en ce qui concerne les en-têtes fusionnés/séparés.</span><span class="sxs-lookup"><span data-stu-id="0912a-146">It is up to the calling application to ensure a cohesive scheme with respect to merged/separate headers.</span></span> |
| [<span data-ttu-id="0912a-147">**\_ADDREQ \_ de l’indicateur \_ de fusion WinHTTP \_ avec \_ point-virgule**</span><span class="sxs-lookup"><span data-stu-id="0912a-147">**WINHTTP\_ADDREQ\_FLAG\_COALESCE\_WITH\_SEMICOLON**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) | <span data-ttu-id="0912a-148">Fusionne les en-têtes du même nom à l’aide d’un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="0912a-148">Merges headers of the same name using a semicolon.</span></span>                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="0912a-149">**remplacement de l' \_ indicateur ADDREQ WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0912a-149">**WINHTTP\_ADDREQ\_FLAG\_REPLACE**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                   | <span data-ttu-id="0912a-150">Remplace ou supprime un en-tête.</span><span class="sxs-lookup"><span data-stu-id="0912a-150">Replaces or removes a header.</span></span> <span data-ttu-id="0912a-151">Si la valeur d’en-tête est vide et que l’en-tête est trouvé, elle est supprimée.</span><span class="sxs-lookup"><span data-stu-id="0912a-151">If the header value is empty and the header is found, it is removed.</span></span> <span data-ttu-id="0912a-152">Si la valeur d’en-tête n’est pas vide, la valeur d’en-tête est remplacée.</span><span class="sxs-lookup"><span data-stu-id="0912a-152">If the header value is not empty, the header value is replaced.</span></span>                                                                                                                                                                            |



 

## <a name="sending-a-request"></a><span data-ttu-id="0912a-153">Envoi d’une demande</span><span class="sxs-lookup"><span data-stu-id="0912a-153">Sending a Request</span></span>

<span data-ttu-id="0912a-154">La fonction [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) établit une connexion au serveur et envoie la demande au site spécifié.</span><span class="sxs-lookup"><span data-stu-id="0912a-154">The [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) function establishes a connection to the server and sends the request to the specified site.</span></span> <span data-ttu-id="0912a-155">Cette fonction requiert un handle [HINTERNET](hinternet-handles-in-winhttp.md) créé par [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).</span><span class="sxs-lookup"><span data-stu-id="0912a-155">This function requires an [HINTERNET](hinternet-handles-in-winhttp.md) handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).</span></span> <span data-ttu-id="0912a-156">[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) peut également envoyer des en-têtes supplémentaires ou des informations facultatives.</span><span class="sxs-lookup"><span data-stu-id="0912a-156">[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) can also send additional headers or optional information.</span></span> <span data-ttu-id="0912a-157">Les informations facultatives sont généralement utilisées pour les opérations qui écrivent des informations sur le serveur, telles que PUT et poster.</span><span class="sxs-lookup"><span data-stu-id="0912a-157">The optional information is generally used for operations that write information to the server, such as PUT and POST.</span></span>

<span data-ttu-id="0912a-158">Une fois que la fonction [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) a envoyé la demande, l’application peut utiliser les fonctions [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) et [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) sur le handle [HINTERNET](hinternet-handles-in-winhttp.md) pour télécharger les ressources du serveur.</span><span class="sxs-lookup"><span data-stu-id="0912a-158">After the [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) function sends the request, the application can use the [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) and [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) functions on the [HINTERNET](hinternet-handles-in-winhttp.md) handle to download the server's resources.</span></span>

## <a name="posting-data-to-the-server"></a><span data-ttu-id="0912a-159">Publication des données sur le serveur</span><span class="sxs-lookup"><span data-stu-id="0912a-159">Posting Data to the Server</span></span>

<span data-ttu-id="0912a-160">Pour la publication de données sur un serveur, le [*verbe http*](glossary.md) dans l’appel à [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) doit être de type « publication » ou « put ».</span><span class="sxs-lookup"><span data-stu-id="0912a-160">To post data to a server, the [*HTTP verb*](glossary.md) in the call to [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) must be either POST or PUT.</span></span> <span data-ttu-id="0912a-161">Quand [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) est appelé, le paramètre *dwTotalLength* doit être défini sur la taille des données en octets.</span><span class="sxs-lookup"><span data-stu-id="0912a-161">When [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) is called, the *dwTotalLength* parameter should be set to the size of the data in bytes.</span></span> <span data-ttu-id="0912a-162">Utilisez ensuite [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata) pour envoyer les données sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="0912a-162">Then use [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata) to post the data to the server.</span></span>

<span data-ttu-id="0912a-163">Vous pouvez également définir le paramètre *lpOptional* de [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) sur l’adresse d’une mémoire tampon qui contient les données à poster sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="0912a-163">Alternatively, set the *lpOptional* parameter of [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) to the address of a buffer that contains data to post to the server.</span></span> <span data-ttu-id="0912a-164">Lorsque vous utilisez cette technique, vous devez définir les paramètres *dwOptionalLength* et *dwTotalLength* de [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) à la taille des données publiées.</span><span class="sxs-lookup"><span data-stu-id="0912a-164">When using this technique, you must set both the *dwOptionalLength* and *dwTotalLength* parameters of [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) to be the size of the data being posted.</span></span> <span data-ttu-id="0912a-165">L’appel de [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) de cette manière élimine la nécessité d’appeler [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata).</span><span class="sxs-lookup"><span data-stu-id="0912a-165">Calling [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) in this manner eliminates the need to call [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata).</span></span>

## <a name="getting-information-about-a-request"></a><span data-ttu-id="0912a-166">Obtention d’informations sur une demande</span><span class="sxs-lookup"><span data-stu-id="0912a-166">Getting Information About a Request</span></span>

<span data-ttu-id="0912a-167">La fonction [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) permet à une application de récupérer des informations sur une requête http.</span><span class="sxs-lookup"><span data-stu-id="0912a-167">The [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) function allows an application to retrieve information about an HTTP request.</span></span> <span data-ttu-id="0912a-168">La fonction requiert un handle [HINTERNET](hinternet-handles-in-winhttp.md) créé par [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), une valeur de niveau d’information et une longueur de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="0912a-168">The function requires an [HINTERNET](hinternet-handles-in-winhttp.md) handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), an information level value, and a buffer length.</span></span> <span data-ttu-id="0912a-169">[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) accepte également une mémoire tampon qui stocke les informations et un index d’en-tête de base zéro qui énumère plusieurs en-têtes portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="0912a-169">[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) also accepts a buffer that stores the information and a zero-based header index that enumerates multiple headers with the same name.</span></span>

<span data-ttu-id="0912a-170">Utilisez l’une des valeurs de niveau d’informations trouvées dans la page des indicateurs d’informations de [**requête**](query-info-flags.md) avec un modificateur pour contrôler le format dans lequel les informations sont stockées dans le paramètre *lpvBuffer* de [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span><span class="sxs-lookup"><span data-stu-id="0912a-170">Use any of the information level values found on the [**Query Info Flags**](query-info-flags.md) page with a modifier to control the format in which the information is stored in the *lpvBuffer* parameter of [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>

## <a name="downloading-resources-from-the-web"></a><span data-ttu-id="0912a-171">Téléchargement de ressources à partir du Web</span><span class="sxs-lookup"><span data-stu-id="0912a-171">Downloading Resources from the Web</span></span>

<span data-ttu-id="0912a-172">Après l’ouverture d’une demande avec la fonction [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) , son envoi au serveur avec [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)et la préparation du descripteur de demande pour recevoir une réponse avec [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse), l’application peut utiliser les fonctions [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) et [**WINHTTPQUERYDATAAVAILABLE**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) pour télécharger la ressource à partir du serveur http.</span><span class="sxs-lookup"><span data-stu-id="0912a-172">After opening a request with the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function, sending it to the server with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), and preparing the request handle to receive a response with [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse), the application can use the [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) and [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) functions to download the resource from the HTTP server.</span></span>

<span data-ttu-id="0912a-173">L’exemple de code suivant montre comment télécharger une ressource avec la sémantique des transactions sécurisées.</span><span class="sxs-lookup"><span data-stu-id="0912a-173">The following sample code shows how to download a resource with secure transaction semantics.</span></span> <span data-ttu-id="0912a-174">L’exemple de code initialise l’interface de programmation d’applications (API) WinHTTP, sélectionne un serveur HTTPs cible, puis ouvre et envoie une demande pour cette ressource sécurisée.</span><span class="sxs-lookup"><span data-stu-id="0912a-174">The sample code initializes the WinHTTP application programming interface (API), selects a target HTTPS server, and then opens and sends a request for this secure resource.</span></span> <span data-ttu-id="0912a-175">[**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) est utilisé avec le handle de demande pour déterminer la quantité de données disponibles pour le téléchargement, puis [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) est utilisé pour lire ces données.</span><span class="sxs-lookup"><span data-stu-id="0912a-175">[**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) is used with the request handle to determine how much data is available for download, and then [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) is used to read that data.</span></span> <span data-ttu-id="0912a-176">Ce processus est répété jusqu’à ce que l’intégralité du document ait été extraite et affichée.</span><span class="sxs-lookup"><span data-stu-id="0912a-176">This process is repeated until the entire document has been retrieved and displayed.</span></span>


```C++
  DWORD dwSize = 0;
  DWORD dwDownloaded = 0;
  LPSTR pszOutBuffer;
  BOOL  bResults = FALSE;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, L"www.microsoft.com",
                               INTERNET_DEFAULT_HTTPS_PORT, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL,
                                   NULL, WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES, 
                                   WINHTTP_FLAG_SECURE );

  // Send a request.
  if( hRequest )
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS, 0,
                                   WINHTTP_NO_REQUEST_DATA, 0, 
                                   0, 0 );


  // End the request.
  if( bResults )
    bResults = WinHttpReceiveResponse( hRequest, NULL );

  // Keep checking for data until there is nothing left.
  if( bResults )
  {
    do 
    {
      // Check for available data.
      dwSize = 0;
      if( !WinHttpQueryDataAvailable( hRequest, &dwSize ) )
        printf( "Error %u in WinHttpQueryDataAvailable.\n",
                GetLastError( ) );

      // Allocate space for the buffer.
      pszOutBuffer = new char[dwSize+1];
      if( !pszOutBuffer )
      {
        printf( "Out of memory\n" );
        dwSize=0;
      }
      else
      {
        // Read the data.
        ZeroMemory( pszOutBuffer, dwSize+1 );

        if( !WinHttpReadData( hRequest, (LPVOID)pszOutBuffer, 
                              dwSize, &dwDownloaded ) )
          printf( "Error %u in WinHttpReadData.\n", GetLastError( ) );
        else
          printf( "%s", pszOutBuffer );

        // Free the memory allocated to the buffer.
        delete [] pszOutBuffer;
      }
    } while( dwSize > 0 );
  }


  // Report any errors.
  if( !bResults )
    printf( "Error %d has occurred.\n", GetLastError( ) );

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
```



 

 



