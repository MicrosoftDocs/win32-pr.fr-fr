---
description: Rappel qui avertit l’hôte des étapes de pipeline qui ne sont pas en mesure de retourner des données de maillage pour l’événement spécifié dans la demande associée.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataNotAvailableCallback\_UINT\_PipeLineStageError\_arr\_UINT\_UINT\_EventID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesCallback :: MeshDataNotAvailableCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A51E7C45-C1F0-4576-8638-9C3B185385BA
api_name:
- IPipeLineStagesCallback.MeshDataNotAvailableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 42391c342e2f11b39d1535b5286a92e161d0fd9b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482584"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventidspanipipelinestagescallbackmeshdatanotavailablecallback-method"></a><span data-ttu-id="e6de2-103"><span id="vspixengine.ipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventid"></span>IPipeLineStagesCallback :: MeshDataNotAvailableCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="e6de2-103"><span id="vspixengine.ipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventid"></span>IPipeLineStagesCallback::MeshDataNotAvailableCallback method</span></span>

<span data-ttu-id="e6de2-104">Rappel qui avertit l’hôte des étapes de pipeline qui ne sont pas en mesure de retourner des données de maillage pour l’événement spécifié dans la demande associée.</span><span class="sxs-lookup"><span data-stu-id="e6de2-104">A callback that notifies the host of which pipeline stages are not able to return mesh data for the event specified in the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6de2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6de2-105">Syntax</span></span>


```C++
HRESULT MeshDataNotAvailableCallback(
   UINT                  numberStages,
   PipeLineStageError [] count0_errors,
   UINT                  width,
   UINT                  height,
   EventID               eid
);
```

## <a name="parameters"></a><span data-ttu-id="e6de2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6de2-106">Parameters</span></span>

<span data-ttu-id="e6de2-107">*numberStages* </span><span class="sxs-lookup"><span data-stu-id="e6de2-107">*numberStages* </span></span>  
<span data-ttu-id="e6de2-108">Nombre d’erreurs d’étape retournées.</span><span class="sxs-lookup"><span data-stu-id="e6de2-108">The number of stage errors returned.</span></span>

<span data-ttu-id="e6de2-109">*\_Erreurs count0* </span><span class="sxs-lookup"><span data-stu-id="e6de2-109">*count0\_errors* </span></span>  
<span data-ttu-id="e6de2-110">Erreurs d’étape de pipeline.</span><span class="sxs-lookup"><span data-stu-id="e6de2-110">The pipeline stage errors.</span></span>

<span data-ttu-id="e6de2-111">*Largeur* </span><span class="sxs-lookup"><span data-stu-id="e6de2-111">*width* </span></span>  
<span data-ttu-id="e6de2-112">Largeur de la chaîne de permutation dans avec l’appel de dessin.</span><span class="sxs-lookup"><span data-stu-id="e6de2-112">The width of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="e6de2-113">Utilisé lors de la demande d’images d’aperçu de pipeline.</span><span class="sxs-lookup"><span data-stu-id="e6de2-113">This is used when requesting pipeline preview images.</span></span>

<span data-ttu-id="e6de2-114">*celle* </span><span class="sxs-lookup"><span data-stu-id="e6de2-114">*height* </span></span>  
<span data-ttu-id="e6de2-115">Hauteur de la chaîne de permutation dans avec l’appel de dessin.</span><span class="sxs-lookup"><span data-stu-id="e6de2-115">The height of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="e6de2-116">Utilisé lors de la demande d’images d’aperçu de pipeline.</span><span class="sxs-lookup"><span data-stu-id="e6de2-116">This is used when requesting pipeline preview images.</span></span>

<span data-ttu-id="e6de2-117">*Numéro* </span><span class="sxs-lookup"><span data-stu-id="e6de2-117">*eid* </span></span>  
<span data-ttu-id="e6de2-118">Événement représenté dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="e6de2-118">The event represented in the results.</span></span>

## <a name="return-value"></a><span data-ttu-id="e6de2-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6de2-119">Return value</span></span>

<span data-ttu-id="e6de2-120">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e6de2-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e6de2-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e6de2-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6de2-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6de2-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e6de2-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6de2-123">Header</span></span></p></td><td><span data-ttu-id="e6de2-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e6de2-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="e6de2-125"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6de2-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="e6de2-126">**IPipeLineStagesCallback**</span><span class="sxs-lookup"><span data-stu-id="e6de2-126">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
