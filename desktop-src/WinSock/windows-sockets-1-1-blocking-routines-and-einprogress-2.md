---
description: Un problème majeur dans le portage d’applications à partir d’un environnement de sockets Berkeley vers un environnement Windows implique un blocage ; autrement dit, l’appel d’une fonction qui ne retourne pas tant que l’opération associée n’est pas terminée.
ms.assetid: 13aedad7-5f3b-4d73-b8e5-be3a095294bc
title: Routines de blocage Windows Sockets 1,1 et EINPROGRESS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ea6d45b4d25578505a3cb4ab4beb7c2c2fe90e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544729"
---
# <a name="windows-sockets-11-blocking-routines-and-einprogress"></a>Routines de blocage Windows Sockets 1,1 et EINPROGRESS

Un problème majeur dans le portage d’applications à partir d’un environnement de sockets Berkeley vers un environnement Windows implique un blocage ; autrement dit, l’appel d’une fonction qui ne retourne pas tant que l’opération associée n’est pas terminée. Un problème survient lorsque l’opération prend un temps arbitrairement long : il s’agit par exemple d’une fonction [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) , qui peut se bloquer jusqu’à ce que des données soient reçues du système homologue. Le comportement par défaut dans le modèle de sockets Berkeley est qu’un socket fonctionne en mode blocage, sauf si le programmeur demande explicitement que les opérations soient traitées comme non bloquantes. Les environnements Windows Sockets 1,1 n’ont pas pu supposer la planification préemptive. Par conséquent, il est fortement recommandé que les programmeurs utilisent les opérations non bloquantes (asynchrones) si possible avec Windows Sockets 1,1. Comme cela n’était pas toujours possible, les fonctionnalités de Pseudo-blocage décrites dans les éléments suivants ont été fournies.

> [!Note]  
> Windows Sockets 2 s’exécute uniquement sur les systèmes d’exploitation préemptif 32 bits où les blocages ne constituent pas un problème. Les pratiques de programmation recommandées pour Windows Sockets 1,1 ne sont pas nécessaires dans Windows Sockets 2.

 

Même sur un socket bloquant, certaines fonctions ( [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind), [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)et [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) , par exemple) se terminent immédiatement. Il n’existe aucune différence entre un blocage et une opération de non-blocage pour ces fonctions. D’autres opérations, telles que [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), peuvent se terminer immédiatement ou prendre une heure arbitraire, en fonction de différentes conditions de transport. En cas d’application à un socket bloquant, ces opérations sont appelées « opérations bloquantes ». Les fonctions suivantes peuvent bloquer :

-   [**reçu**](/windows/desktop/api/winsock/nf-winsock-recv)
-   [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)
-   [**Envoyer**](/windows/desktop/api/Winsock2/nf-winsock2-send)
-   [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto)

Avec Windows Sockets 16 bits 1,1, une opération de blocage qui ne peut pas se terminer immédiatement est gérée par le Pseudo-blocage comme suit.

Le fournisseur de services lance l’opération, puis entre une boucle dans laquelle il distribue les messages Windows (ce qui produit le processeur à un autre thread, si nécessaire), puis vérifie la fin de la fonction Windows Sockets. Si la fonction est terminée ou si [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall) a été appelé, la fonction de blocage se termine avec un résultat approprié.

Un fournisseur de services doit autoriser l’installation d’une fonction de raccordement bloquant qui ne traite pas les messages afin d’éviter la possibilité de réacheminer les messages pendant qu’une opération de blocage est en attente. La fonction de raccordement de blocage la plus simple retourne **false**. Si une DLL Windows Sockets dépend de messages pour une opération interne, elle peut exécuter **PeekMessage**(**hMyWnd**...) avant d’exécuter le hook de blocage d’application afin qu’elle puisse obtenir ses messages sans affecter le reste du système.

Dans un environnement Windows Sockets 1,1 16 bits, si un message Windows est reçu pour un processus pour lequel une opération de blocage est en cours, il existe un risque que l’application tente d’émettre un autre appel Windows Sockets. En raison de la difficulté à gérer cette condition en toute sécurité, Windows Sockets 1,1 ne prend pas en charge ce comportement d’application. Une application n’est pas autorisée à effectuer plusieurs appels de fonction Windows Sockets imbriqués. Un seul appel de fonction en suspens est autorisé pour une tâche particulière. Les seules exceptions sont les deux fonctions fournies pour aider le programmeur dans cette situation : [**WSAIsBlocking**](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) et [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).

La fonction [**WSAIsBlocking**](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) peut être appelée à tout moment pour déterminer si un appel de blocage de Windows sockets 1,1 est en cours. De même, la fonction [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall) peut être appelée à tout moment pour annuler un appel bloquant en cours. Toute autre imbrication de fonctions Windows Sockets échoue avec l’erreur WSAEINPROGRESS.

Il convient de souligner que cette restriction s’applique aux opérations de blocage et de non-blocage. Pour les applications Windows Sockets 2 qui négocient la version 2,0 ou une version ultérieure au moment de l’appel de [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup), aucune restriction sur l’imbrication des opérations ne se termine. Les opérations peuvent devenir imbriquées dans de rares circonstances, par exemple pendant un rappel d’acceptation conditionnelle [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) , ou si un fournisseur de services appelle à son tour une fonction Windows Sockets 2.

Bien que ce mécanisme soit suffisant pour les applications simples, il ne peut pas prendre en charge les exigences complexes de distribution des messages des applications plus avancées (par exemple, celles utilisant le modèle MDI). Pour de telles applications, l’API Windows Sockets comprend la fonction [**WSASetBlockingHook**](/windows/desktop/api/winsock2/nf-winsock2-wsasetblockinghook), qui permet à l’application de spécifier une routine spéciale qui peut être appelée à la place de la routine de distribution de messages par défaut décrite dans la discussion précédente.

Le fournisseur Windows Sockets appelle le hook de blocage uniquement si toutes les conditions suivantes sont vraies :

-   La routine est une routine qui est définie comme pouvant être bloquée.
-   Le socket spécifié est un socket bloquant.
-   La demande ne peut pas être effectuée immédiatement.

Un socket est défini comme bloquant par défaut, mais la fonction [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) avec l’IOCTL **FIONBIO** ou la fonction [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) peut définir un socket en mode non bloquant.

Le hook de blocage n’est jamais appelé et l’application n’a pas besoin de se préoccuper des problèmes de réentrance que le hook de blocage peut introduire, si une application respecte les instructions suivantes :

-   Elle utilise uniquement des sockets non bloquants.
-   Elle utilise les routines [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) et/ou **WSAAsyncGetXByY** au lieu de [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) et des routines **getXbyY** .

Si une application Windows Sockets 1,1 appelle une opération asynchrone ou non bloquante qui prend un pointeur vers un objet mémoire (une mémoire tampon ou une variable globale, par exemple) en tant qu’argument, il est de la responsabilité de l’application de s’assurer que l’objet est disponible pour Windows Sockets tout au long de l’opération. L’application ne doit pas appeler de fonction Windows susceptible d’affecter le mappage ou la viabilité de la mémoire impliquée.

 

 



