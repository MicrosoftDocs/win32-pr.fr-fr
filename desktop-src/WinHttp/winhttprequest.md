---
Description: Cette rubrique fournit des informations sur l’utilisation de l’objet WinHttpRequest COM WinHTTP avec les langages de script.
ms.assetid: 0bbbf3dc-84b8-41d8-8627-e3d80ddcb783
title: Objet WinHttpRequest
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/22/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 907e94a731b2ec150a331347480c461d0d0fa319
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524015"
---
# <a name="winhttprequest-object"></a><span data-ttu-id="d2897-103">Objet WinHttpRequest</span><span class="sxs-lookup"><span data-stu-id="d2897-103">WinHttpRequest object</span></span>

<span data-ttu-id="d2897-104">Cette rubrique fournit des informations sur l’utilisation de l’objet **WinHttpRequest** com WinHTTP avec les langages de script.</span><span class="sxs-lookup"><span data-stu-id="d2897-104">This topic provides information about using the WinHTTP **WinHttpRequest** COM object with scripting languages.</span></span> <span data-ttu-id="d2897-105">Pour plus d’informations, y compris l’API C++ (WinHTTP), consultez [à propos de WinHTTP](about-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="d2897-105">For more information, including the C++ API (WinHTTP) please see [About WinHTTP](about-winhttp.md).</span></span> <span data-ttu-id="d2897-106">Pour une comparaison de ces interfaces, consultez [choix d’une interface WinHTTP](choosing-a-winhttp-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="d2897-106">See [Choosing a WinHTTP Interface](choosing-a-winhttp-interface.md) for a comparison of these interfaces.</span></span>

## <a name="example"></a><span data-ttu-id="d2897-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="d2897-107">Example</span></span>

```javascript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```

```cpp
 IWinHttpRequest *  pIWinHttpRequest = NULL;
 \\..
    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
```

<span data-ttu-id="d2897-108">Exemples de code tirés de la [propriété IWinHttpRequest :: Status](iwinhttprequest-status.md).</span><span class="sxs-lookup"><span data-stu-id="d2897-108">Code examples taken from [IWinHttpRequest::Status property](iwinhttprequest-status.md).</span></span>



## <a name="members"></a><span data-ttu-id="d2897-109">Membres</span><span class="sxs-lookup"><span data-stu-id="d2897-109">Members</span></span>

<span data-ttu-id="d2897-110">L’objet **WinHttpRequest** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d2897-110">The **WinHttpRequest** object has these types of members:</span></span>

-   [<span data-ttu-id="d2897-111">Événements</span><span class="sxs-lookup"><span data-stu-id="d2897-111">Events</span></span>](#events)
-   [<span data-ttu-id="d2897-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d2897-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="d2897-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d2897-113">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="d2897-114">Événements</span><span class="sxs-lookup"><span data-stu-id="d2897-114">Events</span></span>

<span data-ttu-id="d2897-115">L’objet **WinHttpRequest** contient ces événements.</span><span class="sxs-lookup"><span data-stu-id="d2897-115">The **WinHttpRequest** object has these events.</span></span>



| <span data-ttu-id="d2897-116">Événement</span><span class="sxs-lookup"><span data-stu-id="d2897-116">Event</span></span>                                                                            | <span data-ttu-id="d2897-117">Description</span><span class="sxs-lookup"><span data-stu-id="d2897-117">Description</span></span>                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="d2897-118">**OnError**</span><span class="sxs-lookup"><span data-stu-id="d2897-118">**OnError**</span></span>](iwinhttprequestevents-onerror.md)                                 | <span data-ttu-id="d2897-119">Se produit lorsqu’une erreur d’exécution se produit dans l’application.</span><span class="sxs-lookup"><span data-stu-id="d2897-119">Occurs when there is a run-time error in the application.</span></span><br/> |
| [<span data-ttu-id="d2897-120">**OnResponseDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="d2897-120">**OnResponseDataAvailable**</span></span>](iwinhttprequestevents-onresponsedataavailable.md) | <span data-ttu-id="d2897-121">Se produit lorsque des données sont disponibles à partir de la réponse.</span><span class="sxs-lookup"><span data-stu-id="d2897-121">Occurs when data is available from the response.</span></span><br/>          |
| [<span data-ttu-id="d2897-122">**OnResponseFinished**</span><span class="sxs-lookup"><span data-stu-id="d2897-122">**OnResponseFinished**</span></span>](iwinhttprequestevents-onresponsefinished.md)           | <span data-ttu-id="d2897-123">Se produit lorsque les données de réponse sont terminées.</span><span class="sxs-lookup"><span data-stu-id="d2897-123">Occurs when the response data is complete.</span></span><br/>                |
| [<span data-ttu-id="d2897-124">**OnResponseStart**</span><span class="sxs-lookup"><span data-stu-id="d2897-124">**OnResponseStart**</span></span>](iwinhttprequestevents-onresponsestart.md)                 | <span data-ttu-id="d2897-125">Se produit lorsque les données de réponse commencent à être reçues.</span><span class="sxs-lookup"><span data-stu-id="d2897-125">Occurs when the response data starts to be received.</span></span><br/>      |



 

### <a name="methods"></a><span data-ttu-id="d2897-126">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d2897-126">Methods</span></span>

<span data-ttu-id="d2897-127">L’objet **WinHttpRequest** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d2897-127">The **WinHttpRequest** object has these methods.</span></span>



| <span data-ttu-id="d2897-128">Méthode</span><span class="sxs-lookup"><span data-stu-id="d2897-128">Method</span></span>                                                                 | <span data-ttu-id="d2897-129">Description</span><span class="sxs-lookup"><span data-stu-id="d2897-129">Description</span></span>                                                                                                                                                |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2897-130">**Abandon**</span><span class="sxs-lookup"><span data-stu-id="d2897-130">**Abort**</span></span>](iwinhttprequest-abort.md)                                 | <span data-ttu-id="d2897-131">Abandonne une méthode d' [**envoi**](iwinhttprequest-send.md) [WinHTTP](about-winhttp.md) .</span><span class="sxs-lookup"><span data-stu-id="d2897-131">Aborts a [WinHTTP](about-winhttp.md) [**Send**](iwinhttprequest-send.md) method.</span></span><br/>                                                              |
| [<span data-ttu-id="d2897-132">**GetAllResponseHeaders**</span><span class="sxs-lookup"><span data-stu-id="d2897-132">**GetAllResponseHeaders**</span></span>](iwinhttprequest-getallresponseheaders.md) | <span data-ttu-id="d2897-133">Récupère tous les en-têtes de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="d2897-133">Retrieves all HTTP response headers.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="d2897-134">**GetResponseHeader**</span><span class="sxs-lookup"><span data-stu-id="d2897-134">**GetResponseHeader**</span></span>](iwinhttprequest-getresponseheader.md)         | <span data-ttu-id="d2897-135">Récupère les en-têtes de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="d2897-135">Retrieves the HTTP response headers.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="d2897-136">**Afficher**</span><span class="sxs-lookup"><span data-stu-id="d2897-136">**Open**</span></span>](iwinhttprequest-open.md)                                   | <span data-ttu-id="d2897-137">Ouvre une connexion HTTP à une ressource HTTP.</span><span class="sxs-lookup"><span data-stu-id="d2897-137">Opens an HTTP connection to an HTTP resource.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="d2897-138">**Envoyer**</span><span class="sxs-lookup"><span data-stu-id="d2897-138">**Send**</span></span>](iwinhttprequest-send.md)                                   | <span data-ttu-id="d2897-139">Envoie une requête HTTP à un serveur HTTP.</span><span class="sxs-lookup"><span data-stu-id="d2897-139">Sends an HTTP request to an HTTP server.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="d2897-140">**SetAutoLogonPolicy**</span><span class="sxs-lookup"><span data-stu-id="d2897-140">**SetAutoLogonPolicy**</span></span>](iwinhttprequest-setautologonpolicy.md)       | <span data-ttu-id="d2897-141">Définit la [stratégie d’ouverture de session automatique](authentication-in-winhttp.md)actuelle.</span><span class="sxs-lookup"><span data-stu-id="d2897-141">Sets the current [Automatic Logon Policy](authentication-in-winhttp.md).</span></span><br/>                                                |
| [<span data-ttu-id="d2897-142">**SetClientCertificate**</span><span class="sxs-lookup"><span data-stu-id="d2897-142">**SetClientCertificate**</span></span>](iwinhttprequest-setclientcertificate.md)   | <span data-ttu-id="d2897-143">Sélectionne un certificat client à envoyer à un serveur HTTPs (Secure Hypertext Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="d2897-143">Selects a client certificate to send to a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span><br/>                                                    |
| [<span data-ttu-id="d2897-144">**SetCredentials**</span><span class="sxs-lookup"><span data-stu-id="d2897-144">**SetCredentials**</span></span>](iwinhttprequest-setcredentials.md)               | <span data-ttu-id="d2897-145">Définit les informations d’identification à utiliser avec un serveur HTTP, qu’il s’agisse d’un serveur d’origine ou d’un serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="d2897-145">Sets credentials to be used with an HTTP server either an origin or a proxy server.</span></span><br/>                                                             |
| [<span data-ttu-id="d2897-146">**SetProxy**</span><span class="sxs-lookup"><span data-stu-id="d2897-146">**SetProxy**</span></span>](iwinhttprequest-setproxy.md)                           | <span data-ttu-id="d2897-147">Définit les informations du serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="d2897-147">Sets proxy server information.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="d2897-148">**SetRequestHeader**</span><span class="sxs-lookup"><span data-stu-id="d2897-148">**SetRequestHeader**</span></span>](iwinhttprequest-setrequestheader.md)           | <span data-ttu-id="d2897-149">Ajoute, modifie ou supprime un en-tête de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="d2897-149">Adds, changes, or deletes an HTTP request header.</span></span><br/>                                                                                               |
| [<span data-ttu-id="d2897-150">**SetTimeouts**</span><span class="sxs-lookup"><span data-stu-id="d2897-150">**SetTimeouts**</span></span>](iwinhttprequest-settimeouts.md)                     | <span data-ttu-id="d2897-151">Spécifie, en millisecondes, les composants de délai d’attente individuels d’une opération d’envoi/réception.</span><span class="sxs-lookup"><span data-stu-id="d2897-151">Specifies, in milliseconds, the individual time-out components of a send/receive operation.</span></span><br/>                                                     |
| [<span data-ttu-id="d2897-152">**WaitForResponse**</span><span class="sxs-lookup"><span data-stu-id="d2897-152">**WaitForResponse**</span></span>](iwinhttprequest-waitforresponse.md)             | <span data-ttu-id="d2897-153">Spécifie le temps d’attente, en secondes, pour qu’une méthode d' [**envoi**](iwinhttprequest-send.md) asynchrone se termine, avec une valeur de délai d’attente facultative.</span><span class="sxs-lookup"><span data-stu-id="d2897-153">Specifies the wait time, in seconds, for an asynchronous [**Send**](iwinhttprequest-send.md) method to complete, with optional time-out value.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d2897-154">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d2897-154">Properties</span></span>

