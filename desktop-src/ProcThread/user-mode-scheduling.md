---
description: La planification en mode utilisateur (UMS) est un mécanisme léger que les applications peuvent utiliser pour planifier leurs propres threads.
ms.assetid: f9dd92fe-6d7a-452c-893e-e6df1757e377
title: Planification de la User-Mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ceea3c4d4e40d73f48414d074bcb5b4f6e911d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527523"
---
# <a name="user-mode-scheduling"></a>Planification de la User-Mode

La planification en mode utilisateur (UMS) est un mécanisme léger que les applications peuvent utiliser pour planifier leurs propres threads. Une application peut basculer entre les threads UMS en mode utilisateur sans impliquer le [planificateur système](scheduling.md) et regagner le contrôle du processeur si un thread UMS se bloque dans le noyau. Les threads UMS diffèrent des [fibres](fibers.md) en ce que chaque thread UMS a son propre contexte de thread au lieu de partager le contexte de thread d’un thread unique. La possibilité de basculer entre les threads en mode utilisateur rend UMS plus efficace que les [pools de threads](thread-pools.md) pour la gestion d’un grand nombre d’éléments de travail à durée réduite qui nécessitent peu d’appels système.

UMS est recommandé pour les applications avec des exigences de performances élevées qui doivent exécuter efficacement un grand nombre de threads simultanément sur des systèmes multiprocesseurs ou multicœurs. Pour tirer parti de UMS, une application doit implémenter un composant de planificateur qui gère les threads UMS de l’application et détermine le moment où ils doivent s’exécuter. Les développeurs doivent déterminer si leurs exigences en matière de performances d’application justifient le travail impliqué dans le développement d’un tel composant. Les applications avec des exigences de performances modérées peuvent être mieux servies en permettant au planificateur système de planifier leurs threads.

UMS est disponible pour les applications 64 bits qui s’exécutent sur les versions 64 bits de Windows 7 et Windows Server 2008 R2 ou version ultérieure 64 bits de Windows. Cette fonctionnalité n’est pas disponible sur les versions 32 bits de Windows.

Pour plus d’informations, consultez les sections suivantes :

