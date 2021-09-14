---
description: Après avoir créé le consommateur d’événements logiques et le filtre d’événements, vous devez les lier, ce qui permet d’inscrire le consommateur logique pour recevoir une notification concernant les événements spécifiés par le filtre.
ms.assetid: 2fc3d781-2b93-4e9e-90a1-1b975ab40a01
ms.tgt_platform: multiple
title: Liaison d’un filtre d’événements à un consommateur logique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99f44c4b64b98877231b73543d8753c765c3219
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013068"
---
# <a name="binding-an-event-filter-with-a-logical-consumer"></a>Liaison d’un filtre d’événements à un consommateur logique

Après avoir créé le consommateur d’événements logiques et le filtre d’événements, vous devez les lier, ce qui permet d’inscrire le consommateur logique pour recevoir une notification concernant les événements spécifiés par le filtre.

La procédure suivante décrit comment lier un filtre d’événement à un consommateur logique.

**Pour lier un filtre d’événement à un consommateur logique**

1.  Créez une instance de la classe système [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) dans l’espace de stockage WMI.

    La classe [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) est une classe d’association qui lie l’instance de filtre d’événements et l’instance de consommateur logique à l’aide des propriétés de référence de **filtre** et de **consommateur** . Pour plus d’informations, consultez [déclaration d’une classe d’association](declaring-an-association-class.md).

2.  Définissez la propriété **Filter** sur l’instance de votre filtre.
3.  Affectez à la propriété de **consommateur** l’instance de votre consommateur logique.
4.  Définissez la propriété **DeliverSynchronously** pour déterminer le type de remise souhaité.

    La propriété **DeliverSynchronously** détermine quand WMI remet les notifications d’événements de façon synchrone ou asynchrone. L’affectation de la **valeur true** à cette propriété demande une remise synchrone. Utilisez la remise synchrone uniquement lorsque le consommateur permanent peut traiter des événements dans environ 100 microsecondes.

    > [!Note]  
    > Étant donné que le rappel au récepteur peut ne pas être retourné au même niveau d’authentification que celui requis par le client, il est recommandé d’utiliser le mode semi-synchrone au lieu de la communication asynchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

     

5.  Lors de l’annulation de l’inscription de votre consommateur d’événements logiques, veillez à supprimer l’instance [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) .

    Chaque instance [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) représente une inscription pour une notification d’événement spécifique. Lorsque vous supprimez une liaison, WMI désactive l’inscription. Vous devrez peut-être supprimer les instances de consommateur logique et de filtre d’événements pour désactiver l’inscription, en fonction de l’implémentation.

L’exemple de code suivant montre une instance [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) qui associe une instance d’une classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) à un filtre d’événement spécifique (l’instance du consommateur d’événements a été créée dans la rubrique [création d’un consommateur logique](creating-a-logical-consumer.md) et le filtre d’événement a été créé dans la rubrique [création d’un filtre d’événements](creating-an-event-filter.md) ).

``` syntax
instance of __FilterToConsumerBinding
{
    Filter = $FILTER;
    Consumer = $CONSUMER;
    DeliverSynchronously=FALSE;

    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

Deux consommateurs, [**ActiveScriptEventConsumer**](activescripteventconsumer.md) et [**CommandLineEventConsumer**](commandlineeventconsumer.md), ne fonctionneront pas, sauf si leur créateur est membre du groupe Administrateurs local.

**:** Lorsqu’un administrateur crée un abonnement, son SID n’est pas utilisé pour la propriété **CreatorSID** , mais le SID du groupe Administrateurs local est utilisé à la place. Par conséquent, les instances peuvent être créées par des administrateurs différents et l’abonnement fonctionnera toujours. Pour plus d’informations, consultez [réception d’événements en toute sécurité](receiving-events-securely.md).

lorsqu’un filtre est lié à un consommateur logique, l’événement est enregistré par le [suivi d’événements](/windows/desktop/ETW/event-tracing-portal) pour Windows (ETW). Pour plus d’informations, consultez suivi de l' [activité WMI](tracing-wmi-activity.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Réception d’événements à tout moment](receiving-events-at-all-times.md)
</dt> </dl>

 

 