<span data-ttu-id="d2897-155">L’objet **WinHttpRequest** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d2897-155">The **WinHttpRequest** object has these properties.</span></span>



| <span data-ttu-id="d2897-156">Propriété</span><span class="sxs-lookup"><span data-stu-id="d2897-156">Property</span></span>                                                            | <span data-ttu-id="d2897-157">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="d2897-157">Access type</span></span>           | <span data-ttu-id="d2897-158">Description</span><span class="sxs-lookup"><span data-stu-id="d2897-158">Description</span></span>                                                                     |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="d2897-159">**Option**</span><span class="sxs-lookup"><span data-stu-id="d2897-159">**Option**</span></span>](iwinhttprequest-option.md)<br/>                 | <span data-ttu-id="d2897-160">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d2897-160">Read/write</span></span><br/> | <span data-ttu-id="d2897-161">Définit ou récupère une valeur d’option WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="d2897-161">Sets or retrieves a WinHTTP option value.</span></span><br/>                            |
| [<span data-ttu-id="d2897-162">**ResponseBody**</span><span class="sxs-lookup"><span data-stu-id="d2897-162">**ResponseBody**</span></span>](iwinhttprequest-responsebody.md)<br/>     | <span data-ttu-id="d2897-163">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2897-163">Read-only</span></span><br/>  | <span data-ttu-id="d2897-164">Récupère le corps d’entité de réponse sous la forme d’un tableau d’octets non signés.</span><span class="sxs-lookup"><span data-stu-id="d2897-164">Retrieves the response entity body as an array of unsigned bytes.</span></span><br/>    |
| [<span data-ttu-id="d2897-165">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="d2897-165">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)<br/> | <span data-ttu-id="d2897-166">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2897-166">Read-only</span></span><br/>  | <span data-ttu-id="d2897-167">Récupère le corps d’entité de réponse en tant qu' [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="d2897-167">Retrieves the response entity body as an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span><br/> |
| [<span data-ttu-id="d2897-168">**ResponseText**</span><span class="sxs-lookup"><span data-stu-id="d2897-168">**ResponseText**</span></span>](iwinhttprequest-responsetext.md)<br/>     | <span data-ttu-id="d2897-169">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2897-169">Read-only</span></span><br/>  | <span data-ttu-id="d2897-170">Récupère le corps d’entité de réponse sous forme de texte.</span><span class="sxs-lookup"><span data-stu-id="d2897-170">Retrieves the response entity body as text.</span></span><br/>                          |
| [<span data-ttu-id="d2897-171">**Statu**</span><span class="sxs-lookup"><span data-stu-id="d2897-171">**Status**</span></span>](iwinhttprequest-status.md)<br/>                 | <span data-ttu-id="d2897-172">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2897-172">Read-only</span></span><br/>  | <span data-ttu-id="d2897-173">Récupère le code d’état HTTP de la dernière réponse.</span><span class="sxs-lookup"><span data-stu-id="d2897-173">Retrieves the HTTP status code from the last response.</span></span><br/>               |
| [<span data-ttu-id="d2897-174">**StatusText**</span><span class="sxs-lookup"><span data-stu-id="d2897-174">**StatusText**</span></span>](iwinhttprequest-statustext.md)<br/>         | <span data-ttu-id="d2897-175">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2897-175">Read-only</span></span><br/>  | <span data-ttu-id="d2897-176">Récupère le texte d’état HTTP.</span><span class="sxs-lookup"><span data-stu-id="d2897-176">Retrieves HTTP status text.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="d2897-177">Notes</span><span class="sxs-lookup"><span data-stu-id="d2897-177">Remarks</span></span>

