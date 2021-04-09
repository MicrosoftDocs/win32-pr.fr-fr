---
description: Demande à obtenir le contenu d’une texture en mosaïque sous la forme d’un. Fichier DDS (surface DirectDraw).
MS-HAID: vspixengine.ITileRequest\_RequestTextureTileAsync\_EventID\_DWORD\_UINT\_UINT\_UINT\_UINT\_BSTR\_ITextureCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ITileRequest :: RequestTextureTileAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E3F4FAC2-E7D9-4FDF-BE64-73D3EA175A8F
api_name:
- ITileRequest.RequestTextureTileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e22c3b54c1e04242805d698c37a1d4dd2709fa0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109307"
---
# <a name="span-idvspixengineitilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dwordspanitilerequestrequesttexturetileasync-method"></a><span data-ttu-id="5e11f-103"><span id="vspixengine.itilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dword"></span>ITileRequest :: RequestTextureTileAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="5e11f-103"><span id="vspixengine.itilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dword"></span>ITileRequest::RequestTextureTileAsync method</span></span>

<span data-ttu-id="5e11f-104">Demande à obtenir le contenu d’une texture en mosaïque sous la forme d’un. Fichier DDS (surface DirectDraw).</span><span class="sxs-lookup"><span data-stu-id="5e11f-104">Requests to get the contents of a tiled texture as a .DDS (DirectDraw Surface) file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e11f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e11f-105">Syntax</span></span>


```C++
HRESULT RequestTextureTileAsync(
   EventID            eventID,
   DWORD              textureFileptr,
   UINT               tileSubresource,
   UINT               tileX,
   UINT               tileY,
   UINT               tileZ,
   BSTR               ddsFilename,
   ITextureCallback * pRequestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="5e11f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e11f-106">Parameters</span></span>

<span data-ttu-id="5e11f-107">*1001* </span><span class="sxs-lookup"><span data-stu-id="5e11f-107">*eventID* </span></span>  
<span data-ttu-id="5e11f-108">Événement spécifié pour faire correspondre le contenu de la mémoire tampon à (par exemple, une cible de rendu peut changer au fil du temps).</span><span class="sxs-lookup"><span data-stu-id="5e11f-108">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="5e11f-109">*textureFileptr* </span><span class="sxs-lookup"><span data-stu-id="5e11f-109">*textureFileptr* </span></span>  
<span data-ttu-id="5e11f-110">Adresse de l’objet de texture spécifié.</span><span class="sxs-lookup"><span data-stu-id="5e11f-110">The address of the specified texture object.</span></span>

<span data-ttu-id="5e11f-111">*tileSubresource* </span><span class="sxs-lookup"><span data-stu-id="5e11f-111">*tileSubresource* </span></span>  
<span data-ttu-id="5e11f-112">Sous-ressource spécifiée de la vignette.</span><span class="sxs-lookup"><span data-stu-id="5e11f-112">The specified subresource of the tile.</span></span>

<span data-ttu-id="5e11f-113">*tileX* </span><span class="sxs-lookup"><span data-stu-id="5e11f-113">*tileX* </span></span>  
<span data-ttu-id="5e11f-114">Position X de la mosaïque spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5e11f-114">The specified tile X position.</span></span>

<span data-ttu-id="5e11f-115">*mosaïque* </span><span class="sxs-lookup"><span data-stu-id="5e11f-115">*tileY* </span></span>  
<span data-ttu-id="5e11f-116">Position Y de la mosaïque spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5e11f-116">The specified tile Y position.</span></span>

<span data-ttu-id="5e11f-117">*tileZ* </span><span class="sxs-lookup"><span data-stu-id="5e11f-117">*tileZ* </span></span>  
<span data-ttu-id="5e11f-118">Position Z de la mosaïque spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5e11f-118">The specified tile Z position.</span></span>

<span data-ttu-id="5e11f-119">*ddsFilename* </span><span class="sxs-lookup"><span data-stu-id="5e11f-119">*ddsFilename* </span></span>  
<span data-ttu-id="5e11f-120">Chaîne COM qui contient le chemin d’accès du fichier. DDS dans lequel les résultats sont écrits.</span><span class="sxs-lookup"><span data-stu-id="5e11f-120">A COM string that contains the pathname of the .dds file where results are written.</span></span>

<span data-ttu-id="5e11f-121">*pRequestCallback* </span><span class="sxs-lookup"><span data-stu-id="5e11f-121">*pRequestCallback* </span></span>  
<span data-ttu-id="5e11f-122">Adresse du rappel utilisée pour notifier l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="5e11f-122">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="5e11f-123">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="5e11f-123">*requestCookie* </span></span>  
<span data-ttu-id="5e11f-124">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="5e11f-124">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="5e11f-125">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="5e11f-125">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="5e11f-126">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="5e11f-126">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="5e11f-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5e11f-127">Return value</span></span>

<span data-ttu-id="5e11f-128">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5e11f-128">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5e11f-129">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5e11f-129">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e11f-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e11f-130">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5e11f-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="5e11f-131">Header</span></span></p></td><td><span data-ttu-id="5e11f-132">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="5e11f-132">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="5e11f-133"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e11f-133"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="5e11f-134">**ITileRequest**</span><span class="sxs-lookup"><span data-stu-id="5e11f-134">**ITileRequest**</span></span>](/windows/desktop/direct3dtools/itilerequest)

 

 
