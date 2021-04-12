---
description: L’interface IWinHttpRequest fournit toutes les méthodes inégales pour les services HTTP Microsoft Windows (WinHTTP).
ms.assetid: 6417b3b5-b74a-4c7b-acf9-87e2e814a4df
title: Interface IWinHttpRequest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 77ebc8947ad36d2dc9efba121cdd6da2d6de359b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203166"
---
# <a name="iwinhttprequest-interface"></a><span data-ttu-id="c57b4-103">Interface IWinHttpRequest</span><span class="sxs-lookup"><span data-stu-id="c57b4-103">IWinHttpRequest interface</span></span>

<span data-ttu-id="c57b4-104">L’interface **IWinHttpRequest** fournit toutes les méthodes inégales pour les [services http Microsoft Windows (WinHTTP)](about-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="c57b4-104">The **IWinHttpRequest** interface provides all of the nonevent methods for [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md).</span></span>

## <a name="members"></a><span data-ttu-id="c57b4-105">Membres</span><span class="sxs-lookup"><span data-stu-id="c57b4-105">Members</span></span>

<span data-ttu-id="c57b4-106">L’interface **IWinHttpRequest** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c57b4-106">The **IWinHttpRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c57b4-107">**IWinHttpRequest** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c57b4-107">**IWinHttpRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="c57b4-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c57b4-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="c57b4-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c57b4-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c57b4-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c57b4-110">Methods</span></span>

<span data-ttu-id="c57b4-111">L’interface **IWinHttpRequest** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c57b4-111">The **IWinHttpRequest** interface has these methods.</span></span>



| <span data-ttu-id="c57b4-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="c57b4-112">Method</span></span>                                                                 | <span data-ttu-id="c57b4-113">Description</span><span class="sxs-lookup"><span data-stu-id="c57b4-113">Description</span></span>                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c57b4-114">**Abandon**</span><span class="sxs-lookup"><span data-stu-id="c57b4-114">**Abort**</span></span>](iwinhttprequest-abort.md)                                 | <span data-ttu-id="c57b4-115">Abandonne une méthode d' [**envoi**](iwinhttprequest-send.md) [WinHTTP](about-winhttp.md) .</span><span class="sxs-lookup"><span data-stu-id="c57b4-115">Aborts a [WinHTTP](about-winhttp.md) [**Send**](iwinhttprequest-send.md) method.</span></span><br/>                                           |
| [<span data-ttu-id="c57b4-116">**GetAllResponseHeaders**</span><span class="sxs-lookup"><span data-stu-id="c57b4-116">**GetAllResponseHeaders**</span></span>](iwinhttprequest-getallresponseheaders.md) | <span data-ttu-id="c57b4-117">Récupère tous les en-têtes de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="c57b4-117">Retrieves all HTTP response headers.</span></span><br/>                                                                                         |
| [<span data-ttu-id="c57b4-118">**GetResponseHeader**</span><span class="sxs-lookup"><span data-stu-id="c57b4-118">**GetResponseHeader**</span></span>](iwinhttprequest-getresponseheader.md)         | <span data-ttu-id="c57b4-119">Récupère les en-têtes de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="c57b4-119">Retrieves the HTTP response headers.</span></span><br/>                                                                                         |
| [<span data-ttu-id="c57b4-120">**Afficher**</span><span class="sxs-lookup"><span data-stu-id="c57b4-120">**Open**</span></span>](iwinhttprequest-open.md)                                   | <span data-ttu-id="c57b4-121">Ouvre une connexion HTTP à une ressource HTTP.</span><span class="sxs-lookup"><span data-stu-id="c57b4-121">Opens an HTTP connection to an HTTP resource.</span></span><br/>                                                                                |
| [<span data-ttu-id="c57b4-122">**Envoyer**</span><span class="sxs-lookup"><span data-stu-id="c57b4-122">**Send**</span></span>](iwinhttprequest-send.md)                                   | <span data-ttu-id="c57b4-123">Envoie une requête HTTP à un serveur HTTP.</span><span class="sxs-lookup"><span data-stu-id="c57b4-123">Sends an HTTP request to an HTTP server.</span></span><br/>                                                                                     |
| [<span data-ttu-id="c57b4-124">**SetAutoLogonPolicy**</span><span class="sxs-lookup"><span data-stu-id="c57b4-124">**SetAutoLogonPolicy**</span></span>](iwinhttprequest-setautologonpolicy.md)       | <span data-ttu-id="c57b4-125">Définit la [stratégie d’ouverture de session automatique](authentication-in-winhttp.md)actuelle.</span><span class="sxs-lookup"><span data-stu-id="c57b4-125">Sets the current [Automatic Logon Policy](authentication-in-winhttp.md).</span></span><br/>                             |
| [<span data-ttu-id="c57b4-126">**SetClientCertificate**</span><span class="sxs-lookup"><span data-stu-id="c57b4-126">**SetClientCertificate**</span></span>](iwinhttprequest-setclientcertificate.md)   | <span data-ttu-id="c57b4-127">Sélectionne un certificat client à envoyer à un serveur HTTPs (Secure Hypertext Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="c57b4-127">Selects a client certificate to send to a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span><br/>                                 |
| [<span data-ttu-id="c57b4-128">**SetCredentials**</span><span class="sxs-lookup"><span data-stu-id="c57b4-128">**SetCredentials**</span></span>](iwinhttprequest-setcredentials.md)               | <span data-ttu-id="c57b4-129">Définit les informations d’identification à utiliser avec un serveur HTTP, un serveur proxy ou un serveur d’origine.</span><span class="sxs-lookup"><span data-stu-id="c57b4-129">Sets credentials to be used with an HTTP server, either a proxy server or an originating server.</span></span><br/>                             |
| [<span data-ttu-id="c57b4-130">**SetProxy**</span><span class="sxs-lookup"><span data-stu-id="c57b4-130">**SetProxy**</span></span>](iwinhttprequest-setproxy.md)                           | <span data-ttu-id="c57b4-131">Définit les informations du serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="c57b4-131">Sets proxy server information.</span></span><br/>                                                                                               |
| [<span data-ttu-id="c57b4-132">**SetRequestHeader**</span><span class="sxs-lookup"><span data-stu-id="c57b4-132">**SetRequestHeader**</span></span>](iwinhttprequest-setrequestheader.md)           | <span data-ttu-id="c57b4-133">Ajoute, modifie ou supprime un en-tête de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="c57b4-133">Adds, changes, or deletes an HTTP request header.</span></span><br/>                                                                            |
| [<span data-ttu-id="c57b4-134">**SetTimeouts**</span><span class="sxs-lookup"><span data-stu-id="c57b4-134">**SetTimeouts**</span></span>](iwinhttprequest-settimeouts.md)                     | <span data-ttu-id="c57b4-135">Spécifie les différents composants de délai d’attente d’une opération d’envoi/réception, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="c57b4-135">Specifies the individual time-out components of a send/receive operation, in milliseconds.</span></span><br/>                                   |
| [<span data-ttu-id="c57b4-136">**WaitForResponse**</span><span class="sxs-lookup"><span data-stu-id="c57b4-136">**WaitForResponse**</span></span>](iwinhttprequest-waitforresponse.md)             | <span data-ttu-id="c57b4-137">Attend la fin d’une méthode d' [**envoi**](iwinhttprequest-send.md) asynchrone, avec une valeur de délai d’attente facultative, en secondes.</span><span class="sxs-lookup"><span data-stu-id="c57b4-137">Waits for an asynchronous [**Send**](iwinhttprequest-send.md) method to complete, with optional time-out value, in seconds.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c57b4-138">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c57b4-138">Properties</span></span>

<span data-ttu-id="c57b4-139">L’interface **IWinHttpRequest** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c57b4-139">The **IWinHttpRequest** interface has these properties.</span></span>



| <span data-ttu-id="c57b4-140">Propriété</span><span class="sxs-lookup"><span data-stu-id="c57b4-140">Property</span></span>                                                            | <span data-ttu-id="c57b4-141">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="c57b4-141">Access type</span></span>           | <span data-ttu-id="c57b4-142">Description</span><span class="sxs-lookup"><span data-stu-id="c57b4-142">Description</span></span>                                                           |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="c57b4-143">**Option**</span><span class="sxs-lookup"><span data-stu-id="c57b4-143">**Option**</span></span>](iwinhttprequest-option.md)<br/>                 | <span data-ttu-id="c57b4-144">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c57b4-144">Read/write</span></span><br/> | <span data-ttu-id="c57b4-145">Valeur d’option WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="c57b4-145">A WinHTTP option value.</span></span><br/>                                    |
| [<span data-ttu-id="c57b4-146">**ResponseBody**</span><span class="sxs-lookup"><span data-stu-id="c57b4-146">**ResponseBody**</span></span>](iwinhttprequest-responsebody.md)<br/>     | <span data-ttu-id="c57b4-147">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c57b4-147">Read-only</span></span><br/>  | <span data-ttu-id="c57b4-148">Corps d’entité de réponse sous la forme d’un tableau d’octets non signés.</span><span class="sxs-lookup"><span data-stu-id="c57b4-148">The response entity body as an array of unsigned bytes.</span></span><br/>    |
| [<span data-ttu-id="c57b4-149">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="c57b4-149">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)<br/> | <span data-ttu-id="c57b4-150">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c57b4-150">Read-only</span></span><br/>  | <span data-ttu-id="c57b4-151">Corps d’entité de réponse en tant qu' [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="c57b4-151">The response entity body as an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span><br/> |
| [<span data-ttu-id="c57b4-152">**ResponseText**</span><span class="sxs-lookup"><span data-stu-id="c57b4-152">**ResponseText**</span></span>](iwinhttprequest-responsetext.md)<br/>     | <span data-ttu-id="c57b4-153">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c57b4-153">Read-only</span></span><br/>  | <span data-ttu-id="c57b4-154">Corps d’entité de réponse.</span><span class="sxs-lookup"><span data-stu-id="c57b4-154">The response entity body.</span></span><br/>                                  |
| [<span data-ttu-id="c57b4-155">**Statu**</span><span class="sxs-lookup"><span data-stu-id="c57b4-155">**Status**</span></span>](iwinhttprequest-status.md)<br/>                 | <span data-ttu-id="c57b4-156">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c57b4-156">Read-only</span></span><br/>  | <span data-ttu-id="c57b4-157">Code d’état HTTP de la dernière réponse.</span><span class="sxs-lookup"><span data-stu-id="c57b4-157">The HTTP status code from the last response.</span></span><br/>               |
| [<span data-ttu-id="c57b4-158">**StatusText**</span><span class="sxs-lookup"><span data-stu-id="c57b4-158">**StatusText**</span></span>](iwinhttprequest-statustext.md)<br/>         | <span data-ttu-id="c57b4-159">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c57b4-159">Read-only</span></span><br/>  | <span data-ttu-id="c57b4-160">Texte d’état HTTP.</span><span class="sxs-lookup"><span data-stu-id="c57b4-160">The HTTP status text.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="c57b4-161">Notes</span><span class="sxs-lookup"><span data-stu-id="c57b4-161">Remarks</span></span>

