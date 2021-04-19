---
description: Contient un objet pour chaque abonnement de la collection de composants parents.
ms.assetid: ec93d500-32bf-4e67-9eda-c1fe0349faa2
title: Collection SubscriptionsForComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriptionsForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: c8334aa54b56a9dccaa7aa0787d8c997baf0445e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514525"
---
# <a name="subscriptionsforcomponent-collection"></a>Collection SubscriptionsForComponent

Contient un objet pour chaque abonnement de la collection de [**composants**](components.md) parents.

Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membres

La collection **SubscriptionsForComponent** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

## <a name="related-collections"></a>Regroupements connexes

Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**PublisherProperties**](publisherproperties.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**SubscriberProperties**](subscriberproperties.md)

Vous pouvez accéder à cette collection à partir des regroupements suivants :

-   [**Composants**](components.md)

## <a name="properties"></a>Propriétés

Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :

-   [Description](#description)
-   [Enabled](#enabled)
-   [EventClassPartitionID](#eventclasspartitionid)
-   [EventCLSID](#eventclsid)
-   [FilterCriteria](#filtercriteria)
-   [Identifiant](#subscriptionsforcomponent-collection)
-   [InterfaceID](#interfaceid)
-   [MachineName](#machinename)
-   [MethodName](#methodname)
-   [Nom](#machinename)
-   [PerUser](#peruser)
-   [PublisherID](#publisherid)
-   [Mis en file d'attente.](#queued)
-   [SubscriberMoniker](#subscribermoniker)
-   [SubscriberPartitionID](#subscriberpartitionid)
-   [UserName](#username)

### <a name="description"></a>Description



| Entrée | Valeur |
|----------------|-------------------------------------|
| Description    | Description de l’abonnement. |
| Accès         | Lecture/écriture                           |
| Type           | String                              |
| Valeur par défaut        | ""                                  |
| Système minimal | Windows 2000                        |



 

### <a name="enabled"></a>activé



| Entrée | Valeur |
|----------------|----------------------------------------------------------|
| Description    | Indique si l’abonnement est actuellement activé. |
| Accès         | Lecture/écriture                                                |
| Type           | Bool                                                     |
| Default        | Vrai                                                     |
| Système minimal | Windows 2000                                             |



 

### <a name="eventclasspartitionid"></a>EventClassPartitionID



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Lors de l’abonnement à une classe d’événements, utilisé pour représenter le GUID de l’ID de partition contenant la classe d’événements. Quand vous vous abonnez à des classes d’événements, l’abonné a la possibilité de s’abonner à une classe d’événements dans la même partition ou dans une partition différente. |
| Accès         | Lecture/écriture                                                                                                                                                                                                                                          |
| Type           | String                                                                                                                                                                                                                                             |
| Valeur par défaut        | NULL                                                                                                                                                                                                                                               |
| Système minimal | Windows Server 2003                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a>EventCLSID



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------------------|
| Description    | CLSID de la classe d’événements. Vous pouvez indiquer un EventCLSID ou un PublisherID, mais pas les deux. |
| Accès         | WriteOnce                                                                                    |
| Type           | String                                                                                       |
| Valeur par défaut        | N/A                                                                                          |
| Système minimal | Windows 2000                                                                                 |



 

### <a name="filtercriteria"></a>FilterCriteria



| Entrée | Valeur |
|----------------|------------------------------------------------------------------------------------------------------------------|
| Description    | Chaîne indiquant les critères de filtre. Peut être un CLSID pour une classe [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) . |
| Accès         | Lecture/écriture                                                                                                        |
| Type           | String                                                                                                           |
| Valeur par défaut        | N/A                                                                                                              |
| Système minimal | Windows 2000                                                                                                     |



 

### <a name="id"></a>id



| Entrée | Valeur |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Identificateur de l’abonnement. Cette propriété est retournée lorsque la méthode de propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) est appelée sur un objet de cette collection. |
| Accès         | WriteOnce                                                                                                                                                        |
| Type           | String                                                                                                                                                           |
| Valeur par défaut        | <Generated>                                                                                                                                                |
| Système minimal | Windows 2000                                                                                                                                                     |



 

### <a name="interfaceid"></a>InterfaceID



| Entrée | Valeur |
|----------------|------------------------------------------|
| Description    | IID de l’interface à laquelle s’abonner. |
| Accès         | Lecture/écriture                                |
| Type           | String                                   |
| Valeur par défaut        | N/A                                      |
| Système minimal | Windows 2000                             |



 

### <a name="machinename"></a>MachineName



| Entrée | Valeur |
|----------------|---------------------------------------------------------------------------------|
| Description    | Nom de l’ordinateur distant pour les abonnements aux classes d’événements sur un ordinateur distant. |
| Accès         | Lecture/écriture                                                                       |
| Type           | String                                                                          |
| Valeur par défaut        | ""                                                                              |
| Système minimal | Windows 2000                                                                    |



 

### <a name="methodname"></a>MethodName



| Entrée | Valeur |
|----------------|----------------------------------------------|
| Description    | Méthode sur l’interface à laquelle s’abonner. |
| Accès         | Lecture/écriture                                    |
| Type           | String                                       |
| Valeur par défaut        | N/A                                          |
| Système minimal | Windows 2000                                 |



 

### <a name="name"></a>Nom



| Entrée | Valeur |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Nom de l’abonnement. Les espaces supplémentaires au début et à la fin de la chaîne sont supprimés. Cette propriété est retournée lorsque la méthode de propriété [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection. |
| Accès         | Lecture/écriture                                                                                                                                                                                                                          |
| Type           | String                                                                                                                                                                                                                             |
| Valeur par défaut        | « Nouvel abonnement »                                                                                                                                                                                                                 |
| Système minimal | Windows 2000                                                                                                                                                                                                                       |



 

### <a name="peruser"></a>PerUser



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------|
| Description    | Indique si l’abonnement s’applique uniquement à un utilisateur donné, nom d’utilisateur. |
| Accès         | Lecture/écriture                                                                   |
| Type           | Bool                                                                        |
| Default        | False                                                                       |
| Système minimal | Windows 2000                                                                |



 

### <a name="publisherid"></a>PublisherID



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| Description    | ID du serveur de publication. Vous pouvez indiquer un EventCLSID ou un PublisherID, mais pas les deux. |
| Accès         | WriteOnce                                                                               |
| Type           | String                                                                                  |
| Valeur par défaut        | ""                                                                                      |
| Système minimal | Windows 2000                                                                            |



 

### <a name="queued"></a>Mis en file d'attente.



| Entrée | Valeur |
|----------------|-----------------------------------------------|
| Description    | Indique si l’abonnement est mis en file d’attente. |
| Accès         | Lecture/écriture                                     |
| Type           | Bool                                          |
| Default        | False                                         |
| Système minimal | Windows 2000                                  |



 

### <a name="subscribermoniker"></a>SubscriberMoniker



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------------------------------|
| Description    | Moniker d’un abonné marqué comme mis en file d’attente. Une valeur par défaut est générée lorsque Queued est initialement défini sur true. |
| Accès         | Lecture/écriture                                                                                                       |
| Type           | String                                                                                                          |
| Valeur par défaut        | N/A                                                                                                             |
| Système minimal | Windows 2000                                                                                                    |



 

### <a name="subscriberpartitionid"></a>SubscriberPartitionID



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Lors de l’abonnement à une classe d’événements dans la même partition, utilisée pour représenter le GUID de l’ID de partition de l’abonné. Quand vous vous abonnez à des classes d’événements, l’abonné a la possibilité de s’abonner à une classe d’événements dans la même partition ou dans une partition différente. |
| Accès         | WriteOnce                                                                                                                                                                                                                                                       |
| Type           | String                                                                                                                                                                                                                                                          |
| Valeur par défaut        | <Generated>                                                                                                                                                                                                                                               |
| Système minimal | Windows Server 2003                                                                                                                                                                                                                                             |



 

### <a name="username"></a>UserName



| Entrée | Valeur |
|----------------|--------------------------------------------------------------------------|
| Description    | Nom de l’utilisateur auquel s’applique l’abonnement, lorsque PerUser a la valeur true. |
| Accès         | Lecture/écriture                                                                |
| Type           | String                                                                   |
| Valeur par défaut        | N/A                                                                      |
| Système minimal | Windows 2000                                                             |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
