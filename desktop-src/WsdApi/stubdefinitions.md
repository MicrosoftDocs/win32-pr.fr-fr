---
description: Génère des implémentations pour les fonctions stub pour les opérations de type de port.
ms.assetid: 69899302-db54-493b-90de-596750be566f
title: élément stubDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6676cfc6cf55aa9c9961bd614506500d847def0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519967"
---
# <a name="stubdefinitions-element"></a><span data-ttu-id="c7ab1-103">élément stubDefinitions</span><span class="sxs-lookup"><span data-stu-id="c7ab1-103">stubDefinitions element</span></span>

<span data-ttu-id="c7ab1-104">Génère des implémentations pour les fonctions stub pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="c7ab1-104">Generates implementations for stub functions for port-type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="c7ab1-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="c7ab1-105">Usage</span></span>

``` syntax
<stubDefinitions>
  child elements
</stubDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="c7ab1-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="c7ab1-106">Attributes</span></span>

<span data-ttu-id="c7ab1-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="c7ab1-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c7ab1-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c7ab1-108">Child elements</span></span>



| <span data-ttu-id="c7ab1-109">Élément</span><span class="sxs-lookup"><span data-stu-id="c7ab1-109">Element</span></span>                                                         | <span data-ttu-id="c7ab1-110">Description</span><span class="sxs-lookup"><span data-stu-id="c7ab1-110">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7ab1-111">**annulateur**</span><span class="sxs-lookup"><span data-stu-id="c7ab1-111">**deallocator**</span></span>](deallocator.md)<br/>                   | <span data-ttu-id="c7ab1-112">Spécifie le type de annulateur à utiliser par une fonction stub.</span><span class="sxs-lookup"><span data-stu-id="c7ab1-112">Specifies the type of deallocator to be used by a stub function.</span></span><br/> <br/>                                 |
| [<span data-ttu-id="c7ab1-113">**eventArg**</span><span class="sxs-lookup"><span data-stu-id="c7ab1-113">**eventArg**</span></span>](eventarg.md)<br/>                         | <span data-ttu-id="c7ab1-114">Spécifie si les arguments d’événement associés sont inclus dans les fonctions générées.</span><span class="sxs-lookup"><span data-stu-id="c7ab1-114">Specifies whether related event arguments are included in the generated functions.</span></span><br/> <br/>               |
| [<span data-ttu-id="c7ab1-115">**événements**</span><span class="sxs-lookup"><span data-stu-id="c7ab1-115">**events**</span></span>](events.md)<br/>                             | <span data-ttu-id="c7ab1-116">Spécifie si les événements connexes sont inclus dans les fonctions générées.</span><span class="sxs-lookup"><span data-stu-id="c7ab1-116">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="c7ab1-117">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="c7ab1-117">**faultInfo**</span></span>](faultinfo.md)<br/>                       | <span data-ttu-id="c7ab1-118">Spécifie si les paramètres utilisés pour passer les informations d’erreur sont inclus dans les fonctions générées.</span><span class="sxs-lookup"><span data-stu-id="c7ab1-118">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="c7ab1-119">**opération**</span><span class="sxs-lookup"><span data-stu-id="c7ab1-119">**operation**</span></span>](operation.md)<br/>                       | <span data-ttu-id="c7ab1-120">Spécifie une opération pour laquelle du code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="c7ab1-120">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="c7ab1-121">**operationDeallocator**</span><span class="sxs-lookup"><span data-stu-id="c7ab1-121">**operationDeallocator**</span></span>](operationdeallocator.md)<br/> | <span data-ttu-id="c7ab1-122">Spécifie le type de annulateur à utiliser par la fonction stub d’une opération.</span><span class="sxs-lookup"><span data-stu-id="c7ab1-122">Specifies the type of deallocator to be used by an operation's stub function.</span></span><br/> <br/>                    |
| [<span data-ttu-id="c7ab1-123">**portType**</span><span class="sxs-lookup"><span data-stu-id="c7ab1-123">**portType**</span></span>](porttype.md)<br/>                         | <span data-ttu-id="c7ab1-124">Spécifie le type de port pour lequel le code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="c7ab1-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |
| [<span data-ttu-id="c7ab1-125">**serverClass**</span><span class="sxs-lookup"><span data-stu-id="c7ab1-125">**serverClass**</span></span>](serverclass.md)<br/>                   | <span data-ttu-id="c7ab1-126">Spécifie le nom de la classe de serveur côté hôte.</span><span class="sxs-lookup"><span data-stu-id="c7ab1-126">Specifies the name of the host-side server class.</span></span><br/> <br/>                                                |



### <a name="child-element-sequence"></a><span data-ttu-id="c7ab1-127">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c7ab1-127">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  serverClass, 
  eventArg?, 
  events?, 
  operationDeallocator*, 
  deallocator?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="c7ab1-128">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c7ab1-128">Parent elements</span></span>



| <span data-ttu-id="c7ab1-129">Élément</span><span class="sxs-lookup"><span data-stu-id="c7ab1-129">Element</span></span>                         | <span data-ttu-id="c7ab1-130">Description</span><span class="sxs-lookup"><span data-stu-id="c7ab1-130">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="c7ab1-131">**fichier**</span><span class="sxs-lookup"><span data-stu-id="c7ab1-131">**file**</span></span>](file.md)<br/> | <span data-ttu-id="c7ab1-132">Génère un fichier à partir du générateur de code.</span><span class="sxs-lookup"><span data-stu-id="c7ab1-132">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="c7ab1-133">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="c7ab1-133">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="c7ab1-134">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7ab1-134">Minimum supported system</span></span><br/> | <span data-ttu-id="c7ab1-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7ab1-135">Windows Vista</span></span> |
| <span data-ttu-id="c7ab1-136">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="c7ab1-136">Can be empty</span></span>                        | <span data-ttu-id="c7ab1-137">Non</span><span class="sxs-lookup"><span data-stu-id="c7ab1-137">No</span></span>            |



 

 




