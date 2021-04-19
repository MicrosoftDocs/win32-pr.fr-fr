---
description: Cette rubrique explique comment utiliser les raccordements.
ms.assetid: 9ced0ac4-e602-425f-b954-6af9c741699a
title: Vue d’ensemble des hooks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36c5d89f111604418d1dc3ea9a4ebce6fe0a8124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534673"
---
# <a name="hooks-overview"></a>Vue d’ensemble des hooks

Un *raccordement* est un mécanisme par lequel une application peut intercepter des événements, tels que des messages, des actions de la souris et des séquences de touches. Une fonction qui intercepte un type particulier d’événement est appelée procédure de *raccordement*. Une procédure de raccordement peut agir sur chaque événement qu’elle reçoit, puis modifier ou ignorer l’événement.

Voici quelques exemples d’utilisation de Hooks :

-   Surveiller les messages à des fins de débogage
-   Fournir la prise en charge de l’enregistrement et de la lecture des macros
-   Fournir la prise en charge d’une touche d’aide (F1)
-   Simuler une entrée de souris et de clavier
-   Implémenter une application de formation basée sur ordinateur (CBT)

> [!Note]  
> Les raccordements tendent à ralentir le système, car ils augmentent la quantité de traitement que le système doit effectuer pour chaque message. Vous devez installer un hook uniquement lorsque cela est nécessaire et le supprimer dès que possible.

 

Cette section aborde les points suivants :

