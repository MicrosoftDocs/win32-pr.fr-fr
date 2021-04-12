---
title: Méthode IConfigAsfWriter2 ResetMultiPassState
description: La méthode ResetMultiPassState réinitialise le filtre quand un test d’encodage de prétraitement est annulé avant d’être terminé.
ms.assetid: b6687af7-f3cd-4e92-9c76-dddff9063fa0
keywords:
- Méthode ResetMultiPassState format Windows Media
- Méthode ResetMultiPassState format Windows Media, interface IConfigAsfWriter2
- Interface IConfigAsfWriter2 Windows Media format, méthode ResetMultiPassState
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.ResetMultiPassState
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed61e4f0517822a602f2bb88c944bba82fa1f943
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382444"
---
# <a name="iconfigasfwriter2resetmultipassstate-method"></a><span data-ttu-id="2b47c-106">IConfigAsfWriter2 :: ResetMultiPassState, méthode</span><span class="sxs-lookup"><span data-stu-id="2b47c-106">IConfigAsfWriter2::ResetMultiPassState method</span></span>

<span data-ttu-id="2b47c-107">La méthode **ResetMultiPassState** réinitialise le filtre quand un test d’encodage de prétraitement est annulé avant d’être terminé.</span><span class="sxs-lookup"><span data-stu-id="2b47c-107">The **ResetMultiPassState** method resets the filter when a preprocessing encoding pass is canceled before it is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b47c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b47c-108">Syntax</span></span>


```C++
HRESULT ResetMultiPassState();
```



## <a name="parameters"></a><span data-ttu-id="2b47c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2b47c-109">Parameters</span></span>

<span data-ttu-id="2b47c-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="2b47c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2b47c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2b47c-111">Return value</span></span>

<span data-ttu-id="2b47c-112">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2b47c-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2b47c-113">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2b47c-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2b47c-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2b47c-114">Return code</span></span>                                                                                         | <span data-ttu-id="2b47c-115">Description</span><span class="sxs-lookup"><span data-stu-id="2b47c-115">Description</span></span>                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="2b47c-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2b47c-116"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="2b47c-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="2b47c-117">The method succeeded.</span></span><br/>                  |
| <dl> <span data-ttu-id="2b47c-118"><dt>**VFW \_ E \_ non \_ arrêté**</dt></span><span class="sxs-lookup"><span data-stu-id="2b47c-118"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="2b47c-119">Le filtre n’était pas dans un état arrêté.</span><span class="sxs-lookup"><span data-stu-id="2b47c-119">The filter was not in a stopped state.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2b47c-120">Notes</span><span class="sxs-lookup"><span data-stu-id="2b47c-120">Remarks</span></span>

<span data-ttu-id="2b47c-121">Cette méthode doit être appelée pour réinitialiser l’état interne du filtre chaque fois qu’un test d’encodage de prétraitement est annulé avant que le filtre ait reçu un événement de **\_ \_ fin de prétraitement EC** .</span><span class="sxs-lookup"><span data-stu-id="2b47c-121">This method must be called to reset the internal state of the filter whenever a preprocessing encoding pass is canceled before the filter has received an **EC\_PREPROCESS\_COMPLETE** event.</span></span> <span data-ttu-id="2b47c-122">Il n’est pas nécessaire d’appeler cette méthode si la réussite de l’encodage de prétraitement s’est terminée sans erreurs.</span><span class="sxs-lookup"><span data-stu-id="2b47c-122">It is not necessary to call this method if the preprocessing encoding pass completes without errors.</span></span>

## <a name="see-also"></a><span data-ttu-id="2b47c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b47c-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="2b47c-124">[**Interface IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2b47c-124">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> </dl>

 

