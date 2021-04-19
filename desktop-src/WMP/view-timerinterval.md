---
title: VIEW. timerInterval
description: L’attribut timerInterval spécifie ou récupère l’intervalle, en millisecondes, auquel la minuterie déclenche des événements dans le gestionnaire d’événements OnTimer.
ms.assetid: 1a69890f-5ea4-493a-8a9e-04fe60a41804
keywords:
- VIEW. timerInterval Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.timerInterval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790c95fbb2cded134222271d04c4c37dae412b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535870"
---
# <a name="viewtimerinterval"></a><span data-ttu-id="c7f4c-104">VIEW. timerInterval</span><span class="sxs-lookup"><span data-stu-id="c7f4c-104">VIEW.timerInterval</span></span>

<span data-ttu-id="c7f4c-105">L’attribut **timerInterval** spécifie ou récupère l’intervalle, en millisecondes, auquel la minuterie déclenche des événements dans le gestionnaire d’événements **OnTimer** .</span><span class="sxs-lookup"><span data-stu-id="c7f4c-105">The **timerInterval** attribute specifies or retrieves the interval, in milliseconds, at which the timer fires events to the **ontimer** event handler.</span></span>

``` syntax
        elementID.timerInterval
```

## <a name="possible-values"></a><span data-ttu-id="c7f4c-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="c7f4c-106">Possible Values</span></span>

<span data-ttu-id="c7f4c-107">Cet attribut est un **nombre** en lecture/écriture (**long**) avec une valeur par défaut de 1000.</span><span class="sxs-lookup"><span data-stu-id="c7f4c-107">This attribute is a read/write **Number** (**long**) with a default value of 1000.</span></span>



| <span data-ttu-id="c7f4c-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7f4c-108">Value</span></span>        | <span data-ttu-id="c7f4c-109">Description</span><span class="sxs-lookup"><span data-stu-id="c7f4c-109">Description</span></span>                    |
|--------------|--------------------------------|
| <span data-ttu-id="c7f4c-110">0</span><span class="sxs-lookup"><span data-stu-id="c7f4c-110">0</span></span>            | <span data-ttu-id="c7f4c-111">L’événement du minuteur ne se déclenche pas.</span><span class="sxs-lookup"><span data-stu-id="c7f4c-111">The timer event does not fire.</span></span> |
| <span data-ttu-id="c7f4c-112">50 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="c7f4c-112">50 and above</span></span> | <span data-ttu-id="c7f4c-113">Intervalle en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="c7f4c-113">The interval in milliseconds.</span></span>  |



 

<span data-ttu-id="c7f4c-114">Toute valeur inférieure à 50 (y compris les nombres négatifs, mais qui n’inclut pas zéro) génère une erreur et la valeur précédente est conservée.</span><span class="sxs-lookup"><span data-stu-id="c7f4c-114">Any value below 50 (including negative numbers, but not including zero) generates an error and the previous value is maintained.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7f4c-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c7f4c-115">Remarks</span></span>

<span data-ttu-id="c7f4c-116">Cela ne se déclenchera pas automatiquement si aucun gestionnaire d’événements **OnTimer** n’est implémenté.</span><span class="sxs-lookup"><span data-stu-id="c7f4c-116">This will not fire automatically if no **ontimer** event handler is implemented.</span></span> <span data-ttu-id="c7f4c-117">Il n’y a donc pas de dégradation des performances, même si la valeur par défaut est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="c7f4c-117">Thus there is no performance degradation even though the default value is nonzero.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7f4c-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7f4c-118">Requirements</span></span>



| <span data-ttu-id="c7f4c-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7f4c-119">Requirement</span></span> | <span data-ttu-id="c7f4c-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7f4c-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c7f4c-121">Version</span><span class="sxs-lookup"><span data-stu-id="c7f4c-121">Version</span></span><br/> | <span data-ttu-id="c7f4c-122">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="c7f4c-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c7f4c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7f4c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7f4c-124">**Élément VIEW**</span><span class="sxs-lookup"><span data-stu-id="c7f4c-124">**VIEW Element**</span></span>](view-element.md)
</dt> <dt>

[<span data-ttu-id="c7f4c-125">**VIEW. OnTimer**</span><span class="sxs-lookup"><span data-stu-id="c7f4c-125">**VIEW.ontimer**</span></span>](view-ontimer.md)
</dt> </dl>

 

 