-   [Chaînes de raccordement](#hook-chains)
-   [Procédures de Hook](#hook-procedures)
-   [Types de raccordement](#hook-types)
    -   [\_CALLWNDPROC et WH \_ CALLWNDPROCRET](#wh_callwndproc-and-wh_callwndprocret)
    -   [WH \_ CBT](#wh_cbt)
    -   [WH \_ débogage](#wh_debug)
    -   [WH \_ FOREGROUNDIDLE](#wh_foregroundidle)
    -   [WH \_ GETMESSAGE](#wh_getmessage)
    -   [WH \_ JOURNALPLAYBACK](#wh_journalplayback)
    -   [WH \_ JOURNALRECORD](#wh_journalrecord)
    -   [jusqu’au \_ clavier \_](#wh_keyboard_ll)
    -   [\_clavier WH](#wh_keyboard)
    -   [à \_ la \_ une](#wh_mouse_ll)
    -   [à \_ la souris](#wh_mouse)
    -   [\_Msgfilter et WH \_ SYSMSGFILTER](#wh_msgfilter-and-wh_sysmsgfilter)
    -   [WH \_ Shell](#wh_shell)

## <a name="hook-chains"></a>Chaînes de raccordement

Le système prend en charge de nombreux types différents de raccordements ; chaque type fournit l’accès à un aspect différent de son mécanisme de gestion des messages. Par exemple, une application peut utiliser le crochet de la [ \_ souris](#wh_mouse) pour surveiller le trafic des messages pour les messages de la souris.

Le système gère une chaîne de raccordement distincte pour chaque type de raccordement. Une *chaîne de raccordement* est une liste de pointeurs vers des fonctions spéciales de rappel définies par l’application appelées *procédures de raccordement*. Lorsqu’un message est associé à un type particulier de Hook, le système transmet le message à chaque procédure de raccordement référencée dans la chaîne de raccordement, l’une après l’autre. L’action qu’une procédure de hook peut prendre dépend du type de raccordement impliqué. Les procédures de Hook pour certains types de raccordements peuvent uniquement analyser les messages ; d’autres personnes peuvent modifier des messages ou arrêter leur progression dans la chaîne, ce qui les empêche d’atteindre la procédure de hook suivante ou la fenêtre de destination.

## <a name="hook-procedures"></a>Procédures de Hook

Pour tirer parti d’un type particulier de raccordement, le développeur fournit une procédure de raccordement et utilise la fonction [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) pour l’installer dans la chaîne associée au Hook. Une procédure de raccordement doit avoir la syntaxe suivante :

``` syntax
LRESULT CALLBACK HookProc(
  int nCode, 
  WPARAM wParam, 
  LPARAM lParam
)
{
   // process event
   ...

   return CallNextHookEx(NULL, nCode, wParam, lParam);
}
```

*HookProc* est un espace réservé pour un nom défini par l’application.

Le paramètre *nCode* est un code de raccordement que la procédure de raccordement utilise pour déterminer l’action à effectuer. La valeur du code de raccordement dépend du type du hook ; chaque type possède son propre ensemble de codes de raccordement. Les valeurs des paramètres *wParam* et *lParam* dépendent du code de Hook, mais elles contiennent généralement des informations sur un message qui a été envoyé ou publié.

La fonction [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) installe toujours une procédure de raccordement au début d’une chaîne de raccordement. Lorsqu’un événement qui est surveillé par un type de raccordement particulier est détecté, le système appelle la procédure au début de la chaîne de raccordement associée au Hook. Chaque procédure de raccordement dans la chaîne détermine s’il faut passer l’événement à la procédure suivante. Une procédure de hook transmet un événement à la procédure suivante en appelant la fonction [**CallNextHookEx**](/windows/win32/api/winuser/nf-winuser-callnexthookex) .

Notez que les procédures de Hook pour certains types de raccordements peuvent uniquement analyser les messages. le système transmet les messages à chaque procédure de raccordement, qu’une procédure particulière appelle [**CallNextHookEx**](/windows/win32/api/winuser/nf-winuser-callnexthookex)ou non.

Un *raccordement global* surveille les messages de tous les threads dans le même bureau que le thread appelant. Un *raccordement propre au thread* surveille uniquement les messages d’un thread individuel. Une procédure de raccordement globale peut être appelée dans le contexte d’une application dans le même bureau que le thread appelant, de sorte que la procédure doit se trouver dans un module DLL distinct. Une procédure de hook spécifique au thread est appelée uniquement dans le contexte du thread associé. Si une application installe une procédure de Hook pour l’un de ses propres threads, la procédure de raccordement peut être dans le même module que le reste du code de l’application ou dans une DLL. Si l’application installe une procédure de Hook pour un thread d’une autre application, la procédure doit se trouver dans une DLL. Pour plus d’informations, consultez [bibliothèques de liens dynamiques](../dlls/dynamic-link-libraries.md).

> [!Note]  
> Vous devez utiliser des crochets globaux uniquement à des fins de débogage. dans le cas contraire, vous devez les éviter. Les raccordements globaux ont un impact sur les performances du système et provoquent des conflits avec d’autres applications qui implémentent le même type de hook global.

 

## <a name="hook-types"></a>Types de raccordement

Chaque type de raccordement permet à une application de surveiller un aspect différent du mécanisme de gestion des messages du système. Les sections suivantes décrivent les crochets disponibles.

-   [\_CALLWNDPROC et WH \_ CALLWNDPROCRET](#wh_callwndproc-and-wh_callwndprocret)
-   [WH \_ CBT](#wh_cbt)
-   [WH \_ débogage](#wh_debug)
-   [WH \_ FOREGROUNDIDLE](#wh_foregroundidle)
-   [WH \_ GETMESSAGE](#wh_getmessage)
-   [WH \_ JOURNALPLAYBACK](#wh_journalplayback)
-   [WH \_ JOURNALRECORD](#wh_journalrecord)
-   [jusqu’au \_ clavier \_](#wh_keyboard_ll)
-   [\_clavier WH](#wh_keyboard)
-   [à \_ la \_ une](#wh_mouse_ll)
-   [à \_ la souris](#wh_mouse)
-   [\_Msgfilter et WH \_ SYSMSGFILTER](#wh_msgfilter-and-wh_sysmsgfilter)
-   [WH \_ Shell](#wh_shell)

### <a name="wh_callwndproc-and-wh_callwndprocret"></a>\_CALLWNDPROC et WH \_ CALLWNDPROCRET

Les hooks **WH \_ CALLWNDPROC** et **WH \_ CALLWNDPROCRET** vous permettent de surveiller les messages envoyés aux procédures de fenêtre. Le système appelle une procédure de hook **BL \_ CALLWNDPROC** avant de transmettre le message à la procédure de la fenêtre de réception, puis appelle la procédure de hook **BL \_ CALLWNDPROCRET** une fois que la procédure de fenêtre a traité le message.

Le **Hook \_ CALLWNDPROCRET** transmet un pointeur vers une structure [**CWPRETSTRUCT**](/windows/win32/api/winuser/ns-winuser-cwpretstruct) à la procédure de raccordement. La structure contient la valeur de retour de la procédure de fenêtre qui a traité le message, ainsi que les paramètres de message associés au message. La sous-classement de la fenêtre ne fonctionne pas pour les messages définis entre les processus.

Pour plus d’informations, consultez les fonctions de rappel [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) et [*CallWndRetProc*](/windows/win32/api/winuser/nc-winuser-hookproc) .

### <a name="wh_cbt"></a>WH \_ CBT

Le système appelle une procédure de raccordement de la file d’attente de **\_ jeton** de fin avant l’activation, la création, la destruction, la minimisation, l’agrandissement, le déplacement ou le redimensionnement d’une fenêtre, avant d’exécuter une commande système ; avant de supprimer un événement de souris ou de clavier de la file d’attente des messages système ; avant de définir le focus d’entrée La valeur retournée par la procédure de raccordement détermine si le système autorise ou empêche l’une de ces opérations. Le **point \_ de connexion WH** est principalement destiné aux applications de formation basées sur ordinateur (CBT).

Pour plus d’informations, consultez la fonction de rappel [*CBTProc*](/previous-versions/windows/desktop/legacy/ms644977(v=vs.85)) .

Pour plus d’informations, consultez [winEvents](/windows/desktop/WinAuto/winevents-infrastructure).

### <a name="wh_debug"></a>WH \_ débogage

Le système appelle une procédure de hook de **\_ débogage WH** avant d’appeler des procédures de raccordement associées à un autre raccordement dans le système. Vous pouvez utiliser ce hook pour déterminer s’il faut autoriser le système à appeler des procédures de raccordement associées à d’autres types de raccordements.

Pour plus d’informations, consultez la fonction de rappel [*DebugProc*](/previous-versions/windows/desktop/legacy/ms644978(v=vs.85)) .

### <a name="wh_foregroundidle"></a>WH \_ FOREGROUNDIDLE

Le **Hook \_ FOREGROUNDIDLE** vous permet d’effectuer des tâches de faible priorité pendant les périodes pendant lesquelles son thread de premier plan est inactif. Le système appelle une procédure de hook **BL \_ FOREGROUNDIDLE** lorsque le thread de premier plan de l’application est sur le d’être inactif.

Pour plus d’informations, consultez la fonction de rappel [*ForegroundIdleProc*](/previous-versions/windows/desktop/legacy/ms644980(v=vs.85)) .

### <a name="wh_getmessage"></a>WH \_ GETMESSAGE

Le hook de **WH \_ GETMESSAGE** permet à une application de surveiller les messages qui sont retournés par la fonction [**GETMESSAGE**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) . Vous pouvez utiliser le **Hook \_ WH** pour surveiller les entrées de souris et de clavier, ainsi que les autres messages publiés dans la file d’attente de messages.

Pour plus d’informations, consultez la fonction de rappel [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) .

### <a name="wh_journalplayback"></a>WH \_ JOURNALPLAYBACK

Le hook **BL \_ JOURNALPLAYBACK** permet à une application d’insérer des messages dans la file d’attente de messages système. Vous pouvez utiliser ce hook pour lire une série d’événements de souris et de clavier enregistrés précédemment à l’aide de [WH \_ JOURNALRECORD](#wh_journalrecord). L’entrée normale de la souris et du clavier est désactivée tant qu’un hook **BL \_ JOURNALPLAYBACK** est installé. Un **Hook \_ JOURNALPLAYBACK** est un hook global ; il ne peut pas être utilisé en tant que Hook spécifique à un thread.

Le hook **BL \_ JOURNALPLAYBACK** retourne une valeur de délai d’attente. Cette valeur indique au système le nombre de millisecondes à attendre avant de traiter le message actuel du hook de lecture. Cela permet au hook de contrôler le minutage des événements qu’il lit.

Pour plus d’informations, consultez la fonction de rappel [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) .

### <a name="wh_journalrecord"></a>WH \_ JOURNALRECORD

Le **Hook \_ JOURNALRECORD** vous permet de surveiller et d’enregistrer les événements d’entrée. En général, vous utilisez ce hook pour enregistrer une séquence d’événements de souris et de clavier à lire plus tard en utilisant [WH \_ JOURNALPLAYBACK](#wh_journalplayback). Le **Hook \_ JOURNALRECORD** est un hook global ; il ne peut pas être utilisé en tant que Hook spécifique à un thread.

Pour plus d’informations, consultez la fonction de rappel [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) .

### <a name="wh_keyboard_ll"></a>jusqu’au \_ clavier \_

Le **crochet \_ clavier \_ de WH** vous permet de surveiller les événements d’entrée au clavier à publier dans une file d’attente d’entrée de thread.

Pour plus d’informations, consultez la fonction de rappel [*LowLevelKeyboardProc*](/previous-versions/windows/desktop/legacy/ms644985(v=vs.85)) .

### <a name="wh_keyboard"></a>\_clavier WH

Le **crochet \_ clavier** de l permet à une application de surveiller le trafic des messages pour le [**\_ keyversion WM**](/windows/desktop/inputdev/wm-keydown) et les messages [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) sur le le renvoi de la fonction [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) . Vous pouvez utiliser le **crochet \_ clavier de WH** pour surveiller l’entrée au clavier publiée dans une file d’attente de messages.

Pour plus d’informations, consultez la fonction de rappel [*KeyboardProc*](/previous-versions/windows/desktop/legacy/ms644984(v=vs.85)) .

### <a name="wh_mouse_ll"></a>à \_ la \_ une

Le crochet de la souris de la **\_ souris \_** vous permet de surveiller les événements d’entrée de souris sur le point d’être publiés dans une file d’attente d’entrée de thread.

Pour plus d’informations, consultez la fonction de rappel [*LowLevelMouseProc*](/previous-versions/windows/desktop/legacy/ms644986(v=vs.85)) .

### <a name="wh_mouse"></a>à \_ la souris

Le **\_ pointeur de souris WH** vous permet de surveiller les messages de souris sur le point d’être retournés par la fonction [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) . Vous pouvez utiliser le crochet de la **\_ souris** pour surveiller l’entrée de la souris publiée dans une file d’attente de messages.

Pour plus d’informations, consultez la fonction de rappel [*MouseProc*](/previous-versions/windows/desktop/legacy/ms644988(v=vs.85)) .

### <a name="wh_msgfilter-and-wh_sysmsgfilter"></a>\_Msgfilter et WH \_ SYSMSGFILTER

Les hooks **WH \_ msgfilter** et **WH \_ SYSMSGFILTER** vous permettent de surveiller les messages relatifs au traitement d’un menu, d’une barre de défilement, d’une boîte de message ou d’une boîte de dialogue, et de détecter quand une autre fenêtre est sur le lieu d’être activée suite à l’activation de l’utilisateur en appuyant sur les touches Alt + Tab ou ALT + ÉCHAP. Le **Hook \_ msgfilter** peut surveiller uniquement les messages transmis à un menu, une barre de défilement, une boîte de message ou une boîte de dialogue créée par l’application qui a installé la procédure de Hook. Le **Hook \_ SYSMSGFILTER** surveille ces messages pour toutes les applications.

Les hooks **WH \_ msgfilter** et **WH \_ SYSMSGFILTER** vous permettent d’effectuer un filtrage des messages pendant les boucles modales qui est équivalente au filtrage effectué dans la boucle de message principale. Par exemple, une application examine souvent un nouveau message dans la boucle principale entre le moment où il récupère le message dans la file d’attente et le moment où il distribue le message, en effectuant un traitement spécial, le cas échéant. Toutefois, au cours d’une boucle modale, le système récupère et distribue des messages sans permettre à une application de filtrer les messages dans sa boucle de message principale. Si une application installe une procédure de hook **BL \_ msgfilter** ou **WH \_ SYSMSGFILTER** , le système appelle la procédure pendant la boucle modale.

Une application peut appeler le hook **BL \_ msgfilter** directement en appelant la fonction [**CallMsgFilter**](/windows/win32/api/winuser/nf-winuser-callmsgfiltera) . À l’aide de cette fonction, l’application peut utiliser le même code pour filtrer les messages pendant les boucles modales lorsqu’elle est utilisée dans la boucle de message principale. Pour ce faire, encapsulez les opérations de filtrage dans une procédure de hook **BL \_ msgfilter** et appelez **CallMsgFilter** entre les appels aux fonctions [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) et [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) .

``` syntax
while (GetMessage(&msg, (HWND) NULL, 0, 0)) 
{ 
    if (!CallMsgFilter(&qmsg, 0)) 
        DispatchMessage(&qmsg); 
} 
```

Le dernier argument de [**CallMsgFilter**](/windows/win32/api/winuser/nf-winuser-callmsgfiltera) est simplement transmis à la procédure de raccordement ; vous pouvez entrer n’importe quelle valeur. La procédure de raccordement, en définissant une constante telle que **MSGF \_ MAINLOOP**, peut utiliser cette valeur pour déterminer l’emplacement à partir duquel la procédure a été appelée.

Pour plus d’informations, consultez les fonctions de rappel [*MessageProc*](/previous-versions/windows/desktop/legacy/ms644987(v=vs.85)) et [*SysMsgProc*](/previous-versions/windows/desktop/legacy/ms644992(v=vs.85)) .

### <a name="wh_shell"></a>WH \_ Shell

Une application Shell peut utiliser le hook de **\_ Shell WH** pour recevoir des notifications importantes. Le système appelle une procédure de hook de **\_ Shell WH** lorsque l’application de l’interpréteur de commandes va être activée et lorsqu’une fenêtre de niveau supérieur est créée ou détruite.

Notez que les applications d’interpréteur de commandes personnalisées ne reçoivent pas de messages de **\_ Shell** . Par conséquent, toute application qui s’inscrit elle-même en tant qu’interpréteur de commandes par défaut doit appeler la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) avant (ou toute autre application) qui peut recevoir des messages de **\_ Shell** . Cette fonction doit être appelée avec **SPI \_ SETMINIMIZEDMETRICS** et une structure [**MINIMIZEDMETRICS**](/windows/win32/api/winuser/ns-winuser-minimizedmetrics) . Définissez le membre **iArrange** de cette structure sur **ARW \_ Hide**.

Pour plus d’informations, consultez la fonction de rappel [*ShellProc*](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85)) .

 

 
