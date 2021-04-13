---
description: Contient la liste des ordinateurs figurant dans le dossier ordinateurs de l’outil d’administration Services de composants. Il contient un objet pour chaque ordinateur.
ms.assetid: 56e32b47-a9f5-4888-b727-71ad0499da00
title: Collection ComputerList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ComputerList
api_type:
- COM
api_location: ''
ms.openlocfilehash: 379e5e07a86d06961de3f8f3936a260451bf43ae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483224"
---
# <a name="computerlist-collection"></a>Collection ComputerList

Contient la liste des ordinateurs figurant dans le dossier **ordinateurs** de l’outil d’administration Services de composants. Il contient un objet pour chaque ordinateur.

Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membres

La collection **ComputerList** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

## <a name="related-collections"></a>Regroupements connexes

Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Vous pouvez accéder à cette collection à partir des regroupements suivants :

-   [**Causes**](root.md)

## <a name="properties"></a>Propriétés

Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :

-   [Nom](#name)

### <a name="name"></a>Nom



| Entrée | Valeur |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Nom de l’ordinateur. Les espaces supplémentaires au début et à la fin de la chaîne sont supprimés. Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection. |
| Accès         | WriteOnce                                                                                                                                                                                                                                                              |
| Type           | String                                                                                                                                                                                                                                                                 |
| Valeur par défaut        | « Nouvel ordinateur »                                                                                                                                                                                                                                                         |
| Système minimal | Windows 2000                                                                                                                                                                                                                                                           |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
