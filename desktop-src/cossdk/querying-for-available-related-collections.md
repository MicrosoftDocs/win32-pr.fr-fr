---
description: Interrogation des collections associées disponibles
ms.assetid: 9c7d2a01-5dc3-4d35-b938-f1d0525a8286
title: Interrogation des collections associées disponibles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0203df5bb7b5bf89396d5687dc28b19e9b183d56
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317905"
---
# <a name="querying-for-available-related-collections"></a><span data-ttu-id="61173-103">Interrogation des collections associées disponibles</span><span class="sxs-lookup"><span data-stu-id="61173-103">Querying for Available Related Collections</span></span>

<span data-ttu-id="61173-104">Si vous écrivez un outil d’administration à usage général, il est probable que vous devrez écrire des routines pour naviguer dans l’ensemble de la hiérarchie de collection.</span><span class="sxs-lookup"><span data-stu-id="61173-104">If you are writing a general-purpose administration tool, it is likely that you will need to write routines for navigating the entire collection hierarchy.</span></span> <span data-ttu-id="61173-105">Pour prendre cela en charge, COM+ dispose d’une fonctionnalité qui vous permet de Rechercher dynamiquement les collections associées disponibles à partir d’une collection donnée.</span><span class="sxs-lookup"><span data-stu-id="61173-105">To support this, COM+ has a facility that enables you to dynamically query for the related collections that are available from any given collection.</span></span>

<span data-ttu-id="61173-106">La collection [**RelatedCollectionInfo**](relatedcollectioninfo.md) est disponible à partir de n’importe quel regroupement que vous pouvez contenir et contient un élément pour chaque regroupement associé disponible.</span><span class="sxs-lookup"><span data-stu-id="61173-106">The [**RelatedCollectionInfo**](relatedcollectioninfo.md) collection is available from any collection that you might be holding and contains an item for each available related collection.</span></span> <span data-ttu-id="61173-107">Vous pouvez énumérer ces éléments pour déterminer si une collection donnée est disponible.</span><span class="sxs-lookup"><span data-stu-id="61173-107">You can enumerate through these items to determine whether a given collection is available.</span></span>

<span data-ttu-id="61173-108">Vous pouvez obtenir la collection [**RelatedCollectionInfo**](relatedcollectioninfo.md) à partir de n’importe quelle collection que vous conservez à l’aide de la méthode [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) sur l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , en laissant le deuxième paramètre vide à l’emplacement où vous spécifiez normalement la propriété de clé d’un élément parent.</span><span class="sxs-lookup"><span data-stu-id="61173-108">You can get the [**RelatedCollectionInfo**](relatedcollectioninfo.md) collection from any collection you are holding by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, leaving the second parameter blank where you would normally specify a parent item's Key property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61173-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="61173-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61173-110">Navigation dans la hiérarchie de regroupement COM+</span><span class="sxs-lookup"><span data-stu-id="61173-110">Navigating the COM+ Collection Hierarchy</span></span>](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[<span data-ttu-id="61173-111">Remplissage des collections COM+</span><span class="sxs-lookup"><span data-stu-id="61173-111">Populating COM+ Collections</span></span>](populating-com--collections.md)
</dt> <dt>

[<span data-ttu-id="61173-112">Récupération des regroupements sur le catalogue COM+</span><span class="sxs-lookup"><span data-stu-id="61173-112">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