<span data-ttu-id="d2897-178">L’objet **WinHttpRequest** utilise l’interface [**IErrorInfo**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo) pour fournir les données d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d2897-178">The **WinHttpRequest** object uses the [**IErrorInfo**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo) interface to provide error data.</span></span> <span data-ttu-id="d2897-179">Une description et une valeur d’erreur numérique peuvent être obtenues avec l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) dans Microsoft Visual Basic Scripting Edition (VBScript) et l’objet [Error](https://msdn.microsoft.com/library/dww52sbt.aspx) dans Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="d2897-179">A description and numerical error value can be obtained with the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object in Microsoft Visual Basic Scripting Edition (VBScript), and the [Error](https://msdn.microsoft.com/library/dww52sbt.aspx) object in Microsoft JScript.</span></span> <span data-ttu-id="d2897-180">Les 16 bits inférieurs d’un numéro d’erreur correspondent aux valeurs figurant dans les [**messages d’erreur**](error-messages.md).</span><span class="sxs-lookup"><span data-stu-id="d2897-180">The lower 16 bits of an error number correspond to the values found in [**Error Messages**](error-messages.md).</span></span>

> [!Note]  
> <span data-ttu-id="d2897-181">Pour Windows XP et Windows 2000, consultez [Configuration requise](winhttp-start-page.md)pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="d2897-181">For Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d2897-182">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2897-182">Requirements</span></span>



| <span data-ttu-id="d2897-183">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2897-183">Requirement</span></span> | <span data-ttu-id="d2897-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2897-184">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2897-185">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2897-185">Minimum supported client</span></span><br/> | <span data-ttu-id="d2897-186">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2897-186">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="d2897-187">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2897-187">Minimum supported server</span></span><br/> | <span data-ttu-id="d2897-188">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2897-188">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="d2897-189">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="d2897-189">Redistributable</span></span><br/>          | <span data-ttu-id="d2897-190">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d2897-190">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="d2897-191">MIDL</span><span class="sxs-lookup"><span data-stu-id="d2897-191">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d2897-192"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d2897-192"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="d2897-193">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d2897-193">Library</span></span><br/>                  | <dl> <span data-ttu-id="d2897-194"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2897-194"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="d2897-195">DLL</span><span class="sxs-lookup"><span data-stu-id="d2897-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2897-196"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2897-196"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d2897-197">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2897-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2897-198">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="d2897-198">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

