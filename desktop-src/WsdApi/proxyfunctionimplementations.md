---
description: Génère des implémentations pour les fonctions proxy pour les opérations de type de port.
ms.assetid: 9505ee5f-fdb9-41b8-9537-0c5d29f90168
title: élément proxyFunctionImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9f03834ca59ede41f2f3c3dff00d7dacdd54db
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995756"
---
# <a name="proxyfunctionimplementations-element"></a><span data-ttu-id="06bdb-103">élément proxyFunctionImplementations</span><span class="sxs-lookup"><span data-stu-id="06bdb-103">proxyFunctionImplementations element</span></span>

<span data-ttu-id="06bdb-104">Génère des implémentations pour les fonctions proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="06bdb-104">Generates implementations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="06bdb-105">Usage</span><span class="sxs-lookup"><span data-stu-id="06bdb-105">Usage</span></span>

``` syntax
<proxyFunctionImplementations>
  child elements
</proxyFunctionImplementations>
```

## <a name="attributes"></a><span data-ttu-id="06bdb-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="06bdb-106">Attributes</span></span>

<span data-ttu-id="06bdb-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="06bdb-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="06bdb-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="06bdb-108">Child elements</span></span>



| <span data-ttu-id="06bdb-109">Élément</span><span class="sxs-lookup"><span data-stu-id="06bdb-109">Element</span></span>                                     | <span data-ttu-id="06bdb-110">Description</span><span class="sxs-lookup"><span data-stu-id="06bdb-110">Description</span></span>                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06bdb-111">**async**</span><span class="sxs-lookup"><span data-stu-id="06bdb-111">**async**</span></span>](async.md)<br/>           | <span data-ttu-id="06bdb-112">Spécifie si les opérations asynchrones sont incluses dans les fonctions proxy générées.</span><span class="sxs-lookup"><span data-stu-id="06bdb-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="06bdb-113">**événements**</span><span class="sxs-lookup"><span data-stu-id="06bdb-113">**events**</span></span>](events.md)<br/>         | <span data-ttu-id="06bdb-114">Spécifie si les événements connexes sont inclus dans les fonctions générées.</span><span class="sxs-lookup"><span data-stu-id="06bdb-114">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="06bdb-115">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="06bdb-115">**faultInfo**</span></span>](faultinfo.md)<br/>   | <span data-ttu-id="06bdb-116">Spécifie si les paramètres utilisés pour passer les informations d’erreur sont inclus dans les fonctions générées.</span><span class="sxs-lookup"><span data-stu-id="06bdb-116">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="06bdb-117">**opération**</span><span class="sxs-lookup"><span data-stu-id="06bdb-117">**operation**</span></span>](operation.md)<br/>   | <span data-ttu-id="06bdb-118">Spécifie une opération pour laquelle du code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="06bdb-118">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="06bdb-119">**portType**</span><span class="sxs-lookup"><span data-stu-id="06bdb-119">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="06bdb-120">Spécifie le type de port pour lequel le code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="06bdb-120">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |
| [<span data-ttu-id="06bdb-121">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="06bdb-121">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="06bdb-122">Spécifie le nom de la classe de proxy côté client.</span><span class="sxs-lookup"><span data-stu-id="06bdb-122">Specifies the name of the client-side proxy class.</span></span><br/> <br/>                                               |



### <a name="child-element-sequence"></a><span data-ttu-id="06bdb-123">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="06bdb-123">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="06bdb-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="06bdb-124">Parent elements</span></span>



| <span data-ttu-id="06bdb-125">Élément</span><span class="sxs-lookup"><span data-stu-id="06bdb-125">Element</span></span>                         | <span data-ttu-id="06bdb-126">Description</span><span class="sxs-lookup"><span data-stu-id="06bdb-126">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="06bdb-127">**txt**</span><span class="sxs-lookup"><span data-stu-id="06bdb-127">**file**</span></span>](file.md)<br/> | <span data-ttu-id="06bdb-128">Génère un fichier à partir du générateur de code.</span><span class="sxs-lookup"><span data-stu-id="06bdb-128">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="06bdb-129">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="06bdb-129">Element information</span></span>



| <span data-ttu-id="06bdb-130">Étiquette</span><span class="sxs-lookup"><span data-stu-id="06bdb-130">Label</span></span> | <span data-ttu-id="06bdb-131">Value</span><span class="sxs-lookup"><span data-stu-id="06bdb-131">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="06bdb-132">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06bdb-132">Minimum supported system</span></span><br/> | <span data-ttu-id="06bdb-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06bdb-133">Windows Vista</span></span> |
| <span data-ttu-id="06bdb-134">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="06bdb-134">Can be empty</span></span>                        | <span data-ttu-id="06bdb-135">Oui</span><span class="sxs-lookup"><span data-stu-id="06bdb-135">Yes</span></span>           |



 

 




