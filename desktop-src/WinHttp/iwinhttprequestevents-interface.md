---
description: Fournit des événements pour les services HTTP Microsoft Windows (WinHTTP).
ms.assetid: 0721d7f9-2e84-41a9-be52-89c8d638eb90
title: Interface IWinHttpRequestEvents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequestEvents
api_type:
- COM
api_location:
- HttpRequest.idl
ms.openlocfilehash: 3cdd0bf10c0d4bd75351ddaab6e88ce7182850fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519503"
---
# <a name="iwinhttprequestevents-interface"></a><span data-ttu-id="73e1e-103">Interface IWinHttpRequestEvents</span><span class="sxs-lookup"><span data-stu-id="73e1e-103">IWinHttpRequestEvents interface</span></span>

<span data-ttu-id="73e1e-104">L’interface **IWinHttpRequestEvents** fournit des événements pour les [services http Microsoft Windows (WinHTTP)](about-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="73e1e-104">The **IWinHttpRequestEvents** interface provides events for [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md).</span></span> <span data-ttu-id="73e1e-105">Elle utilise uniquement des méthodes d’événement.</span><span class="sxs-lookup"><span data-stu-id="73e1e-105">It uses only event methods.</span></span>

## <a name="members"></a><span data-ttu-id="73e1e-106">Membres</span><span class="sxs-lookup"><span data-stu-id="73e1e-106">Members</span></span>

<span data-ttu-id="73e1e-107">L’interface **IWinHttpRequestEvents** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="73e1e-107">The **IWinHttpRequestEvents** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="73e1e-108">**IWinHttpRequestEvents** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="73e1e-108">**IWinHttpRequestEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="73e1e-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="73e1e-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="73e1e-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="73e1e-110">Methods</span></span>

<span data-ttu-id="73e1e-111">L’interface **IWinHttpRequestEvents** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="73e1e-111">The **IWinHttpRequestEvents** interface has these methods.</span></span>



| <span data-ttu-id="73e1e-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="73e1e-112">Method</span></span>                                                                           | <span data-ttu-id="73e1e-113">Description</span><span class="sxs-lookup"><span data-stu-id="73e1e-113">Description</span></span>                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="73e1e-114">**OnError**</span><span class="sxs-lookup"><span data-stu-id="73e1e-114">**OnError**</span></span>](iwinhttprequestevents-onerror.md)                                 | <span data-ttu-id="73e1e-115">Se produit lorsqu’une erreur d’exécution se produit dans l’application.</span><span class="sxs-lookup"><span data-stu-id="73e1e-115">Occurs when there is a run-time error in the application.</span></span><br/> |
| [<span data-ttu-id="73e1e-116">**OnResponseDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="73e1e-116">**OnResponseDataAvailable**</span></span>](iwinhttprequestevents-onresponsedataavailable.md) | <span data-ttu-id="73e1e-117">Se produit lorsque des données sont disponibles à partir de la réponse.</span><span class="sxs-lookup"><span data-stu-id="73e1e-117">Occurs when data is available from the response.</span></span><br/>          |
| [<span data-ttu-id="73e1e-118">**OnResponseFinished**</span><span class="sxs-lookup"><span data-stu-id="73e1e-118">**OnResponseFinished**</span></span>](iwinhttprequestevents-onresponsefinished.md)           | <span data-ttu-id="73e1e-119">Se produit lorsque les données de réponse sont terminées.</span><span class="sxs-lookup"><span data-stu-id="73e1e-119">Occurs when the response data is complete.</span></span><br/>                |
| [<span data-ttu-id="73e1e-120">**OnResponseStart**</span><span class="sxs-lookup"><span data-stu-id="73e1e-120">**OnResponseStart**</span></span>](iwinhttprequestevents-onresponsestart.md)                 | <span data-ttu-id="73e1e-121">Se produit lorsque les données de réponse commencent à être reçues.</span><span class="sxs-lookup"><span data-stu-id="73e1e-121">Occurs when the response data starts to be received.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="73e1e-122">Notes</span><span class="sxs-lookup"><span data-stu-id="73e1e-122">Remarks</span></span>

<span data-ttu-id="73e1e-123">La procédure suivante décrit comment s’inscrire pour les notifications.</span><span class="sxs-lookup"><span data-stu-id="73e1e-123">The following procedure describes how to register for notifications.</span></span>

1.  <span data-ttu-id="73e1e-124">Obtient une interface [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) en appelant **QueryInterface** sur un objet [**IWinHttpRequest**](iwinhttprequest-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="73e1e-124">Get an [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) interface by calling **QueryInterface** on an [**IWinHttpRequest**](iwinhttprequest-interface.md) object.</span></span>
2.  <span data-ttu-id="73e1e-125">Appelez [FindConnectionPoint](/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) sur l’interface retournée et transmettez **IID \_ IWinHttpRequestEvents** à *riid*.</span><span class="sxs-lookup"><span data-stu-id="73e1e-125">Call [FindConnectionPoint](/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) on the returned interface and pass **IID\_IWinHttpRequestEvents** to *riid*.</span></span>
3.  <span data-ttu-id="73e1e-126">Appelez [Advise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) sur le point de connexion retourné et transmettez un pointeur vers une interface **IUnknown** sur un objet qui implémente **IWinHttpRequestEvents** à *punk*.</span><span class="sxs-lookup"><span data-stu-id="73e1e-126">Call [Advise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) on the returned connection point and pass a pointer to an **IUnknown** interface on an object that implements **IWinHttpRequestEvents** to *pUnk*.</span></span>

<span data-ttu-id="73e1e-127">Les notifications peuvent être arrêtées en appelant [Unadvise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise) sur le point de connexion retourné à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="73e1e-127">Notifications can be terminated by calling [Unadvise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise) on the connection point returned in step 2.</span></span>

<span data-ttu-id="73e1e-128">Pour afficher du code qui s’inscrit pour les notifications COM, consultez la section client de l’article [points de connexion com](/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points) .</span><span class="sxs-lookup"><span data-stu-id="73e1e-128">To view some code that registers for COM notifications, see the Client section of the [COM Connection Points](/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points) article.</span></span>

> [!Note]  
> <span data-ttu-id="73e1e-129">Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="73e1e-129">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="73e1e-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73e1e-130">Requirements</span></span>



| <span data-ttu-id="73e1e-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73e1e-131">Requirement</span></span> | <span data-ttu-id="73e1e-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="73e1e-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="73e1e-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73e1e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="73e1e-134">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73e1e-134">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="73e1e-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73e1e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="73e1e-136">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73e1e-136">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="73e1e-137">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="73e1e-137">Redistributable</span></span><br/>          | <span data-ttu-id="73e1e-138">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="73e1e-138">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="73e1e-139">MIDL</span><span class="sxs-lookup"><span data-stu-id="73e1e-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="73e1e-140"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="73e1e-140"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73e1e-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73e1e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73e1e-142">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="73e1e-142">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="73e1e-143">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="73e1e-143">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

