---
title: Single-Threaded Apartments
description: Single-Threaded Apartments
ms.assetid: 2f345ae2-8314-4067-a6d6-5a0275941ed4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f0a8cb1422b6866d9e0d043fdd46c895e6d335b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382936"
---
# <a name="single-threaded-apartments"></a>Single-Threaded Apartments

L’utilisation de cloisonnements à thread unique (le processus de modèle Apartment) offre un paradigme basé sur les messages pour gérer plusieurs objets exécutés simultanément. Elle vous permet d’écrire du code plus efficace en autorisant un thread, pendant qu’il attend la fin d’une opération longue, afin d’autoriser l’exécution d’un autre thread.

Chaque thread dans un processus qui est initialisé comme un processus de modèle cloisonné, et qui récupère et distribue des messages de fenêtre, est un thread cloisonné à thread unique. Chaque thread vit dans son propre cloisonnement. Dans un cloisonnement, les pointeurs d’interface peuvent être passés sans marshaling et, par conséquent, tous les objets d’un thread cloisonné de thread unique communiquent directement.

Regroupement logique d’objets connexes qui s’exécutent tous sur le même thread et qui, par conséquent, doivent avoir une exécution synchrone, peuvent résider sur le même thread cloisonné de thread unique. Toutefois, un objet de modèle Apartment ne peut pas résider sur plus d’un thread. Les appels aux objets d’autres threads doivent être effectués dans le contexte du thread propriétaire. par conséquent, le modèle COM distribué passe automatiquement les threads pour vous lorsque vous appelez sur un proxy.

Les modèles interprocessus et interthreads sont similaires. Lorsqu’il est nécessaire de passer un pointeur d’interface à un objet dans un autre cloisonnement (sur un autre thread) au sein du même processus, vous utilisez le même modèle de marshaling que celui utilisé par les objets de différents processus pour passer des pointeurs au-delà des limites du processus. En obtenant un pointeur vers l’objet de marshaling standard, vous pouvez marshaler des pointeurs d’interface à travers les limites de thread (entre les cloisonnements) de la même façon que vous le feriez entre les processus. (Les pointeurs d’interface doivent être marshalés lorsqu’ils sont transmis entre les cloisonnements.)

Les règles pour les cloisonnements à thread unique sont simples, mais il est important de les suivre avec soin :

-   Chaque objet doit résider sur un seul thread (dans un thread unique cloisonné).
-   Initialisez la bibliothèque COM pour chaque thread.
-   Marshaler tous les pointeurs vers des objets lors de leur passage entre des cloisonnements.
-   Chaque cloisonnement à thread unique doit avoir une boucle de message pour gérer les appels d’autres processus et des appartements au sein du même processus. Les Apartments à thread unique sans objets (client uniquement) ont également besoin d’une boucle de message pour distribuer les messages de diffusion utilisés par certaines applications.
-   Les objets basés sur des DLL ou in-process n’appellent pas les fonctions d’initialisation COM. au lieu de cela, ils inscrivent leur modèle de thread avec la valeur nommée **ThreadingModel** sous la clé [InprocServer32](inprocserver32.md) dans le registre. Les objets reconnaissants au cloisonnement doivent également écrire des points d’entrée de DLL avec soin. Des considérations spéciales s’appliquent aux serveurs de thread dans les processus. Pour plus d’informations, consultez [problèmes de Threading du serveur in-process](in-process-server-threading-issues.md).

Si plusieurs objets peuvent résider sur un seul thread, aucun objet de modèle Apartment ne peut résider sur plus d’un thread.

Chaque thread d’un processus client ou d’un serveur hors processus doit appeler [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize), ou appeler [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) et spécifier coinit \_ APARTMENTTHREADED pour le paramètre *dwCoInit* . Le cloisonnement principal est le thread qui appelle **CoInitializeEx** en premier. Pour plus d’informations sur les serveurs in-process, consultez [problèmes de Threading du serveur in-process](in-process-server-threading-issues.md).

Tous les appels à un objet doivent être effectués sur son thread (dans son cloisonnement). Il est interdit d’appeler directement un objet à partir d’un autre thread. l’utilisation d’objets de cette manière libre de threads peut entraîner des problèmes pour les applications. L’implication de cette règle est que tous les pointeurs vers des objets doivent être marshalés lorsqu’ils sont transmis entre les cloisonnements. COM fournit les deux fonctions suivantes à cet effet :

