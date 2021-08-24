---
description: Pour permettre à votre application de fonctionner avec le gestionnaire de synchronisation, vous devez implémenter un objet COM (Component Object Model) pour gérer les notifications de synchronisation que vous recevez de SyncMgr.
title: Utilisation du gestionnaire de synchronisation à partir d’un programme
ms.topic: article
ms.date: 05/31/2018
ms.assetid: bf18d493-0fe7-46e7-9686-f7ee75b3039b
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 11e959399624d30e1e6d7ce87fb8bb247de7c9c420ef9b2427c7b9bdeb00e7f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709379"
---
# <a name="using-synchronization-manager-from-a-program"></a>Utilisation du gestionnaire de synchronisation à partir d’un programme

Pour permettre à votre application de fonctionner avec le gestionnaire de synchronisation, vous devez implémenter un objet COM (Component Object Model) pour gérer les notifications de synchronisation que vous recevez de SyncMgr. Le gestionnaire de votre application effectue la synchronisation pour les éléments que vous gérez. Inclus dans votre gestionnaire, vous devez implémenter l’interface [**ISyncMgrSynchronize**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) . En outre, vous devez fournir un objet énumérateur et [**ISyncMgrEnumItems**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems) pour tous les éléments séparés que votre application peut synchroniser.

SyncMgr implémente [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) et [**ISyncMgrSynchronizeInvoke**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronizeinvoke).

SyncMgr appelle les méthodes de votre [**ISyncMgrSynchronize**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) pour obtenir des informations sur les éléments que votre application gère et les informations sur le gestionnaire que vous fournissez pour synchroniser ces éléments.

Au moment de l’exécution, le processus de synchronisation suit ces étapes.

1.  SyncMgr informe votre application qu’il est temps que la synchronisation se produise pour l’un des éléments que votre application gère en appelant votre méthode [**ISyncMgrSynchronize :: Initialize**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-initialize) .
2.  SyncMgr appelle [**ISyncMgrSynchronize :: EnumSyncMgrItems**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-enumsyncmgritems) pour obtenir l’interface [**ISyncMgrEnumItems**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems) pour les éléments gérés par votre application.
3.  SyncMgr appelle [**ISyncMgrSynchronize :: SetProgressCallback**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-setprogresscallback) pour fournir votre gestionnaire avec le pointeur d’interface pour l’interface [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) . Votre gestionnaire utilise cette interface pour rappeler le SyncMgr pendant la synchronisation.
4.  SyncMgr appelle ensuite votre méthode [**ISyncMgrSynchronize ::P repareforsync**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync) pour permettre à votre gestionnaire d’afficher n’importe quel élément d’interface utilisateur nécessaire avant le début de la synchronisation. Par exemple, une application de messagerie peut afficher une boîte de dialogue d’ouverture de session utilisateur.
5.  Votre gestionnaire appelle [**ISyncMgrSynchronizeCallback :: EnableModeless**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-enablemodeless) avant et après l’affichage des éléments d’interface utilisateur. Votre gestionnaire appelle [**ISyncMgrSynchronizeCallback ::P repareforsynccompleted**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-prepareforsynccompleted) lorsque vous avez terminé.
6.  SyncMgr appelle votre méthode [**ISyncMgrSynchronize :: Synchronize**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-synchronize) pour démarrer la synchronisation.

Pendant le processus de synchronisation, SyncMgr continue d’appeler des méthodes dans votre interface [**ISyncMgrSynchronize**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) . Il peut envoyer vos erreurs de gestionnaire, la progression et les notifications. Il peut également énumérer les éléments que votre application gère ou autoriser votre application à afficher les propriétés des éléments.

Votre gestionnaire appelle des méthodes dans [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) pour déterminer si un élément doit être ignoré, pour consigner les erreurs et pour poster des informations de progression pendant le processus de synchronisation.

Pour plus d’informations, consultez les pages de référence associées pour les interfaces impliquées.

Une fois la synchronisation terminée, votre gestionnaire appelle [**ISyncMgrSynchronizeCallback :: SynchronizeCompleted**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-synchronizecompleted).

 

 



