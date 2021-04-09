---
description: Génère des déclarations IDL pour les fonctions de proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.
ms.assetid: 240ef2b3-ed72-45bb-b653-441c4e5540b5
title: élément subscriptionIdlFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e1eba60e327778efb1589436a09e62d043d2960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867602"
---
# <a name="subscriptionidlfunctiondeclarations-element"></a><span data-ttu-id="ad9e6-103">élément subscriptionIdlFunctionDeclarations</span><span class="sxs-lookup"><span data-stu-id="ad9e6-103">subscriptionIdlFunctionDeclarations element</span></span>

<span data-ttu-id="ad9e6-104">Génère des déclarations IDL pour les fonctions de proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.</span><span class="sxs-lookup"><span data-stu-id="ad9e6-104">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="ad9e6-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="ad9e6-105">Usage</span></span>

``` syntax
<subscriptionIdlFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionIdlFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="ad9e6-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="ad9e6-106">Attributes</span></span>



| <span data-ttu-id="ad9e6-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="ad9e6-107">Attribute</span></span>                 | <span data-ttu-id="ad9e6-108">Type</span><span class="sxs-lookup"><span data-stu-id="ad9e6-108">Type</span></span>               | <span data-ttu-id="ad9e6-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ad9e6-109">Required</span></span>      | <span data-ttu-id="ad9e6-110">Description</span><span class="sxs-lookup"><span data-stu-id="ad9e6-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad9e6-111">**EAP**</span><span class="sxs-lookup"><span data-stu-id="ad9e6-111">**extensible**</span></span><br/> | <span data-ttu-id="ad9e6-112">boolean</span><span class="sxs-lookup"><span data-stu-id="ad9e6-112">boolean</span></span><br/> | <span data-ttu-id="ad9e6-113">Non</span><span class="sxs-lookup"><span data-stu-id="ad9e6-113">No</span></span><br/> | <span data-ttu-id="ad9e6-114">La possibilité d’ajouter des points d’extensibilité aux fonctions et aux interfaces.</span><span class="sxs-lookup"><span data-stu-id="ad9e6-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="ad9e6-115">Cette valeur est toujours définie sur true.</span><span class="sxs-lookup"><span data-stu-id="ad9e6-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="ad9e6-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ad9e6-116">Child elements</span></span>



| <span data-ttu-id="ad9e6-117">Élément</span><span class="sxs-lookup"><span data-stu-id="ad9e6-117">Element</span></span>                                                           | <span data-ttu-id="ad9e6-118">Description</span><span class="sxs-lookup"><span data-stu-id="ad9e6-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ad9e6-119">**notificationInterface**</span><span class="sxs-lookup"><span data-stu-id="ad9e6-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="ad9e6-120">Spécifie le nom de l’interface de notification utilisée avec les abonnements aux événements.</span><span class="sxs-lookup"><span data-stu-id="ad9e6-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="ad9e6-121">**opération**</span><span class="sxs-lookup"><span data-stu-id="ad9e6-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="ad9e6-122">Spécifie une opération pour laquelle du code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="ad9e6-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="ad9e6-123">**portType**</span><span class="sxs-lookup"><span data-stu-id="ad9e6-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="ad9e6-124">Spécifie le type de port pour lequel le code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="ad9e6-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |



### <a name="child-element-sequence"></a><span data-ttu-id="ad9e6-125">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ad9e6-125">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="ad9e6-126">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ad9e6-126">Parent elements</span></span>



| <span data-ttu-id="ad9e6-127">Élément</span><span class="sxs-lookup"><span data-stu-id="ad9e6-127">Element</span></span>                         | <span data-ttu-id="ad9e6-128">Description</span><span class="sxs-lookup"><span data-stu-id="ad9e6-128">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="ad9e6-129">**fichier**</span><span class="sxs-lookup"><span data-stu-id="ad9e6-129">**file**</span></span>](file.md)<br/> | <span data-ttu-id="ad9e6-130">Génère un fichier à partir du générateur de code.</span><span class="sxs-lookup"><span data-stu-id="ad9e6-130">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="ad9e6-131">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="ad9e6-131">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="ad9e6-132">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad9e6-132">Minimum supported system</span></span><br/> | <span data-ttu-id="ad9e6-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad9e6-133">Windows Vista</span></span> |
| <span data-ttu-id="ad9e6-134">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="ad9e6-134">Can be empty</span></span>                        | <span data-ttu-id="ad9e6-135">Oui</span><span class="sxs-lookup"><span data-stu-id="ad9e6-135">Yes</span></span>           |



 

 




