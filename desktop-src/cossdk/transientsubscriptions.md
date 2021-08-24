---
description: Contient un objet pour chaque abonnement temporaire. Les abonnements temporaires peuvent être créés à la volée pour les instances d’objets en cours d’exécution, et ils disparaissent quand l’objet est détruit.
ms.assetid: beee291c-e03f-4ee0-b1f2-99dcf113c46e
title: Collection TransientSubscriptions
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientSubscriptions
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5053a4fd488ed38a637b4296f94caf20887f3ed924ae6d11b8f6a242669eccad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853929"
---
# <a name="transientsubscriptions-collection"></a>Collection TransientSubscriptions

Contient un objet pour chaque abonnement temporaire. Les abonnements temporaires peuvent être créés à la volée pour les instances d’objets en cours d’exécution, et ils disparaissent quand l’objet est détruit.

Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membres

La collection **TransientSubscriptions** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

## <a name="related-collections"></a>Regroupements connexes

Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**TransientPublisherProperties**](transientpublisherproperties.md)
-   [**TransientSubscriberProperties**](transientsubscriberproperties.md)

Vous pouvez accéder à cette collection à partir des regroupements suivants :

-   [**Causes**](root.md)

## <a name="properties"></a>Propriétés

Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :

-   [Description](#description)
-   [Activé](#enabled)
-   [EventClassPartitionID](#eventclasspartitionid)
-   [EventCLSID](#eventclsid)
-   [FilterCriteria](#filtercriteria)
-   [Identifiant](#transientsubscriptions-collection)
-   [InterfaceID](#interfaceid)
-   [MethodName](#methodname)
-   [Nom](#methodname)
-   [PerUser](#peruser)
-   [PublisherID](#publisherid)
-   [SubscriberInterface](#subscriberinterface)
-   [SubscriberPartitionID](#subscriberpartitionid)
-   [UserName](#username)

### <a name="description"></a>Description



| Entrée | Value |
|----------------|-------------------------------------|
| Description    | Description de l’abonnement. |
| Accès         | Lecture/écriture                           |
| Type           | String                              |
| Valeur par défaut        | ""                                  |
| Système minimal | Windows 2000                        |



 

### <a name="enabled"></a>activé



| Entrée | Value |
|----------------|----------------------------------------------------------|
| Description    | Indique si l’abonnement est actuellement activé. |
| Accès         | Lecture/écriture                                                |
| Type           | Bool                                                     |
| Par défaut        | Vrai                                                     |
| Système minimal | Windows 2000                                             |



 

### <a name="eventclasspartitionid"></a>EventClassPartitionID



| Entrée | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Lors de l’abonnement à une classe d’événements, utilisé pour représenter le GUID de l’ID de partition contenant la classe d’événements. Quand vous vous abonnez à des classes d’événements, l’abonné a la possibilité de s’abonner à une classe d’événements dans la même partition ou dans une partition différente. |
| Accès         | Lecture/écriture                                                                                                                                                                                                                                          |
| Type           | String                                                                                                                                                                                                                                             |
| Valeur par défaut        | NULL                                                                                                                                                                                                                                               |
| Système minimal | Windows Server 2003                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a>EventCLSID



| Entrée | Value |
|----------------|----------------------------------------------------------------------------------------------|
| Description    | CLSID de la classe d’événements. Vous pouvez indiquer un EventCLSID ou un PublisherID, mais pas les deux. |
| Accès         | WriteOnce                                                                                    |
| Type           | String                                                                                       |
| Valeur par défaut        | N/A                                                                                          |
| Système minimal | Windows 2000                                                                                 |



 

### <a name="filtercriteria"></a>FilterCriteria



| Entrée | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| Description    | Chaîne qui indique les critères de filtre. Peut être un CLSID pour une classe [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) . |
| Accès         | Lecture/écriture                                                                                                            |
| Type           | String                                                                                                               |
| Valeur par défaut        | N/A                                                                                                                  |
| Système minimal | Windows 2000                                                                                                         |



 

### <a name="id"></a>ID



| Entrée | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Identificateur de l’abonnement. Cette propriété est retournée lorsque la méthode de propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) est appelée sur un objet de cette collection. |
| Accès         | WriteOnce                                                                                                                                                        |
| Type           | String                                                                                                                                                           |
| Valeur par défaut        | <Generated>                                                                                                                                                |
| Système minimal | Windows 2000                                                                                                                                                     |



 

### <a name="interfaceid"></a>InterfaceID



| Entrée | Value |
|----------------|----------------------------------|
| Description    | IID pour lequel l’interface est abonnée. |
| Accès         | WriteOnce                        |
| Type           | String                           |
| Valeur par défaut        | N/A                              |
| Système minimal | Windows 2000                     |



 

### <a name="methodname"></a>MethodName



| Entrée | Value |
|----------------|----------------------------------------------|
| Description    | Méthode sur l’interface à laquelle s’abonner. |
| Accès         | Lecture/écriture                                    |
| Type           | String                                       |
| Valeur par défaut        | N/A                                          |
| Système minimal | Windows 2000                                 |



 

### <a name="name"></a>Name



| Entrée | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Nom de l’abonnement. Les espaces supplémentaires au début et à la fin de la chaîne sont supprimés. Cette propriété est retournée lorsque la méthode de propriété [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection. |
| Accès         | Lecture/écriture                                                                                                                                                                                                                              |
| Type           | String                                                                                                                                                                                                                                 |
| Valeur par défaut        | « Nouvel abonnement »                                                                                                                                                                                                                     |
| Système minimal | Windows 2000                                                                                                                                                                                                                           |



 

### <a name="peruser"></a>PerUser



| Entrée | Value |
|----------------|---------------------------------------------------------------------------------------------------------|
| Description    | Indique si l’abonnement s’applique uniquement à un utilisateur donné, représenté par la propriété UserName. |
| Accès         | Lecture/écriture                                                                                               |
| Type           | Bool                                                                                                    |
| Default        | False                                                                                                   |
| Système minimal | Windows 2000                                                                                            |



 

### <a name="publisherid"></a>PublisherID



| Entrée | Value |
|----------------|-------------------------------------------------------------------------------------|
| Description    | ID du serveur de publication. Vous pouvez indiquer un EventCLSID ou un PublisherID, mais pas les deux. |
| Accès         | WriteOnce                                                                           |
| Type           | String                                                                              |
| Valeur par défaut        | ""                                                                                  |
| Système minimal | Windows 2000                                                                        |



 

### <a name="subscriberinterface"></a>SubscriberInterface



| Entrée | Value |
|----------------|------------------------------------------|
| Description    | Pointeur vers l’interface de l’abonné. |
| Accès         | Lecture/écriture                                |
| Type           | Variante                                  |
| Par défaut        | N/A                                      |
| Système minimal | Windows 2000                             |



 

### <a name="subscriberpartitionid"></a>SubscriberPartitionID



| Entrée | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Lors de l’abonnement à une classe d’événements dans la même partition, utilisée pour représenter le GUID de l’ID de partition de l’abonné. Quand vous vous abonnez à des classes d’événements, l’abonné a la possibilité de s’abonner à une classe d’événements dans la même partition ou dans une partition différente. |
| Accès         | WriteOnce                                                                                                                                                                                                                                                       |
| Type           | String                                                                                                                                                                                                                                                          |
| Valeur par défaut        | <Generated>                                                                                                                                                                                                                                               |
| Système minimal | Windows Server 2003                                                                                                                                                                                                                                             |



 

### <a name="username"></a>UserName



| Entrée | Value |
|----------------|-------------------------------------------------------------------------|
| Description    | Nom de l’utilisateur auquel s’applique l’abonnement lorsque PerUser a la valeur true. |
| Accès         | Lecture/écriture                                                               |
| Type           | String                                                                  |
| Valeur par défaut        | N/A                                                                     |
| Système minimal | Windows 2000                                                            |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
