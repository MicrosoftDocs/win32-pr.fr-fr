---
description: Interrogation des collections associées disponibles
ms.assetid: 9c7d2a01-5dc3-4d35-b938-f1d0525a8286
title: Interrogation des collections associées disponibles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0203df5bb7b5bf89396d5687dc28b19e9b183d56
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403425"
---
# <a name="querying-for-available-related-collections"></a>Interrogation des collections associées disponibles

Si vous écrivez un outil d’administration à usage général, il est probable que vous devrez écrire des routines pour naviguer dans l’ensemble de la hiérarchie de collection. Pour prendre cela en charge, COM+ dispose d’une fonctionnalité qui vous permet de Rechercher dynamiquement les collections associées disponibles à partir d’une collection donnée.

La collection [**RelatedCollectionInfo**](relatedcollectioninfo.md) est disponible à partir de n’importe quel regroupement que vous pouvez contenir et contient un élément pour chaque regroupement associé disponible. Vous pouvez énumérer ces éléments pour déterminer si une collection donnée est disponible.

Vous pouvez obtenir la collection [**RelatedCollectionInfo**](relatedcollectioninfo.md) à partir de n’importe quelle collection que vous conservez à l’aide de la méthode [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) sur l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , en laissant le deuxième paramètre vide à l’emplacement où vous spécifiez normalement la propriété de clé d’un élément parent.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Navigation dans la hiérarchie de regroupement COM+](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[Remplissage des collections COM+](populating-com--collections.md)
</dt> <dt>

[Récupération des regroupements sur le catalogue COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



