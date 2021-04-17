---
description: Rappel qui avertit l’hôte des étapes de pipeline utilisées par l’appel de dessin de la demande dans.
MS-HAID: vspixengine.IPipeLineStagesCallback\_GetSupportedStages\_DWORD\_PipeLineStage\_arr\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesCallback :: GetSupportedStages, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F7046A41-5C9C-42FE-B1E2-879A47CE08E3
api_name:
- IPipeLineStagesCallback.GetSupportedStages
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c55c7f8bfa6b5b69ea2a46dd6023021a6b4ab6c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521135"
---
# <a name="span-idvspixengineipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uintspanipipelinestagescallbackgetsupportedstages-method"></a><span data-ttu-id="f5017-103"><span id="vspixengine.ipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uint"></span>IPipeLineStagesCallback :: GetSupportedStages, méthode</span><span class="sxs-lookup"><span data-stu-id="f5017-103"><span id="vspixengine.ipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uint"></span>IPipeLineStagesCallback::GetSupportedStages method</span></span>

<span data-ttu-id="f5017-104">Rappel qui avertit l’hôte des étapes de pipeline utilisées par l’appel de dessin de la demande dans.</span><span class="sxs-lookup"><span data-stu-id="f5017-104">A callback that notifies the host of which pipeline stages are used by the draw call of the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5017-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5017-105">Syntax</span></span>


```C++
HRESULT GetSupportedStages(
   DWORD            numColumns,
   PipeLineStage [] count0_pStages,
   UINT             swapChainWidth,
   UINT             swapChainHeight
);
```

## <a name="parameters"></a><span data-ttu-id="f5017-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5017-106">Parameters</span></span>

<span data-ttu-id="f5017-107">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="f5017-107">*numColumns* </span></span>  
<span data-ttu-id="f5017-108">Nombre d’étapes retournées.</span><span class="sxs-lookup"><span data-stu-id="f5017-108">The number of stages returned.</span></span>

<span data-ttu-id="f5017-109">*count0 \_ pStages* </span><span class="sxs-lookup"><span data-stu-id="f5017-109">*count0\_pStages* </span></span>  
<span data-ttu-id="f5017-110">Étapes du pipeline.</span><span class="sxs-lookup"><span data-stu-id="f5017-110">The pipeline stages.</span></span>

<span data-ttu-id="f5017-111">*swapChainWidth* </span><span class="sxs-lookup"><span data-stu-id="f5017-111">*swapChainWidth* </span></span>  
<span data-ttu-id="f5017-112">Largeur de la chaîne de permutation dans avec l’appel de dessin.</span><span class="sxs-lookup"><span data-stu-id="f5017-112">The width of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="f5017-113">Utilisé lors de la demande d’images d’aperçu de pipeline.</span><span class="sxs-lookup"><span data-stu-id="f5017-113">This is used when requesting pipeline preview images.</span></span>

<span data-ttu-id="f5017-114">*swapChainHeight* </span><span class="sxs-lookup"><span data-stu-id="f5017-114">*swapChainHeight* </span></span>  
<span data-ttu-id="f5017-115">Hauteur de la chaîne de permutation dans avec l’appel de dessin.</span><span class="sxs-lookup"><span data-stu-id="f5017-115">The height of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="f5017-116">Utilisé lors de la demande d’images d’aperçu de pipeline.</span><span class="sxs-lookup"><span data-stu-id="f5017-116">This is used when requesting pipeline preview images.</span></span>

## <a name="return-value"></a><span data-ttu-id="f5017-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f5017-117">Return value</span></span>

<span data-ttu-id="f5017-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f5017-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f5017-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f5017-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5017-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5017-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f5017-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5017-121">Header</span></span></p></td><td><span data-ttu-id="f5017-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f5017-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="f5017-123"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5017-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="f5017-124">**IPipeLineStagesCallback**</span><span class="sxs-lookup"><span data-stu-id="f5017-124">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