<span data-ttu-id="c57b4-162">L’interface **IWinHttpRequest** définie dans HttpRequest. idl est implémentée par une classe avec l’ID **CLSID \_ WinHttpRequest**.</span><span class="sxs-lookup"><span data-stu-id="c57b4-162">The **IWinHttpRequest** interface defined in httprequest.idl is implemented by a class with id of **CLSID\_WinHttpRequest**.</span></span> <span data-ttu-id="c57b4-163">Une application obtient cette interface en appelant [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) avec l’ID de classe **CLSID \_ WinHttpRequest** et l’ID d’interface **\_ IWinHttpRequest IID**.</span><span class="sxs-lookup"><span data-stu-id="c57b4-163">An application obtain this interface by calling [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) with a class id of **CLSID\_WinHttpRequest** and an interface id of **IID\_IWinHttpRequest**.</span></span>

> [!Note]  
> <span data-ttu-id="c57b4-164">Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="c57b4-164">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c57b4-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c57b4-165">Requirements</span></span>



| <span data-ttu-id="c57b4-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c57b4-166">Requirement</span></span> | <span data-ttu-id="c57b4-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="c57b4-167">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c57b4-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c57b4-168">Minimum supported client</span></span><br/> | <span data-ttu-id="c57b4-169">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c57b4-169">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="c57b4-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c57b4-170">Minimum supported server</span></span><br/> | <span data-ttu-id="c57b4-171">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c57b4-171">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="c57b4-172">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="c57b4-172">Redistributable</span></span><br/>          | <span data-ttu-id="c57b4-173">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="c57b4-173">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="c57b4-174">MIDL</span><span class="sxs-lookup"><span data-stu-id="c57b4-174">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c57b4-175"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c57b4-175"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="c57b4-176">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c57b4-176">Library</span></span><br/>                  | <dl> <span data-ttu-id="c57b4-177"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c57b4-177"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="c57b4-178">DLL</span><span class="sxs-lookup"><span data-stu-id="c57b4-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c57b4-179"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c57b4-179"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c57b4-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c57b4-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c57b4-181">**IWinHttpRequestEvents**</span><span class="sxs-lookup"><span data-stu-id="c57b4-181">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="c57b4-182">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="c57b4-182">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

