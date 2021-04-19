---
description: Génère des déclarations pour les fonctions stub pour les opérations de type de port.
ms.assetid: d43baeff-c941-4ce9-a6ae-8aa61ef44048
title: élément stubDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ceaa8871928031edff90db0491483cfd06bdcc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522472"
---
# <a name="stubdeclarations-element"></a><span data-ttu-id="0f0b5-103">élément stubDeclarations</span><span class="sxs-lookup"><span data-stu-id="0f0b5-103">stubDeclarations element</span></span>

<span data-ttu-id="0f0b5-104">Génère des déclarations pour les fonctions stub pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="0f0b5-104">Generates declarations for stub functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="0f0b5-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="0f0b5-105">Usage</span></span>

``` syntax
<stubDeclarations>
  child elements
</stubDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="0f0b5-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="0f0b5-106">Attributes</span></span>

<span data-ttu-id="0f0b5-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="0f0b5-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0f0b5-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0f0b5-108">Child elements</span></span>



| <span data-ttu-id="0f0b5-109">Élément</span><span class="sxs-lookup"><span data-stu-id="0f0b5-109">Element</span></span>                                   | <span data-ttu-id="0f0b5-110">Description</span><span class="sxs-lookup"><span data-stu-id="0f0b5-110">Description</span></span>                                                                                      |
|-------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f0b5-111">**événements**</span><span class="sxs-lookup"><span data-stu-id="0f0b5-111">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="0f0b5-112">Spécifie si les événements connexes sont inclus dans les fonctions générées.</span><span class="sxs-lookup"><span data-stu-id="0f0b5-112">Specifies whether related events are included in the generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="0f0b5-113">**opération**</span><span class="sxs-lookup"><span data-stu-id="0f0b5-113">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="0f0b5-114">Spécifie une opération pour laquelle du code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="0f0b5-114">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                 |
| [<span data-ttu-id="0f0b5-115">**portType**</span><span class="sxs-lookup"><span data-stu-id="0f0b5-115">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="0f0b5-116">Spécifie le type de port pour lequel le code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="0f0b5-116">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                |



### <a name="child-element-sequence"></a><span data-ttu-id="0f0b5-117">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0f0b5-117">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  events?
)
```

## <a name="parent-elements"></a><span data-ttu-id="0f0b5-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0f0b5-118">Parent elements</span></span>



| <span data-ttu-id="0f0b5-119">Élément</span><span class="sxs-lookup"><span data-stu-id="0f0b5-119">Element</span></span>                         | <span data-ttu-id="0f0b5-120">Description</span><span class="sxs-lookup"><span data-stu-id="0f0b5-120">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="0f0b5-121">**fichier**</span><span class="sxs-lookup"><span data-stu-id="0f0b5-121">**file**</span></span>](file.md)<br/> | <span data-ttu-id="0f0b5-122">Génère un fichier à partir du générateur de code.</span><span class="sxs-lookup"><span data-stu-id="0f0b5-122">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="0f0b5-123">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="0f0b5-123">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="0f0b5-124">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f0b5-124">Minimum supported system</span></span><br/> | <span data-ttu-id="0f0b5-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f0b5-125">Windows Vista</span></span> |
| <span data-ttu-id="0f0b5-126">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="0f0b5-126">Can be empty</span></span>                        | <span data-ttu-id="0f0b5-127">Oui</span><span class="sxs-lookup"><span data-stu-id="0f0b5-127">Yes</span></span>           |



 

 




