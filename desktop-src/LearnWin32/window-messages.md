---
title: Messages de fenêtre (prise en main de Win32 et C++)
description: Messages de fenêtre (prise en main de Win32 et C++)
ms.assetid: 90c20456-44ed-4f0f-a6d3-b6c5660f0bc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c00da564396e0f95947e33fb7d8db8b217ac5cdf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103837"
---
# <a name="window-messages-get-started-with-win32-and-c"></a>Messages de fenêtre (prise en main de Win32 et C++)

Une application GUI doit répondre aux événements de l’utilisateur et du système d’exploitation.

- Les **événements de l’utilisateur** incluent toutes les façons dont quelqu’un peut interagir avec votre programme : les clics de souris, les frappes de touche, les gestes à écran tactile, et ainsi de suite.
- Les **événements du système d’exploitation** incluent tout ce qui est « en dehors » du programme qui peut affecter le comportement du programme. Par exemple, l’utilisateur peut brancher un nouveau périphérique matériel, ou Windows peut passer à un état d’alimentation faible (veille ou veille prolongée).

Ces événements peuvent se produire à tout moment pendant l’exécution du programme, dans presque n’importe quel ordre. Comment structurer un programme dont le déroulement de l’exécution ne peut pas être prédit à l’avance ?

Pour résoudre ce problème, Windows utilise un modèle de transmission de messages. Le système d’exploitation communique avec la fenêtre de votre application en lui transmettant des messages. Un message est simplement un code numérique qui désigne un événement particulier. Par exemple, si l’utilisateur appuie sur le bouton gauche de la souris, la fenêtre reçoit un message avec le code de message suivant.

```C++
#define WM_LBUTTONDOWN    0x0201
```

Certains messages sont associés à des données. Par exemple, le message [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) comprend la coordonnée x et la coordonnée y du curseur de la souris.

Pour transmettre un message à une fenêtre, le système d’exploitation appelle la procédure de fenêtre inscrite pour cette fenêtre. (Et maintenant vous savez à quoi sert la procédure de fenêtre.)

## <a name="the-message-loop"></a>Boucle de messages

Une application recevra des milliers de messages pendant son exécution. (Considérez que chaque clic de souris et bouton de souris génère un message.) En outre, une application peut avoir plusieurs fenêtres, chacune avec sa propre procédure de fenêtre. Comment le programme reçoit-il tous ces messages et les remet à la procédure de fenêtre appropriée ? L’application a besoin d’une boucle pour récupérer les messages et les distribuer aux fenêtres appropriées.

Pour chaque thread qui crée une fenêtre, le système d’exploitation crée une file d’attente pour les messages de fenêtre. Cette file d’attente contient les messages de toutes les fenêtres créées sur ce thread. La file d’attente elle-même est masquée dans votre programme. Vous ne pouvez pas manipuler la file d’attente directement. Toutefois, vous pouvez extraire un message de la file d’attente en appelant la fonction [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) .

```C++
MSG msg;
GetMessage(&msg, NULL, 0, 0);
```

Cette fonction supprime le premier message du début de la file d’attente. Si la file d’attente est vide, la fonction se bloque jusqu’à ce qu’un autre message soit mis en file d’attente. Le fait que les blocs [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) ne permettront pas à votre programme de ne pas répondre. S’il n’y a aucun message, il n’y a rien à faire pour le programme. Si vous devez effectuer un traitement en arrière-plan, vous pouvez créer des threads supplémentaires qui continuent à s’exécuter lorsque **GetMessage** attend un autre message. (Voir [éviter les goulots d’étranglement dans votre procédure de fenêtre](writing-the-window-procedure.md).)

Le premier paramètre de [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) est l’adresse d’une structure [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) . Si la fonction aboutit, elle remplit la structure **MSG** avec des informations sur le message. Cela comprend la fenêtre cible et le code du message. Les trois autres paramètres vous permettent de filtrer les messages que vous recevez de la file d’attente. Dans presque tous les cas, vous allez définir ces paramètres sur zéro.

Même si la structure [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) contient des informations sur le message, vous n’examinerez presque jamais cette structure directement. Au lieu de cela, vous le transmettez directement à deux autres fonctions.

```C++
TranslateMessage(&msg); 
DispatchMessage(&msg);
```

