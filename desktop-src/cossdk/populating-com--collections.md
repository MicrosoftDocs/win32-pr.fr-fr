---
description: Remplissage des collections COM+
ms.assetid: df86cbab-dcb8-46ac-aebf-8516276b6e81
title: Remplissage des collections COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 521d85521eb7e3750d06920a570ddeaf4d7e9b20
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317877"
---
# <a name="populating-com-collections"></a><span data-ttu-id="60026-103">Remplissage des collections COM+</span><span class="sxs-lookup"><span data-stu-id="60026-103">Populating COM+ Collections</span></span>

<span data-ttu-id="60026-104">Une fois que vous avez récupéré une collection et que vous pouvez travailler directement avec les éléments qu’elle contient, vous devez remplir la collection à l’aide de la méthode [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) .</span><span class="sxs-lookup"><span data-stu-id="60026-104">After you have retrieved a collection and before you can work directly with the items it contains, you must populate the collection by using the [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) method.</span></span> <span data-ttu-id="60026-105">Cette instruction extrait des données pour le contenu de la collection à partir du catalogue COM+.</span><span class="sxs-lookup"><span data-stu-id="60026-105">This fetches data for the collection's contents from the COM+ catalog.</span></span>

<span data-ttu-id="60026-106">Il est important de comprendre que chaque fois que vous utilisez des objets comadmin pour manipuler des éléments ou des données dans des collections, vous travaillez vraiment sur des données mises en cache de façon temporaire ; vous ne travaillez pas directement avec le catalogue persistant.</span><span class="sxs-lookup"><span data-stu-id="60026-106">It is important to understand that whenever you use the COMAdmin objects to manipulate items or data in collections, you are really working on transiently cached data; you are not working directly with the persisted catalog.</span></span> <span data-ttu-id="60026-107">Rien ne fait que vous utilisez une collection ou l’un de ses éléments est reflété sur le catalogue tant que vous n’avez pas appelé [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) sur la collection.</span><span class="sxs-lookup"><span data-stu-id="60026-107">Nothing that you do with a collection or any of its items is reflected on the catalog until you call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) on the collection.</span></span> <span data-ttu-id="60026-108">Pour plus d’informations, consultez [enregistrement ou rejet des modifications](saving-or-discarding-changes.md).</span><span class="sxs-lookup"><span data-stu-id="60026-108">For more detail, see [Saving or Discarding Changes](saving-or-discarding-changes.md).</span></span>

<span data-ttu-id="60026-109">Tout appel ultérieur à [**remplir**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate), avant d’appeler [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), a pour effet d’ignorer les modifications en attente de tous les éléments de la collection.</span><span class="sxs-lookup"><span data-stu-id="60026-109">Any subsequent calls to [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate), prior to calling [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), has the effect of discarding pending changes to all items in the collection.</span></span> <span data-ttu-id="60026-110">Le **remplissage** remplit toujours le cache dans lequel vous travaillez, quelles que soient les données qui sont conservées dans le magasin de données de catalogue sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="60026-110">**Populate** always populates the cache you're working in with whatever data is persisted on the underlying catalog data store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60026-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="60026-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60026-112">Navigation dans la hiérarchie de regroupement COM+</span><span class="sxs-lookup"><span data-stu-id="60026-112">Navigating the COM+ Collection Hierarchy</span></span>](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[<span data-ttu-id="60026-113">Interrogation des collections associées disponibles</span><span class="sxs-lookup"><span data-stu-id="60026-113">Querying for Available Related Collections</span></span>](querying-for-available-related-collections.md)
</dt> <dt>

[<span data-ttu-id="60026-114">Récupération des regroupements sur le catalogue COM+</span><span class="sxs-lookup"><span data-stu-id="60026-114">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



