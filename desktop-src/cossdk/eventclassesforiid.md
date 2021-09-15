---
description: Récupère des informations sur les classes d’événements.
ms.assetid: 33a87692-cacf-4a1c-974e-8d0e20295333
title: Collection EventClassesForIID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventClassesForIID
api_type:
- COM
api_location: ''
ms.openlocfilehash: 635ff6e87d68bfdcb4e82a24673c4ced00a7f81d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519337"
---
# <a name="eventclassesforiid-collection"></a>Collection EventClassesForIID

Récupère des informations sur les classes d’événements.

La connexion entre le serveur de publication et le ou les abonnés est gérée par un objet [**EventClass**](/windows/desktop/api/eventsys/nn-eventsys-ieventclass) , qui est un composant com+ contenant les interfaces et les méthodes utilisées par un serveur de publication pour déclencher des événements.

Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membres

La collection **EventClassesForIID** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

## <a name="related-collections"></a>Regroupements connexes

Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Vous pouvez accéder à cette collection à partir des regroupements suivants :

-   [**Causes**](root.md)

## <a name="properties"></a>Propriétés

Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :

-   [Application](#application)
-   [Nombre de bits](#bitness)
-   [IDENTIFICATEUR](#clsid)
-   [Description](#description)
-   [IsPrivateComponent](#isprivatecomponent)
-   [ProgID](#progid)

### <a name="application"></a>Application



| Entrée | Valeur |
|----------------|----------------------------------------------------------|
| Description    | GUID de l’application contenant la classe d’événements. |
| Access         | Lecture seule                                                 |
| Type           | String                                                   |
| Valeur par défaut        | N/A                                                      |
| Système minimal | Windows XP                                               |



 

### <a name="bitness"></a>Nombre de bits



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Représente le type de bits binaire de la classe d’événements. sur les systèmes qui utilisent la Windows 64 bits, cette propriété permet de faire la distinction entre les composants 64 bits et les composants 32 bits. |
| Access         | Lecture seule                                                                                                                                                                |
| Type           | Valeurs possibles longues : COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0X2)                                                                                           |
| Default        | N/A                                                                                                                                                                     |
| Système minimal | Windows XP                                                                                                                                                              |



 

### <a name="clsid"></a>CLSID



| Entrée | Valeur |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | GUID de la classe d’événements. Cette propriété est retournée lorsque la méthode de propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) est appelée sur un objet de cette collection. |
| Access         | Lecture seule                                                                                                                                                      |
| Type           | String                                                                                                                                                        |
| Valeur par défaut        | N/A                                                                                                                                                           |
| Système minimal | Windows XP                                                                                                                                                    |



 

### <a name="description"></a>Description



| Entrée | Valeur |
|----------------|----------------------------|
| Description    | Décrit la classe d’événements. |
| Access         | Lecture seule                   |
| Type           | String                     |
| Valeur par défaut        | ""                         |
| Système minimal | Windows XP                 |



 

### <a name="isprivatecomponent"></a>IsPrivateComponent



| Entrée | Valeur |
|----------------|---------------------------------------------------------|
| Description    | Indique si le composant de la classe d’événements est privé. |
| Access         | Lecture seule                                                |
| Type           | Bool                                                    |
| Default        | False                                                   |
| Système minimal | Windows XP                                              |



 

### <a name="progid"></a>ProgID



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Nom convivial utilisé pour identifier la classe d’événements. Cette propriété est retournée lorsque la méthode de propriété [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection. |
| Access         | Lecture seule                                                                                                                                                                            |
| Type           | String                                                                                                                                                                              |
| Valeur par défaut        | ""                                                                                                                                                                                  |
| Système minimal | Windows XP                                                                                                                                                                          |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