-   [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) marshale une interface dans un objet de flux qui est retourné à l’appelant.
-   [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream) démarshale un pointeur d’interface à partir d’un objet de flux et le libère.

Ces fonctions encapsulent les appels aux fonctions [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) et [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) , qui requièrent l’utilisation de l' \_ indicateur InProc MSHCTX.

En général, le marshaling est effectué automatiquement par COM. Par exemple, lors du passage d’un pointeur d’interface en tant que paramètre dans un appel de méthode sur un proxy à un objet d’un autre cloisonnement, ou lors de l’appel de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance), com effectue le marshaling automatiquement. Toutefois, dans certains cas spéciaux, où l’enregistreur d’application passe des pointeurs d’interface entre les cloisonnements sans utiliser les mécanismes COM normaux, le writer doit gérer le marshaling manuellement.

Si un cloisonnement (Apartment 1) dans un processus a un pointeur d’interface et qu’un autre cloisonnement (Apartment 2) requiert son utilisation, Apartment 1 doit appeler [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) pour marshaler l’interface. Le flux créé par cette fonction est thread-safe et doit être stocké dans une variable qui est accessible par Apartment 2. Apartment 2 doit passer ce flux à [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream) pour démarshaler l’interface et récupérer un pointeur vers un proxy via lequel il peut accéder à l’interface. Le cloisonnement principal doit rester actif jusqu’à ce que le client ait terminé tout le travail COM (car certains objets in-process sont chargés dans le cloisonnement principal, comme décrit dans les [problèmes de Threading du serveur in-process](in-process-server-threading-issues.md)). Une fois qu’un objet a été passé entre les threads de cette manière, il est très facile de passer des pointeurs d’interface en tant que paramètres. De cette façon, COM distribué effectue le marshaling et le basculement de threads pour l’application.

Pour gérer les appels d’autres processus et cloisonnés au sein d’un même processus, chaque cloisonnement à thread unique doit avoir une boucle de message. Cela signifie que la fonction de travail du thread doit avoir une boucle GetMessage/DispatchMessage. Si d’autres primitives de synchronisation sont utilisées pour la communication entre les threads, la fonction [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) peut être utilisée pour attendre les messages et pour les événements de synchronisation de threads. La documentation de cette fonction a un exemple de ce type de boucle de combinaison.

COM crée une fenêtre masquée à l’aide de la classe Windows « OleMainThreadWndClass » dans chaque cloisonnement à thread unique. Un appel à un objet est reçu en tant que message de fenêtre dans cette fenêtre masquée. Lorsque l’appartement de l’objet récupère et distribue le message, la fenêtre masquée la reçoit. La procédure de fenêtre appellera ensuite la méthode d’interface correspondante de l’objet.

Lorsque plusieurs clients appellent un objet, les appels sont mis en file d’attente dans la file d’attente de messages et l’objet reçoit un appel chaque fois que son cloisonnement récupère et distribue des messages. Étant donné que les appels sont synchronisés par COM et que les appels sont toujours remis par le thread qui appartient au cloisonnement de l’objet, les implémentations d’interface de l’objet n’ont pas besoin de synchronisation. Les Apartments à thread unique peuvent implémenter [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) pour leur permettre d’annuler des appels ou de recevoir des messages de fenêtre si nécessaire.

L’objet peut être réentré si l’une de ses implémentations de méthode d’interface récupère et distribue des messages ou effectue un appel ORPC à un autre thread, provoquant ainsi la remise d’un autre appel à l’objet (par le même cloisonnement). OLE n’empêche pas la réentrance sur le même thread, mais il peut aider à assurer la sécurité des threads. Cela est identique à la façon dont une procédure de fenêtre peut être réentrée si elle récupère et distribue des messages lors du traitement d’un message. Toutefois, l’appel d’un serveur cloisonné à thread unique hors processus qui appelle un autre serveur à thread unique cloisonné permet de réentrer le premier serveur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accès aux interfaces à travers les Apartments](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Choix du modèle de thread](choosing-the-threading-model.md)
</dt> <dt>

[Apartments (cloisonnés) multithread](multithreaded-apartments.md)
</dt> <dt>

[Problèmes liés aux threads du serveur in-process](in-process-server-threading-issues.md)
</dt> <dt>

[Processus, threads et Apartments](processes--threads--and-apartments.md)
</dt> <dt>

[Communication monothread et multithread](single-threaded-and-multithreaded-communication.md)
</dt> </dl>

 

 