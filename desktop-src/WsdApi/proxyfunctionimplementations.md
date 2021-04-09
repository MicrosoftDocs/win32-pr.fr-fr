---
description: Génère des implémentations pour les fonctions proxy pour les opérations de type de port.
ms.assetid: 9505ee5f-fdb9-41b8-9537-0c5d29f90168
title: élément proxyFunctionImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a27e217cfa3d0a9efd204a1b18c7b2f0ca16f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867345"
---
# <a name="proxyfunctionimplementations-element"></a><span data-ttu-id="93cae-103">élément proxyFunctionImplementations</span><span class="sxs-lookup"><span data-stu-id="93cae-103">proxyFunctionImplementations element</span></span>

<span data-ttu-id="93cae-104">Génère des implémentations pour les fonctions proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="93cae-104">Generates implementations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="93cae-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="93cae-105">Usage</span></span>

``` syntax
<proxyFunctionImplementations>
  child elements
</proxyFunctionImplementations>
```

## <a name="attributes"></a><span data-ttu-id="93cae-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="93cae-106">Attributes</span></span>

<span data-ttu-id="93cae-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="93cae-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="93cae-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="93cae-108">Child elements</span></span>



| <span data-ttu-id="93cae-109">Élément</span><span class="sxs-lookup"><span data-stu-id="93cae-109">Element</span></span>                                     | <span data-ttu-id="93cae-110">Description</span><span class="sxs-lookup"><span data-stu-id="93cae-110">Description</span></span>                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93cae-111">**async**</span><span class="sxs-lookup"><span data-stu-id="93cae-111">**async**</span></span>](async.md)<br/>           | <span data-ttu-id="93cae-112">Spécifie si les opérations asynchrones sont incluses dans les fonctions proxy générées.</span><span class="sxs-lookup"><span data-stu-id="93cae-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="93cae-113">**événements**</span><span class="sxs-lookup"><span data-stu-id="93cae-113">**events**</span></span>](events.md)<br/>         | <span data-ttu-id="93cae-114">Spécifie si les événements connexes sont inclus dans les fonctions générées.</span><span class="sxs-lookup"><span data-stu-id="93cae-114">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="93cae-115">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="93cae-115">**faultInfo**</span></span>](faultinfo.md)<br/>   | <span data-ttu-id="93cae-116">Spécifie si les paramètres utilisés pour passer les informations d’erreur sont inclus dans les fonctions générées.</span><span class="sxs-lookup"><span data-stu-id="93cae-116">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="93cae-117">**opération**</span><span class="sxs-lookup"><span data-stu-id="93cae-117">**operation**</span></span>](operation.md)<br/>   | <span data-ttu-id="93cae-118">Spécifie une opération pour laquelle du code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="93cae-118">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="93cae-119">**portType**</span><span class="sxs-lookup"><span data-stu-id="93cae-119">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="93cae-120">Spécifie le type de port pour lequel le code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="93cae-120">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |
| [<span data-ttu-id="93cae-121">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="93cae-121">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="93cae-122">Spécifie le nom de la classe de proxy côté client.</span><span class="sxs-lookup"><span data-stu-id="93cae-122">Specifies the name of the client-side proxy class.</span></span><br/> <br/>                                               |



### <a name="child-element-sequence"></a><span data-ttu-id="93cae-123">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="93cae-123">Child element sequence</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="93cae-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="93cae-124">Parent elements</span></span>



| <span data-ttu-id="93cae-125">Élément</span><span class="sxs-lookup"><span data-stu-id="93cae-125">Element</span></span>                         | <span data-ttu-id="93cae-126">Description</span><span class="sxs-lookup"><span data-stu-id="93cae-126">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="93cae-127">**fichier**</span><span class="sxs-lookup"><span data-stu-id="93cae-127">**file**</span></span>](file.md)<br/> | <span data-ttu-id="93cae-128">Génère un fichier à partir du générateur de code.</span><span class="sxs-lookup"><span data-stu-id="93cae-128">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="93cae-129">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="93cae-129">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="93cae-130">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93cae-130">Minimum supported system</span></span><br/> | <span data-ttu-id="93cae-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93cae-131">Windows Vista</span></span> |
| <span data-ttu-id="93cae-132">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="93cae-132">Can be empty</span></span>                        | <span data-ttu-id="93cae-133">Oui</span><span class="sxs-lookup"><span data-stu-id="93cae-133">Yes</span></span>           |



 

 




