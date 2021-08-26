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
ms.openlocfilehash: 68ccdd222f4fe205e58adf5195df694ec1256804
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879929"
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



| Entrée | Valeur |
|----------------|-------------------------------------|
| Description    | Description de l’abonnement. |
| Access         | Lecture/écriture                           |
| Type           | Chaîne                              |
| Valeur par défaut        | ""                                  |
| Système minimal | Windows 2000                        |



 

### <a name="enabled"></a>activé



| Entrée | Valeur |
|----------------|----------------------------------------------------------|
| Description    | Indique si l’abonnement est actuellement activé. |
| Access         | Lecture/écriture                                                |
| Type           | Bool                                                     |
| Default        | Vrai                                                     |
| Système minimal | Windows 2000                                             |



 

### <a name="eventclasspartitionid"></a>EventClassPartitionID



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Lors de l’abonnement à une classe d’événements, utilisé pour représenter le GUID de l’ID de partition contenant la classe d’événements. Quand vous vous abonnez à des classes d’événements, l’abonné a la possibilité de s’abonner à une classe d’événements dans la même partition ou dans une partition différente. |
| Access         | Lecture/écriture                                                                                                                                                                                                                                          |
| Type           | Chaîne                                                                                                                                                                                                                                             |
| Valeur par défaut        | NULL                                                                                                                                                                                                                                               |
| Système minimal | Windows Server 2003                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a>EventCLSID



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------------------|
| Description    | CLSID de la classe d’événements. Vous pouvez indiquer un EventCLSID ou un PublisherID, mais pas les deux. |
| Access         | WriteOnce                                                                                    |
| Type           | Chaîne                                                                                       |
| Valeur par défaut        | N/A                                                                                          |
| Système minimal | Windows 2000                                                                                 |



 

### <a name="filtercriteria"></a>FilterCriteria



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| Description    | Chaîne qui indique les critères de filtre. Peut être un CLSID pour une classe [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) . |
| Access         | Lecture/écriture                                                                                                            |
| Type           | Chaîne                                                                                                               |
| Valeur par défaut        | N/A                                                                                                                  |
| Système minimal | Windows 2000                                                                                                         |



 

### <a name="id"></a>id



| Entrée | Valeur |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Identificateur de l’abonnement. Cette propriété est retournée lorsque la méthode de propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) est appelée sur un objet de cette collection. |
| Access         | WriteOnce                                                                                                                                                        |
| Type           | Chaîne                                                                                                                                                           |
| Valeur par défaut        | &lt;Généré&gt;                                                                                                                                                |
| Système minimal | Windows 2000                                                                                                                                                     |



 

### <a name="interfaceid"></a>InterfaceID



| Entrée | Valeur |
|----------------|----------------------------------|
| Description    | IID pour lequel l’interface est abonnée. |
| Access         | WriteOnce                        |
| Type           | Chaîne                           |
| Valeur par défaut        | N/A                              |
| Système minimal | Windows 2000                     |



 

### <a name="methodname"></a>MethodName



| Entrée | Valeur |
|----------------|----------------------------------------------|
| Description    | Méthode sur l’interface à laquelle s’abonner. |
| Access         | Lecture/écriture                                    |
| Type           | Chaîne                                       |
| Valeur par défaut        | N/A                                          |
| Système minimal | Windows 2000                                 |



 

### <a name="name"></a>Nom



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Nom de l’abonnement. Les espaces supplémentaires au début et à la fin de la chaîne sont supprimés. Cette propriété est retournée lorsque la méthode de propriété [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection. |
| Access         | Lecture/écriture                                                                                                                                                                                                                              |
| Type           | Chaîne                                                                                                                                                                                                                                 |
| Valeur par défaut        | « Nouvel abonnement »                                                                                                                                                                                                                     |
| Système minimal | Windows 2000                                                                                                                                                                                                                           |



 

### <a name="peruser"></a>PerUser



| Entrée | Valeur |
|----------------|---------------------------------------------------------------------------------------------------------|
| Description    | Indique si l’abonnement s’applique uniquement à un utilisateur donné, représenté par la propriété UserName. |
| Access         | Lecture/écriture                                                                                               |
| Type           | Bool                                                                                                    |
| Default        | False                                                                                                   |
| Système minimal | Windows 2000                                                                                            |



 

### <a name="publisherid"></a>PublisherID



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------------------|
| Description    | ID du serveur de publication. Vous pouvez indiquer un EventCLSID ou un PublisherID, mais pas les deux. |
| Access         | WriteOnce                                                                           |
| Type           | Chaîne                                                                              |
| Valeur par défaut        | ""                                                                                  |
| Système minimal | Windows 2000                                                                        |



 

### <a name="subscriberinterface"></a>SubscriberInterface



| Entrée | Valeur |
|----------------|------------------------------------------|
| Description    | Pointeur vers l’interface de l’abonné. |
| Access         | Lecture/écriture                                |
| Type           | Variante                                  |
| Default        | N/A                                      |
| Système minimal | Windows 2000                             |



 

### <a name="subscriberpartitionid"></a>SubscriberPartitionID



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Lors de l’abonnement à une classe d’événements dans la même partition, utilisée pour représenter le GUID de l’ID de partition de l’abonné. Quand vous vous abonnez à des classes d’événements, l’abonné a la possibilité de s’abonner à une classe d’événements dans la même partition ou dans une partition différente. |
| Access         | WriteOnce                                                                                                                                                                                                                                                       |
| Type           | Chaîne                                                                                                                                                                                                                                                          |
| Valeur par défaut        | &lt;Généré&gt;                                                                                                                                                                                                                                               |
| Système minimal | Windows Server 2003                                                                                                                                                                                                                                             |



 

### <a name="username"></a>UserName



| Entrée | Valeur |
|----------------|-------------------------------------------------------------------------|
| Description    | Nom de l’utilisateur auquel s’applique l’abonnement lorsque PerUser a la valeur true. |
| Access         | Lecture/écriture                                                               |
| Type           | Chaîne                                                                  |
| Valeur par défaut        | N/A                                                                     |
| Système minimal | Windows 2000                                                            |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
