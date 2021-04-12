---
description: Fonction de rappel utilisée pour informer l’hôte des frames capturés.
MS-HAID: vspixengine.IFrameListCallback\_ResultCallback\_DWORD\_DWORD\_arr\_DWORD\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IFrameListCallback :: ResultCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AEB340C6-74AA-4F8B-86D0-9C0366ECDE70
api_name:
- IFrameListCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 00a991ec2d380d9c052f02ed69bb71d233fd0d93
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482664"
---
# <a name="span-idvspixengineiframelistcallback_resultcallback_dword_dword_arr_dword_arrspaniframelistcallbackresultcallback-method"></a><span data-ttu-id="b4593-103"><span id="vspixengine.iframelistcallback_resultcallback_dword_dword_arr_dword_arr"></span>IFrameListCallback :: ResultCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="b4593-103"><span id="vspixengine.iframelistcallback_resultcallback_dword_dword_arr_dword_arr"></span>IFrameListCallback::ResultCallback method</span></span>

<span data-ttu-id="b4593-104">Fonction de rappel utilisée pour informer l’hôte des frames capturés.</span><span class="sxs-lookup"><span data-stu-id="b4593-104">A callback function used to notify the host of which frames were captured.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4593-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4593-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD    numFrames,
   DWORD [] count0_frameNumbers,
   DWORD [] count0_frameEventIDs
);
```

## <a name="parameters"></a><span data-ttu-id="b4593-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4593-106">Parameters</span></span>

<span data-ttu-id="b4593-107">*numFrames* </span><span class="sxs-lookup"><span data-stu-id="b4593-107">*numFrames* </span></span>  
<span data-ttu-id="b4593-108">Nombre de trames capturées.</span><span class="sxs-lookup"><span data-stu-id="b4593-108">The number of frames captured.</span></span>

<span data-ttu-id="b4593-109">*count0 \_ frameNumbers* </span><span class="sxs-lookup"><span data-stu-id="b4593-109">*count0\_frameNumbers* </span></span>  
<span data-ttu-id="b4593-110">Nombre de frames des frames capturés.</span><span class="sxs-lookup"><span data-stu-id="b4593-110">The frame numbers of the captured frames.</span></span>

<span data-ttu-id="b4593-111">*count0 \_ frameEventIDs* </span><span class="sxs-lookup"><span data-stu-id="b4593-111">*count0\_frameEventIDs* </span></span>  
<span data-ttu-id="b4593-112">Événement final associé à chaque frame.</span><span class="sxs-lookup"><span data-stu-id="b4593-112">The final event associated with each frame.</span></span>

## <a name="return-value"></a><span data-ttu-id="b4593-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b4593-113">Return value</span></span>

<span data-ttu-id="b4593-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b4593-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b4593-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b4593-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4593-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4593-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b4593-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4593-117">Header</span></span></p></td><td><span data-ttu-id="b4593-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b4593-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b4593-119"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4593-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b4593-120">**IFrameListCallback**</span><span class="sxs-lookup"><span data-stu-id="b4593-120">**IFrameListCallback**</span></span>](/windows/desktop/direct3dtools/iframelistcallback)

 

 
