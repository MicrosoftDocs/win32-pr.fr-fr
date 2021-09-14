---
description: Récupère des informations sur les propriétés prises en charge par une collection spécifiée.
ms.assetid: 5e3963c0-6769-4b5b-8636-2d8c98a8776b
title: PropertyInfo, collection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: bd9fdd2262d4499efd6a86fbc5b99bae786016f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008185"
---
# <a name="propertyinfo-collection"></a>PropertyInfo, collection

Récupère des informations sur les propriétés prises en charge par une collection spécifiée. La collection **PropertyInfo** est accessible à partir de n’importe quel objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) à l’aide de la méthode [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) . La collection **PropertyInfo** contient un objet pour chaque propriété prise en charge par la collection d’origine.

## <a name="members"></a>Membres

La collection **PropertyInfo** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

## <a name="related-collections"></a>Regroupements connexes

Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :

-   **PropertyInfo**
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Vous pouvez accéder à cette collection à partir de chaque collection.

## <a name="properties"></a>Propriétés

Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :

-   [Nom](#name)

### <a name="name"></a>Name



| Entrée | Valeur |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Nom de la propriété. Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection. |
| Access         | Lecture seule                                                                                                                                                                                         |
| Type           | String                                                                                                                                                                                           |
| Valeur par défaut        | None                                                                                                                                                                                             |
| Système minimal | Windows 2000                                                                                                                                                                                     |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