-   [Planificateur UMS](#ums-scheduler)
-   [Thread UMS Scheduler](#ums-scheduler-thread)
-   [Threads de travail UMS, contextes de thread et listes de saisie semi-automatique](#ums-worker-threads-thread-contexts-and-completion-lists)
-   [Fonction de point d’entrée du planificateur UMS](#ums-scheduler-entry-point-function)
-   [Exécution du thread UMS](#ums-thread-execution)
-   [Meilleures pratiques pour UMS](#ums-best-practices)

## <a name="ums-scheduler"></a>Planificateur UMS

Le planificateur UMS d’une application est responsable de la création, de la gestion et de la suppression des threads UMS et de la détermination du thread UMS à exécuter. Le planificateur d’une application effectue les tâches suivantes :

-   Crée un thread UMS Scheduler pour chaque processeur sur lequel l’application va exécuter des threads de travail UMS.
-   Crée des threads de travail UMS pour effectuer le travail de l’application.
-   Gère sa propre file d’attente de threads de travail prête à être exécutée, et sélectionne les threads à exécuter en fonction des stratégies de planification de l’application.
-   Crée et surveille une ou plusieurs listes de saisie semi-automatique dans lesquelles le système met en file d’attente les threads une fois le traitement terminé dans le noyau. Celles-ci incluent les threads de travail nouvellement créés et les threads précédemment bloqués sur un appel système qui a été débloqué.
-   Fournit une fonction de point d’entrée du planificateur pour gérer les notifications du système. Le système appelle la fonction de point d’entrée lorsqu’un thread de planificateur est créé, lorsqu’un thread de travail se bloque sur un appel système ou lorsqu’un thread de travail produit explicitement le contrôle.
-   Effectue des tâches de nettoyage pour les threads de travail dont l’exécution est terminée.
-   Effectue un arrêt ordonné du planificateur lorsqu’il est demandé par l’application.

## <a name="ums-scheduler-thread"></a>Thread UMS Scheduler

Un thread UMS Scheduler est un thread ordinaire qui s’est converti en UMS en appelant la fonction [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode) . Le planificateur système détermine le moment où le thread du planificateur UMS s’exécute en fonction de sa priorité par rapport à d’autres threads prêts. Le processeur sur lequel le thread du planificateur s’exécute est influencé par l’affinité du thread, comme pour les threads non UMS.

L’appelant de [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode) spécifie une liste de saisie semi-automatique et une fonction de point d’entrée [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) à associer au thread UMS Scheduler. Le système appelle la fonction de point d’entrée spécifiée lorsqu’il a fini de convertir le thread appelant en UMS. La fonction de point d’entrée du planificateur est chargée de déterminer l’action suivante appropriée pour le thread spécifié. Pour plus d’informations, consultez [fonction de point d’entrée du planificateur UMS](#ums-scheduler-entry-point-function) plus loin dans cette rubrique.

Une application peut créer un thread UMS Scheduler pour chaque processeur qui sera utilisé pour exécuter des threads UMS. L’application peut également définir l’affinité de chaque thread UMS Scheduler pour un processeur logique spécifique, ce qui a pour effet d’exclure les threads non liés de s’exécuter sur ce processeur, ce qui les réserve efficacement pour ce thread Scheduler. N’oubliez pas que la définition de l’affinité des threads de cette manière peut affecter les performances globales du système en privant les autres processus qui peuvent s’exécuter sur le système. Pour plus d’informations sur l’affinité de thread, consultez [plusieurs processeurs](multiple-processors.md).

## <a name="ums-worker-threads-thread-contexts-and-completion-lists"></a>Threads de travail UMS, contextes de thread et listes de saisie semi-automatique

Un thread de travail UMS est créé en appelant [**CreateRemoteThreadEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex) avec l' \_ attribut de thread UMS de l’attribut de thread proc et en \_ \_ \_ spécifiant un contexte de thread UMS et une liste de saisie semi-automatique.

Un contexte de thread UMS représente l’état de thread UMS d’un thread de travail et est utilisé pour identifier le thread de travail dans les appels de fonction UMS. Elle est créée en appelant [**CreateUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext).

Une liste de saisie semi-automatique est créée en appelant la fonction [**CreateUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist) . Une liste de saisie semi-automatique reçoit les threads de travail UMS dont l’exécution est terminée dans le noyau et qui sont prêts à être exécutés en mode utilisateur. Seul le système peut mettre les threads de travail en file d’attente dans une liste de saisie semi-automatique. Les nouveaux threads de travail UMS sont automatiquement mis en file d’attente dans la liste de saisie semi-automatique spécifiée lors de la création des threads. Les threads de travail bloqués précédemment sont également mis en file d’attente dans la liste de saisie semi-automatique lorsqu’ils ne sont plus bloqués.

Chaque thread UMS Scheduler est associé à une seule liste de saisie semi-automatique. Toutefois, la même liste de saisie semi-automatique peut être associée à un nombre quelconque de threads de planification UMS, et un thread de planificateur peut récupérer des contextes UMS à partir d’une liste de saisie semi-automatique pour laquelle il a un pointeur.

Chaque liste de saisie semi-automatique est associée à un événement qui est signalé par le système lorsqu’il met en file d’attente un ou plusieurs threads de travail dans une liste vide. La fonction [**GetUmsCompletionListEvent**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent) récupère un handle pour l’événement pour une liste de saisie semi-automatique spécifiée. Une application peut attendre plusieurs événements de liste de saisie semi-automatique et d’autres événements qui ont un sens pour l’application.

## <a name="ums-scheduler-entry-point-function"></a>Fonction de point d’entrée du planificateur UMS

La fonction de point d’entrée du planificateur d’une application est implémentée en tant que fonction [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) . Le système appelle la fonction de point d’entrée du planificateur de l’application aux moments suivants :

-   Lorsqu’un thread non UMS est converti en thread UMS Scheduler en appelant [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode).
-   Quand un thread de travail UMS appelle [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield).
-   Quand un thread de travail UMS se bloque sur un service système tel qu’un appel système ou une erreur de page.

Le paramètre *reason* de la fonction [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) spécifie la raison pour laquelle la fonction de point d’entrée a été appelée. Si la fonction de point d’entrée a été appelée en raison de la création d’un nouveau thread UMS Scheduler, le paramètre *SchedulerParam* contient les données spécifiées par l’appelant de [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode). Si la fonction de point d’entrée a été appelée parce qu’un thread de travail UMS a été généré, le paramètre *SchedulerParam* contient les données spécifiées par l’appelant de [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield). Si la fonction de point d’entrée a été appelée parce qu’un thread de travail UMS a été bloqué dans le noyau, le paramètre *SchedulerParam* a la valeur null.

La fonction de point d’entrée du planificateur est chargée de déterminer l’action suivante appropriée pour le thread spécifié. Par exemple, si un thread de travail est bloqué, la fonction de point d’entrée du planificateur peut exécuter le prochain thread de travail UMS prêt disponible.

Lorsque la fonction de point d’entrée du planificateur est appelée, le planificateur de l’application doit tenter de récupérer tous les éléments de sa liste de saisie semi-automatique associée en appelant la fonction [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) . Cette fonction récupère une liste de contextes de thread UMS dont le traitement est terminé dans le noyau et qui sont prêts à être exécutés en mode utilisateur. Le planificateur de l’application ne doit pas exécuter de threads UMS directement à partir de cette liste, car cela peut provoquer un comportement imprévisible dans l’application. Au lieu de cela, le planificateur doit récupérer tous les contextes de thread UMS en appelant la fonction [**GetNextUmsListItem**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem) une fois pour chaque contexte, insérer les contextes de thread UMS dans la file d’attente de threads prête du planificateur, puis exécuter uniquement les threads UMS à partir de la file d’attente de threads prête.

Si le planificateur n’a pas besoin d’attendre plusieurs événements, il doit appeler [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) avec un paramètre de délai d’expiration différent de zéro afin que la fonction attende l’événement de liste de saisie semi-automatique avant de retourner. Si le planificateur doit attendre plusieurs événements de liste de saisie semi-automatique, il doit appeler **DequeueUmsCompletionListItems** avec un paramètre timeout égal à zéro pour que la fonction soit retournée immédiatement, même si la liste de saisie semi-automatique est vide. Dans ce cas, le planificateur peut attendre explicitement les événements de la liste de saisie semi-automatique, par exemple, en utilisant [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects).

## <a name="ums-thread-execution"></a>Exécution du thread UMS

Un thread de travail UMS nouvellement créé est mis en file d’attente dans la liste de saisie semi-automatique spécifiée et ne commence pas à s’exécuter jusqu’à ce que le planificateur UMS de l’application le sélectionne pour s’exécuter. Cela diffère des threads non UMS, que le planificateur système planifie automatiquement d’exécuter à moins que l’appelant ne crée explicitement le thread suspendu.

Le planificateur exécute un thread de travail en appelant [**ExecuteUmsThread**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread) avec le contexte UMS du thread de travail. Un thread de travail UMS s’exécute jusqu’à ce qu’il génère en appelant la fonction [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield) , des blocs ou des terminaisons.

## <a name="ums-best-practices"></a>Meilleures pratiques pour UMS

Les applications qui implémentent UMS doivent suivre les meilleures pratiques suivantes :

-   Les structures sous-jacentes pour les contextes de thread UMS sont gérées par le système et ne doivent pas être modifiées directement. Utilisez plutôt [**QueryUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation) et [**SetUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation) pour récupérer et définir des informations sur un thread de travail UMS.
-   Pour éviter les blocages, le thread UMS Scheduler ne doit pas partager les verrous avec les threads de travail UMS. Cela comprend les verrous créés par l’application et les verrous système acquis indirectement par des opérations telles que l’allocation à partir du tas ou le chargement de dll. Par exemple, supposons que le planificateur exécute un thread de travail UMS qui charge une DLL. Le thread de travail acquiert le verrou et les blocs du chargeur. Le système appelle la fonction de point d’entrée du planificateur, qui charge ensuite une DLL. Cela provoque un interblocage, car le verrou du chargeur est déjà maintenu et ne peut pas être libéré tant que le premier thread n’est pas débloqué. Pour éviter ce problème, déléguez le travail qui peut partager des verrous avec les threads de travail UMS avec un thread de travail UMS dédié ou un thread non UMS.
-   UMS est plus efficace lorsque la plupart des traitements s’effectuent en mode utilisateur. Dans la mesure du possible, évitez d’effectuer des appels système dans les threads de travail UMS.
-   Les threads de travail UMS ne doivent pas supposer que le planificateur système est en cours d’utilisation. Cette hypothèse peut avoir des effets subtils ; par exemple, si un thread dans le code inconnu définit une priorité ou une affinité de thread, le planificateur UMS peut toujours le remplacer. Le code qui suppose que le planificateur système est utilisé peut ne pas se comporter comme prévu et peut s’arrêter lorsqu’il est appelé par un thread UMS.
-   Le système peut avoir besoin de verrouiller le contexte de thread d’un thread de travail UMS. Par exemple, un appel de procédure asynchrone en mode noyau (APC) peut modifier le contexte du thread UMS, de sorte que le contexte de thread doit être verrouillé. Si le planificateur tente d’exécuter le contexte de thread UMS pendant qu’il est verrouillé, l’appel échoue. Ce comportement est lié à la conception et le planificateur doit être conçu pour réessayer d’accéder au contexte de thread UMS.

 

 
