---
description: Demandes pour obtenir le contenu brut d’une vignette.
MS-HAID: vspixengine.ITileRequest_RequestBufferTileAsync_EventID_DWORD_BSTR_UINT_IBufferObjectDataCallback_ptr_DWORD_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ITileRequest :: RequestBufferTileAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2D68766F-1BED-439E-AC51-790471DA4F70
api_name:
- ITileRequest.RequestBufferTileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 83f013b4bc3235ece2850c75324333e4b59d298f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200833"
---
# <a name="span-idvspixengineitilerequest_requestbuffertileasync_eventid_dword_bstr_uint_ibufferobjectdatacallback_ptr_dword_dwordspanitilerequestrequestbuffertileasync-method"></a><span data-ttu-id="e281a-103"><span id="vspixengine.itilerequest_requestbuffertileasync_eventid_dword_bstr_uint_ibufferobjectdatacallback_ptr_dword_dword"></span>ITileRequest :: RequestBufferTileAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="e281a-103"><span id="vspixengine.itilerequest_requestbuffertileasync_eventid_dword_bstr_uint_ibufferobjectdatacallback_ptr_dword_dword"></span>ITileRequest::RequestBufferTileAsync method</span></span>

<span data-ttu-id="e281a-104">Demandes pour obtenir le contenu brut d’une vignette.</span><span class="sxs-lookup"><span data-stu-id="e281a-104">Requests to get the raw contents of a tile.</span></span>

## <a name="syntax"></a><span data-ttu-id="e281a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e281a-105">Syntax</span></span>


```C++
HRESULT RequestBufferTileAsync(
   EventID                     eventID,
   DWORD                       RequestedDataUID,
   BSTR                        File,
   UINT                        tileIndex,
   IBufferObjectDataCallback * requestCallback,
   DWORD                       requestCookie,
   DWORD                       progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="e281a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e281a-106">Parameters</span></span>

<span data-ttu-id="e281a-107">*1001* </span><span class="sxs-lookup"><span data-stu-id="e281a-107">*eventID* </span></span>  
<span data-ttu-id="e281a-108">Événement spécifié qui correspond au contenu de la vignette (par exemple, une cible de rendu peut changer au fil du temps).</span><span class="sxs-lookup"><span data-stu-id="e281a-108">The specified event to match the tile's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="e281a-109">*RequestedDataUID* </span><span class="sxs-lookup"><span data-stu-id="e281a-109">*RequestedDataUID* </span></span>  
<span data-ttu-id="e281a-110">Adresse de la mosaïque spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e281a-110">The address of the specified tile.</span></span>

<span data-ttu-id="e281a-111">*Txt* </span><span class="sxs-lookup"><span data-stu-id="e281a-111">*File* </span></span>  
<span data-ttu-id="e281a-112">Chaîne COM qui contient le nom du chemin d’accès du fichier dans lequel les résultats sont écrits.</span><span class="sxs-lookup"><span data-stu-id="e281a-112">A COM string that contains the pathname of the file where results are written.</span></span>

<span data-ttu-id="e281a-113">*tileIndex* </span><span class="sxs-lookup"><span data-stu-id="e281a-113">*tileIndex* </span></span>  
<span data-ttu-id="e281a-114">Index de la mosaïque spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e281a-114">The index of the specified tile.</span></span>

<span data-ttu-id="e281a-115">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="e281a-115">*requestCallback* </span></span>  
<span data-ttu-id="e281a-116">Adresse du rappel utilisée pour notifier l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="e281a-116">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="e281a-117">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="e281a-117">*requestCookie* </span></span>  
<span data-ttu-id="e281a-118">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="e281a-118">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="e281a-119">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="e281a-119">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="e281a-120">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="e281a-120">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="e281a-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e281a-121">Return value</span></span>

<span data-ttu-id="e281a-122">Si cette méthode est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="e281a-122">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="e281a-123">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e281a-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e281a-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e281a-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e281a-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="e281a-125">Header</span></span></p></td><td><span data-ttu-id="e281a-126">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e281a-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="e281a-127"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e281a-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="e281a-128">**ITileRequest**</span><span class="sxs-lookup"><span data-stu-id="e281a-128">**ITileRequest**</span></span>](/windows/desktop/direct3dtools/itilerequest)

 

 
