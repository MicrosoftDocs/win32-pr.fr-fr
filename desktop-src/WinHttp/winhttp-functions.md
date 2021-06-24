---
description: Cette rubrique identifie les fonctions fournies par WinHTTP.
ms.assetid: dcb56d5d-ed0d-49bb-95bf-940a49c033f1
title: Fonctions WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf5f9db8fcde5589a86556111bec6df3b2b18c76
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587744"
---
# <a name="winhttp-functions"></a><span data-ttu-id="64743-103">Fonctions WinHTTP</span><span class="sxs-lookup"><span data-stu-id="64743-103">WinHTTP Functions</span></span>

<span data-ttu-id="64743-104">WinHTTP fournit les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="64743-104">WinHTTP provides the following functions:</span></span>

<dl> <dt>

[<span data-ttu-id="64743-105">**WinHttpAddRequestHeaders**</span><span class="sxs-lookup"><span data-stu-id="64743-105">**WinHttpAddRequestHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)
</dt> <dd>

<span data-ttu-id="64743-106">Ajoute un ou plusieurs en-têtes de requête HTTP au descripteur de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="64743-106">Adds one or more HTTP request headers to the HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-107">**WinHttpCheckPlatform**</span><span class="sxs-lookup"><span data-stu-id="64743-107">**WinHttpCheckPlatform**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcheckplatform)
</dt> <dd>

<span data-ttu-id="64743-108">Détermine si la plateforme actuelle est prise en charge par WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="64743-108">Determines whether the current platform is supported by WinHTTP.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-109">**WinHttpCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="64743-109">**WinHttpCloseHandle**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)
</dt> <dd>