La fonction [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) est liée à l’entrée au clavier. Il traduit les séquences de touches (touche enfoncée, touche précédente) en caractères. Vous n’avez pas vraiment besoin de savoir comment cette fonction fonctionne ; n’oubliez pas de l’appeler avant [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage). Le lien vers la documentation MSDN vous donne plus d’informations, si vous êtes curieux.

La fonction [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) indique au système d’exploitation d’appeler la procédure de fenêtre de la fenêtre qui est la cible du message. En d’autres termes, le système d’exploitation recherche le handle de fenêtre dans son tableau de fenêtres, recherche le pointeur de fonction associé à la fenêtre et appelle la fonction.

Par exemple, supposons que l’utilisateur appuie sur le bouton gauche de la souris. Cela provoque une chaîne d’événements :

1. Le système d’exploitation place un message [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) dans la file d’attente de messages.
2. Votre programme appelle la fonction [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) .
3. [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) extrait le message [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) à partir de la file d’attente et remplit la structure [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) .
4. Votre programme appelle les fonctions [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) et [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) .
5. À l’intérieur de [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), le système d’exploitation appelle votre procédure de fenêtre.
6. Votre procédure de fenêtre peut soit répondre au message, soit l’ignorer.

Lorsque la procédure de fenêtre retourne, elle retourne à [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage). Cela revient à la boucle de message pour le message suivant. Tant que votre programme est en cours d’exécution, les messages continuent d’arriver dans la file d’attente. Par conséquent, vous devez disposer d’une boucle qui extrait continuellement des messages de la file d’attente et les distribue. Vous pouvez considérer la boucle comme suit :

```C++
// WARNING: Don't actually write your loop this way.

while (1)      
{
    GetMessage(&msg, NULL, 0,  0);
    TranslateMessage(&msg); 
    DispatchMessage(&msg);
}
```

Comme écrit, bien sûr, cette boucle ne se terminerait jamais. C’est là qu’intervient la valeur de retour de la fonction [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) . Normalement, **GetMessage** retourne une valeur différente de zéro. Lorsque vous souhaitez quitter l’application et sortir de la boucle de message, appelez la fonction [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) .

```C++
        PostQuitMessage(0);
```

La fonction [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) place un message [**WM \_ Quit**](/windows/desktop/winmsg/wm-quit) dans la file d’attente de messages. **WM \_ QUIT** est un message spécial : il fait en sorte que [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) retourne zéro et signale la fin de la boucle de message. Voici la boucle de message révisée.

```C++
// Correct.

MSG msg = { };
while (GetMessage(&msg, NULL, 0, 0) > 0)
{
    TranslateMessage(&msg);
    DispatchMessage(&msg);
}
```

Tant que la fonction [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) retourne une valeur différente de zéro, l’expression de la boucle **while** prend la valeur true. Une fois que vous avez appelé [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage), l’expression devient false et le programme s’arrête hors de la boucle. (L’un des résultats intéressants de ce comportement est que votre procédure de fenêtre ne reçoit jamais de message [**WM \_ Quit**](/windows/desktop/winmsg/wm-quit) . Par conséquent, il n’est pas nécessaire d’avoir une instruction case pour ce message dans votre procédure de fenêtre.)

La prochaine question évidente est l’appel de [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage). Nous reviendrons à cette question dans la rubrique [fermeture de la fenêtre](closing-the-window.md), mais nous devons d’abord écrire notre procédure de fenêtre.

## <a name="posted-messages-versus-sent-messages"></a>Messages publiés et messages envoyés

La section précédente a abordé les messages qui passent dans une file d’attente. Parfois, le système d’exploitation appellera directement une procédure de fenêtre, en ignorant la file d’attente.

La terminologie de cette distinction peut prêter à confusion :

-   La *publication* d’un message signifie que le message est placé dans la file d’attente de messages et est distribué via la boucle de message ([**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) et [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)).
-   L' *envoi* d’un message signifie que le message ignore la file d’attente et que le système d’exploitation appelle directement la procédure de fenêtre.

Pour le moment, la différence n’est pas très importante. La procédure de fenêtre gère tous les messages. Toutefois, certains messages contournent la file d’attente et accèdent directement à votre procédure de fenêtre. Toutefois, il peut faire la différence si votre application communique entre Windows. Pour plus d’informations sur ce problème, consultez la rubrique [à propos des messages et des files d’attente de messages](/windows/desktop/winmsg/about-messages-and-message-queues).

## <a name="next"></a>Suivant

[Écriture de la procédure de fenêtre](writing-the-window-procedure.md)
