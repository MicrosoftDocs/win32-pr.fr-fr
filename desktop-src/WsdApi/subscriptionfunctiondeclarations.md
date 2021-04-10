---
description: Génère des déclarations d’implémentation pour les fonctions proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.
ms.assetid: 0e5b2232-c9bf-4741-921d-bb3bce4ee293
title: élément subscriptionFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8957dcec6133d98830659fa76e2b7939079d3c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104211059"
---
# <a name="subscriptionfunctiondeclarations-element"></a><span data-ttu-id="59d99-103">élément subscriptionFunctionDeclarations</span><span class="sxs-lookup"><span data-stu-id="59d99-103">subscriptionFunctionDeclarations element</span></span>

<span data-ttu-id="59d99-104">Génère des déclarations d’implémentation pour les fonctions proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.</span><span class="sxs-lookup"><span data-stu-id="59d99-104">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="59d99-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="59d99-105">Usage</span></span>

``` syntax
<subscriptionFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="59d99-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="59d99-106">Attributes</span></span>



| <span data-ttu-id="59d99-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="59d99-107">Attribute</span></span>                 | <span data-ttu-id="59d99-108">Type</span><span class="sxs-lookup"><span data-stu-id="59d99-108">Type</span></span>               | <span data-ttu-id="59d99-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="59d99-109">Required</span></span>      | <span data-ttu-id="59d99-110">Description</span><span class="sxs-lookup"><span data-stu-id="59d99-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59d99-111">**EAP**</span><span class="sxs-lookup"><span data-stu-id="59d99-111">**extensible**</span></span><br/> | <span data-ttu-id="59d99-112">boolean</span><span class="sxs-lookup"><span data-stu-id="59d99-112">boolean</span></span><br/> | <span data-ttu-id="59d99-113">Non</span><span class="sxs-lookup"><span data-stu-id="59d99-113">No</span></span><br/> | <span data-ttu-id="59d99-114">La possibilité d’ajouter des points d’extensibilité aux fonctions et aux interfaces.</span><span class="sxs-lookup"><span data-stu-id="59d99-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="59d99-115">Cette valeur est toujours définie sur true.</span><span class="sxs-lookup"><span data-stu-id="59d99-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="59d99-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="59d99-116">Child elements</span></span>



| <span data-ttu-id="59d99-117">Élément</span><span class="sxs-lookup"><span data-stu-id="59d99-117">Element</span></span>                                                           | <span data-ttu-id="59d99-118">Description</span><span class="sxs-lookup"><span data-stu-id="59d99-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59d99-119">**notificationInterface**</span><span class="sxs-lookup"><span data-stu-id="59d99-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="59d99-120">Spécifie le nom de l’interface de notification utilisée avec les abonnements aux événements.</span><span class="sxs-lookup"><span data-stu-id="59d99-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="59d99-121">**opération**</span><span class="sxs-lookup"><span data-stu-id="59d99-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="59d99-122">Spécifie une opération pour laquelle du code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="59d99-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="59d99-123">**portType**</span><span class="sxs-lookup"><span data-stu-id="59d99-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="59d99-124">Spécifie le type de port pour lequel le code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="59d99-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |



### <a name="child-element-sequence"></a><span data-ttu-id="59d99-125">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="59d99-125">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="59d99-126">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="59d99-126">Parent elements</span></span>



| <span data-ttu-id="59d99-127">Élément</span><span class="sxs-lookup"><span data-stu-id="59d99-127">Element</span></span>                         | <span data-ttu-id="59d99-128">Description</span><span class="sxs-lookup"><span data-stu-id="59d99-128">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="59d99-129">**fichier**</span><span class="sxs-lookup"><span data-stu-id="59d99-129">**file**</span></span>](file.md)<br/> | <span data-ttu-id="59d99-130">Génère un fichier à partir du générateur de code.</span><span class="sxs-lookup"><span data-stu-id="59d99-130">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="59d99-131">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="59d99-131">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="59d99-132">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59d99-132">Minimum supported system</span></span><br/> | <span data-ttu-id="59d99-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59d99-133">Windows Vista</span></span> |
| <span data-ttu-id="59d99-134">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="59d99-134">Can be empty</span></span>                        | <span data-ttu-id="59d99-135">Oui</span><span class="sxs-lookup"><span data-stu-id="59d99-135">Yes</span></span>           |



 

 




