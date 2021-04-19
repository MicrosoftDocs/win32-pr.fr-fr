---
description: Fonction de rappel utilisée pour informer l’hôte des informations de résumé du journal de graphisme.
MS-HAID: vspixengine.ISummaryCallback\_ResultCallback\_DWORD\_SummaryItem\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ISummaryCallback :: ResultCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 07569D26-45A6-41A5-868D-8038BAB9079B
api_name:
- ISummaryCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c4ea46550628ec9701ab6b0e6bb3af9ab71a2499
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515329"
---
# <a name="span-idvspixengineisummarycallback_resultcallback_dword_summaryitem_arrspanisummarycallbackresultcallback-method"></a><span data-ttu-id="4d5d7-103"><span id="vspixengine.isummarycallback_resultcallback_dword_summaryitem_arr"></span>ISummaryCallback :: ResultCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="4d5d7-103"><span id="vspixengine.isummarycallback_resultcallback_dword_summaryitem_arr"></span>ISummaryCallback::ResultCallback method</span></span>

<span data-ttu-id="4d5d7-104">Fonction de rappel utilisée pour informer l’hôte des informations de résumé du journal de graphisme.</span><span class="sxs-lookup"><span data-stu-id="4d5d7-104">A callback function used to notify the host of graphics log summary information.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d5d7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d5d7-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD          count,
   SummaryItem [] count0_summaryItem
);
```

## <a name="parameters"></a><span data-ttu-id="4d5d7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4d5d7-106">Parameters</span></span>

<span data-ttu-id="4d5d7-107">*saut* </span><span class="sxs-lookup"><span data-stu-id="4d5d7-107">*count* </span></span>  
<span data-ttu-id="4d5d7-108">Nombre d’éléments d’informations de résumé retournés.</span><span class="sxs-lookup"><span data-stu-id="4d5d7-108">The number of summary information items returned.</span></span>

<span data-ttu-id="4d5d7-109">*count0 \_ summaryItem* </span><span class="sxs-lookup"><span data-stu-id="4d5d7-109">*count0\_summaryItem* </span></span>  
<span data-ttu-id="4d5d7-110">Éléments d’informations de résumé (paires clé-valeur).</span><span class="sxs-lookup"><span data-stu-id="4d5d7-110">The summary information items (key-value pairs).</span></span>

## <a name="return-value"></a><span data-ttu-id="4d5d7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4d5d7-111">Return value</span></span>

<span data-ttu-id="4d5d7-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4d5d7-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4d5d7-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4d5d7-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d5d7-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d5d7-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4d5d7-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="4d5d7-115">Header</span></span></p></td><td><span data-ttu-id="4d5d7-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="4d5d7-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="4d5d7-117"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d5d7-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="4d5d7-118">**ISummaryCallback**</span><span class="sxs-lookup"><span data-stu-id="4d5d7-118">**ISummaryCallback**</span></span>](/windows/desktop/direct3dtools/isummarycallback)

 

 
