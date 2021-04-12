---
description: Fonction de rappel utilisée pour informer l’hôte de la progression de l’analyse hors connexion.
MS-HAID: vspixengine.IOfflineAnalysisCallback\_OfflineAnalysisProgress\_DWORD\_DOUBLE
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IOfflineAnalysisCallback :: OfflineAnalysisProgress, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 17847FD7-A10A-4E52-90AD-ADE446D87E73
api_name:
- IOfflineAnalysisCallback.OfflineAnalysisProgress
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4184be5d8d40b0ef46fe5e0029e9e4b1f38cf120
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392860"
---
# <a name="span-idvspixengineiofflineanalysiscallback_offlineanalysisprogress_dword_doublespaniofflineanalysiscallbackofflineanalysisprogress-method"></a><span data-ttu-id="dbb59-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysisprogress_dword_double"></span>IOfflineAnalysisCallback :: OfflineAnalysisProgress, méthode</span><span class="sxs-lookup"><span data-stu-id="dbb59-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysisprogress_dword_double"></span>IOfflineAnalysisCallback::OfflineAnalysisProgress method</span></span>

<span data-ttu-id="dbb59-104">Fonction de rappel utilisée pour informer l’hôte de la progression de l’analyse hors connexion.</span><span class="sxs-lookup"><span data-stu-id="dbb59-104">A callback function used to notify the host of offline analysis progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbb59-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dbb59-105">Syntax</span></span>


```C++
HRESULT OfflineAnalysisComplete(
   DWORD   cookie,
   HRESULT result,
   BSTR    outputFullFileName
);
```

## <a name="parameters"></a><span data-ttu-id="dbb59-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dbb59-106">Parameters</span></span>

<span data-ttu-id="dbb59-107">*cookie* </span><span class="sxs-lookup"><span data-stu-id="dbb59-107">*cookie* </span></span>  
<span data-ttu-id="dbb59-108">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="dbb59-108">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="dbb59-109">*avancement* </span><span class="sxs-lookup"><span data-stu-id="dbb59-109">*progress* </span></span>  
<span data-ttu-id="dbb59-110">Pourcentage de progression.</span><span class="sxs-lookup"><span data-stu-id="dbb59-110">The progress percentage.</span></span>

## <a name="return-value"></a><span data-ttu-id="dbb59-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dbb59-111">Return value</span></span>

<span data-ttu-id="dbb59-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dbb59-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dbb59-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dbb59-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbb59-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dbb59-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="dbb59-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="dbb59-115">Header</span></span></p></td><td><span data-ttu-id="dbb59-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="dbb59-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="dbb59-117"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbb59-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="dbb59-118">**IOfflineAnalysisCallback**</span><span class="sxs-lookup"><span data-stu-id="dbb59-118">**IOfflineAnalysisCallback**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscallback)

 

 
