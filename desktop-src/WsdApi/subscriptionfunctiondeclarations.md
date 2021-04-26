---
description: Génère des déclarations d’implémentation pour les fonctions proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.
ms.assetid: 0e5b2232-c9bf-4741-921d-bb3bce4ee293
title: élément subscriptionFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7389b30ef7da17f9466fa8aefd24fa04f4c99f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995456"
---
# <a name="subscriptionfunctiondeclarations-element"></a><span data-ttu-id="0109c-103">élément subscriptionFunctionDeclarations</span><span class="sxs-lookup"><span data-stu-id="0109c-103">subscriptionFunctionDeclarations element</span></span>

<span data-ttu-id="0109c-104">Génère des déclarations d’implémentation pour les fonctions proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.</span><span class="sxs-lookup"><span data-stu-id="0109c-104">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="0109c-105">Usage</span><span class="sxs-lookup"><span data-stu-id="0109c-105">Usage</span></span>

``` syntax
<subscriptionFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="0109c-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="0109c-106">Attributes</span></span>



| <span data-ttu-id="0109c-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="0109c-107">Attribute</span></span>                 | <span data-ttu-id="0109c-108">Type</span><span class="sxs-lookup"><span data-stu-id="0109c-108">Type</span></span>               | <span data-ttu-id="0109c-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0109c-109">Required</span></span>      | <span data-ttu-id="0109c-110">Description</span><span class="sxs-lookup"><span data-stu-id="0109c-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0109c-111">**EAP**</span><span class="sxs-lookup"><span data-stu-id="0109c-111">**extensible**</span></span><br/> | <span data-ttu-id="0109c-112">boolean</span><span class="sxs-lookup"><span data-stu-id="0109c-112">boolean</span></span><br/> | <span data-ttu-id="0109c-113">Non</span><span class="sxs-lookup"><span data-stu-id="0109c-113">No</span></span><br/> | <span data-ttu-id="0109c-114">La possibilité d’ajouter des points d’extensibilité aux fonctions et aux interfaces.</span><span class="sxs-lookup"><span data-stu-id="0109c-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="0109c-115">Cette valeur est toujours définie sur true.</span><span class="sxs-lookup"><span data-stu-id="0109c-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="0109c-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0109c-116">Child elements</span></span>



| <span data-ttu-id="0109c-117">Élément</span><span class="sxs-lookup"><span data-stu-id="0109c-117">Element</span></span>                                                           | <span data-ttu-id="0109c-118">Description</span><span class="sxs-lookup"><span data-stu-id="0109c-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0109c-119">**notificationInterface**</span><span class="sxs-lookup"><span data-stu-id="0109c-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="0109c-120">Spécifie le nom de l’interface de notification utilisée avec les abonnements aux événements.</span><span class="sxs-lookup"><span data-stu-id="0109c-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="0109c-121">**opération**</span><span class="sxs-lookup"><span data-stu-id="0109c-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="0109c-122">Spécifie une opération pour laquelle du code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="0109c-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="0109c-123">**portType**</span><span class="sxs-lookup"><span data-stu-id="0109c-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="0109c-124">Spécifie le type de port pour lequel le code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="0109c-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |



### <a name="child-element-sequence"></a><span data-ttu-id="0109c-125">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0109c-125">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="0109c-126">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0109c-126">Parent elements</span></span>



| <span data-ttu-id="0109c-127">Élément</span><span class="sxs-lookup"><span data-stu-id="0109c-127">Element</span></span>                         | <span data-ttu-id="0109c-128">Description</span><span class="sxs-lookup"><span data-stu-id="0109c-128">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="0109c-129">**txt**</span><span class="sxs-lookup"><span data-stu-id="0109c-129">**file**</span></span>](file.md)<br/> | <span data-ttu-id="0109c-130">Génère un fichier à partir du générateur de code.</span><span class="sxs-lookup"><span data-stu-id="0109c-130">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="0109c-131">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="0109c-131">Element information</span></span>



| <span data-ttu-id="0109c-132">Étiquette</span><span class="sxs-lookup"><span data-stu-id="0109c-132">Label</span></span> | <span data-ttu-id="0109c-133">Value</span><span class="sxs-lookup"><span data-stu-id="0109c-133">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="0109c-134">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0109c-134">Minimum supported system</span></span><br/> | <span data-ttu-id="0109c-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0109c-135">Windows Vista</span></span> |
| <span data-ttu-id="0109c-136">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="0109c-136">Can be empty</span></span>                        | <span data-ttu-id="0109c-137">Oui</span><span class="sxs-lookup"><span data-stu-id="0109c-137">Yes</span></span>           |



 

 




