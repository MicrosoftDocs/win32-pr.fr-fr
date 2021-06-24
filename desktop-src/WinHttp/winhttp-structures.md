---
description: Cette rubrique identifie les structures que WinHTTP utilise.
ms.assetid: e1567393-162e-48d4-8e6b-7620e351136c
title: Structures WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9d6f0cdbb467e916b1a6ac54b90491cbee9efdb
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587982"
---
# <a name="winhttp-structures"></a><span data-ttu-id="52e7f-103">Structures WinHTTP</span><span class="sxs-lookup"><span data-stu-id="52e7f-103">WinHTTP structures</span></span>

<span data-ttu-id="52e7f-104">WinHTTP utilise les structures suivantes :</span><span class="sxs-lookup"><span data-stu-id="52e7f-104">WinHTTP uses the following structures:</span></span>

<dl> <dt>

[<span data-ttu-id="52e7f-105">**HTTP_VERSION_INFO**</span><span class="sxs-lookup"><span data-stu-id="52e7f-105">**HTTP_VERSION_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info)
</dt> <dd>

<span data-ttu-id="52e7f-106">Contient la version HTTP globale.</span><span class="sxs-lookup"><span data-stu-id="52e7f-106">Contains the global HTTP version.</span></span>

</dd> <dt>

[<span data-ttu-id="52e7f-107">**URL_COMPONENTS**</span><span class="sxs-lookup"><span data-stu-id="52e7f-107">**URL_COMPONENTS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-url_components)
</dt> <dd>

<span data-ttu-id="52e7f-108">Contient les parties constituantes d’une URL.</span><span class="sxs-lookup"><span data-stu-id="52e7f-108">Contains the constituent parts of a URL.</span></span> <span data-ttu-id="52e7f-109">Cette structure est utilisée avec les fonctions [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) et [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) .</span><span class="sxs-lookup"><span data-stu-id="52e7f-109">This structure is used with the [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) functions.</span></span>

</dd> <dt>

[<span data-ttu-id="52e7f-110">**WINHTTP_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="52e7f-110">**WINHTTP_ASYNC_RESULT**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_async_result)
</dt> <dd>

<span data-ttu-id="52e7f-111">Contient le résultat d’un appel à une fonction asynchrone.</span><span class="sxs-lookup"><span data-stu-id="52e7f-111">Contains the result of a call to an asynchronous function.</span></span> <span data-ttu-id="52e7f-112">Cette structure est utilisée avec le prototype de [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) .</span><span class="sxs-lookup"><span data-stu-id="52e7f-112">This structure is used with the [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) prototype.</span></span>

</dd> <dt>

[<span data-ttu-id="52e7f-113">**WINHTTP_AUTOPROXY_OPTIONS**</span><span class="sxs-lookup"><span data-stu-id="52e7f-113">**WINHTTP_AUTOPROXY_OPTIONS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)
</dt> <dd>

