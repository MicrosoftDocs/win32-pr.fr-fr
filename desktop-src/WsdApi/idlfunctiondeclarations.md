---
description: Génère des déclarations IDL pour les fonctions de proxy pour les opérations de type de port.
ms.assetid: e56fdd68-b72d-4167-9e4c-b5bbf103880b
title: élément idlFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1afa43676898231f739804185b8bf5d6e2b4faf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106537001"
---
# <a name="idlfunctiondeclarations-element"></a><span data-ttu-id="2a2e1-103">élément idlFunctionDeclarations</span><span class="sxs-lookup"><span data-stu-id="2a2e1-103">idlFunctionDeclarations element</span></span>

<span data-ttu-id="2a2e1-104">Génère des déclarations IDL pour les fonctions de proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="2a2e1-104">Generates IDL declarations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="2a2e1-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="2a2e1-105">Usage</span></span>

``` syntax
<idlFunctionDeclarations>
  child elements
</idlFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="2a2e1-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="2a2e1-106">Attributes</span></span>

<span data-ttu-id="2a2e1-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="2a2e1-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2a2e1-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2a2e1-108">Child elements</span></span>



| <span data-ttu-id="2a2e1-109">Élément</span><span class="sxs-lookup"><span data-stu-id="2a2e1-109">Element</span></span>                                   | <span data-ttu-id="2a2e1-110">Description</span><span class="sxs-lookup"><span data-stu-id="2a2e1-110">Description</span></span>                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2a2e1-111">**async**</span><span class="sxs-lookup"><span data-stu-id="2a2e1-111">**async**</span></span>](async.md)<br/>         | <span data-ttu-id="2a2e1-112">Spécifie si les opérations asynchrones sont incluses dans les fonctions proxy générées.</span><span class="sxs-lookup"><span data-stu-id="2a2e1-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="2a2e1-113">**eventArg**</span><span class="sxs-lookup"><span data-stu-id="2a2e1-113">**eventArg**</span></span>](eventarg.md)<br/>   | <span data-ttu-id="2a2e1-114">Spécifie si les arguments d’événement associés sont inclus dans les fonctions générées.</span><span class="sxs-lookup"><span data-stu-id="2a2e1-114">Specifies whether related event arguments are included in the generated functions.</span></span><br/> <br/>               |
| [<span data-ttu-id="2a2e1-115">**événements**</span><span class="sxs-lookup"><span data-stu-id="2a2e1-115">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="2a2e1-116">Spécifie si les événements connexes sont inclus dans les fonctions générées.</span><span class="sxs-lookup"><span data-stu-id="2a2e1-116">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="2a2e1-117">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="2a2e1-117">**faultInfo**</span></span>](faultinfo.md)<br/> | <span data-ttu-id="2a2e1-118">Spécifie si les paramètres utilisés pour passer les informations d’erreur sont inclus dans les fonctions générées.</span><span class="sxs-lookup"><span data-stu-id="2a2e1-118">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="2a2e1-119">**opération**</span><span class="sxs-lookup"><span data-stu-id="2a2e1-119">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="2a2e1-120">Spécifie une opération pour laquelle du code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="2a2e1-120">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="2a2e1-121">**portType**</span><span class="sxs-lookup"><span data-stu-id="2a2e1-121">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="2a2e1-122">Spécifie le type de port pour lequel le code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="2a2e1-122">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |



### <a name="child-element-sequence"></a><span data-ttu-id="2a2e1-123">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2a2e1-123">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  eventArg?, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="2a2e1-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2a2e1-124">Parent elements</span></span>



| <span data-ttu-id="2a2e1-125">Élément</span><span class="sxs-lookup"><span data-stu-id="2a2e1-125">Element</span></span>                         | <span data-ttu-id="2a2e1-126">Description</span><span class="sxs-lookup"><span data-stu-id="2a2e1-126">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="2a2e1-127">**fichier**</span><span class="sxs-lookup"><span data-stu-id="2a2e1-127">**file**</span></span>](file.md)<br/> | <span data-ttu-id="2a2e1-128">Génère un fichier à partir du générateur de code.</span><span class="sxs-lookup"><span data-stu-id="2a2e1-128">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="2a2e1-129">Notes</span><span class="sxs-lookup"><span data-stu-id="2a2e1-129">Remarks</span></span>

<span data-ttu-id="2a2e1-130">Cet élément génère des déclarations de fonctions membres correspondant aux opérations appelées par le contrat.</span><span class="sxs-lookup"><span data-stu-id="2a2e1-130">This element generates declarations of member functions corresponding to operations called out by the contract.</span></span> <span data-ttu-id="2a2e1-131">Ces déclarations sont dans un format approprié à la consommation par le compilateur MIDL et sont généralement utilisées dans les fichiers. idl.</span><span class="sxs-lookup"><span data-stu-id="2a2e1-131">These declarations are in a form appropriate for consumption by the MIDL compiler and are generally used in .idl files.</span></span>

<span data-ttu-id="2a2e1-132">Exemple :</span><span class="sxs-lookup"><span data-stu-id="2a2e1-132">Example:</span></span>

``` syntax
<idlFunctionDeclarations events = "true"/>
```

## <a name="element-information"></a><span data-ttu-id="2a2e1-133">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="2a2e1-133">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="2a2e1-134">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a2e1-134">Minimum supported system</span></span><br/> | <span data-ttu-id="2a2e1-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2a2e1-135">Windows Vista</span></span> |
| <span data-ttu-id="2a2e1-136">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="2a2e1-136">Can be empty</span></span>                        | <span data-ttu-id="2a2e1-137">Oui</span><span class="sxs-lookup"><span data-stu-id="2a2e1-137">Yes</span></span>           |



 

 




