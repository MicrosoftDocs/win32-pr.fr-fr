---
description: Les abonnements temporaires ne peuvent pas être définis à l’aide de l’outil d’administration Services de composants. Vous devez utiliser les interfaces d’administration COM+ pour créer ou mettre à jour un abonnement temporaire.
ms.assetid: 28d48d59-abb2-4682-ab54-60b6aa7b31b1
title: Inscription d’un abonnement temporaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f93b543a4602b0b4ed7ed4177133f3eb8f543a0db02750af8657ab36f310993
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990439"
---
# <a name="registering-a-transient-subscription"></a>Inscription d’un abonnement temporaire

Les abonnements temporaires demandent un événement pour un objet d’abonné spécifique qui existe déjà. Les abonnements temporaires sont stockés dans le catalogue COM+, mais l’abonnement est supprimé si le système d’événements ou le système d’exploitation est arrêté. Contrairement aux abonnements persistants, les abonnements temporaires sont liés à un objet particulier et sont stockés uniquement dans le système d’événements. En cas de problème avec le système d’exploitation ou le système d’exploitation, l’abonnement disparaît. Les abonnements temporaires peuvent être plus efficaces que les abonnements persistants, mais vous devez gérer leurs cycles de vie d’objet.

Les abonnements temporaires ne peuvent pas être définis à l’aide de l’outil d’administration Services de composants. Vous devez utiliser les interfaces d’administration COM+ pour créer ou mettre à jour un abonnement temporaire.

## <a name="visual-basic"></a>Visual Basic

La procédure suivante décrit comment créer un abonnement temporaire à l’aide de Microsoft Visual Basic :

1.  Spécifiez un abonnement transitoire en ajoutant une nouvelle entrée à la collection [**TransientSubscriptions**](transientsubscriptions.md) et en affectant à la propriété SubscriberInterface l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) de l’objet abonné. Les événements COM+ ne créent pas de nouvelle instance de l’objet d’abonné lors du déclenchement d’un événement, mais utilisent à la place l’instance que vous spécifiez. Les événements COM+ contiennent un décompte de références pour l’objet abonné jusqu’à ce que l’abonnement soit supprimé du système.
2.  Créez une application serveur COM+ (un .exe, un .dll ou un fichier. ocx) avec un objet qui implémente les interfaces ou les méthodes auxquelles vous voulez vous abonner.
3.  Créez votre abonnement temporaire en utilisant le code suivant, en passant le CLSID de l’objet de [classe d’événements](the-com--event-class-object.md) et l’instance de l’objet d’abonné. À l’aide de l’outil d’administration Services de composants, vous pouvez obtenir la propriété EventCLSID en cliquant avec le bouton droit sur le composant COM+, en sélectionnant **Propriétés**, puis en sélectionnant l’onglet **général** .

    ``` syntax
    Public Function CreateTransientSubscription( _
      ByVal clsid As String, ByVal objref As Object) As String 
        Dim oCOMAdminCatalog As COMAdmin.COMAdminCatalog
        Dim oTSCol As COMAdminCatalogCollection
        Dim oSubscription As ICatalogObject
        Dim objvar As Variant
        On Error GoTo CreateTransientSubscriptionError
        Set oCOMAdminCatalog = CreateObject("COMAdmin.COMAdminCatalog")
        'Gets the TransientSubscriptions collection
        Set oTSCol = oCOMAdminCatalog.GetCollection( _
          "TransientSubscriptions")
        Set oSubscription = oTSCol.Add
        Set objvar = objref
        oSubscription.Value("SubscriberInterface") = objref
        oSubscription.Value("EventCLSID") = clsid
        oSubscription.Value("Name") = "TransientSubscription"
        oTSCol.SaveChanges
        CreateTransientSubscription = oSubscription.Value("ID")
        Set oSubscription = Nothing
        Set oTSCol = Nothing
        Set oCOMAdminCatalog = Nothing
        Set objvar = Nothing
        Exit Function
    CreateTransientSubscriptionError:
        CreateTransientSubscription = ""
        Err.Raise Err.Number, "[CreateTransientSubscription]" & _
          Err.Source, Err.Description
    End Function
    ```

L’exemple suivant illustre l’appel de la fonction CreateTransientSubscription pour s’abonner à une interface appelée IStockTicker, qui a une méthode appelée UpdateStock.

1.  Créez une classe d’événements qui prend en charge l’interface IStockTicker, qui a une méthode, UpdateStock.
2.  Dans votre projet d’abonné, ajoutez une classe qui implémente l’interface IStockTicker.
3.  Lorsque vous souhaitez vous abonner, exécutez le code suivant :

    ``` syntax
    Dim oMyTicker As Object
    Dim sSubscriptionID As String
    Set oMyTicker = CreateObject("TheProject.CMyTicker")
    sSubscriptionID = CreateTransientSubscription( _
      "{..CLSID for the Event Class..}", oMyTicker)
    ```

La fonction CreateTransientSubscription retourne une chaîne, qui est un GUID qui peut être utilisé comme un handle ou un cookie pour révoquer l’abonnement ultérieurement. Pour supprimer l’abonnement, appelez la méthode [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de [**COMAdminCatalogCollection**](comadmincatalogcollection.md) sur la collection [**TransientSubscriptions**](transientsubscriptions.md) , en transmettant l’index correspondant à l’abonnement avec le GUID précédemment reçu.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription d’un abonnement](registering-a-subscription.md)
</dt> </dl>

 

 