<span data-ttu-id="52e7f-114">Utilisé pour indiquer à la fonction [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) s’il faut spécifier l’URL du fichier de configuration automatique du proxy ou pour localiser automatiquement l’URL avec des requêtes DHCP ou DNS sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="52e7f-114">Used to indicate to the [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function whether to specify the URL of the Proxy Auto-Configuration (PAC) file or to automatically locate the URL with DHCP or DNS queries to the network.</span></span>

</dd> <dt>

[<span data-ttu-id="52e7f-115">**WINHTTP_CERTIFICATE_INFO**</span><span class="sxs-lookup"><span data-stu-id="52e7f-115">**WINHTTP_CERTIFICATE_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info)
</dt> <dd>

<span data-ttu-id="52e7f-116">Contient les informations de certificat retournées par le serveur.</span><span class="sxs-lookup"><span data-stu-id="52e7f-116">Contains certificate information returned from the server.</span></span> <span data-ttu-id="52e7f-117">Cette structure est utilisée par la fonction [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) .</span><span class="sxs-lookup"><span data-stu-id="52e7f-117">This structure is used by the [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) function.</span></span>

</dd> <dt>

[<span data-ttu-id="52e7f-118">**WINHTTP_CONNECTION_GROUP**</span><span class="sxs-lookup"><span data-stu-id="52e7f-118">**WINHTTP_CONNECTION_GROUP**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_connection_group)
</dt> <dd>

<span data-ttu-id="52e7f-119">Représente un groupe de connexions.</span><span class="sxs-lookup"><span data-stu-id="52e7f-119">Represents a connection group.</span></span>

</dd> <dt>

[<span data-ttu-id="52e7f-120">**WINHTTP_CONNECTION_INFO**</span><span class="sxs-lookup"><span data-stu-id="52e7f-120">**WINHTTP_CONNECTION_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info)
</dt> <dd>

<span data-ttu-id="52e7f-121">Contient l’adresse IP source et de destination de la demande qui a généré la réponse.</span><span class="sxs-lookup"><span data-stu-id="52e7f-121">Contains the source and destination IP address of the request that generated the response.</span></span>

</dd> <dt>

[<span data-ttu-id="52e7f-122">**WINHTTP_CREDS**</span><span class="sxs-lookup"><span data-stu-id="52e7f-122">**WINHTTP_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds)
</dt> <dd>

<span data-ttu-id="52e7f-123">Contient les informations d’identification de l’utilisateur utilisées pour l’authentification du serveur et du proxy.</span><span class="sxs-lookup"><span data-stu-id="52e7f-123">Contains user credential information used for server and proxy authentication.</span></span>

> [!Note]
> <span data-ttu-id="52e7f-124">Cette structure est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="52e7f-124">This structure has been deprecated.</span></span> <span data-ttu-id="52e7f-125">Au lieu de cela, il est recommandé d’utiliser la structure [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) .</span><span class="sxs-lookup"><span data-stu-id="52e7f-125">Instead, the use of the [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure is recommended.</span></span>

</dd> <dt>

[<span data-ttu-id="52e7f-126">**WINHTTP_CREDS_EX**</span><span class="sxs-lookup"><span data-stu-id="52e7f-126">**WINHTTP_CREDS_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex)
</dt> <dd>

<span data-ttu-id="52e7f-127">Contient les informations d’identification de l’utilisateur utilisées pour l’authentification du serveur et du proxy.</span><span class="sxs-lookup"><span data-stu-id="52e7f-127">Contains user credential information used for server and proxy authentication.</span></span>

</dd> <dt>

[<span data-ttu-id="52e7f-128">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span><span class="sxs-lookup"><span data-stu-id="52e7f-128">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config)
</dt> <dd>

<span data-ttu-id="52e7f-129">Contient les informations de configuration du proxy Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="52e7f-129">Contains the Internet Explorer proxy configuration information.</span></span>

</dd> <dt>

[<span data-ttu-id="52e7f-130">**WINHTTP_HOST_CONNECTION_GROUP**</span><span class="sxs-lookup"><span data-stu-id="52e7f-130">**WINHTTP_HOST_CONNECTION_GROUP**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_host_connection_group)
</dt> <dd>

<span data-ttu-id="52e7f-131">Représente une collection de groupes de connexions.</span><span class="sxs-lookup"><span data-stu-id="52e7f-131">Represents a collection of connection groups.</span></span>

</dd> <dt>

[<span data-ttu-id="52e7f-132">**WINHTTP_MATCH_CONNECTION_GUID**</span><span class="sxs-lookup"><span data-stu-id="52e7f-132">**WINHTTP_MATCH_CONNECTION_GUID**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_match_connection_group)
</dt> <dd>

<span data-ttu-id="52e7f-133">Représente le GUID d’une connexion, à des fins de correspondance des connexions.</span><span class="sxs-lookup"><span data-stu-id="52e7f-133">Represents the GUID of a connection, for purposes of connection-matching.</span></span>

</dd> <dt>

[<span data-ttu-id="52e7f-134">**WINHTTP_PROXY_INFO**</span><span class="sxs-lookup"><span data-stu-id="52e7f-134">**WINHTTP_PROXY_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)
</dt> <dd>

<span data-ttu-id="52e7f-135">Contient la configuration de la session ou du proxy par défaut.</span><span class="sxs-lookup"><span data-stu-id="52e7f-135">Contains the session or default proxy configuration.</span></span>

</dd> <dt>

[<span data-ttu-id="52e7f-136">**WINHTTP_PROXY_RESULT**</span><span class="sxs-lookup"><span data-stu-id="52e7f-136">**WINHTTP_PROXY_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result)
</dt> <dd>

<span data-ttu-id="52e7f-137">Collection d’entrées de résultat de proxy fournies par [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span><span class="sxs-lookup"><span data-stu-id="52e7f-137">A collection of proxy result entries provided by [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="52e7f-138">**WINHTTP_PROXY_RESULT_ENTRY**</span><span class="sxs-lookup"><span data-stu-id="52e7f-138">**WINHTTP_PROXY_RESULT_ENTRY**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> <dd>

<span data-ttu-id="52e7f-139">Entrée de résultat d’un appel à [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span><span class="sxs-lookup"><span data-stu-id="52e7f-139">A result entry from a call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="52e7f-140">**WINHTTP_QUERY_CONNECTION_GROUP_RESULT**</span><span class="sxs-lookup"><span data-stu-id="52e7f-140">**WINHTTP_QUERY_CONNECTION_GROUP_RESULT**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_query_connection_group_result)
</dt> <dd>

<span data-ttu-id="52e7f-141">Représente une description de l’état actuel des connexions de WinHttp.</span><span class="sxs-lookup"><span data-stu-id="52e7f-141">Represents a description of the current state of WinHttp's connections.</span></span>

</dd> <dt>

[<span data-ttu-id="52e7f-142">**WINHTTP_REQUEST_STATS**</span><span class="sxs-lookup"><span data-stu-id="52e7f-142">**WINHTTP_REQUEST_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats)
</dt> <dd>

<span data-ttu-id="52e7f-143">Contient des statistiques pour une demande.</span><span class="sxs-lookup"><span data-stu-id="52e7f-143">Contains statistics for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="52e7f-144">**WINHTTP_REQUEST_TIMES**</span><span class="sxs-lookup"><span data-stu-id="52e7f-144">**WINHTTP_REQUEST_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times)
</dt> <dd>

<span data-ttu-id="52e7f-145">Contient les informations de minutage d’une demande.</span><span class="sxs-lookup"><span data-stu-id="52e7f-145">Contains timing information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="52e7f-146">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="52e7f-146">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info)
</dt> <dd>

<span data-ttu-id="52e7f-147">Contient les informations de chiffrement et de connexion SChannel pour une demande.</span><span class="sxs-lookup"><span data-stu-id="52e7f-147">Contains SChannel connection and cipher information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="52e7f-148">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="52e7f-148">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_async_result)
</dt> <dd>

<span data-ttu-id="52e7f-149">État du résultat d’une opération WebSocket.</span><span class="sxs-lookup"><span data-stu-id="52e7f-149">Result status of a WebSocket operation.</span></span>

</dd> <dt>

[<span data-ttu-id="52e7f-150">**WINHTTP_WEB_SOCKET_STATUS**</span><span class="sxs-lookup"><span data-stu-id="52e7f-150">**WINHTTP_WEB_SOCKET_STATUS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_status)
</dt> <dd>

<span data-ttu-id="52e7f-151">État d’une opération WebSocket.</span><span class="sxs-lookup"><span data-stu-id="52e7f-151">Status of a WebSocket operation.</span></span>

</dd> </dl>
