---
description: La méthode SetDelayTime définit le délai d’attente de l’info-bulle associée à l’objet MSWebDVD.
ms.assetid: bb1086e1-57e2-495a-9b7b-2d349a516e72
title: SetDelayTime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7653777be7e6603494d9ba04a671ed46d3d949
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480585"
---
# <a name="setdelaytime"></a><span data-ttu-id="78296-103">SetDelayTime</span><span class="sxs-lookup"><span data-stu-id="78296-103">SetDelayTime</span></span>

> [!Note]  
> <span data-ttu-id="78296-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="78296-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="78296-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="78296-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="78296-106">La `SetDelayTime` méthode définit le délai d’attente pour l’info-bulle associée à l’objet **mswebdvd** .</span><span class="sxs-lookup"><span data-stu-id="78296-106">The `SetDelayTime` method sets the delay time for the ToolTip associated with the **MSWebDVD** object.</span></span>

``` syntax
MSWebDVD.SetDelayTime(iDelayType, iNewVal)
```

## <a name="parameters"></a><span data-ttu-id="78296-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78296-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78296-108"><span id="iDelayType"></span><span id="idelaytype"></span><span id="IDELAYTYPE"></span>*iDelayType*</span><span class="sxs-lookup"><span data-stu-id="78296-108"><span id="iDelayType"></span><span id="idelaytype"></span><span id="IDELAYTYPE"></span>*iDelayType*</span></span>
</dt> <dd>

<span data-ttu-id="78296-109">Spécifie le type de délai sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="78296-109">Specifies the type of delay as an Integer.</span></span>



| <span data-ttu-id="78296-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="78296-110">Value</span></span> | <span data-ttu-id="78296-111">Description</span><span class="sxs-lookup"><span data-stu-id="78296-111">Description</span></span>                                                                                                                                                                                                                                      |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78296-112">-1</span><span class="sxs-lookup"><span data-stu-id="78296-112">-1</span></span>    | <span data-ttu-id="78296-113">Pour rétablir la valeur par défaut du délai d’attente de autopop, affectez la valeur-1 à *iNewVal* .</span><span class="sxs-lookup"><span data-stu-id="78296-113">To reset the autopop delay time to its default value, set *iNewVal* to -1.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="78296-114">0</span><span class="sxs-lookup"><span data-stu-id="78296-114">0</span></span>     | <span data-ttu-id="78296-115">Définissez la durée pendant laquelle une fenêtre d’info-bulle reste visible si le pointeur est immobile dans le rectangle englobant d’un outil.</span><span class="sxs-lookup"><span data-stu-id="78296-115">Set the length of time a ToolTip window remains visible if the pointer is stationary within a tool's bounding rectangle.</span></span>                                                                                                                         |
| <span data-ttu-id="78296-116">1</span><span class="sxs-lookup"><span data-stu-id="78296-116">1</span></span>     | <span data-ttu-id="78296-117">Définissez la durée pendant laquelle un pointeur doit rester immobile dans le rectangle englobant d’un outil avant que la fenêtre d’info-bulle ne s’affiche.</span><span class="sxs-lookup"><span data-stu-id="78296-117">Set the length of time a pointer must remain stationary within a tool's bounding rectangle before the ToolTip window appears.</span></span>                                                                                                                    |
| <span data-ttu-id="78296-118">2</span><span class="sxs-lookup"><span data-stu-id="78296-118">2</span></span>     | <span data-ttu-id="78296-119">Définissez le temps nécessaire pour que les fenêtres d’info-bulle suivantes s’affichent lorsque le pointeur se déplace d’un outil à un autre.</span><span class="sxs-lookup"><span data-stu-id="78296-119">Set the length of time it takes for subsequent ToolTip windows to appear as the pointer moves from one tool to another.</span></span>                                                                                                                          |
| <span data-ttu-id="78296-120">3</span><span class="sxs-lookup"><span data-stu-id="78296-120">3</span></span>     | <span data-ttu-id="78296-121">Définissez tous les délais d’attente sur les proportions par défaut.</span><span class="sxs-lookup"><span data-stu-id="78296-121">Set all delay times to default proportions.</span></span> <span data-ttu-id="78296-122">Le temps de autopop est dix fois l’heure initiale et l’heure de réaffichage est le cinquième de l’heure initiale.</span><span class="sxs-lookup"><span data-stu-id="78296-122">The autopop time is ten times the initial time and the reshow time is one-fifth the initial time.</span></span> <span data-ttu-id="78296-123">Si cet indicateur est défini, utilisez une valeur positive de iNewVal pour spécifier l’heure initiale, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="78296-123">If this flag is set, use a positive value of iNewVal to specify the initial time, in milliseconds.</span></span> |



 

</dd> <dt>

<span data-ttu-id="78296-124"><span id="iNewVal"></span><span id="inewval"></span><span id="INEWVAL"></span>*iNewVal*</span><span class="sxs-lookup"><span data-stu-id="78296-124"><span id="iNewVal"></span><span id="inewval"></span><span id="INEWVAL"></span>*iNewVal*</span></span>
</dt> <dd>

<span data-ttu-id="78296-125">Spécifie le délai, en millisecondes, sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="78296-125">Specifies the delay, in milliseconds, as an Integer.</span></span>



| <span data-ttu-id="78296-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="78296-126">Value</span></span>                    | <span data-ttu-id="78296-127">Description</span><span class="sxs-lookup"><span data-stu-id="78296-127">Description</span></span>                                                   |
|--------------------------|---------------------------------------------------------------|
| <span data-ttu-id="78296-128">-1</span><span class="sxs-lookup"><span data-stu-id="78296-128">-1</span></span>                       | <span data-ttu-id="78296-129">Définit le délai spécifié dans *iDelayType* à sa valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="78296-129">Sets the delay specified in *iDelayType* to its default value</span></span> |
| <span data-ttu-id="78296-130">toute autre valeur négative</span><span class="sxs-lookup"><span data-stu-id="78296-130">any other negative value</span></span> | <span data-ttu-id="78296-131">Définit tous les types de retard à leur valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="78296-131">Sets all delay types to their default value.</span></span>                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78296-132">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="78296-132">Return Value</span></span>

<span data-ttu-id="78296-133">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="78296-133">No return value.</span></span>

 

 



