---
description: Contient une liste des protocoles à utiliser par DCOM. Elle contient un objet pour chaque protocole.
ms.assetid: f553ce01-39b6-4dc3-9696-978b390a5c7d
title: Collection DCOMProtocols
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DCOMProtocols
api_type:
- COM
api_location: ''
ms.openlocfilehash: f387c9ba1d46b99c44a3d6616df95f7b6f9cece959a943b63ed12ce6fe8af900
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548018"
---
# <a name="dcomprotocols-collection"></a>Collection DCOMProtocols

Contient une liste des protocoles à utiliser par DCOM. Elle contient un objet pour chaque protocole.

Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membres

La collection **DCOMProtocols** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

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
-   [Commande](#order)
-   [ProtocolCode](#protocolcode)

### <a name="name"></a>Name



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Nom du protocole. Cette propriété est retournée lorsque la méthode de propriété [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection. |
| Accès         | Lecture/écriture                                                                                                                                                   |
| Type           | String                                                                                                                                                      |
| Valeur par défaut        | « Nouveau protocole »                                                                                                                                              |
| Système minimal | Windows 2000                                                                                                                                                |



 

### <a name="order"></a>Commande



| Entrée | Valeur |
|----------------|-----------------------------------------|
| Description    | Ordre dans lequel le protocole doit être essayé. |
| Accès         | Lecture/écriture                               |
| Type           | Long (0-65000)                          |
| Default        | 0                                       |
| Système minimal | Windows 2000                            |



 

### <a name="protocolcode"></a>ProtocolCode



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Code qui spécifie la séquence de protocole RPC. Les codes de protocole pris en charge sont les suivants : ncacn \_ IP \_ TCP, ncacn \_ http, ncacn \_ SPX. Cette propriété est retournée lorsque la méthode de propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) est appelée sur un objet de cette collection. |
| Accès         | WriteOnce                                                                                                                                                                                                                                                                   |
| Type           | String                                                                                                                                                                                                                                                                      |
| Valeur par défaut        | ""                                                                                                                                                                                                                                                                          |
| Système minimal | Windows 2000                                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
