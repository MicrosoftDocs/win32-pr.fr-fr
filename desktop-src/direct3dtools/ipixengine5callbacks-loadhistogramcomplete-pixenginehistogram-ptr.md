---
description: Fonction de rappel utilisée pour notifier l’hôte lorsqu’une charge d’histogramme est terminée.
MS-HAID: vspixengine.IPixEngine5Callbacks\_LoadHistogramComplete\_PixEngineHistogram\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5Callbacks :: LoadHistogramComplete, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A72DB49E-06C8-4061-9872-C4380D90EEB2
api_name:
- IPixEngine5Callbacks.LoadHistogramComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d0e468422f722a8bd549d63f34225833462856b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106543069"
---
# <a name="span-idvspixengineipixengine5callbacks_loadhistogramcomplete_pixenginehistogram_ptrspanipixengine5callbacksloadhistogramcomplete-method"></a><span data-ttu-id="ebbb4-103"><span id="vspixengine.ipixengine5callbacks_loadhistogramcomplete_pixenginehistogram_ptr"></span>IPixEngine5Callbacks :: LoadHistogramComplete, méthode</span><span class="sxs-lookup"><span data-stu-id="ebbb4-103"><span id="vspixengine.ipixengine5callbacks_loadhistogramcomplete_pixenginehistogram_ptr"></span>IPixEngine5Callbacks::LoadHistogramComplete method</span></span>

<span data-ttu-id="ebbb4-104">Fonction de rappel utilisée pour notifier l’hôte lorsqu’une charge d’histogramme est terminée.</span><span class="sxs-lookup"><span data-stu-id="ebbb4-104">A callback function used to notify the host when a histogram load has been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebbb4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebbb4-105">Syntax</span></span>


```C++
HRESULT LoadHistogramAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   BSTR                       histogramDataFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="ebbb4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebbb4-106">Parameters</span></span>

<span data-ttu-id="ebbb4-107">*histogramme* </span><span class="sxs-lookup"><span data-stu-id="ebbb4-107">*histogram* </span></span>  
<span data-ttu-id="ebbb4-108">Adresse des données de l’histogramme pour l’histogramme chargé.</span><span class="sxs-lookup"><span data-stu-id="ebbb4-108">The address of histogram data for the loaded histogram.</span></span>

## <a name="return-value"></a><span data-ttu-id="ebbb4-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ebbb4-109">Return value</span></span>

<span data-ttu-id="ebbb4-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ebbb4-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ebbb4-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ebbb4-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebbb4-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebbb4-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ebbb4-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="ebbb4-113">Header</span></span></p></td><td><span data-ttu-id="ebbb4-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ebbb4-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="ebbb4-115"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebbb4-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="ebbb4-116">**IPixEngine5Callbacks**</span><span class="sxs-lookup"><span data-stu-id="ebbb4-116">**IPixEngine5Callbacks**</span></span>](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