<span data-ttu-id="64743-110">Ferme un handle [HINTERNET](hinternet-handles-in-winhttp.md) unique.</span><span class="sxs-lookup"><span data-stu-id="64743-110">Closes a single [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-111">**WinHttpConnect**</span><span class="sxs-lookup"><span data-stu-id="64743-111">**WinHttpConnect**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)
</dt> <dd>

<span data-ttu-id="64743-112">Spécifie le serveur cible initial d’une requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="64743-112">Specifies the initial target server of an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-113">**WinHttpCrackUrl**</span><span class="sxs-lookup"><span data-stu-id="64743-113">**WinHttpCrackUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)
</dt> <dd>

<span data-ttu-id="64743-114">Sépare une URL en ses composants, par exemple, le nom d’hôte et le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="64743-114">Separates a URL into its component parts, for example, host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-115">**WinHttpCreateProxyResolver**</span><span class="sxs-lookup"><span data-stu-id="64743-115">**WinHttpCreateProxyResolver**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateproxyresolver)
</dt> <dd>

<span data-ttu-id="64743-116">Crée un handle pour une utilisation par [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span><span class="sxs-lookup"><span data-stu-id="64743-116">Creates a handle for use by [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="64743-117">**WinHttpCreateUrl**</span><span class="sxs-lookup"><span data-stu-id="64743-117">**WinHttpCreateUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)
</dt> <dd>

<span data-ttu-id="64743-118">Crée une URL à partir de composants, par exemple, le nom d’hôte et le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="64743-118">Creates a URL from component parts, for example, the host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-119">**WinHttpDetectAutoProxyConfigUrl**</span><span class="sxs-lookup"><span data-stu-id="64743-119">**WinHttpDetectAutoProxyConfigUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl)
</dt> <dd>

<span data-ttu-id="64743-120">Recherche l’URL du fichier de configuration automatique du proxy (PAC).</span><span class="sxs-lookup"><span data-stu-id="64743-120">Finds the URL for the Proxy Auto-Configuration (PAC) file.</span></span> <span data-ttu-id="64743-121">Cette fonction signale l’URL du fichier PAC, mais ne télécharge pas le fichier.</span><span class="sxs-lookup"><span data-stu-id="64743-121">This function reports the URL of the PAC file, but it does not download the file.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-122">**WinHttpFreeProxyResult**</span><span class="sxs-lookup"><span data-stu-id="64743-122">**WinHttpFreeProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpfreeproxyresult)
</dt> <dd>

<span data-ttu-id="64743-123">Libère les données récupérées à partir d’un appel précédent à [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span><span class="sxs-lookup"><span data-stu-id="64743-123">Frees the data retrieved from a previous call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="64743-124">**WinHttpFreeQueryConnectionGroupResult**</span><span class="sxs-lookup"><span data-stu-id="64743-124">**WinHttpFreeQueryConnectionGroupResult**</span></span>](/windows/win32/api/Winhttp/nf-winhttp-winhttpfreequeryconnectiongroupresult)
</dt> <dd>

<span data-ttu-id="64743-125">Libère la mémoire allouée par un appel précédent à [WinHttpQueryConnectionGroup](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup).</span><span class="sxs-lookup"><span data-stu-id="64743-125">Frees the memory allocated by a previous call to [WinHttpQueryConnectionGroup](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup).</span></span>

</dd> <dt>

[<span data-ttu-id="64743-126">**WinHttpGetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="64743-126">**WinHttpGetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="64743-127">Récupère la configuration du proxy WinHTTP par défaut à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="64743-127">Retrieves the default WinHTTP proxy configuration from the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-128">**WinHTTPGetIEProxyConfigForCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="64743-128">**WinHTTPGetIEProxyConfigForCurrentUser**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)
</dt> <dd>

<span data-ttu-id="64743-129">Obtient la configuration du proxy Internet Explorer (IE) pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="64743-129">Obtains the Internet Explorer (IE) proxy configuration for the current user.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-130">**WinHttpGetProxyForUrl**</span><span class="sxs-lookup"><span data-stu-id="64743-130">**WinHttpGetProxyForUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)
</dt> <dd>

<span data-ttu-id="64743-131">Récupère les informations de proxy pour l’URL spécifiée.</span><span class="sxs-lookup"><span data-stu-id="64743-131">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-132">**WinHttpGetProxyForUrlEx**</span><span class="sxs-lookup"><span data-stu-id="64743-132">**WinHttpGetProxyForUrlEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)
</dt> <dd>

<span data-ttu-id="64743-133">Récupère les informations de proxy pour l’URL spécifiée.</span><span class="sxs-lookup"><span data-stu-id="64743-133">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-134">**WinHttpGetProxyResult**</span><span class="sxs-lookup"><span data-stu-id="64743-134">**WinHttpGetProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)
</dt> <dd>

<span data-ttu-id="64743-135">Récupère les résultats d’un appel à [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span><span class="sxs-lookup"><span data-stu-id="64743-135">Retrieves the results of a call to [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="64743-136">**WinHttpOpen**</span><span class="sxs-lookup"><span data-stu-id="64743-136">**WinHttpOpen**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)
</dt> <dd>

<span data-ttu-id="64743-137">Initialise l’utilisation des fonctions WinHTTP par une application.</span><span class="sxs-lookup"><span data-stu-id="64743-137">Initializes an application's use of the WinHTTP functions.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-138">**WinHttpOpenRequest**</span><span class="sxs-lookup"><span data-stu-id="64743-138">**WinHttpOpenRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)
</dt> <dd>

<span data-ttu-id="64743-139">Crée un handle de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="64743-139">Creates an HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-140">**WinHttpQueryAuthSchemes**</span><span class="sxs-lookup"><span data-stu-id="64743-140">**WinHttpQueryAuthSchemes**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)
</dt> <dd>

<span data-ttu-id="64743-141">Retourne les schémas d’autorisation pris en charge par le serveur.</span><span class="sxs-lookup"><span data-stu-id="64743-141">Returns the authorization schemes that the server supports.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-142">**WinHttpQueryConnectionGroup**</span><span class="sxs-lookup"><span data-stu-id="64743-142">**WinHttpQueryConnectionGroup**</span></span>](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup)
</dt> <dd>

<span data-ttu-id="64743-143">Récupère une description de l’état actuel des connexions de WinHttp.</span><span class="sxs-lookup"><span data-stu-id="64743-143">Retrieves a description of the current state of WinHttp's connections.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-144">**WinHttpQueryDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="64743-144">**WinHttpQueryDataAvailable**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)
</dt> <dd>

<span data-ttu-id="64743-145">Retourne le nombre d’octets de données qui sont immédiatement disponibles pour être lus avec [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).</span><span class="sxs-lookup"><span data-stu-id="64743-145">Returns the number of bytes of data that are available immediately to be read with [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).</span></span>

</dd> <dt>

[<span data-ttu-id="64743-146">**WinHttpQueryHeaders**</span><span class="sxs-lookup"><span data-stu-id="64743-146">**WinHttpQueryHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
</dt> <dd>

<span data-ttu-id="64743-147">Récupère les informations d’en-tête associées à une requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="64743-147">Retrieves header information associated with an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-148">**WinHttpQueryOption**</span><span class="sxs-lookup"><span data-stu-id="64743-148">**WinHttpQueryOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)
</dt> <dd>

<span data-ttu-id="64743-149">Interroge une option Internet sur le handle spécifié.</span><span class="sxs-lookup"><span data-stu-id="64743-149">Queries an Internet option on the specified handle.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-150">**WinHttpReadData**</span><span class="sxs-lookup"><span data-stu-id="64743-150">**WinHttpReadData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)
</dt> <dd>

<span data-ttu-id="64743-151">Lit les données à partir d’un descripteur ouvert par la fonction [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) .</span><span class="sxs-lookup"><span data-stu-id="64743-151">Reads data from a handle opened by the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-152">**WinHttpReceiveResponse**</span><span class="sxs-lookup"><span data-stu-id="64743-152">**WinHttpReceiveResponse**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)
</dt> <dd>

<span data-ttu-id="64743-153">Termine une requête HTTP qui est lancée par [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="64743-153">Ends an HTTP request that is initiated by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="64743-154">**WinHttpResetAutoProxy**</span><span class="sxs-lookup"><span data-stu-id="64743-154">**WinHttpResetAutoProxy**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpresetautoproxy)
</dt> <dd>

<span data-ttu-id="64743-155">Réinitialise le proxy automatique.</span><span class="sxs-lookup"><span data-stu-id="64743-155">Resets the auto-proxy.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-156">**WinHttpSendRequest**</span><span class="sxs-lookup"><span data-stu-id="64743-156">**WinHttpSendRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)
</dt> <dd>

<span data-ttu-id="64743-157">Envoie la requête spécifiée au serveur HTTP.</span><span class="sxs-lookup"><span data-stu-id="64743-157">Sends the specified request to the HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-158">**WinHttpSetCredentials**</span><span class="sxs-lookup"><span data-stu-id="64743-158">**WinHttpSetCredentials**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)
</dt> <dd>

<span data-ttu-id="64743-159">Transmet les informations d’identification d’autorisation requises au serveur.</span><span class="sxs-lookup"><span data-stu-id="64743-159">Passes the required authorization credentials to the server.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-160">**WinHttpSetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="64743-160">**WinHttpSetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="64743-161">Définit la configuration par défaut du proxy WinHTTP dans le registre.</span><span class="sxs-lookup"><span data-stu-id="64743-161">Sets the default WinHTTP proxy configuration in the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-162">**WinHttpSetOption**</span><span class="sxs-lookup"><span data-stu-id="64743-162">**WinHttpSetOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)
</dt> <dd>

<span data-ttu-id="64743-163">Définit une option Internet.</span><span class="sxs-lookup"><span data-stu-id="64743-163">Sets an Internet option.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-164">**WinHttpSetStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="64743-164">**WinHttpSetStatusCallback**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)
</dt> <dd>

<span data-ttu-id="64743-165">Définit une fonction de rappel que WinHTTP peut appeler lorsque la progression est effectuée au cours d’une opération.</span><span class="sxs-lookup"><span data-stu-id="64743-165">Sets up a callback function that WinHTTP can call as progress is made during an operation.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-166">**WinHttpSetTimeouts**</span><span class="sxs-lookup"><span data-stu-id="64743-166">**WinHttpSetTimeouts**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)
</dt> <dd>

<span data-ttu-id="64743-167">Définit les différents délais d’attente impliqués dans les transactions HTTP.</span><span class="sxs-lookup"><span data-stu-id="64743-167">Sets the various time-outs that are involved with HTTP transactions.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-168">**WinHttpTimeFromSystemTime**</span><span class="sxs-lookup"><span data-stu-id="64743-168">**WinHttpTimeFromSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)
</dt> <dd>

<span data-ttu-id="64743-169">Met en forme une date et une heure en fonction de la spécification HTTP version 1,0.</span><span class="sxs-lookup"><span data-stu-id="64743-169">Formats a date and time according to the HTTP version 1.0 specification.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-170">**WinHttpTimeToSystemTime**</span><span class="sxs-lookup"><span data-stu-id="64743-170">**WinHttpTimeToSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)
</dt> <dd>

<span data-ttu-id="64743-171">Prend une chaîne de date/heure HTTP et la convertit en une structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="64743-171">Takes an HTTP time/date string and converts it to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-172">**WinHttpWriteData**</span><span class="sxs-lookup"><span data-stu-id="64743-172">**WinHttpWriteData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)
</dt> <dd>

<span data-ttu-id="64743-173">Écrit des données de requête sur un serveur HTTP.</span><span class="sxs-lookup"><span data-stu-id="64743-173">Writes request data to an HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-174">**WinHttpWebSocketClose**</span><span class="sxs-lookup"><span data-stu-id="64743-174">**WinHttpWebSocketClose**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose)
</dt> <dd>

<span data-ttu-id="64743-175">Ferme une connexion WebSocket.</span><span class="sxs-lookup"><span data-stu-id="64743-175">Closes a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-176">**WinHttpWebSocketCompleteUpgrade**</span><span class="sxs-lookup"><span data-stu-id="64743-176">**WinHttpWebSocketCompleteUpgrade**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketcompleteupgrade)
</dt> <dd>

<span data-ttu-id="64743-177">Termine une négociation WebSocket démarrée par [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="64743-177">Completes a WebSocket handshake started by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="64743-178">**WinHttpWebSocketQueryCloseStatus**</span><span class="sxs-lookup"><span data-stu-id="64743-178">**WinHttpWebSocketQueryCloseStatus**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketqueryclosestatus)
</dt> <dd>

<span data-ttu-id="64743-179">Obtient l’état de fermeture envoyé par un serveur.</span><span class="sxs-lookup"><span data-stu-id="64743-179">Gets the close status sent by a server.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-180">**WinHttpWebSocketReceive**</span><span class="sxs-lookup"><span data-stu-id="64743-180">**WinHttpWebSocketReceive**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive)
</dt> <dd>

<span data-ttu-id="64743-181">Reçoit des données à partir d’une connexion WebSocket.</span><span class="sxs-lookup"><span data-stu-id="64743-181">Receives data from a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-182">**WinHttpWebSocketSend**</span><span class="sxs-lookup"><span data-stu-id="64743-182">**WinHttpWebSocketSend**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend)
</dt> <dd>

<span data-ttu-id="64743-183">Envoie des données via une connexion WebSocket.</span><span class="sxs-lookup"><span data-stu-id="64743-183">Sends data over a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="64743-184">**WinHttpWebSocketShutdown**</span><span class="sxs-lookup"><span data-stu-id="64743-184">**WinHttpWebSocketShutdown**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown)
</dt> <dd>

<span data-ttu-id="64743-185">Envoie un frame de fermeture à une connexion WebSocket.</span><span class="sxs-lookup"><span data-stu-id="64743-185">Sends a close frame to a WebSocket connection.</span></span>

</dd> </dl>

 

 
