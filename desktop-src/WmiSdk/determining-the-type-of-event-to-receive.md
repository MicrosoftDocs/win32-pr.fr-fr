---
description: 'Avant de vous inscrire pour recevoir un événement, vous devez déterminer les types d’événements à recevoir : intrinsèque ou extrinsèque.'
ms.assetid: 46cdfcfa-42c6-4169-bc4d-725867224889
ms.tgt_platform: multiple
title: Détermination du type d’événement à recevoir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 477f3d10536e5b0622e1e64b6cec9abdf4183c7d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237096"
---
# <a name="determining-the-type-of-event-to-receive"></a>Détermination du type d’événement à recevoir

Avant de vous inscrire pour recevoir un événement, vous devez déterminer les types d’événements à recevoir : [intrinsèque](#intrinsic-events) ou [extrinsèque](#extrinsic-events). Pour plus d’informations sur la réception d’événements, consultez [réception d’un événement WMI](receiving-a-wmi-event.md). Pour plus d’informations sur la façon de fournir des événements, consultez [développement d’un fournisseur WMI](developing-a-wmi-provider.md) et [écriture d’un fournisseur d’événements](writing-an-event-provider.md). Pour plus d’informations sur les problèmes de sécurité liés à la réception et à la fourniture d’événements, consultez [sécurisation des événements WMI.](securing-wmi-events.md)

## <a name="intrinsic-events"></a>Événements intrinsèques

Un événement intrinsèque est un événement qui se produit en réponse à une modification dans le modèle de données WMI standard. Chaque classe d'événement intrinsèque représente un type spécifique de modification et se produit lorsque WMI ou un fournisseur crée, supprime ou modifie un espace de noms, une classe ou une instance de classe. Par exemple, la création d’une instance de [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) se traduirait par une instance [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) .

WMI crée des événements intrinsèques pour les objets stockés dans l’espace de stockage WMI. Un fournisseur génère des événements intrinsèques pour les classes dynamiques, mais WMI peut créer une instance pour une classe dynamique si aucun fournisseur n’est disponible. WMI utilise l’interrogation pour détecter les modifications. Le tableau suivant répertorie les classes système que WMI utilise pour signaler des événements intrinsèques.



| Classe système                                                           | Description                                                                                                                                                                                             |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_\_ClassCreationEvent**](--classcreationevent.md)                 | Avertit un consommateur lorsqu’une classe est créée.                                                                                                                                                            |
| [**\_\_ClassDeletionEvent**](--classdeletionevent.md)                 | Avertit un consommateur lorsqu’une classe est supprimée.                                                                                                                                                            |
| [**\_\_ClassModificationEvent**](--classmodificationevent.md)         | Avertit un consommateur lorsqu’une classe est modifiée.                                                                                                                                                           |
| [**\_\_InstanceCreationEvent**](--instancecreationevent.md)           | Avertit un consommateur lorsqu’une instance de classe est créée.                                                                                                                                                   |
| [**\_\_InstanceOperationEvent**](--instanceoperationevent.md)         | Avertit un consommateur lorsqu’un événement d’instance se produit, par exemple la création, la suppression ou la modification de l’instance. Vous pouvez utiliser cette classe dans les requêtes pour récupérer tous les événements de type associés à une instance. |
| [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md)           | Avertit un consommateur lorsqu’une instance est supprimée.                                                                                                                                                        |
| [**\_\_InstanceModificationEvent**](--instancemodificationevent.md)   | Avertit un consommateur lorsqu’une instance est modifiée.                                                                                                                                                       |
| [**\_\_NamespaceCreationEvent**](--namespacecreationevent.md)         | Avertit un consommateur lorsqu’un espace de noms est créé.                                                                                                                                                        |
| [**\_\_NamespaceDeletionEvent**](--namespacedeletionevent.md)         | Avertit un consommateur lorsqu’un espace de noms est supprimé.                                                                                                                                                        |
| [**\_\_NamespaceModificationEvent**](--namespacemodificationevent.md) | Avertit un consommateur lorsqu’un espace de noms est modifié.                                                                                                                                                       |
| [**\_\_ConsumerFailureEvent**](--consumerfailureevent.md)             | Avertit un consommateur lorsqu’un autre événement est abandonné en raison d’un échec sur la partie d’un consommateur d’événements.                                                                                                 |
| [**\_\_EventDroppedEvent**](--eventdroppedevent.md)                   | Avertit un consommateur lorsqu’un autre événement est supprimé au lieu d’être remis au consommateur d’événements demandeur.                                                                                       |
| [**\_\_EventQueueOverflowEvent**](--eventqueueoverflowevent.md)       | Avertit un consommateur lorsqu’un événement est abandonné à la suite d’un dépassement de capacité de la file d’attente de remise.                                                                                                                  |
| [**\_\_MethodInvocationEvent**](--methodinvocationevent.md)           | Avertit un consommateur lorsqu’un événement d’appel de méthode se produit.                                                                                                                                                    |



 

## <a name="extrinsic-events"></a>Événements extrinsèques

Un événement extrinsèque est une occurrence prédéfinie qui ne peut pas être liée directement à des modifications dans le modèle de données WMI. Par conséquent, WMI permet à un fournisseur d’événements de définir une classe d’événements qui décrit l’événement. Par exemple, un événement qui décrit un ordinateur qui bascule en mode veille est un événement extrinsèque. Un fournisseur dérive un événement extrinsèque de la classe système [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) , qui est une sous-classe de la classe de système d' [**\_ \_ événements**](--event.md) . Le [Registre système](/previous-versions/windows/desktop/regprov/system-registry-provider) et les fournisseurs [SNMP](snmp-provider.md) définissent des classes d’événements extrinsèques, telles que **RegistryKeyChangeEvent**, qui avertissent un consommateur lorsqu’une clé de Registre est modifiée. Pour plus d’informations, consultez [inscription aux événements de Registre système](registering-for-system-registry-events.md) et [écriture d’un fournisseur d’événements](writing-an-event-provider.md).

Dans l’exemple suivant, un fournisseur d’événements signale des violations de sécurité à un ou plusieurs bâtiments. La classe suivante peut être définie pour l’événement extrinsèque représentant une violation de sécurité.

``` syntax
class SecurityViolationEvent : __ExtrinsicEvent
{
   string Building;           // building where violation occurred
   sint32 EntranceNumber;     // entrance where violation occurred
   datetime TimeOfDetection;  // date and time of violation
}
```

Pour recevoir les notifications de violation de sécurité, un consommateur s’inscrit pour le type d’événement SecurityViolationEvent. Sauf indication contraire, un consommateur reçoit une notification de toutes les violations de sécurité pendant toutes les périodes de temps et dans tous les bâtiments. La classe d’événements contient également des informations que les consommateurs peuvent utiliser pour demander des événements plus spécifiques.

Dans l’exemple suivant, la requête inscrit le consommateur pour les événements de violation de sécurité dans la génération 24 uniquement.

`SELECT * FROM SecurityViolationEvent WHERE Building = 24;`

 

 
