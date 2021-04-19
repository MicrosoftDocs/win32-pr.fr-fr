---
description: Demande une liste de résultats de l’historique des pixels dans le pixel, le rendu cible/UAV et le frame spécifiés.
MS-HAID: vspixengine.IPixelHistoryRequest\_RequestAsync\_DWORD\_Point2D\_DWORD\_IPixelHistoryCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixelHistoryRequest :: RequestAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 00A90033-FC57-4BEE-B950-82E678437F2A
api_name:
- IPixelHistoryRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f0209730e0e388b67281451a0337928257c1bae7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522727"
---
# <a name="span-idvspixengineipixelhistoryrequest_requestasync_dword_point2d_dword_ipixelhistorycallback_ptr_dword_dwordspanipixelhistoryrequestrequestasync-method"></a><span data-ttu-id="b6884-103"><span id="vspixengine.ipixelhistoryrequest_requestasync_dword_point2d_dword_ipixelhistorycallback_ptr_dword_dword"></span>IPixelHistoryRequest :: RequestAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="b6884-103"><span id="vspixengine.ipixelhistoryrequest_requestasync_dword_point2d_dword_ipixelhistorycallback_ptr_dword_dword"></span>IPixelHistoryRequest::RequestAsync method</span></span>

<span data-ttu-id="b6884-104">Demande une liste de résultats de l’historique des pixels dans le pixel, le rendu cible/UAV et le frame spécifiés.</span><span class="sxs-lookup"><span data-stu-id="b6884-104">Requests a list of pixel history results in the specified pixel, render tartget /UAV, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6884-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6884-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                   frameNumber,
   Point2D                 pixel,
   DWORD                   renderTargetPtr,
   IPixelHistoryCallback * requestCallback,
   DWORD                   requestCookie,
   DWORD                   progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="b6884-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6884-106">Parameters</span></span>

<span data-ttu-id="b6884-107">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="b6884-107">*frameNumber* </span></span>  
<span data-ttu-id="b6884-108">Frame spécifié.</span><span class="sxs-lookup"><span data-stu-id="b6884-108">The specified frame.</span></span>

<span data-ttu-id="b6884-109">*pixellisé* </span><span class="sxs-lookup"><span data-stu-id="b6884-109">*pixel* </span></span>  
<span data-ttu-id="b6884-110">Pixel spécifié.</span><span class="sxs-lookup"><span data-stu-id="b6884-110">The specified pixel.</span></span>

<span data-ttu-id="b6884-111">*renderTargetPtr* </span><span class="sxs-lookup"><span data-stu-id="b6884-111">*renderTargetPtr* </span></span>  
<span data-ttu-id="b6884-112">Cible de rendu spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b6884-112">The specified render target.</span></span>

<span data-ttu-id="b6884-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="b6884-113">*requestCallback* </span></span>  
<span data-ttu-id="b6884-114">Adresse d’un rappel utilisé pour notifify l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="b6884-114">The address of a callback used to notifify the host of results.</span></span>

<span data-ttu-id="b6884-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="b6884-115">*requestCookie* </span></span>  
<span data-ttu-id="b6884-116">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="b6884-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="b6884-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="b6884-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="b6884-118">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="b6884-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="b6884-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b6884-119">Return value</span></span>

<span data-ttu-id="b6884-120">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b6884-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b6884-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b6884-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6884-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6884-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b6884-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6884-123">Header</span></span></p></td><td><span data-ttu-id="b6884-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b6884-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b6884-125"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6884-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b6884-126">**IPixelHistoryRequest**</span><span class="sxs-lookup"><span data-stu-id="b6884-126">**IPixelHistoryRequest**</span></span>](/windows/desktop/direct3dtools/ipixelhistoryrequest)

 

 
