---
title: Assistances pour l’implémentation de serveur hors processus
description: Assistances pour l’implémentation de serveur hors processus
ms.assetid: 18641a84-56f8-4d27-9ddb-fa64011ac8ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 264d3f26b179b3ecb659ef93785c8c223b6c524e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382975"
---
# <a name="out-of-process-server-implementation-helpers"></a>Assistances pour l’implémentation de serveur hors processus

Quatre fonctions d’assistance qui peuvent être appelées par des serveurs hors processus sont disponibles pour simplifier le travail d’écriture de code serveur. En général, les clients COM et les serveurs COM in-process ne les appellent pas. Ces fonctions sont conçues pour aider à éviter les conditions de concurrence dans l’activation du serveur lorsque les serveurs comportent plusieurs cloisonnements ou plusieurs objets de classe. Ils peuvent également être utilisés aussi facilement pour les serveurs d’objets à un seul thread et à classe unique. Les fonctions sont les suivantes :

-   [**CoAddRefServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess)
-   [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess)
-   [**CoSuspendClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-cosuspendclassobjects)
-   [**CoResumeClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-coresumeclassobjects)

Pour s’arrêter correctement, un serveur COM doit effectuer le suivi du nombre d’instances d’objet qu’il a instanciées et du nombre de fois que sa méthode [**IClassFactory :: LockServer,**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) a été appelée. Ce n’est que lorsque ces deux nombres atteignent la valeur zéro et que le serveur est arrêté. Dans les serveurs COM monothread, la décision d’arrêter a été coordonnée avec les demandes d’activation entrantes, qui ont été sérialisées par la file d’attente de messages. Le serveur, lors de la réception d’une version sur son instance d’objet finale et de la décision d’arrêter, révoque ses objets de classe avant la distribution d’autres demandes d’activation. Si une demande d’activation a été envoyée après ce point, COM reconnaît que les objets de classe ont été révoqués et retournerait une erreur au gestionnaire de contrôle des services, ce qui entraînerait l’exécution d’une nouvelle instance du processus serveur local.

Toutefois, dans un serveur de modèles cloisonnés, dans lequel des objets de classe différents sont inscrits sur différents cloisonnements, et dans tous les serveurs à thread libre, cette décision d’arrêt doit être coordonnée avec les demandes d’activation sur plusieurs threads afin qu’un thread du serveur ne décide pas de s’arrêter alors qu’un autre thread du serveur est occupé à traiter des objets de classe ou des Une approche classique mais difficile à résoudre consiste à avoir le serveur, après avoir révoqué ses objets de classe, revérifier son nombre d’instances et rester actif jusqu’à ce que toutes les instances aient été libérées.

Pour faciliter la gestion de ces types de conditions de concurrence pour les rédacteurs de serveur, COM fournit deux fonctions de décompte de références :

-   [**CoAddRefServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess) incrémente un décompte de références globales par processus.
-   [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess) décrémente le décompte de références globales par processus.

Lorsque le nombre de références globales par processus atteint zéro, COM appelle automatiquement [**CoSuspendClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-cosuspendclassobjects), ce qui empêche toute nouvelle demande d’activation d’entrer dans. Le serveur peut ensuite annuler l’inscription de ses différents objets de classe à partir de ses différents threads, sans craindre qu’une autre demande d’activation arrive. Toutes les nouvelles demandes d’activation sont désormais gérées par le SCM lançant une nouvelle instance du processus serveur local.

Le moyen le plus simple pour une application serveur locale d’utiliser ces fonctions consiste à appeler [**CoAddRefServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess) dans le constructeur pour chacun de ses objets d’instance et dans chacune de ses méthodes [**IClassFactory :: LockServer,**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) lorsque le paramètre de *troupeau* a la **valeur true**. L’application serveur doit également appeler [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess) dans le destructeur de chacun de ses objets d’instance et dans chacune de ses méthodes IClassFactory ::**LockServer,** lorsque le paramètre de *troupeau* a la **valeur false**.

