---
description: Fonction de rappel utilisée pour informer l’hôte que l’analyse hors connexion est terminée.
MS-HAID: vspixengine.IOfflineAnalysisCallback\_OfflineAnalysisComplete\_DWORD\_HRESULT\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IOfflineAnalysisCallback :: OfflineAnalysisComplete, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36E10709-51DC-4657-B184-F1F807ABBBB4
api_name:
- IOfflineAnalysisCallback.OfflineAnalysisComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a1ece7106bee1c49f97238bf06348b049d3f7167
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522735"
---
# <a name="span-idvspixengineiofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstrspaniofflineanalysiscallbackofflineanalysiscomplete-method"></a><span data-ttu-id="fbac6-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstr"></span>IOfflineAnalysisCallback :: OfflineAnalysisComplete, méthode</span><span class="sxs-lookup"><span data-stu-id="fbac6-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstr"></span>IOfflineAnalysisCallback::OfflineAnalysisComplete method</span></span>

<span data-ttu-id="fbac6-104">Fonction de rappel utilisée pour informer l’hôte que l’analyse hors connexion est terminée.</span><span class="sxs-lookup"><span data-stu-id="fbac6-104">A callback function used to notify the host that offline analysis has completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbac6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fbac6-105">Syntax</span></span>


```C++
HRESULT OfflineAnalysisComplete(
   DWORD   cookie,
   HRESULT result,
   BSTR    outputFullFileName
);
```

## <a name="parameters"></a><span data-ttu-id="fbac6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fbac6-106">Parameters</span></span>

<span data-ttu-id="fbac6-107">*cookie* </span><span class="sxs-lookup"><span data-stu-id="fbac6-107">*cookie* </span></span>  
<span data-ttu-id="fbac6-108">Cookie qui identifie de façon unique la demande qui a initié l’analyse hors connexion.</span><span class="sxs-lookup"><span data-stu-id="fbac6-108">A cookie that uniquely identifies the request which initiated offline analysis.</span></span>

<span data-ttu-id="fbac6-109">*venir* </span><span class="sxs-lookup"><span data-stu-id="fbac6-109">*result* </span></span>  
<span data-ttu-id="fbac6-110">Indique si l’analyse hors connexion a réussi ou échoué.</span><span class="sxs-lookup"><span data-stu-id="fbac6-110">Indicates whether offline analysis succeeded or failed.</span></span> <span data-ttu-id="fbac6-111">Si elle réussit, les résultats ont été écrits dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="fbac6-111">If it succeeded, results were written to a file.</span></span>

<span data-ttu-id="fbac6-112">*outputFullFileName* </span><span class="sxs-lookup"><span data-stu-id="fbac6-112">*outputFullFileName* </span></span>  
<span data-ttu-id="fbac6-113">Chaîne COM contianing le nom du fichier dans lequel les résultats de l’analyse hors connexion ont été écrits.</span><span class="sxs-lookup"><span data-stu-id="fbac6-113">A COM string contianing the name of the file where offline analysis results were written.</span></span>

## <a name="return-value"></a><span data-ttu-id="fbac6-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fbac6-114">Return value</span></span>

<span data-ttu-id="fbac6-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fbac6-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fbac6-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fbac6-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbac6-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fbac6-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fbac6-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="fbac6-118">Header</span></span></p></td><td><span data-ttu-id="fbac6-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="fbac6-119">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="fbac6-120"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbac6-120"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="fbac6-121">**IOfflineAnalysisCallback**</span><span class="sxs-lookup"><span data-stu-id="fbac6-121">**IOfflineAnalysisCallback**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscallback)

 

 
