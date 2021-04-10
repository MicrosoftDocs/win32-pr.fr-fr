---
description: Récupère des informations sur d’autres collections relatives à la collection à partir de laquelle elle est appelée.
ms.assetid: daea5b23-6a13-46f4-89c8-0d93b614311e
title: Collection RelatedCollectionInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RelatedCollectionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 21a9a1905d75c81d605f30a3f6cffced8837034d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200979"
---
# <a name="relatedcollectioninfo-collection"></a>Collection RelatedCollectionInfo

Récupère des informations sur d’autres collections relatives à la collection à partir de laquelle elle est appelée. La collection **RelatedCollectionInfo** est accessible à partir de n’importe quel objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) à l’aide de la méthode [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) . La collection **RelatedCollectionInfo** contient un objet pour chaque collection qui est accessible à partir de la collection d’origine. Les regroupements connexes suivent la hiérarchie de regroupement de l’outil d’administration Services de composants.

Cette collection ne prend pas en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membres

La collection **RelatedCollectionInfo** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

## <a name="related-collections"></a>Regroupements connexes

Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :

-   [**PropertyInfo**](propertyinfo.md)
-   **RelatedCollectionInfo**

Vous pouvez accéder à cette collection à partir de chaque collection.

## <a name="properties"></a>Propriétés

Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :

-   [Nom](#name)

### <a name="name"></a>Nom



| Entrée | Valeur |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Nom de la collection associée. Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection. |
| Accès         | Lecture seule                                                                                                                                                                                                   |
| Type           | String                                                                                                                                                                                                     |
| Default        | None                                                                                                                                                                                                       |
| Système minimal | Windows 2000                                                                                                                                                                                               |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
