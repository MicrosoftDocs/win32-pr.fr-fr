---
title: Synchronisation des appels
description: Synchronisation des appels
ms.assetid: e74407ef-f500-4d13-aef4-ca6bb37d5858
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec9254aceaaa8a6fa26d56d4a86987cc955b90dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232740"
---
# <a name="call-synchronization"></a>Synchronisation des appels

Les applications COM doivent être en mesure de traiter correctement les entrées utilisateur lors du traitement d’un ou de plusieurs appels de COM ou du système d’exploitation. COM assure la synchronisation des appels uniquement pour les cloisonnements à thread unique. Les Apartments (cloisonnés) multithread ne reçoivent pas d’appels lors de l’appel (sur le même thread). Les cloisonnements multithread ne peuvent pas effectuer d’appels synchronisés d’entrée. Les appels asynchrones sont convertis en appels synchrones dans des Apartments multithread. Le filtre de messages n’est appelé pour aucun thread dans un cloisonnement multithread. Pour plus d’informations sur les problèmes liés aux threads, consultez [processus, threads et Apartments](processes--threads--and-apartments.md).

Les appels COM entre les processus se répartissent en trois catégories, comme suit :

<dl> <dt>

<span id="Synchronous_calls"></span><span id="synchronous_calls"></span><span id="SYNCHRONOUS_CALLS"></span>*Appels synchrones*
</dt> <dd>

La majeure partie de la communication qui a lieu dans COM est synchrone. Lors de l’exécution d’appels synchrones, l’appelant attend la réponse avant de continuer et peut recevoir des messages entrants en attente. COM entre une boucle modale pour attendre la réponse, recevoir et distribuer d’autres messages de manière contrôlée.

</dd> <dt>

<span id="Asynchronous_notifications"></span><span id="asynchronous_notifications"></span><span id="ASYNCHRONOUS_NOTIFICATIONS"></span>*Notifications asynchrones*
</dt> <dd>

Lors de l’envoi de notifications asynchrones, l’appelant n’attend pas la réponse. COM utilise [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) ou des événements de haut niveau pour envoyer des notifications asynchrones, en fonction de la plateforme. COM définit cinq méthodes asynchrones de [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink):

-   [**N''est**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange)
-   [**OnViewChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange)
-   [**OnRename**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onrename)
-   [**OnSave**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onsave)
-   [**OnClose**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onclose)

> [!Note]  
> Alors que COM traite un appel asynchrone, les appels synchrones ne peuvent pas être effectués. Par exemple, l’implémentation d’une application conteneur de [**OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange) ne peut pas contenir un appel à [**IPersistStorage :: Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststorage-save). Ces appels sont les seuls appels asynchrones pris en charge par COM. Il n’existe aucun moyen de créer une interface personnalisée qui est asynchrone à ce stade.

 

</dd> <dt>

<span id="Input-synchronized_calls"></span><span id="input-synchronized_calls"></span><span id="INPUT-SYNCHRONIZED_CALLS"></span>*Appels synchronisés en entrée*
</dt> <dd>

Lors de l’exécution d’appels synchronisés en entrée, l’objet appelé doit terminer l’appel avant de générer le contrôle. Cela permet de s’assurer que la gestion du focus fonctionne correctement et que les données entrées par l’utilisateur sont traitées de manière appropriée. Ces appels sont effectués par COM via la fonction [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) , sans entrer de boucle modale. Lors du traitement d’un appel synchronisé en entrée, l’objet appelé ne doit pas appeler une fonction ou méthode (y compris des méthodes synchrones) qui peut donner le contrôle. Les méthodes suivantes sont synchronisées entre les entrées

-   [**IOleWindow::GetWindow**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-getwindow)
-   [**IOleInPlaceActiveObject :: OnFrameWindowActivate**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-onframewindowactivate)
-   [**IOleInPlaceActiveObject :: OnDocWindowActivate**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-ondocwindowactivate)
-   [**IOleInPlaceActiveObject :: ResizeBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-resizeborder)
-   [**IOleInPlaceUIWindow::GetBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)
-   [**IOleInPlaceUIWindow::RequestBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)
-   [**IOleInPlaceUIWindow::SetBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)
-   [**IOleInPlaceFrame :: SetMenu**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)
-   [**IOleInPlaceFrame :: SetStatusText**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)
-   [**IOleInPlaceObject::SetObjectRects**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-setobjectrects)

</dd> </dl>

Pour réduire les problèmes qui peuvent survenir à partir du traitement des messages asynchrones, la majorité des appels de méthode COM sont synchrones. Avec la communication synchrone, il n’est pas nécessaire de disposer d’un code spécial pour distribuer et gérer les messages entrants. Lorsqu’une application effectue un appel de méthode synchrone, COM entre une boucle d’attente modale qui gère les réponses requises et distribue les messages entrants aux applications susceptibles de les traiter.

COM gère les appels de méthode en assignant un identificateur appelé *ID de thread logique*. Une nouvelle est affectée lorsqu’un utilisateur sélectionne une commande de menu ou lorsque l’application lance une nouvelle opération COM. Les appels suivants liés à l’appel COM initial reçoivent le même ID de thread logique que l’appel initial.

 

 