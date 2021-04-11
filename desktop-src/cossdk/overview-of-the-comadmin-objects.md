---
description: Les objets comadmin offrent un modèle objet simple qui vous permet d’accéder au catalogue COM+.
ms.assetid: 84cee7a7-f7a6-41a0-afd5-fae56365612e
title: Vue d’ensemble des objets comadmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22837cbe0548b623463234d1a03d17288eba2149
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111674"
---
# <a name="overview-of-the-comadmin-objects"></a><span data-ttu-id="a5eac-103">Vue d’ensemble des objets comadmin</span><span class="sxs-lookup"><span data-stu-id="a5eac-103">Overview of the COMAdmin Objects</span></span>

<span data-ttu-id="a5eac-104">Les objets comadmin offrent un modèle objet simple qui vous permet d’accéder au catalogue COM+.</span><span class="sxs-lookup"><span data-stu-id="a5eac-104">The COMAdmin objects offer a simple object model that provides you with access to the COM+ catalog.</span></span> <span data-ttu-id="a5eac-105">Dans ce cas, ils servent à modéliser toutes les fonctionnalités fournies par l’outil d’administration Services de composants.</span><span class="sxs-lookup"><span data-stu-id="a5eac-105">In doing so, they serve to model all the functionality provided by the Component Services administrative tool.</span></span> <span data-ttu-id="a5eac-106">Chaque fois que vous effectuez une administration COM+, vous interagissez avec le catalogue COM+.</span><span class="sxs-lookup"><span data-stu-id="a5eac-106">Whenever you do any kind of COM+ administration, you are interacting with the COM+ catalog.</span></span> <span data-ttu-id="a5eac-107">Pour obtenir une description du catalogue, consultez [accès au catalogue com+](accessing-the-com--catalog.md).</span><span class="sxs-lookup"><span data-stu-id="a5eac-107">For a description of the catalog, see [Accessing the COM+ Catalog](accessing-the-com--catalog.md).</span></span>

<span data-ttu-id="a5eac-108">Les informations que vous obtenez à partir de l’outil d’administration Services de composants ou à l’aide des objets comadmin sont structurées de la même façon, et les actions que vous effectuez dans l’un ou l’autre contexte sont analogues.</span><span class="sxs-lookup"><span data-stu-id="a5eac-108">The information you obtain either from the Component Services administrative tool or by using the COMAdmin objects is structured similarly, and the actions you perform in either context are analogous.</span></span> <span data-ttu-id="a5eac-109">La corrélation de base entre l’utilisation du composant logiciel enfichable Services de composants et l’administration par programme est que les dossiers de l’arborescence de la console du composant logiciel enfichable correspondent aux regroupements dans le catalogue COM+.</span><span class="sxs-lookup"><span data-stu-id="a5eac-109">The basic correlation between using the Component Services snap-in and programmatic administration is that folders in the console tree of the snap-in correspond to collections in the COM+ catalog.</span></span> <span data-ttu-id="a5eac-110">Autrement dit, chaque dossier du composant logiciel enfichable contient tous les éléments d’un même type ; par exemple, les **applications com+** contiennent des applications com+ installées : chaque collection du catalogue com+ contient des éléments d’un type uniforme.</span><span class="sxs-lookup"><span data-stu-id="a5eac-110">That is, just as each folder in the snap-in contains items all of a kind; for example, **COM+ Applications** holds installed COM+ applications—each collection in the COM+ catalog holds items of a uniform kind.</span></span> <span data-ttu-id="a5eac-111">De plus, tout comme chaque élément d’un dossier a des propriétés que vous pouvez définir sur une feuille de propriétés, chaque élément d’une collection expose des propriétés que vous pouvez définir.</span><span class="sxs-lookup"><span data-stu-id="a5eac-111">Further, just as each item in a folder has properties that you can set on a property sheet, each item in a collection exposes properties that you can set.</span></span>

<span data-ttu-id="a5eac-112">Pour vous permettre de configurer des objets dans cette structure, les objets comadmin vous fournissent les moyens d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="a5eac-112">To enable you to configure objects within this structure, the COMAdmin objects provide you with the means to do the following:</span></span>

-   <span data-ttu-id="a5eac-113">Accéder au catalogue COM+</span><span class="sxs-lookup"><span data-stu-id="a5eac-113">Access the COM+ catalog</span></span>
-   <span data-ttu-id="a5eac-114">Accéder aux regroupements dans le catalogue</span><span class="sxs-lookup"><span data-stu-id="a5eac-114">Access collections in the catalog</span></span>
-   <span data-ttu-id="a5eac-115">Accéder aux éléments dans les collections</span><span class="sxs-lookup"><span data-stu-id="a5eac-115">Access items in collections</span></span>
-   <span data-ttu-id="a5eac-116">Accéder aux propriétés des éléments des collections</span><span class="sxs-lookup"><span data-stu-id="a5eac-116">Access properties on the items in the collections</span></span>

<span data-ttu-id="a5eac-117">Pour prendre en charge ces actions, la bibliothèque comadmin fournit les trois classes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a5eac-117">To support these actions, the COMAdmin Library provides the following three classes:</span></span>

-   <span data-ttu-id="a5eac-118">[**COMAdminCatalog**](comadmincatalog.md), qui représente le catalogue lui-même.</span><span class="sxs-lookup"><span data-stu-id="a5eac-118">[**COMAdminCatalog**](comadmincatalog.md), which represents the catalog itself.</span></span>
-   <span data-ttu-id="a5eac-119">[**COMAdminCatalogCollection**](comadmincatalogcollection.md), qui représente n’importe quelle collection.</span><span class="sxs-lookup"><span data-stu-id="a5eac-119">[**COMAdminCatalogCollection**](comadmincatalogcollection.md), which represents any collection.</span></span>
-   <span data-ttu-id="a5eac-120">[**COMAdminCatalogObject**](comadmincatalogobject.md), qui représente tout élément d’une collection.</span><span class="sxs-lookup"><span data-stu-id="a5eac-120">[**COMAdminCatalogObject**](comadmincatalogobject.md), which represents any item in a collection.</span></span>

<span data-ttu-id="a5eac-121">Pour obtenir une description plus complète de ces classes, consultez [Description Résumé des classes comadmin](summary-description-of-the-comadmin-classes.md) dans cette section.</span><span class="sxs-lookup"><span data-stu-id="a5eac-121">For fuller descriptions of these classes, see [Summary Description of the COMAdmin Classes](summary-description-of-the-comadmin-classes.md) in this section.</span></span>

<span data-ttu-id="a5eac-122">Pour obtenir une idée rapide des actions classiques que vous effectuez dans l’administration par programme, consultez [exemple d’introduction à l’aide du catalogue d’administration com+](introductory-example-using-the-com--administration-catalog.md).</span><span class="sxs-lookup"><span data-stu-id="a5eac-122">To get a quick idea of typical actions you perform in programmatic administration, see [Introductory Example Using the COM+ Administration Catalog](introductory-example-using-the-com--administration-catalog.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5eac-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a5eac-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5eac-124">Opérations d’administration COM+ dans les transactions</span><span class="sxs-lookup"><span data-stu-id="a5eac-124">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="a5eac-125">Gestion des erreurs d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="a5eac-125">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="a5eac-126">Exemple d’introduction utilisant le catalogue d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="a5eac-126">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="a5eac-127">Récupération des regroupements sur le catalogue COM+</span><span class="sxs-lookup"><span data-stu-id="a5eac-127">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="a5eac-128">Définition des propriétés et enregistrement des modifications dans le catalogue COM+</span><span class="sxs-lookup"><span data-stu-id="a5eac-128">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



