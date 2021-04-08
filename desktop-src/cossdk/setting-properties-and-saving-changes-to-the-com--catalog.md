---
description: Chaque élément d’une collection expose des propriétés.
ms.assetid: d9af57ea-c5b3-4017-bdc2-e43b86b3ddcd
title: Modification des propriétés dans le catalogue COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ed2bade8886fe08bb7ed1ece179b35677569f1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748276"
---
# <a name="editing-properties-in-the-com-catalog"></a><span data-ttu-id="28e39-103">Modification des propriétés dans le catalogue COM+</span><span class="sxs-lookup"><span data-stu-id="28e39-103">Editing Properties in the COM+ Catalog</span></span>

<span data-ttu-id="28e39-104">Chaque élément d’une collection expose des propriétés.</span><span class="sxs-lookup"><span data-stu-id="28e39-104">Each item in a collection exposes properties.</span></span> <span data-ttu-id="28e39-105">Ces propriétés permettent de conserver les données de configuration de l’élément représenté par l’élément.</span><span class="sxs-lookup"><span data-stu-id="28e39-105">These properties serve to hold configuration data for whatever element the item represents.</span></span> <span data-ttu-id="28e39-106">Dans l’outil d’administration Services de composants, ces propriétés s’affichent sur une page de propriétés à laquelle vous accédez en cliquant avec le bouton droit sur un élément dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="28e39-106">In the Component Services administrative tool, these properties appear on a property page that you access by right-clicking an item in a folder.</span></span>

<span data-ttu-id="28e39-107">Étant donné que les éléments d’une collection donnée représentent le même type d’élément, ces éléments exposent un ensemble de propriétés qui est cohérent dans la collection.</span><span class="sxs-lookup"><span data-stu-id="28e39-107">Because the items in a given collection all represent the same kind of thing, those items expose a set of properties that is consistent across the collection.</span></span> <span data-ttu-id="28e39-108">Par exemple, la collection d' [**applications**](applications.md) expose une propriété Name, une propriété AppID, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="28e39-108">For example, the [**Applications**](applications.md) collection exposes a Name property, an AppID property, and so forth.</span></span> <span data-ttu-id="28e39-109">Cela est analogue à la façon dont chaque application de l’outil d’administration Services de composants dispose d’une page de propriétés régulièrement structurée disponible.</span><span class="sxs-lookup"><span data-stu-id="28e39-109">This is analogous to how each application in the Component Services administrative tool has a consistently structured property page available for it.</span></span> <span data-ttu-id="28e39-110">Pour obtenir la liste des propriétés disponibles pour la collection d' **applications** , consultez **applications**.</span><span class="sxs-lookup"><span data-stu-id="28e39-110">For a list of properties available to the **Applications** collection, see **Applications**.</span></span> <span data-ttu-id="28e39-111">Pour obtenir la liste des propriétés disponibles pour la collection de [**composants**](components.md) , consultez **composants**.</span><span class="sxs-lookup"><span data-stu-id="28e39-111">For a list of properties available to the [**Components**](components.md) collection, see **Components**.</span></span>

<span data-ttu-id="28e39-112">Pour obtenir la liste complète des propriétés exposées par les éléments de chaque collection, consultez [regroupements d’administration com+](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="28e39-112">For a complete list of properties exposed by items in each collection, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="28e39-113">Vous représentez un élément dans une collection à l’aide d’un objet créé à partir de la classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .</span><span class="sxs-lookup"><span data-stu-id="28e39-113">You represent an item in a collection by using an object created from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span> <span data-ttu-id="28e39-114">Cet objet vous permet de définir et d’accéder à l’une des propriétés exposées par l’élément.</span><span class="sxs-lookup"><span data-stu-id="28e39-114">This object enables you to set and get any of the properties exposed by the item.</span></span> <span data-ttu-id="28e39-115">Lors de la définition des propriétés, il est également possible que vous soyez en mesure d’utiliser un autre enregistreur dans le catalogue COM+.</span><span class="sxs-lookup"><span data-stu-id="28e39-115">When setting properties, it is also possible that you might be contending with another writer to the COM+ catalog.</span></span> <span data-ttu-id="28e39-116">Pour plus d’informations, consultez [obtention et définition des propriétés](getting-and-setting-properties.md).</span><span class="sxs-lookup"><span data-stu-id="28e39-116">For more information, see [Getting and Setting Properties](getting-and-setting-properties.md).</span></span>

<span data-ttu-id="28e39-117">Une fois que vous avez défini les propriétés, aucune modification n’est réellement validée tant que vous n’avez pas enregistré explicitement les modifications.</span><span class="sxs-lookup"><span data-stu-id="28e39-117">After you have set properties, no changes are actually committed until you explicitly save changes.</span></span> <span data-ttu-id="28e39-118">Pour plus d’informations, consultez [enregistrement ou rejet des modifications](saving-or-discarding-changes.md).</span><span class="sxs-lookup"><span data-stu-id="28e39-118">For more information, see [Saving or Discarding Changes](saving-or-discarding-changes.md).</span></span>

<span data-ttu-id="28e39-119">Lorsque vous enregistrez des modifications, le catalogue COM+ met en œuvre une logique de configuration pour s’assurer que vous ne définissez pas de configurations incompatibles.</span><span class="sxs-lookup"><span data-stu-id="28e39-119">When you save changes, the COM+ catalog enforces some configuration logic to ensure that you don't set things to incompatible configurations.</span></span> <span data-ttu-id="28e39-120">Elle modifie également certaines propriétés lorsque vous modifiez explicitement certaines autres propriétés.</span><span class="sxs-lookup"><span data-stu-id="28e39-120">It also changes some properties for you when you explicitly change certain other properties.</span></span> <span data-ttu-id="28e39-121">Pour plus d’informations, consultez [interdépendances entre les propriétés](interdependencies-between-properties.md).</span><span class="sxs-lookup"><span data-stu-id="28e39-121">For more information, see [Interdependencies Between Properties](interdependencies-between-properties.md).</span></span>

<span data-ttu-id="28e39-122">En outre, COM+ dispose d’une fonctionnalité qui vous permet d’effectuer des requêtes dynamiques pour voir quelles propriétés sont disponibles pour les éléments d’une collection donnée.</span><span class="sxs-lookup"><span data-stu-id="28e39-122">Additionally, COM+ has a facility that enables you to dynamically query to see what properties are available for the items in a given collection.</span></span> <span data-ttu-id="28e39-123">Pour plus d’informations, consultez [interrogation des propriétés disponibles](querying-for-available-properties.md).</span><span class="sxs-lookup"><span data-stu-id="28e39-123">For details, see [Querying for Available Properties](querying-for-available-properties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="28e39-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="28e39-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28e39-125">Opérations d’administration COM+ dans les transactions</span><span class="sxs-lookup"><span data-stu-id="28e39-125">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="28e39-126">Gestion des erreurs d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="28e39-126">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="28e39-127">Exemple d’introduction utilisant le catalogue d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="28e39-127">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="28e39-128">Vue d’ensemble des objets comadmin</span><span class="sxs-lookup"><span data-stu-id="28e39-128">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="28e39-129">Récupération des regroupements sur le catalogue COM+</span><span class="sxs-lookup"><span data-stu-id="28e39-129">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



