---
description: Génère des déclarations d’implémentation pour les fonctions de proxy pour les opérations de type de port.
ms.assetid: 6ba7dbb6-6598-4569-97e1-d703e4b896c7
title: élément functionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b82aca30f94fc8fcec80701a74b56e83ab674c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203006"
---
# <a name="functiondeclarations-element"></a><span data-ttu-id="e4d0d-103">élément functionDeclarations</span><span class="sxs-lookup"><span data-stu-id="e4d0d-103">functionDeclarations element</span></span>

<span data-ttu-id="e4d0d-104">Génère des déclarations d’implémentation pour les fonctions de proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="e4d0d-104">Generates implementation declarations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="e4d0d-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="e4d0d-105">Usage</span></span>

``` syntax
<functionDeclarations>
  child elements
</functionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="e4d0d-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="e4d0d-106">Attributes</span></span>

<span data-ttu-id="e4d0d-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="e4d0d-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e4d0d-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e4d0d-108">Child elements</span></span>



| <span data-ttu-id="e4d0d-109">Élément</span><span class="sxs-lookup"><span data-stu-id="e4d0d-109">Element</span></span>                                   | <span data-ttu-id="e4d0d-110">Description</span><span class="sxs-lookup"><span data-stu-id="e4d0d-110">Description</span></span>                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4d0d-111">**async**</span><span class="sxs-lookup"><span data-stu-id="e4d0d-111">**async**</span></span>](async.md)<br/>         | <span data-ttu-id="e4d0d-112">Spécifie si les opérations asynchrones sont incluses dans les fonctions proxy générées.</span><span class="sxs-lookup"><span data-stu-id="e4d0d-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="e4d0d-113">**événements**</span><span class="sxs-lookup"><span data-stu-id="e4d0d-113">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="e4d0d-114">Spécifie si les événements connexes sont inclus dans les fonctions générées.</span><span class="sxs-lookup"><span data-stu-id="e4d0d-114">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="e4d0d-115">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="e4d0d-115">**faultInfo**</span></span>](faultinfo.md)<br/> | <span data-ttu-id="e4d0d-116">Spécifie si les paramètres utilisés pour passer les informations d’erreur sont inclus dans les fonctions générées.</span><span class="sxs-lookup"><span data-stu-id="e4d0d-116">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="e4d0d-117">**opération**</span><span class="sxs-lookup"><span data-stu-id="e4d0d-117">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="e4d0d-118">Spécifie une opération pour laquelle du code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="e4d0d-118">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="e4d0d-119">**portType**</span><span class="sxs-lookup"><span data-stu-id="e4d0d-119">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="e4d0d-120">Spécifie le type de port pour lequel le code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="e4d0d-120">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |



### <a name="child-element-sequence"></a><span data-ttu-id="e4d0d-121">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e4d0d-121">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="e4d0d-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e4d0d-122">Parent elements</span></span>



| <span data-ttu-id="e4d0d-123">Élément</span><span class="sxs-lookup"><span data-stu-id="e4d0d-123">Element</span></span>                         | <span data-ttu-id="e4d0d-124">Description</span><span class="sxs-lookup"><span data-stu-id="e4d0d-124">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="e4d0d-125">**fichier**</span><span class="sxs-lookup"><span data-stu-id="e4d0d-125">**file**</span></span>](file.md)<br/> | <span data-ttu-id="e4d0d-126">Génère un fichier à partir du générateur de code.</span><span class="sxs-lookup"><span data-stu-id="e4d0d-126">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="e4d0d-127">Notes</span><span class="sxs-lookup"><span data-stu-id="e4d0d-127">Remarks</span></span>

<span data-ttu-id="e4d0d-128">Cet élément génère des déclarations de fonctions membres correspondant aux opérations appelées par le contrat.</span><span class="sxs-lookup"><span data-stu-id="e4d0d-128">This element generates declarations of member functions corresponding to operations called out by the contract.</span></span> <span data-ttu-id="e4d0d-129">Ces déclarations sont dans un format approprié à la consommation par un compilateur C++ et sont généralement utilisées dans les fichiers. cpp.</span><span class="sxs-lookup"><span data-stu-id="e4d0d-129">These declarations are in a form appropriate for consumption by a C++ compiler and are generally used in .cpp files.</span></span>

<span data-ttu-id="e4d0d-130">Exemple :</span><span class="sxs-lookup"><span data-stu-id="e4d0d-130">Example:</span></span>

``` syntax
<functionDeclarations events = "true"/>
```

## <a name="element-information"></a><span data-ttu-id="e4d0d-131">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="e4d0d-131">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="e4d0d-132">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4d0d-132">Minimum supported system</span></span><br/> | <span data-ttu-id="e4d0d-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d0d-133">Windows Vista</span></span> |
| <span data-ttu-id="e4d0d-134">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="e4d0d-134">Can be empty</span></span>                        | <span data-ttu-id="e4d0d-135">Oui</span><span class="sxs-lookup"><span data-stu-id="e4d0d-135">Yes</span></span>           |



 

 




