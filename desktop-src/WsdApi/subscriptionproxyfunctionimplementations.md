---
description: Génère des implémentations pour les fonctions proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.
ms.assetid: aa26a3f1-df1e-4caa-9ada-6f4a6627b6b8
title: élément subscriptionProxyFunctionImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb57fa21910f9b39440257bc72918519b35c6a57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112983"
---
# <a name="subscriptionproxyfunctionimplementations-element"></a><span data-ttu-id="b8e6d-103">élément subscriptionProxyFunctionImplementations</span><span class="sxs-lookup"><span data-stu-id="b8e6d-103">subscriptionProxyFunctionImplementations element</span></span>

<span data-ttu-id="b8e6d-104">Génère des implémentations pour les fonctions proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.</span><span class="sxs-lookup"><span data-stu-id="b8e6d-104">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="b8e6d-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="b8e6d-105">Usage</span></span>

``` syntax
<subscriptionProxyFunctionImplementations
  extensible = "boolean">
  child elements
</subscriptionProxyFunctionImplementations>
```

## <a name="attributes"></a><span data-ttu-id="b8e6d-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="b8e6d-106">Attributes</span></span>



| <span data-ttu-id="b8e6d-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="b8e6d-107">Attribute</span></span>                 | <span data-ttu-id="b8e6d-108">Type</span><span class="sxs-lookup"><span data-stu-id="b8e6d-108">Type</span></span>               | <span data-ttu-id="b8e6d-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b8e6d-109">Required</span></span>      | <span data-ttu-id="b8e6d-110">Description</span><span class="sxs-lookup"><span data-stu-id="b8e6d-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8e6d-111">**EAP**</span><span class="sxs-lookup"><span data-stu-id="b8e6d-111">**extensible**</span></span><br/> | <span data-ttu-id="b8e6d-112">boolean</span><span class="sxs-lookup"><span data-stu-id="b8e6d-112">boolean</span></span><br/> | <span data-ttu-id="b8e6d-113">Non</span><span class="sxs-lookup"><span data-stu-id="b8e6d-113">No</span></span><br/> | <span data-ttu-id="b8e6d-114">La possibilité d’ajouter des points d’extensibilité aux fonctions et aux interfaces.</span><span class="sxs-lookup"><span data-stu-id="b8e6d-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="b8e6d-115">Cette valeur est toujours définie sur true.</span><span class="sxs-lookup"><span data-stu-id="b8e6d-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="b8e6d-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b8e6d-116">Child elements</span></span>



| <span data-ttu-id="b8e6d-117">Élément</span><span class="sxs-lookup"><span data-stu-id="b8e6d-117">Element</span></span>                                                           | <span data-ttu-id="b8e6d-118">Description</span><span class="sxs-lookup"><span data-stu-id="b8e6d-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8e6d-119">**notificationInterface**</span><span class="sxs-lookup"><span data-stu-id="b8e6d-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="b8e6d-120">Spécifie le nom de l’interface de notification utilisée avec les abonnements aux événements.</span><span class="sxs-lookup"><span data-stu-id="b8e6d-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="b8e6d-121">**opération**</span><span class="sxs-lookup"><span data-stu-id="b8e6d-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="b8e6d-122">Spécifie une opération pour laquelle du code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="b8e6d-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="b8e6d-123">**portType**</span><span class="sxs-lookup"><span data-stu-id="b8e6d-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="b8e6d-124">Spécifie le type de port pour lequel le code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="b8e6d-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |
| [<span data-ttu-id="b8e6d-125">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="b8e6d-125">**proxyClass**</span></span>](proxyclass.md)<br/>                       | <span data-ttu-id="b8e6d-126">Spécifie le nom de la classe de proxy côté client.</span><span class="sxs-lookup"><span data-stu-id="b8e6d-126">Specifies the name of the client-side proxy class.</span></span><br/> <br/>                              |



### <a name="child-element-sequence"></a><span data-ttu-id="b8e6d-127">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b8e6d-127">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="b8e6d-128">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b8e6d-128">Parent elements</span></span>



| <span data-ttu-id="b8e6d-129">Élément</span><span class="sxs-lookup"><span data-stu-id="b8e6d-129">Element</span></span>                         | <span data-ttu-id="b8e6d-130">Description</span><span class="sxs-lookup"><span data-stu-id="b8e6d-130">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="b8e6d-131">**fichier**</span><span class="sxs-lookup"><span data-stu-id="b8e6d-131">**file**</span></span>](file.md)<br/> | <span data-ttu-id="b8e6d-132">Génère un fichier à partir du générateur de code.</span><span class="sxs-lookup"><span data-stu-id="b8e6d-132">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="b8e6d-133">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b8e6d-133">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="b8e6d-134">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8e6d-134">Minimum supported system</span></span><br/> | <span data-ttu-id="b8e6d-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8e6d-135">Windows Vista</span></span> |
| <span data-ttu-id="b8e6d-136">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="b8e6d-136">Can be empty</span></span>                        | <span data-ttu-id="b8e6d-137">Oui</span><span class="sxs-lookup"><span data-stu-id="b8e6d-137">Yes</span></span>           |



 

 




