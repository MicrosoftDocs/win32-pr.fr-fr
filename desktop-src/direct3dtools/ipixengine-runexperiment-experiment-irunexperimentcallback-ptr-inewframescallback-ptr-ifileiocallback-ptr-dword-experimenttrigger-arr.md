---
description: Exécute une expérience.
MS-HAID: vspixengine.IPixEngine\_RunExperiment\_Experiment\_IRunExperimentCallback\_ptr\_INewFramesCallback\_ptr\_IFileIOCallback\_ptr\_DWORD\_ExperimentTrigger\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine :: RunExperiment, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A2EEC278-C074-44B3-94DC-E2D9DC770576
api_name:
- IPixEngine.RunExperiment
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c656d57dda496b6c1d8c128dc5e832ec40ef13f7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109055"
---
# <a name="span-idvspixengineipixengine_runexperiment_experiment_irunexperimentcallback_ptr_inewframescallback_ptr_ifileiocallback_ptr_dword_experimenttrigger_arrspanipixenginerunexperiment-method"></a><span data-ttu-id="2fd83-103"><span id="vspixengine.ipixengine_runexperiment_experiment_irunexperimentcallback_ptr_inewframescallback_ptr_ifileiocallback_ptr_dword_experimenttrigger_arr"></span>IPixEngine :: RunExperiment, méthode</span><span class="sxs-lookup"><span data-stu-id="2fd83-103"><span id="vspixengine.ipixengine_runexperiment_experiment_irunexperimentcallback_ptr_inewframescallback_ptr_ifileiocallback_ptr_dword_experimenttrigger_arr"></span>IPixEngine::RunExperiment method</span></span>

<span data-ttu-id="2fd83-104">Exécute une expérience.</span><span class="sxs-lookup"><span data-stu-id="2fd83-104">Runs an experiment.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fd83-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2fd83-105">Syntax</span></span>


```C++
HRESULT RunExperiment(
   Experiment               experiment,
   IRunExperimentCallback * pRequestCallback,
   INewFramesCallback*      callbacks,
   IFileIOCallback*         pFileIOCallback,
   DWORD                    triggersCount,
   ExperimentTrigger []     count4_triggersBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="2fd83-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2fd83-106">Parameters</span></span>

<span data-ttu-id="2fd83-107">*expérimenté* </span><span class="sxs-lookup"><span data-stu-id="2fd83-107">*experiment* </span></span>  
<span data-ttu-id="2fd83-108">Décrit l’expérience à exécuter.</span><span class="sxs-lookup"><span data-stu-id="2fd83-108">Describes the experiment to be run.</span></span>

<span data-ttu-id="2fd83-109">*pRequestCallback* </span><span class="sxs-lookup"><span data-stu-id="2fd83-109">*pRequestCallback* </span></span>  
<span data-ttu-id="2fd83-110">Adresse d’une fonction utilisée pour informer l’hôte que le moteur a démarré l’expérimentation.</span><span class="sxs-lookup"><span data-stu-id="2fd83-110">The address of a function used to notify the host that engine has started the experiment.</span></span>

<span data-ttu-id="2fd83-111">*rappels* </span><span class="sxs-lookup"><span data-stu-id="2fd83-111">*callbacks* </span></span>  
<span data-ttu-id="2fd83-112">Adresse d’une fonction utilisée pour informer l’hôte que de nouveaux frames ont été capturés.</span><span class="sxs-lookup"><span data-stu-id="2fd83-112">The address of a function used to notify the host that new frames have been captured.</span></span>

<span data-ttu-id="2fd83-113">*pFileIOCallback* </span><span class="sxs-lookup"><span data-stu-id="2fd83-113">*pFileIOCallback* </span></span>  
<span data-ttu-id="2fd83-114">Adresse d’une fonction utilisée pour notifier l’hôte des erreurs d’e/s de fichier lors de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="2fd83-114">The address of a function used to notify the host of file IO errors during parsing.</span></span>

<span data-ttu-id="2fd83-115">*triggersCount* </span><span class="sxs-lookup"><span data-stu-id="2fd83-115">*triggersCount* </span></span>  
<span data-ttu-id="2fd83-116">Nombre de déclencheurs dans l’expérience.</span><span class="sxs-lookup"><span data-stu-id="2fd83-116">The number of triggers in the experiment.</span></span>

<span data-ttu-id="2fd83-117">*count4 \_ triggersBuffer* </span><span class="sxs-lookup"><span data-stu-id="2fd83-117">*count4\_triggersBuffer* </span></span>  
<span data-ttu-id="2fd83-118">Déclencheurs de capture.</span><span class="sxs-lookup"><span data-stu-id="2fd83-118">Capture triggers.</span></span>

## <a name="return-value"></a><span data-ttu-id="2fd83-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2fd83-119">Return value</span></span>

<span data-ttu-id="2fd83-120">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2fd83-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2fd83-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2fd83-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fd83-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2fd83-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="2fd83-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="2fd83-123">Header</span></span></p></td><td><span data-ttu-id="2fd83-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="2fd83-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="2fd83-125"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fd83-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="2fd83-126">**IPixEngine**</span><span class="sxs-lookup"><span data-stu-id="2fd83-126">**IPixEngine**</span></span>](/windows/desktop/direct3dtools/ipixengine)

 

 
