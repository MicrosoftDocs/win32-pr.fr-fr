---
description: Les valeurs de synchronisation peuvent être automatiquement déterminées ou restreintes par la configuration d’autres propriétés, telles que les exigences transactionnelles et l’activation juste-à-temps (JIT).
ms.assetid: 16771121-cb10-42b4-babc-59270188495a
title: Dépendances de synchronisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c139d0d6e78288b25e42bd0a84b29432cebb44ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860969"
---
# <a name="synchronization-dependencies"></a><span data-ttu-id="b5664-103">Dépendances de synchronisation</span><span class="sxs-lookup"><span data-stu-id="b5664-103">Synchronization Dependencies</span></span>

<span data-ttu-id="b5664-104">Les valeurs de synchronisation peuvent être automatiquement déterminées ou restreintes par la configuration d’autres propriétés, telles que les exigences transactionnelles et l’activation juste-à-temps (JIT).</span><span class="sxs-lookup"><span data-stu-id="b5664-104">Synchronization values can be automatically determined or constrained by the configuration of other properties, such as transactional requirements and just-in-time (JIT) activation.</span></span> <span data-ttu-id="b5664-105">Par exemple, COM+ applique la synchronisation pour les composants transactionnels et activés par le JIT.</span><span class="sxs-lookup"><span data-stu-id="b5664-105">For example, COM+ enforces synchronization both for transactional and for JIT-activated components.</span></span>

<span data-ttu-id="b5664-106">Ces dépendances existent, car les composants qui sont activés juste-à-temps ou qui participent à des transactions doivent avoir une isolation et un comportement d’accès concurrentiel appropriés.</span><span class="sxs-lookup"><span data-stu-id="b5664-106">These dependencies exist because components that are JIT-activated or participating in transactions must have proper isolation and concurrency behavior.</span></span> <span data-ttu-id="b5664-107">Par conséquent, COM+ requiert que l’accès à ces composants soit sérialisé en appliquant la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="b5664-107">Therefore, COM+ requires that access to these components be serialized by enforcing synchronization.</span></span> <span data-ttu-id="b5664-108">(Pour plus d’informations sur ces dépendances, consultez [activation juste-à-temps de com+](com--just-in-time-activation.md).)</span><span class="sxs-lookup"><span data-stu-id="b5664-108">(For details on these dependencies, see [COM+ Just-in-Time Activation](com--just-in-time-activation.md).)</span></span>

<span data-ttu-id="b5664-109">Les tableaux suivants présentent les caractéristiques des valeurs d’attribut de synchronisation COM+.</span><span class="sxs-lookup"><span data-stu-id="b5664-109">The following tables show the characteristics of the COM+ synchronization attribute values.</span></span>

### <a name="transactional-requirement"></a><span data-ttu-id="b5664-110">Exigence transactionnelle</span><span class="sxs-lookup"><span data-stu-id="b5664-110">Transactional requirement</span></span>



| <span data-ttu-id="b5664-111">Lorsque les transactions sont définies sur</span><span class="sxs-lookup"><span data-stu-id="b5664-111">When transactions are set to</span></span> | <span data-ttu-id="b5664-112">La synchronisation peut être définie sur</span><span class="sxs-lookup"><span data-stu-id="b5664-112">Synchronization can be set to</span></span>                    |
|------------------------------|--------------------------------------------------|
| <span data-ttu-id="b5664-113">Désactivé</span><span class="sxs-lookup"><span data-stu-id="b5664-113">Disabled</span></span><br/>          | <span data-ttu-id="b5664-114">Tout, en fonction de l’activation JIT</span><span class="sxs-lookup"><span data-stu-id="b5664-114">Anything, depending on JIT activation</span></span><br/> |
| <span data-ttu-id="b5664-115">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5664-115">Not Supported</span></span><br/>     | <span data-ttu-id="b5664-116">Tout, en fonction de l’activation JIT</span><span class="sxs-lookup"><span data-stu-id="b5664-116">Anything, depending on JIT activation</span></span><br/> |
| <span data-ttu-id="b5664-117">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5664-117">Supported</span></span><br/>         | <span data-ttu-id="b5664-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b5664-118">Required</span></span><br/>                              |
| <span data-ttu-id="b5664-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b5664-119">Required</span></span><br/>          | <span data-ttu-id="b5664-120">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b5664-120">Required</span></span><br/>                              |
| <span data-ttu-id="b5664-121">Nouveau requis</span><span class="sxs-lookup"><span data-stu-id="b5664-121">Requires New</span></span><br/>      | <span data-ttu-id="b5664-122">Obligatoire ou requiert New</span><span class="sxs-lookup"><span data-stu-id="b5664-122">Required or Requires New</span></span><br/>              |



 

### <a name="jit-activation"></a><span data-ttu-id="b5664-123">Activation juste-à-temps</span><span class="sxs-lookup"><span data-stu-id="b5664-123">JIT Activation</span></span>



| <span data-ttu-id="b5664-124">Lorsque l’activation JIT a la valeur</span><span class="sxs-lookup"><span data-stu-id="b5664-124">When JIT Activation is set to</span></span> | <span data-ttu-id="b5664-125">La synchronisation peut être définie sur</span><span class="sxs-lookup"><span data-stu-id="b5664-125">Synchronization can be set to</span></span>       |
|-------------------------------|-------------------------------------|
| <span data-ttu-id="b5664-126">activé</span><span class="sxs-lookup"><span data-stu-id="b5664-126">Enabled</span></span><br/>            | <span data-ttu-id="b5664-127">Obligatoire ou requiert New</span><span class="sxs-lookup"><span data-stu-id="b5664-127">Required or Requires New</span></span><br/> |
| <span data-ttu-id="b5664-128">Désactivé</span><span class="sxs-lookup"><span data-stu-id="b5664-128">Disabled</span></span><br/>           | <span data-ttu-id="b5664-129">Rien</span><span class="sxs-lookup"><span data-stu-id="b5664-129">Anything</span></span><br/>                 |



 

<span data-ttu-id="b5664-130">Pour plus d’informations sur la façon dont les attributs transaction, activation JIT et synchronisation se comportent, consultez [Configuration des transactions](configuring-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="b5664-130">For more detail about how transaction, JIT Activation, and Synchronization attributes behave together, see [Configuring Transactions](configuring-transactions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5664-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b5664-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5664-132">Définition de l’attribut de synchronisation</span><span class="sxs-lookup"><span data-stu-id="b5664-132">Setting the Synchronization Attribute</span></span>](setting-the-synchronization-attribute.md)
</dt> <dt>

[<span data-ttu-id="b5664-133">Valeurs d’attribut de synchronisation</span><span class="sxs-lookup"><span data-stu-id="b5664-133">Synchronization Attribute Values</span></span>](synchronization-attribute-values.md)
</dt> </dl>

 

 