Enfin, l’application serveur doit prêter attention au code de retour de [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess)et, si elle retourne 0, l’application serveur doit lancer son nettoyage, qui, pour un serveur avec plusieurs threads, signifie généralement qu’elle doit signaler ses différents threads pour quitter leurs boucles de message et appeler [**CoAddRefServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess) et [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess). Si les fonctions de gestion de la durée de vie des processus serveur sont utilisées, elles doivent être utilisées dans les instances d’objet et la méthode [**LockServer,**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) ; dans le cas contraire, l’application serveur peut être arrêtée prématurément.

Quand une demande [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) est effectuée, com contacte le serveur, marshale l’interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) de l’objet de classe, retourne au processus client, démarshale l’interface **IClassFactory** et le retourne au client. À ce stade, les clients appellent généralement [**LockServer,**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) avec la **valeur true** pour empêcher l’arrêt du processus serveur. Toutefois, il existe un délai entre le moment où l’objet de classe est marshalé et celui où le client appelle **LockServer,** dans lequel un autre client peut se connecter au même serveur, obtenir une instance et libérer cette instance, provoquant ainsi l’arrêt du serveur et la sortie du premier client et son séchage avec un pointeur **IClassFactory** déconnecté. Pour éviter cette condition de concurrence, COM ajoute un appel implicite à **LockServer,** avec la **valeur true** à l’objet de classe lorsqu’il marshale l’interface **IClassFactory** et un appel implicite à **LockServer,** avec la **valeur false** lorsque le client libère l’interface **IClassFactory** . Par conséquent, il n’est pas nécessaire de rappeler à distance **LockServer,** sur le serveur, et le proxy pour **LockServer,** retourne simplement S \_ OK sans la communication à distance effective de l’appel.

Il existe une autre condition de concurrence liée à l’activation lors de l’initialisation d’un processus serveur hors processus. Un serveur COM qui inscrit plusieurs classes appelle en général [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) avec \_ \_ le serveur local REGCLS pour chaque CLSID qu’il prend en charge. Après avoir effectué cette opération pour toutes les classes, le serveur entre dans sa boucle de message. Pour un serveur COM à thread unique, toutes les demandes d’activation sont bloquées jusqu’à ce que le serveur entre dans la boucle de message. Toutefois, pour un serveur de modèle cloisonné qui inscrit des objets de classe différents dans différents cloisonnements et pour tous les serveurs à threads libres, les demandes d’activation peuvent arriver plus tôt que cela. Dans le cas de serveurs de modèles cloisonnés, les demandes d’activation peuvent arriver dès qu’un thread a entré sa boucle de message. Dans le cas de serveurs à threads libres, une demande d’activation peut arriver dès que le premier objet de classe est inscrit. Dans la mesure où une activation peut se produire au début, il est également possible que la version finale se produise (et par conséquent provoque l’arrêt du serveur) avant que le reste du serveur ait pu terminer l’initialisation.

Pour éliminer ces conditions de concurrence et simplifier la tâche de l’enregistreur de serveur, n’importe quel serveur qui souhaite inscrire plusieurs objets de classe avec COM doit appeler [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) avec \_ \_ le serveur local REGCLS \| REGCLS \_ suspendu pour chaque CLSID différent pris en charge par le serveur. Une fois que toutes les classes ont été inscrites et que le processus serveur est prêt à accepter les demandes d’activation entrantes, le serveur doit effectuer un appel à [**CoResumeClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-coresumeclassobjects). Cette fonction indique à COM d’informer le SCM sur toutes les classes inscrites, et il commence à autoriser les demandes d’activation dans le processus serveur. L’utilisation de ces fonctions offre les avantages suivants :

-   Un seul appel est adressé au SCM, quel que soit le nombre de CLSID inscrits, ce qui réduit le temps d’enregistrement global (et donc le temps de démarrage de l’application serveur).
-   Si le serveur possède plusieurs cloisonnements et que différents CLSID sont inscrits dans des cloisonnements différents, ou si le serveur est un serveur libre de threads, aucune demande d’activation ne se produira jusqu’à ce que le serveur appelle [**CoResumeClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-coresumeclassobjects), ce qui permet au serveur d’inscrire tous ses CLSID et d’être correctement configuré avant d’avoir à gérer les demandes d’activation et les demandes d’arrêt possibles.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Responsabilités du serveur COM](com-server-responsibilities.md)
</dt> </dl>

 

 