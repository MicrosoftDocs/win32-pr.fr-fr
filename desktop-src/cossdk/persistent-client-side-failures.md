---
description: Échecs de Client-Side persistant
ms.assetid: f991db71-8319-414d-8a25-2d02bc7c8b51
title: Échecs de Client-Side persistant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e832ec8339c33263600a1657b8d29ef2d2aecf4ceb3e000666f9db5776b3ac13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305772"
---
# <a name="persistent-client-side-failures"></a>Échecs de Client-Side persistant

Dans certains cas, [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) pouvez déplacer un message vers la file d’attente de destination. Par exemple, si les contrôles d’accès à la file d’attente n’autorisent pas le déplacement du message du client vers le serveur, le message incriminé est déplacé vers la file d’attente de lettres mortes côté client. Dans ce cas, le service de composants en file d’attente COM+ autorise l’Association d’une classe d’exception à un composant. Pour associer la classe d’exception au composant, utilisez l’onglet **avancé** de la page Propriétés du composant de l’outil d’administration Services de composants. Vous pouvez également associer la classe d’exception par programme, à l’aide de l’attribut de composant de catalogue ExceptionClass des fonctions d’administration COM+.

La classe d’exception est définie en tant que ProgID ou CLSID d’un composant qui implémente [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol). Le service Queued Components a un moniteur de file d’attente de lettres mortes qui analyse la file d’attente de lettres mortes Xact. S’il y a un message dans la file d’attente, le moniteur de file d’attente de lettres mortes instancie le gestionnaire d’exceptions associé au composant cible et appelle [**IPlaybackControl :: FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry), ce qui indique qu’il y a eu une erreur côté client irrécupérable.

En plus de [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol), le gestionnaire d’exceptions doit implémenter le même jeu d’interfaces que le composant serveur pour lequel il gère les exceptions. Quand [**IPlaybackControl :: FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry) est appelé, le temps d’exécution des composants en file d’attente lit le message ayant échoué dans le gestionnaire d’exceptions. Cela permet au gestionnaire d’exceptions d’implémenter un autre comportement pour les messages qui ne peuvent pas être déplacés vers le serveur, par exemple en générant une transaction de compensation.

Si le gestionnaire d’exceptions termine tous les appels de méthode lus, le message est supprimé de la file d’attente de lettres mortes Xact et est fermé. Toutefois, si le gestionnaire d’exceptions abandonne le message en retournant un état d’échec de l’un des appels de méthode, le message est retourné à la file d’attente de lettres mortes Xact. La séquence d’événements suivante montre comment les exceptions côté client sont gérées :

1.  Message Queuing ne parvient pas à remettre un message au serveur et place le message dans la file d’attente de lettres mortes Xact.
2.  L’écouteur de file d’attente de lettres mortes (DLQL) recherche un message dans la file d’attente de lettres mortes Xact.
3.  Le DLQL récupère le CLSID du composant cible à partir du message et recherche une classe d’exception.
4.  Le DLQL instancie la classe d’exception.
5.  DLQL interroge [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol) pour la classe d’exception.
6.  DLQL appelle la méthode [**IPlaybackControl :: FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry) dans la classe d’exception.
7.  DLQL lit tous les appels de méthode et de propriété du message à la classe d’exception.
8.  Le DLQL supprime le message si le gestionnaire d’exceptions termine la transaction avec succès. Le gestionnaire d’exceptions peut émettre [**IObjectContext :: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), et le message reste dans la file d’attente de lettres mortes.

Si l’une des étapes précédentes échoue, le message est conservé dans la file d’attente de lettres mortes Xact.

Au démarrage, DLQL lit chaque message sur la file d’attente de lettres mortes transactionnelle Message Queuing et instancie la classe d’exception pour chaque message Queued Components. Après une seule passe dans la file d’attente, elle attend de nouveaux messages. Il traite ensuite chaque nouveau message de la file d’attente de lettres mortes à son arrivée.

Si vous devez intervenir dans le processus décrit ici ou si vous devez déplacer un message incohérent hors de sa file d’attente Rest finale, utilisez l’utilitaire de déplacement de messages. Pour plus d’informations sur l’utilitaire de déplacement de messages, consultez [gestion des erreurs](handling-errors-in-queued-components.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Erreurs côté client](client-side-errors.md)
</dt> <dt>

[Erreurs côté serveur](server-side-errors.md)
</dt> </dl>

 

 



