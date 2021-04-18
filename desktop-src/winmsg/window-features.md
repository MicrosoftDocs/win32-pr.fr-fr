---
description: Cette vue d’ensemble décrit les fonctionnalités de Windows, telles que les types de fenêtres, les États, la taille et la position.
ms.assetid: 8318c22f-85a2-490e-8233-ee1e234890d9
title: Caractéristiques des fenêtres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 228c6b4ab59102cae38a248935fbbad32198f2e0
ms.sourcegitcommit: 8755905962e156f29203705d09d6df8b7d0e2fca
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "106543378"
---
# <a name="window-features"></a>Caractéristiques des fenêtres

Cette vue d’ensemble décrit les fonctionnalités de Windows, telles que les types de fenêtres, les États, la taille et la position.

-   [Types de fenêtres](#window-types)
    -   [Fenêtres superposées](#overlapped-windows)
    -   [Fenêtres indépendantes](#pop-up-windows)
    -   [Fenêtres enfants](#child-windows)
        -   [Plaçant](#positioning)
        -   [Portion](#clipping)
        -   [Relation avec la fenêtre parente](#relationship-to-parent-window)
        -   [Messages](#size-and-position-messages)
    -   [Fenêtres superposées](#layered-windows)
    -   [Fenêtres de message uniquement](#message-only-windows)
-   [Relations entre les fenêtres](#window-relationships)
    -   [Fenêtres de premier plan et d’arrière-plan](#foreground-and-background-windows)
    -   [Fenêtres détenues](#owned-windows)
    -   [Ordre de plan](#z-order)
-   [Affichage de l’état de la fenêtre](#window-show-state)
    -   [Fenêtre active](#active-window)
    -   [Fenêtres désactivées](#disabled-windows)
    -   [Visibilité de la fenêtre](#window-visibility)
    -   [Fenêtres réduites, agrandies et restaurées](#minimized-maximized-and-restored-windows)
-   [Taille et position de la fenêtre](#window-size-and-position)
    -   [Taille et position par défaut](#default-size-and-position)
    -   [Taille du suivi](#tracking-size)
    -   [Commandes système](#system-commands)
    -   [Fonctions de taille et de position](#size-and-position-functions)
    -   [Messages de taille et de position](#size-and-position-messages)
-   [Animation de fenêtre](#window-animation)
-   [Disposition des fenêtres et mise en miroir](#window-layout-and-mirroring)
    -   [Boîtes de dialogue de mise en miroir et boîtes de message](#mirroring-dialog-boxes-and-message-boxes)
    -   [Mise en miroir de contextes de périphérique non associés à une fenêtre](#mirroring-device-contexts-not-associated-with-a-window)
-   [Destruction de fenêtre](#window-destruction)

## <a name="window-types"></a>Types de fenêtres

Cette section contient les rubriques suivantes qui décrivent les types de fenêtre.

-   [Fenêtres superposées](#overlapped-windows)
-   [Fenêtres indépendantes](#pop-up-windows)
-   [Fenêtres enfants](#child-windows)
-   [Fenêtres superposées](#layered-windows)
-   [Fenêtres de message uniquement](#message-only-windows)

### <a name="overlapped-windows"></a>Fenêtres superposées

Une *fenêtre Overlapped* est une fenêtre de niveau supérieur (fenêtre non enfant) qui a une barre de titre, une bordure et une zone cliente. Il est destiné à servir de fenêtre principale d’une application. Il peut également avoir un menu fenêtre, des boutons réduire et agrandir et des barres de défilement. Une fenêtre Overlapped utilisée en tant que fenêtre principale comprend généralement tous ces composants.

En spécifiant le style [**WS \_ OVERLAPPED**](window-styles.md) ou **WS \_ OVERLAPPEDWINDOW** dans la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , une application crée une fenêtre Overlapped. Si vous utilisez le style avec **\_ chevauchement WS** , la fenêtre a une barre de titre et une bordure. Si vous utilisez le style **WS \_ OVERLAPPEDWINDOW** , la fenêtre a une barre de titre, une bordure de redimensionnement, un menu fenêtre et des boutons réduire et agrandir.

### <a name="pop-up-windows"></a>Fenêtres indépendantes

Une *fenêtre indépendante* est un type spécial de fenêtre avec chevauchement utilisé pour les boîtes de dialogue, les boîtes de message et d’autres fenêtres temporaires qui s’affichent en dehors de la fenêtre principale d’une application. Les barres de titre sont facultatives pour les fenêtres indépendantes. Sinon, les fenêtres indépendantes sont les mêmes que les fenêtres avec chevauchement du style [**de \_ chevauchement WS**](window-styles.md) .

Vous créez une fenêtre indépendante en spécifiant le style de fenêtre [**\_ contextuelle WS**](window-styles.md) dans [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa). Pour inclure une barre de titre, spécifiez le style de **\_ légende WS** . Utilisez le style **WS \_ POPUPWINDOW** pour créer une fenêtre indépendante qui comporte une bordure et un menu fenêtre. Le style de **\_ légende WS** doit être combiné avec le style **WS \_ POPUPWINDOW** pour afficher le menu fenêtre.

### <a name="child-windows"></a>Fenêtres enfants

Une *fenêtre enfant* a le style [**WS \_ Child**](window-styles.md) et est limitée à la zone cliente de sa fenêtre parente. Une application utilise généralement des fenêtres enfants pour diviser la zone cliente d’une fenêtre parente en zones fonctionnelles. Vous créez une fenêtre enfant en spécifiant le style **WS \_ Child** dans la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .

Une fenêtre enfant doit avoir une fenêtre parente. La fenêtre parente peut être une fenêtre Overlapped, une fenêtre indépendante ou même une autre fenêtre enfant. Vous spécifiez la fenêtre parente lorsque vous appelez [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa). Si vous spécifiez le style [**WS \_ Child**](window-styles.md) dans **CreateWindowEx** mais que vous ne spécifiez pas de fenêtre parente, le système ne crée pas la fenêtre.

Une fenêtre enfant a une zone cliente, mais aucune autre fonctionnalité, sauf si elle est explicitement demandée. Une application peut demander une barre de titre, un menu fenêtre, des boutons réduire et agrandir, une bordure et des barres de défilement pour une fenêtre enfant, mais une fenêtre enfant ne peut pas avoir de menu. Si l’application spécifie un handle de menu, lors de l’inscription de la classe de fenêtre de l’enfant ou de la création de la fenêtre enfant, le handle de menu est ignoré. Si aucun style de bordure n’est spécifié, le système crée une fenêtre sans bordure. Une application peut utiliser des fenêtres enfants sans bordure pour diviser la zone cliente d’une fenêtre parente tout en conservant les divisions invisibles pour l’utilisateur.

Cette section décrit les aspects suivants des fenêtres enfants :

-   [Plaçant](#positioning)
-   [Portion](#clipping)
-   [Relation avec la fenêtre parente](#relationship-to-parent-window)
-   [Messages](#size-and-position-messages)

#### <a name="positioning"></a>Plaçant

Le système positionne toujours une fenêtre enfant par rapport à l’angle supérieur gauche de la zone cliente de la fenêtre parente. Aucune partie d’une fenêtre enfant ne s’affiche en dehors des bordures de sa fenêtre parente. Si une application crée une fenêtre enfant plus grande que la fenêtre parente ou positionne une fenêtre enfant pour qu’une partie ou la totalité de la fenêtre enfant s’étende au-delà des limites du parent, le système découpe la fenêtre enfant. autrement dit, la partie située en dehors de la zone cliente de la fenêtre parente n’est pas affichée. Les actions qui affectent la fenêtre parente peuvent également affecter la fenêtre enfant, comme suit.



| Fenêtre parente | Fenêtre enfant                                                                                                             |
|---------------|--------------------------------------------------------------------------------------------------------------------------|
| Détruit     | Détruit avant la destruction de la fenêtre parente.                                                                         |
| Hidden        | Masqué avant que la fenêtre parente ne soit masquée. Une fenêtre enfant est visible uniquement lorsque la fenêtre parente est visible.             |
| Ramené         | Déplacé avec la zone cliente de la fenêtre parente. La fenêtre enfant est chargée de peindre sa zone cliente après le déplacement. |
| Démontré         | Indiqué après l’affichage de la fenêtre parente.                                                                                  |



 

#### <a name="clipping"></a>Portion

Le système ne détoure pas automatiquement une fenêtre enfant de la zone cliente de la fenêtre parente. Cela signifie que la fenêtre parente dessine sur la fenêtre enfant si elle effectue un dessin au même emplacement que la fenêtre enfant. Toutefois, le système découpe la fenêtre enfant de la zone cliente de la fenêtre parente si la fenêtre parente a le style [**WS \_ CLIPCHILDREN**](window-styles.md) . Si la fenêtre enfant est découpée, la fenêtre parente ne peut pas dessiner dessus.

Une fenêtre enfant peut chevaucher d’autres fenêtres enfants dans la même zone cliente. Une fenêtre enfant qui partage la même fenêtre parente qu’une ou plusieurs autres fenêtres enfants est appelée une *fenêtre sœur*. Les fenêtres sœurs peuvent être dessinées dans la zone cliente de chacune d’elles, sauf si l’une des fenêtres enfants a le style [**WS \_ CLIPSIBLINGS**](window-styles.md) . Si une fenêtre enfant a ce style, toute partie de sa fenêtre sœur qui se trouve dans la fenêtre enfant est découpée.

Si une fenêtre a le style [**WS \_ CLIPCHILDREN**](window-styles.md) ou **WS \_ CLIPSIBLINGS** , une légère perte de performances se produit. Chaque fenêtre utilise des ressources système, de sorte qu’une application ne doit pas utiliser les fenêtres enfants sans discrimination. Pour de meilleures performances, une application qui doit diviser logiquement sa fenêtre principale doit le faire dans la procédure de fenêtre de la fenêtre principale plutôt qu’en utilisant des fenêtres enfants.

#### <a name="relationship-to-parent-window"></a>Relation avec la fenêtre parente

Une application peut modifier la fenêtre parente d’une fenêtre enfant existante en appelant la fonction [**SetParent,**](/windows/win32/api/winuser/nf-winuser-setparent) . Dans ce cas, le système supprime la fenêtre enfant de la zone cliente de l’ancienne fenêtre parente et la déplace vers la zone cliente de la nouvelle fenêtre parente. Si **SetParent,** spécifie un handle **null** , la fenêtre du bureau devient la nouvelle fenêtre parente. Dans ce cas, la fenêtre enfant est dessinée sur le bureau, en dehors des bordures de toute autre fenêtre. La fonction [**GetParent**](/windows/win32/api/winuser/nf-winuser-getparent) récupère un handle vers la fenêtre parente d’une fenêtre enfant.

La fenêtre parente libère une partie de sa zone cliente dans une fenêtre enfant, et la fenêtre enfant reçoit toutes les entrées de cette zone. La classe de fenêtre n’a pas besoin d’être la même pour chacune des fenêtres enfants de la fenêtre parente. Cela signifie qu’une application peut remplir une fenêtre parente avec des fenêtres enfants qui s’affichent différemment et effectuent différentes tâches. Par exemple, une boîte de dialogue peut contenir de nombreux types de contrôles, chacun d’entre eux étant une fenêtre enfant qui accepte différents types de données de l’utilisateur.

Une fenêtre enfant n’a qu’une seule fenêtre parente, mais un parent peut avoir n’importe quel nombre de fenêtres enfants. Chaque fenêtre enfant, à son tour, peut avoir des fenêtres enfants. Dans cette chaîne de fenêtres, chaque fenêtre enfant est appelée une fenêtre descendante de la fenêtre parente d’origine. Une application utilise la fonction [**IsChild,**](/windows/win32/api/winuser/nf-winuser-ischild) pour déterminer si une fenêtre donnée est une fenêtre enfant ou une fenêtre descendante d’une fenêtre parente donnée.

La fonction [**EnumChildWindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) énumère les fenêtres enfants d’une fenêtre parente. Ensuite, **EnumChildWindows** passe le handle de chaque fenêtre enfant à une fonction de rappel définie par l’application. Les fenêtres descendantes de la fenêtre parente donnée sont également énumérées.

#### <a name="messages"></a>Messages

Le système transmet les messages d’entrée d’une fenêtre enfant directement à la fenêtre enfant. les messages ne sont pas transmis par le biais de la fenêtre parente. La seule exception est si la fenêtre enfant a été désactivée par la fonction [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) . Dans ce cas, le système transmet à la fenêtre parente à la place tous les messages d’entrée qui seraient passés à la fenêtre enfant. Cela permet à la fenêtre parente d’examiner les messages d’entrée et d’activer la fenêtre enfant, si nécessaire.

Une fenêtre enfant peut avoir un identificateur entier unique. Les identificateurs de fenêtre enfants sont importants lorsque vous travaillez avec des fenêtres de contrôle. Une application dirige l’activité d’un contrôle en lui envoyant des messages. L’application utilise l’identificateur de fenêtre enfant du contrôle pour diriger les messages vers le contrôle. En outre, un contrôle envoie des messages de notification à sa fenêtre parente. Un message de notification comprend l’identificateur de fenêtre enfant du contrôle, que le parent utilise pour identifier le contrôle qui a envoyé le message. Une application spécifie l’identificateur de fenêtre enfant pour d’autres types de fenêtres enfants en affectant une valeur au paramètre *HMENU* de la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) plutôt qu’à un handle de menu.

### <a name="layered-windows"></a>Fenêtres superposées

L’utilisation d’une fenêtre superposée peut améliorer considérablement les performances et les effets visuels d’une fenêtre qui a une forme complexe, anime sa forme ou souhaite utiliser les effets de la fusion alpha. Le système compose et repeint automatiquement les fenêtres superposées et les fenêtres des applications sous-jacentes. Par conséquent, les fenêtres superposées sont rendues en douceur, sans le scintillement typique des régions de fenêtre complexes. En outre, les fenêtres superposées peuvent être partiellement translucides, c’est-à-dire qu’elles sont à fusion alpha.

Pour créer une fenêtre superposée, spécifiez le style de fenêtre étendue **WS par \_ \_ couches** en appelant la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , ou appelez la fonction [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) pour définir **WS \_ ex en \_ couches** après la création de la fenêtre. Après l’appel de **CreateWindowEx** , la fenêtre superposée ne devient visible qu’une fois que la fonction [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) ou [**UpdateLayeredWindow**](/windows/win32/api/winuser/nf-winuser-updatelayeredwindow) a été appelée pour cette fenêtre.

> [!Note]  
> À partir de Windows 8, **WS \_ ex \_ Layered** peut être utilisé avec les fenêtres enfants et les fenêtres de niveau supérieur. Les versions précédentes de Windows prennent en charge **WS \_ ex \_ Layered** uniquement pour les fenêtres de niveau supérieur.

 

Pour définir le niveau d’opacité ou la clé de couleur de transparence pour une fenêtre en couches donnée, appelez [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes). Après l’appel, le système peut toujours demander à la fenêtre de peindre lorsque la fenêtre est affichée ou redimensionnée. Toutefois, étant donné que le système stocke l’image d’une fenêtre superposée, le système ne demande pas à la fenêtre de peindre si des parties de celle-ci sont révélées à la suite d’un déplacement de la fenêtre relative sur le bureau. Les applications héritées n’ont pas besoin de restructurer leur code de peinture s’ils souhaitent ajouter des effets de translucidité ou de transparence pour une fenêtre, car le système redirige la peinture des fenêtres qui ont appelé **SetLayeredWindowAttributes** vers la mémoire hors écran, puis la recompose pour obtenir l’effet souhaité.

Pour une animation plus rapide et plus efficace ou si une alpha par pixel est nécessaire, appelez [**UpdateLayeredWindow**](/windows/win32/api/winuser/nf-winuser-updatelayeredwindow). **UpdateLayeredWindow** doit être utilisé principalement lorsque l’application doit fournir directement la forme et le contenu d’une fenêtre superposée, sans utiliser le mécanisme de redirection fourni par le système par le biais de [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes). En outre, l’utilisation de **UpdateLayeredWindow** utilise directement la mémoire de manière plus efficace, car le système n’a pas besoin de la mémoire supplémentaire requise pour stocker l’image de la fenêtre redirigée. Pour une efficacité maximale de l’animation des fenêtres, appelez **UpdateLayeredWindow** pour modifier la position et la taille d’une fenêtre superposée. Notez qu’après l’appel de **SetLayeredWindowAttributes** , les appels **UpdateLayeredWindow** suivants échouent jusqu’à ce que le bit de style de superposition soit effacé et redéfini.

Le test de positionnement d’une fenêtre superposée est basé sur la forme et la transparence de la fenêtre. Cela signifie que les zones de la fenêtre qui sont à clé de couleur ou dont la valeur alpha est égale à zéro laissent passer les messages de la souris. Toutefois, si la fenêtre superposée a le style de fenêtre étendu **WS \_ ex \_ transparent** , la forme de la fenêtre superposée est ignorée et les événements de souris sont transmis à d’autres fenêtres sous la fenêtre superposée.

### <a name="message-only-windows"></a>Message-Only Windows

Une *fenêtre de message uniquement* vous permet d’envoyer et de recevoir des messages. Elle n’est pas visible, elle n’a pas d’ordre de plan, ne peut pas être énumérée et ne reçoit pas de messages de diffusion. La fenêtre distribue simplement des messages.

Pour créer une fenêtre de message uniquement, spécifiez la constante de [ \_ message HWND](#message-only-windows) ou un handle vers une fenêtre de message uniquement existante dans le paramètre *HWndParent* de la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Vous pouvez également remplacer une fenêtre existante par une fenêtre de message uniquement en spécifiant \_ le message HWND dans le paramètre *hWndNewParent* de la fonction [**SetParent,**](/windows/win32/api/winuser/nf-winuser-setparent) .

Pour rechercher des fenêtres de message uniquement, spécifiez [ \_ message HWND](#message-only-windows) dans le paramètre *HwndParent* de la fonction [**FindWindowEx**](/windows/win32/api/winuser/nf-winuser-findwindowexa) . En outre, **FindWindowEx** recherche les fenêtres de message uniquement ainsi que les fenêtres de niveau supérieur si les paramètres *hwndParent* et *hwndChildAfter* sont **null**.

## <a name="window-relationships"></a>Relations entre les fenêtres

Une fenêtre peut être liée de nombreuses façons à l’utilisateur ou à une autre fenêtre. Une fenêtre peut être une fenêtre détenue, une fenêtre de premier plan ou une fenêtre d’arrière-plan. Une fenêtre a également un ordre de plan par rapport à d’autres fenêtres. Pour plus d'informations, voir les rubriques suivantes :

-   [Fenêtres de premier plan et d’arrière-plan](#foreground-and-background-windows)
-   [Fenêtres détenues](#owned-windows)
-   [Ordre de plan](#z-order)

### <a name="foreground-and-background-windows"></a>Fenêtres de premier plan et d’arrière-plan

Chaque processus peut avoir plusieurs threads d’exécution et chaque thread peut créer des fenêtres. Le thread qui a créé la fenêtre avec laquelle l’utilisateur travaille actuellement est appelé le thread de premier plan et la fenêtre est appelée *fenêtre de premier plan*. Tous les autres threads sont des threads d’arrière-plan et les fenêtres créées par les threads d’arrière-plan sont appelées *fenêtres d’arrière-plan*

Chaque thread a un niveau de priorité qui détermine la quantité de temps processeur reçue par le thread. Bien qu’une application puisse définir le niveau de priorité de ses threads, normalement le thread de premier plan a un niveau de priorité légèrement supérieur à celui des threads d’arrière-plan. Étant donné qu’il a une priorité plus élevée, le thread de premier plan reçoit plus de temps processeur que les threads d’arrière-plan. Le thread de premier plan a une priorité de base normale de 9 ; un thread d’arrière-plan a une priorité de base normale de 7.

L’utilisateur définit la fenêtre de premier plan en cliquant sur une fenêtre, ou à l’aide de la combinaison de touches ALT + TAB ou ALT + ÉCHAP. Pour récupérer un handle de la fenêtre de premier plan, utilisez la fonction [**GetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-getforegroundwindow) . Pour vérifier si la fenêtre de votre application est la fenêtre de premier plan, comparez le handle retourné par **GetForegroundWindow** à celui de la fenêtre de votre application.

Une application définit la fenêtre de premier plan à l’aide de la fonction [**SetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-setforegroundwindow) .

Le système limite les processus qui peuvent définir la fenêtre de premier plan. Un processus peut définir la fenêtre de premier plan uniquement si :

- Toutes les conditions suivantes sont vraies :
  - Le processus appelant **SetForegroundWindow** appartient à une application de bureau, pas à une application UWP ou à une application Windows Store conçue pour Windows 8 ou 8,1.
  - Le processus de premier plan n’a pas désactivé les appels à **SetForegroundWindow** par un appel précédent à la fonction [**LockSetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-locksetforegroundwindow) .
  - Le délai d’attente du verrou de premier plan a expiré (voir [ **SPI_GETFOREGROUNDLOCKTIMEOUT** dans **SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa#SPI_GETFOREGROUNDLOCKTIMEOUT)).
  - Aucun menu n’est actif.
- En outre, au moins une des conditions suivantes est remplie :
  - Le processus appelant est le processus de premier plan.
  - Le processus appelant a été démarré par le processus de premier plan.
  - Il n’existe actuellement aucune fenêtre de premier plan, et donc aucun processus de premier plan.
  - Le processus appelant a reçu le dernier événement d’entrée.
  - Le processus de premier plan ou le processus appelant est en cours de débogage.

Il est possible qu’un processus soit refusé au droit de définir la fenêtre de premier plan, même s’il remplit ces conditions.

Un processus qui peut définir la fenêtre de premier plan peut permettre à un autre processus de définir la fenêtre de premier plan en appelant la fonction [**AllowSetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-allowsetforegroundwindow) , ou en appelant la fonction [**BroadcastSystemMessage**](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessage) avec l’indicateur **BSF \_ ALLOWSFW** . Le processus de premier plan peut désactiver les appels à [**SetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-setforegroundwindow) en appelant la fonction [**LockSetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-locksetforegroundwindow) .

### <a name="owned-windows"></a>Fenêtres détenues

Une fenêtre superposée ou contextuelle peut appartenir à une autre fenêtre superposée ou indépendante. La propriété d’un propriétaire place plusieurs contraintes sur une fenêtre.

-   Une fenêtre appartenant est toujours au-dessus de son propriétaire dans l’ordre de plan.
-   Le système détruit automatiquement une fenêtre détenue lorsque son propriétaire est détruit.
-   Une fenêtre appartenant est masquée lorsque son propriétaire est réduit.

Seule une fenêtre superposée ou contextuelle peut être une fenêtre propriétaire ; une fenêtre enfant ne peut pas être une fenêtre propriétaire. Une application crée une fenêtre propriétaire en spécifiant le descripteur de fenêtre du propriétaire comme paramètre *hwndParent* de [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) lorsqu’elle crée une fenêtre avec le style [**WS \_ OVERLAPPED**](window-styles.md) ou **WS \_ Popup** . Le paramètre *hwndParent* doit identifier une fenêtre superposée ou indépendante. Si *hwndParent* identifie une fenêtre enfant, le système affecte la propriété à la fenêtre parente de niveau supérieur de la fenêtre enfant. Après la création d’une fenêtre propriétaire, une application ne peut pas transférer la propriété de la fenêtre vers une autre fenêtre.

Les boîtes de dialogue et les boîtes de message sont des fenêtres détenues par défaut. Une application spécifie la fenêtre propriétaire lors de l’appel d’une fonction qui crée une boîte de dialogue ou une boîte de message.

Une application peut utiliser la fonction [**GetWindow**](/windows/win32/api/winuser/nf-winuser-getwindow) avec l’indicateur de **\_ propriétaire GW** pour récupérer un handle vers le propriétaire d’une fenêtre.

### <a name="z-order"></a>Ordre de plan

L' *ordre de plan* d’une fenêtre indique la position de la fenêtre dans une pile de fenêtres superposées. Cette pile de fenêtres est orientée le long d’un axe imaginaire, l’axe z, qui s’étend vers l’extérieur de l’écran. La fenêtre située en haut de l’ordre de plan chevauche toutes les autres fenêtres. La fenêtre en bas de l’ordre de plan est chevauchée par toutes les autres fenêtres.

Le système conserve l’ordre de plan dans une seule liste. Elle ajoute des fenêtres à l’ordre de plan selon qu’il s’agit de fenêtres de premier plan, de fenêtres de niveau supérieur ou de fenêtres enfants. Une *fenêtre* de premier plan chevauche toutes les autres fenêtres non-au-dessus, qu’il s’agisse de la fenêtre active ou de la fenêtre de premier plan. Une fenêtre au premier plan a le style **WS \_ ex le \_ plus élevé** . Toutes les fenêtres de niveau supérieur s’affichent dans l’ordre de plan avant les fenêtres qui ne sont pas au premier plan. Une fenêtre enfant est regroupée avec son parent dans l’ordre de plan.

Quand une application crée une fenêtre, le système la place en haut de l’ordre de plan pour les fenêtres du même type. Vous pouvez utiliser la fonction [**BringWindowToTop**](/windows/win32/api/winuser/nf-winuser-bringwindowtotop) pour amener une fenêtre au sommet de l’ordre de plan pour les fenêtres du même type. Vous pouvez réorganiser l’ordre de plan à l’aide des fonctions [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) et [**DeferWindowPos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos) .

L’utilisateur modifie l’ordre de plan en activant une autre fenêtre. Le système positionne la fenêtre active en haut de l’ordre de plan pour les fenêtres du même type. Quand une fenêtre s’affiche en haut de l’ordre de plan, il s’agit donc de ses fenêtres enfants. Vous pouvez utiliser la fonction [**GetTopWindow**](/windows/win32/api/winuser/nf-winuser-gettopwindow) pour rechercher toutes les fenêtres enfants d’une fenêtre parente et retourner un handle vers la fenêtre enfant la plus élevée dans l’ordre de plan. La fonction [**GetNextWindow**](/windows/win32/api/winuser/nf-winuser-getnextwindow) récupère un handle vers la fenêtre suivante ou précédente dans l’ordre de plan.

## <a name="window-show-state"></a>Affichage de l’état de la fenêtre

À un moment donné, une fenêtre peut être active ou inactive ; masqué ou visible ; et réduite, agrandie ou restaurée. Ces qualités sont désignées collectivement dans la *fenêtre afficher l’État*. Les rubriques suivantes traitent de l’état de l’affichage de la fenêtre :

-   [Fenêtre active](#active-window)
-   [Fenêtres désactivées](#disabled-windows)
-   [Visibilité de la fenêtre](#window-visibility)
-   [Fenêtres réduites, agrandies et restaurées](#minimized-maximized-and-restored-windows)

### <a name="active-window"></a>Fenêtre active

Une *fenêtre active* est la fenêtre de niveau supérieur de l’application avec laquelle l’utilisateur travaille actuellement. Pour permettre à l’utilisateur d’identifier facilement la fenêtre active, le système la place en haut de l’ordre de plan et change la couleur de sa barre de titre et de sa bordure en couleurs de fenêtre active définies par le système. Seule une fenêtre de niveau supérieur peut être une fenêtre active. Lorsque l’utilisateur travaille avec une fenêtre enfant, le système active la fenêtre parente de niveau supérieur associée à la fenêtre enfant.

Une seule fenêtre de niveau supérieur dans le système est active à la fois. L’utilisateur active une fenêtre de niveau supérieur en cliquant dessus (ou l’une de ses fenêtres enfants), ou en utilisant la combinaison de touches ALT + ECHAP ou ALT + TAB. Une application active une fenêtre de niveau supérieur en appelant la fonction [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) . D’autres fonctions peuvent entraîner l’activation par le système d’une fenêtre de niveau supérieur différente, notamment [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos), [**DeferWindowPos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos), [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement)et [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow). Bien qu’une application puisse activer une autre fenêtre de niveau supérieur à tout moment, pour éviter de déroutantr l’utilisateur, elle doit le faire uniquement en réponse à une action de l’utilisateur. Une application utilise la fonction [**GetActiveWindow**](/windows/win32/api/winuser/nf-winuser-getactivewindow) pour récupérer un handle de la fenêtre active.

Lorsque l’activation passe d’une fenêtre de niveau supérieur d’une application à la fenêtre de niveau supérieur d’une autre, le système envoie un message [**WM \_ ACTIVATEAPP**](wm-activateapp.md) aux deux applications, en les avertissant de la modification. Lorsque l’activation passe à une autre fenêtre de niveau supérieur dans la même application, le système envoie un message d' [**\_ activation WM**](../inputdev/wm-activate.md) à la fois Windows.

### <a name="disabled-windows"></a>Fenêtres désactivées

Une fenêtre peut être désactivée. Une *fenêtre désactivée* ne reçoit aucune entrée de clavier ou de souris de l’utilisateur, mais elle peut recevoir des messages d’autres fenêtres, d’autres applications et du système. Une application désactive généralement une fenêtre pour empêcher l’utilisateur d’utiliser la fenêtre. Par exemple, une application peut désactiver un bouton de commande dans une boîte de dialogue pour empêcher l’utilisateur de la choisir. Une application peut activer une fenêtre désactivée à tout moment ; l’activation d’une fenêtre restaure l’entrée normale.

Par défaut, une fenêtre est activée lors de la création. Toutefois, une application peut spécifier le style [**WS \_ Disabled**](window-styles.md) pour désactiver une nouvelle fenêtre. Une application active ou désactive une fenêtre existante à l’aide de la fonction [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) . Le système envoie un message [**WM \_ Enable**](wm-enable.md) à une fenêtre lorsque son état activé est sur le paragraphe de la modification. Une application peut déterminer si une fenêtre est activée à l’aide de la fonction [**IsWindowEnabled**](/windows/win32/api/winuser/nf-winuser-iswindowenabled) .

Quand une fenêtre enfant est désactivée, le système passe les messages d’entrée de la souris de l’enfant à la fenêtre parente. Le parent utilise les messages pour déterminer s’il faut activer la fenêtre enfant. Pour plus d’informations, consultez [entrée de la souris](../inputdev/mouse-input.md).

Une seule fenêtre à la fois peut recevoir une entrée au clavier. On dit que cette fenêtre a le focus clavier. Si une application utilise la fonction [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) pour désactiver une fenêtre focus clavier, la fenêtre perd le focus clavier en plus d’être désactivée. **EnableWindow** définit ensuite le focus clavier sur la **valeur null**, ce qui signifie qu’aucune fenêtre n’a le focus. Si une fenêtre enfant, ou une autre fenêtre descendante, a le focus clavier, la fenêtre descendante perd le focus lorsque la fenêtre parente est désactivée. Pour plus d’informations, consultez [entrée au clavier](../inputdev/keyboard-input.md).

### <a name="window-visibility"></a>Visibilité de la fenêtre

Une fenêtre peut être soit visible, soit masquée. Le système affiche une *fenêtre visible* à l’écran. Elle masque une *fenêtre masquée* en ne la dessinant pas. Si une fenêtre est visible, l'utilisateur peut lui fournir des entrées dont elle affiche la sortie. Si une fenêtre est masquée, elle est en réalité désactivée. Une fenêtre masquée peut traiter des messages du système ou d'autres fenêtres, mais ne peut pas traiter d'entrée utilisateur ou afficher une sortie. Une application définit l’état de visibilité d’une fenêtre lors de la création de la fenêtre. Plus tard, l’application peut modifier l’état de visibilité.

Une fenêtre est visible lorsque le style [**WS \_ visible**](window-styles.md) est défini pour la fenêtre. Par défaut, la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) crée une fenêtre masquée, sauf si l’application spécifie le style **WS \_ visible** . En règle générale, une application définit le style **WS \_ visible** après avoir créé une fenêtre pour que les détails du processus de création soient masqués pour l’utilisateur. Par exemple, une application peut conserver une nouvelle fenêtre masquée pendant qu’elle personnalise l’apparence de la fenêtre. Si le **style \_ visible WS** est spécifié dans **CreateWindowEx**, le système envoie le message [**WM \_ ShowWindow**](wm-showwindow.md) à la fenêtre après la création de la fenêtre, mais avant de l’afficher.

Une application peut déterminer si une fenêtre est visible à l’aide de la fonction [**IsWindowVisible**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) . Une application peut afficher (rendre visible) ou masquer une fenêtre à l’aide de la fonction [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow), [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos), [**DeferWindowPos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos)ou [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) ou [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) . Ces fonctions affichent ou masquent une fenêtre en définissant ou en supprimant le style [**WS \_ visible**](window-styles.md) pour la fenêtre. Ils envoient également le message [**\_ ShowWindow WM**](wm-showwindow.md) à la fenêtre avant de l’illustrer ou de le masquer.

Lorsqu’une fenêtre propriétaire est réduite, le système masque automatiquement les fenêtres détenues associées. De même, lorsqu’une fenêtre propriétaire est restaurée, le système affiche automatiquement les fenêtres détenues associées. Dans les deux cas, le système envoie le message [**WM \_ ShowWindow**](wm-showwindow.md) aux fenêtres détenues avant de les masquer ou de les montrer. Parfois, une application peut avoir besoin de masquer les fenêtres détenues sans avoir à réduire ou à masquer le propriétaire. Dans ce cas, l’application utilise la fonction [**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups) . Cette fonction définit ou supprime le style [**WS \_ visible**](window-styles.md) pour toutes les fenêtres détenues et envoie le message **WM \_ ShowWindow** aux fenêtres détenues avant de les masquer ou de les afficher. Le masquage d’une fenêtre propriétaire n’a aucun effet sur l’état de visibilité des fenêtres détenues.

Quand une fenêtre parente est visible, ses fenêtres enfants associées sont également visibles. De même, lorsque la fenêtre parente est masquée, ses fenêtres enfants sont également masquées. La réduction de la fenêtre parente n’a aucun effet sur l’état de visibilité des fenêtres enfants. autrement dit, les fenêtres enfants sont réduites en même temps que le parent, mais le style [**WS \_ visible**](window-styles.md) n’est pas modifié.

Même si une fenêtre a le style [**WS \_ visible**](window-styles.md) , il se peut que l’utilisateur ne soit pas en mesure de voir la fenêtre à l’écran ; les autres fenêtres peuvent se chevaucher complètement ou être déplacées au-delà du bord de l’écran. En outre, une fenêtre enfant visible est soumise aux règles de découpage établies par sa relation parent-enfant. Si la fenêtre parente de la fenêtre n’est pas visible, elle n’est pas non plus visible. Si la fenêtre parente se déplace au-delà du bord de l’écran, la fenêtre enfant se déplace également, car une fenêtre enfant est dessinée par rapport à l’angle supérieur gauche du parent. Par exemple, un utilisateur peut déplacer la fenêtre parente contenant la fenêtre enfant suffisamment loin du bord de l’écran pour que l’utilisateur ne puisse pas voir la fenêtre enfant, même si la fenêtre enfant et sa fenêtre parente possèdent toutes les deux le style **WS \_ visible** .

### <a name="minimized-maximized-and-restored-windows"></a>Fenêtres réduites, agrandies et restaurées

Une *fenêtre agrandie* est une fenêtre avec le style [**WS \_ Maximize**](window-styles.md) . Par défaut, le système élargit une fenêtre agrandie afin qu'elle remplisse l'écran ou la zone cliente d'une fenêtre parente, s'il s'agit d'une fenêtre enfant. Bien que la taille d’une fenêtre puisse être définie sur la même taille qu’une fenêtre agrandie, une fenêtre agrandie est légèrement différente. Le système déplace automatiquement la barre de titre de la fenêtre vers le haut de l’écran ou vers le haut de la zone cliente de la fenêtre parente. En outre, le système désactive la bordure de dimensionnement de la fenêtre et la fonctionnalité de positionnement de la fenêtre de la barre de titre (afin que l’utilisateur ne puisse pas déplacer la fenêtre en faisant glisser la barre de titre).

Une *fenêtre réduite* est une fenêtre avec le style [**WS \_ Minimize**](window-styles.md) . Par défaut, le système diminue une fenêtre réduite jusqu'à la taille de son bouton dans la barre des tâches et la déplace vers la barre des tâches. Une *fenêtre restaurée* est une fenêtre qui a été retournée à sa taille et à sa position précédentes, autrement dit, la taille qu’elle avait avant qu’elle soit réduite ou agrandie.

Si une application spécifie le style [**WS \_ Maximize**](window-styles.md) ou **WS \_ Minimize** dans la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , la fenêtre est initialement agrandie ou réduite. Après la création d’une fenêtre, une application peut utiliser la fonction [**CloseWindow**](/windows/win32/api/winuser/nf-winuser-closewindow) pour réduire la fenêtre. La fonction [**ArrangeIconicWindows**](/windows/win32/api/winuser/nf-winuser-arrangeiconicwindows) réorganise les icônes sur le bureau ou réorganise les fenêtres enfants réduites d’une fenêtre parente dans la fenêtre parente. La fonction [**OpenIcon**](/windows/win32/api/winuser/nf-winuser-openicon) restaure une fenêtre réduite à sa taille et à sa position précédentes.

La fonction [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) peut réduire, agrandir ou restaurer une fenêtre. Il peut également définir les États de visibilité et d’activation de la fenêtre. La fonction [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) comprend les mêmes fonctionnalités que **ShowWindow**, mais elle peut remplacer les positions réduites, agrandies et restaurées par défaut de la fenêtre.

Les fonctions [**IsZoomed**](/windows/win32/api/winuser/nf-winuser-iszoomed) et [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) déterminent si une fenêtre donnée est agrandie ou réduite, respectivement. La fonction [**GetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-getwindowplacement) récupère les positions réduites, agrandies et restaurées pour la fenêtre, et détermine également l’état d’affichage de la fenêtre.

Lorsque le système reçoit une commande pour agrandir ou restaurer une fenêtre réduite, il envoie un message [**WM \_ QUERYOPEN**](wm-queryopen.md) à la fenêtre. Si la procédure de fenêtre retourne la **valeur false**, le système ignore la commande agrandir ou restaurer.

Le système définit automatiquement la taille et la position d’une fenêtre agrandie sur les valeurs par défaut définies par le système pour une fenêtre agrandie. Pour remplacer ces valeurs par défaut, une application peut appeler la fonction [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) ou traiter le message [**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) qui est reçu par une fenêtre lorsque le système est sur le paragraphe d’agrandir la fenêtre. **WM \_ GETMINMAXINFO** comprend un pointeur vers une structure [**minmaxinfo,**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) contenant les valeurs utilisées par le système pour définir la taille et la position agrandies. Le remplacement de ces valeurs remplace les valeurs par défaut.

## <a name="window-size-and-position"></a>Taille et position de la fenêtre

La taille et la position d’une fenêtre sont exprimées sous la forme d’un rectangle englobant, en fonction des coordonnées relatives à l’écran ou à la fenêtre parente. Les coordonnées d’une fenêtre de niveau supérieur sont relatives au coin supérieur gauche de l’écran. les coordonnées d’une fenêtre enfant sont relatives au coin supérieur gauche de la fenêtre parente. Une application spécifie la taille et la position initiales d’une fenêtre lorsqu’elle crée la fenêtre, mais elle peut modifier la taille et la position de la fenêtre à tout moment. Pour plus d’informations, consultez [remplissage de formes](../gdi/filled-shapes.md).

Cette section contient les rubriques suivantes :

-   [Taille et position par défaut](#default-size-and-position)
-   [Taille du suivi](#tracking-size)
-   [Commandes système](#system-commands)
-   [Fonctions de taille et de position](#size-and-position-functions)
-   [Messages de taille et de position](#size-and-position-messages)

### <a name="default-size-and-position"></a>Taille et position par défaut

Une application peut permettre au système de calculer la taille initiale ou la position d’une fenêtre de niveau supérieur en spécifiant CW \_ usedefault dans [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa). Si l’application définit les coordonnées de la fenêtre sur CW \_ usedefault et n’a pas créé d’autres fenêtres de niveau supérieur, le système définit la position de la nouvelle fenêtre par rapport à l’angle supérieur gauche de l’écran ; sinon, elle définit la position par rapport à la position de la fenêtre de niveau supérieur que l’application a créée récemment. Si les paramètres Width et Height sont définis sur CW \_ usedefault, le système calcule la taille de la nouvelle fenêtre. Si l’application a créé d’autres fenêtres de niveau supérieur, le système base la taille de la nouvelle fenêtre sur la taille de la fenêtre de niveau supérieur la plus récemment créée de l’application. Si vous spécifiez CW \_ usedefault lors de la création d’une fenêtre enfant ou indépendante, le système définit la taille de la fenêtre à sa taille minimale par défaut.

### <a name="tracking-size"></a>Taille du suivi

Le système conserve une taille de suivi minimale et maximale pour une fenêtre du style [**WS \_ THICKFRAME**](window-styles.md) ; une fenêtre avec ce style a une bordure de redimensionnement. La *taille de suivi minimale* est la plus petite taille de fenêtre que vous pouvez produire en faisant glisser la bordure de dimensionnement de la fenêtre. De même, la *taille maximale de suivi* est la plus grande taille de fenêtre que vous pouvez produire en faisant glisser la bordure de redimensionnement.

Les tailles de suivi minimales et maximales d’une fenêtre sont définies sur les valeurs par défaut définies par le système lorsque le système crée la fenêtre. Une application peut découvrir les valeurs par défaut et les remplacer en traitant le message [**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) . Pour plus d’informations, consultez [messages relatifs à la taille et](#size-and-position-messages)à la position.

### <a name="system-commands"></a>Commandes système

Une application dotée d’un menu fenêtre peut modifier la taille et la position de cette fenêtre en envoyant des commandes système. Les commandes système sont générées lorsque l’utilisateur choisit des commandes dans le menu fenêtre. Une application peut émuler l’action de l’utilisateur en envoyant un message [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md) à la fenêtre. Les commandes système suivantes affectent la taille et la position d’une fenêtre.



| Commande      | Description                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SC \_ Close    | Ferme la fenêtre. Cette commande envoie un message de [**\_ fermeture WM**](wm-close.md) à la fenêtre. La fenêtre exécute les étapes nécessaires au nettoyage et à la destruction. |
| SC \_ maximiser | Agrandit la fenêtre.                                                                                                                                                |
| SC \_ réduire | Réduit la fenêtre.                                                                                                                                                |
| \_déplacement SC     | Déplace la fenêtre.                                                                                                                                                    |
| \_restauration SC  | Restaure la taille et la position précédentes d’une fenêtre réduite ou agrandie.                                                                                          |
| \_taille SC     | Démarre une commande Size. Pour modifier la taille de la fenêtre, utilisez la souris ou le clavier.                                                                                  |



 

### <a name="size-and-position-functions"></a>Fonctions de taille et de position

Après la création d’une fenêtre, une application peut définir la taille ou la position de la fenêtre en appelant l’une des différentes fonctions, notamment [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement), [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow), [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)et [**DeferWindowPos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos). **SetWindowPlacement** définit la position réduite d’une fenêtre, la position agrandie, la taille et la position restaurées et l’état d’affichage. Les fonctions **MoveWindow** et **SetWindowPos** sont similaires. les deux définissent la taille ou la position d’une seule fenêtre d’application. La fonction **SetWindowPos** comprend un ensemble d’indicateurs qui affectent l’état de l’affichage de la fenêtre ; **MoveWindow** n’inclut pas ces indicateurs. Utilisez les fonctions [**BeginDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-begindeferwindowpos), **DeferWindowPos** et [**EndDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos) pour définir simultanément la position d’un certain nombre de fenêtres, y compris la taille, la position, la position dans l’ordre de plan et l’état d’affichage.

Une application peut récupérer les coordonnées du rectangle englobant d’une fenêtre à l’aide de la fonction [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) . **GetWindowRect** remplit une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) avec les coordonnées des angles supérieur gauche et inférieur droit de la fenêtre. Les coordonnées sont relatives au coin supérieur gauche de l’écran, même pour une fenêtre enfant. La fonction [**ScreenToClient**](/windows/win32/api/winuser/nf-winuser-screentoclient) ou [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) mappe les coordonnées d’écran du rectangle englobant d’une fenêtre enfant à des coordonnées relatives à la zone cliente de la fenêtre parente.

La fonction [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) récupère les coordonnées de la zone cliente d’une fenêtre. **GetClientRect** remplit une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) avec les coordonnées des angles supérieur gauche et inférieur droit de la zone cliente, mais les coordonnées sont relatives à la zone cliente elle-même. Cela signifie que les coordonnées du coin supérieur gauche d’une zone cliente sont toujours (0,0), et les coordonnées du coin inférieur droit sont la largeur et la hauteur de la zone cliente.

La fonction [**CascadeWindows**](/windows/win32/api/winuser/nf-winuser-cascadewindows) cascade les fenêtres sur le bureau ou répercute les fenêtres enfants de la fenêtre parente spécifiée. La fonction [**TileWindows**](/windows/win32/api/winuser/nf-winuser-tilewindows) vignette les fenêtres sur le bureau ou vignette les fenêtres enfants de la fenêtre parente spécifiée.

### <a name="size-and-position-messages"></a>Messages de taille et de position

Le système envoie le message [**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) à une fenêtre dont la taille ou la position est sur le point de changer. Par exemple, le message est envoyé lorsque l’utilisateur clique sur **déplacer** ou **dimensionner** dans le menu fenêtre, ou clique sur la bordure de redimensionnement ou sur la barre de titre. le message est également envoyé lorsqu’une application appelle [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) pour déplacer ou dimensionner la fenêtre. **WM \_ GETMINMAXINFO** comprend un pointeur vers une structure [**minmaxinfo,**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) contenant la taille et la position agrandies par défaut de la fenêtre, ainsi que les tailles de suivi minimales et maximales par défaut. Une application peut remplacer les valeurs par défaut en traitant **WM \_ GETMINMAXINFO** et en définissant les membres appropriés de **minmaxinfo,**. Une fenêtre doit avoir le style [**WS \_ THICKFRAME**](window-styles.md) ou **WS \_ Caption** pour recevoir **WM \_ GETMINMAXINFO**. Une fenêtre avec le style **WS \_ THICKFRAME** reçoit ce message pendant le processus de création de fenêtre, ainsi qu’en cas de déplacement ou de dimensionnement.

Le système envoie le message [**WM \_ WINDOWPOSCHANGING**](wm-windowposchanging.md) à une fenêtre dont la taille, la position, la position dans l’ordre de plan ou l’état d’affichage est sur le point de changer. Ce message comprend un pointeur vers une structure [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) qui spécifie la nouvelle taille de la fenêtre, sa position, sa position dans l’ordre de plan et l’état d’affichage. En définissant les membres de **WINDOWPOS**, une application peut affecter la nouvelle taille, la position et l’apparence de la fenêtre.

Après la modification de la taille, de la position, de la position de la fenêtre dans l’ordre de plan ou de l’affichage de l’État, le système envoie le message [**WM \_ WINDOWPOSCHANGED**](wm-windowposchanged.md) à la fenêtre. Ce message comprend un pointeur vers [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) qui informe la fenêtre de sa nouvelle taille, position, position dans l’ordre de plan et afficher l’État. La définition des membres de la structure **WINDOWPOS** qui est transmise avec **WM \_ WINDOWPOSCHANGED** n’a aucun effet sur la fenêtre. Une fenêtre qui doit traiter les messages de [**\_ taille WM**](wm-size.md) et de [**\_ déplacement WM**](wm-move.md) doit passer le **WM \_ WINDOWPOSCHANGED** à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ; sinon, le système n’envoie pas de messages de **\_ taille WM** et **WM \_ Move** à la fenêtre.

Le système envoie le message [**WM \_ NCCALCSIZE**](wm-nccalcsize.md) à une fenêtre lors de la création ou de la taille de la fenêtre. Le système utilise le message pour calculer la taille de la zone client d’une fenêtre et la position de la zone cliente par rapport à l’angle supérieur gauche de la fenêtre. Une fenêtre passe généralement ce message à la procédure de fenêtre par défaut ; Toutefois, ce message peut être utile dans les applications qui personnalisent la zone non cliente d’une fenêtre ou qui conservent des parties de la zone cliente lorsque la fenêtre est dimensionnée. Pour plus d’informations, consultez [peinture et dessin](../gdi/painting-and-drawing.md).

## <a name="window-animation"></a>Animation de fenêtre

Vous pouvez produire des effets spéciaux lors de l’émission ou du masquage de fenêtres à l’aide de la fonction [**AnimateWindow**](/windows/win32/api/winuser/nf-winuser-animatewindow) . Quand la fenêtre est animée de cette manière, le système effectue une opération de Roll, de glissement ou de disparition en fondu de la fenêtre, selon les indicateurs que vous spécifiez dans un appel à **AnimateWindow**.

Par défaut, le système utilise l' *animation de roulement*. Avec cet effet, la fenêtre s’affiche pour lancer l’ouverture (affichage de la fenêtre) ou la roulette fermée (masquage de la fenêtre). Vous pouvez utiliser le paramètre *dwFlags* pour spécifier si la fenêtre est dérouler horizontalement, verticalement ou en diagonale.

Lorsque vous spécifiez l’indicateur de **\_ diapositive aw** , le système utilise l' *animation de diapositives*. Avec cet effet, la fenêtre s’affiche pour faire une diapositive dans l’affichage (affichage de la fenêtre) ou détourer de l’affichage (masquage de la fenêtre). Vous pouvez utiliser le paramètre *dwFlags* pour spécifier si la fenêtre glisse horizontalement, verticalement ou en diagonale.

Lorsque vous spécifiez l’indicateur **aw \_ Blend** , le système utilise un *fondu à fusion alpha*.

Vous pouvez également utiliser l’indicateur **aw \_ Center** pour faire apparaître une fenêtre pour la réduire vers l’intérieur ou l’étendre vers l’extérieur.

## <a name="window-layout-and-mirroring"></a>Disposition des fenêtres et mise en miroir

La disposition de la fenêtre définit comment les objets de texte et les objets GDI (Windows Graphics Device Interface) sont disposés dans une fenêtre ou un contexte de périphérique (DC). Certains langages, tels que l’anglais, le français et l’allemand, requièrent une disposition de gauche à droite (LTR). D’autres langages, tels que l’arabe et l’hébreu, requièrent une disposition de droite à gauche (RTL). La disposition de la fenêtre s’applique au texte, mais affecte également les autres éléments GDI de la fenêtre, y compris les bitmaps, les icônes, l’emplacement de l’origine, les boutons, les contrôles d’arborescence en cascade et si la coordonnée horizontale augmente au fur et à mesure que vous vous rendez à gauche ou à droite. Par exemple, une fois qu’une application a défini la disposition RTL, l’origine est positionnée sur le bord droit de la fenêtre ou du périphérique, et le nombre représentant la coordonnée horizontale augmente à mesure que vous déplacez la gauche. Toutefois, tous les objets ne sont pas affectés par la disposition d’une fenêtre. Par exemple, la disposition pour les boîtes de dialogue, les boîtes de message et les contextes de périphérique qui ne sont pas associés à une fenêtre, tels que les contrôleurs de schéma et les DC d’imprimante, doit être gérée séparément. Les spécificités de ces dernières sont mentionnées plus loin dans cette rubrique.

Les fonctions de fenêtre vous permettent de spécifier ou de modifier la disposition des fenêtres en arabe et en hébreu dans les versions de Windows. Notez que le passage à une disposition RTL (également connue sous le nom de mise en miroir) n’est pas pris en charge pour les fenêtres qui ont le style [cs \_ OWNDC](about-window-classes.md) ou pour un contrôleur de périphérique avec le \_ mode graphique GM Advanced.

Par défaut, la disposition de la fenêtre est de gauche à droite (LTR). Pour définir la disposition de fenêtre RTL, appelez [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) avec le style **WS \_ ex \_ LAYOUTRTL**. De même, par défaut, une fenêtre enfant (autrement dit, celle créée avec le style [**WS \_ enfant**](window-styles.md) et avec un paramètre *HWND* parent valide dans l’appel à [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou **CreateWindowEx**) a la même disposition que son parent. Pour désactiver l’héritage de la mise en miroir pour toutes les fenêtres enfants, spécifiez **WS \_ ex \_ NOINHERITLAYOUT** dans l’appel à **CreateWindowEx**. Notez que la mise en miroir n’est pas héritée par les fenêtres détenues (celles créées sans le style **WS \_ Child** ) ou celles créées avec le paramètre *HWND* parent de **CreateWindowEx** ayant la valeur **null**. Pour désactiver l’héritage de la mise en miroir pour une fenêtre individuelle, traitez le message [**WM \_ NCCREATE**](wm-nccreate.md) avec [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) et [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) pour désactiver l’indicateur **WS \_ ex \_ LAYOUTRTL** . Ce traitement s’ajoute à tout autre traitement nécessaire. Le fragment de code suivant montre comment procéder.


```
SetWindowLong (hWnd, 
               GWL_EXSTYLE, 
               GetWindowLong(hWnd,GWL_EXSTYLE) & ~WS_EX_LAYOUTRTL))
```



Vous pouvez définir la disposition par défaut sur RTL en appelant [**SetProcessDefaultLayout**](/windows/win32/api/winuser/nf-winuser-setprocessdefaultlayout)(disposition \_ RTL). Toutes les fenêtres créées après l’appel seront mises en miroir, mais les fenêtres existantes ne seront pas affectées. Pour désactiver la mise en miroir par défaut, appelez **SetProcessDefaultLayout**(0).

Notez que [**SetProcessDefaultLayout**](/windows/win32/api/winuser/nf-winuser-setprocessdefaultlayout) reflète uniquement les contrôleurs de jeu des fenêtres mises en miroir. Pour mettre en miroir n’importe quel contrôleur de contrôleur, appelez [**setLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout)(HDC, disposition \_ RTL). Pour plus d’informations, consultez la discussion sur la mise en miroir des contextes de périphérique non associés à Windows, qui est abordé plus loin dans cette rubrique.

Les bitmaps et les icônes dans une fenêtre mise en miroir sont également mises en miroir par défaut. Toutefois, ces derniers ne doivent pas être mis en miroir. Par exemple, les personnes qui ont du texte, un logo commercial ou une horloge analogique ne doivent pas être mises en miroir. Pour désactiver la mise en miroir des bitmaps, appelez [**setLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout) avec le \_ bit layout BITMAPORIENTATIONPRESERVED bit défini dans *dwLayout*. Pour désactiver la mise en miroir dans un DC, appelez **setLayout**(HDC, 0).

Pour interroger la disposition par défaut actuelle, appelez [**GetProcessDefaultLayout**](/windows/win32/api/winuser/nf-winuser-getprocessdefaultlayout). EN cas de retour correct, *pdwDefaultLayout* contient la disposition \_ RTL ou 0. Pour interroger les paramètres de disposition du contexte de périphérique, appelez [**GetLayout**](/windows/win32/api/wingdi/nf-wingdi-getlayout). En cas de retour correct, **GetLayout** retourne une **valeur DWORD** qui indique les paramètres de disposition selon les paramètres de la disposition \_ RTL et de la disposition \_ BITMAPORIENTATIONPRESERVED bits.

Après la création d’une fenêtre, vous modifiez la disposition à l’aide de la fonction [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) . Par exemple, cela est nécessaire lorsque l’utilisateur change la langue de l’interface utilisateur d’une fenêtre existante en arabe ou en Hébreu. Toutefois, lorsque vous modifiez la disposition d’une fenêtre existante, vous devez invalider et mettre à jour la fenêtre pour vous assurer que le contenu de la fenêtre est bien dessiné sur la même disposition. L’exemple de code suivant provient d’un exemple de code qui modifie la disposition des fenêtres en fonction des besoins :


```
// Using ANSI versions of GetWindowLong and SetWindowLong because Unicode
// is not needed for these calls

lExStyles = GetWindowLongA(hWnd, GWL_EXSTYLE);

// Check whether new layout is opposite the current layout
if (!!(pLState -> IsRTLLayout) != !!(lExStyles & WS_EX_LAYOUTRTL))
{
    // the following lines will update the window layout

    lExStyles ^= WS_EX_LAYOUTRTL;        // toggle layout
    SetWindowLongA(hWnd, GWL_EXSTYLE, lExStyles);
    InvalidateRect(hWnd, NULL, TRUE);    // to update layout in the client area
}
```



Dans la mise en miroir, vous devez penser en termes de « Near » et « Far » au lieu de « Left » et « Right ». Dans le cas contraire, vous risquez de rencontrer des problèmes. Une pratique de codage commune qui provoque des problèmes dans une fenêtre mise en miroir se produit lors du mappage entre les coordonnées d’écran et les coordonnées clientes. Par exemple, les applications utilisent souvent du code semblable au suivant pour positionner un contrôle dans une fenêtre :


```
// DO NOT USE THIS IF APPLICATION MIRRORS THE WINDOW

// get coordinates of the window in screen coordinates
GetWindowRect(hControl, (LPRECT) &rControlRect);  

// map screen coordinates to client coordinates in dialog
ScreenToClient(hDialog, (LPPOINT) &rControlRect.left); 
ScreenToClient(hDialog, (LPPOINT) &rControlRect.right);
```



Cela entraîne des problèmes de mise en miroir, car le bord gauche du rectangle devient le bord droit dans une fenêtre mise en miroir, et vice versa. Pour éviter ce problème, remplacez les appels [**ScreenToClient**](/windows/win32/api/winuser/nf-winuser-screentoclient) par un appel à [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) comme suit :


```
// USE THIS FOR MIRRORING

GetWindowRect(hControl, (LPRECT) &rControlRect);
MapWindowPoints(NULL, hDialog, (LPPOINT) &rControlRect, 2)
```



Ce code fonctionne, car, sur les plateformes qui prennent en charge la mise en miroir, [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) est modifié pour permuter les coordonnées de point gauche et droit lorsque la fenêtre du client est mise en miroir. Pour plus d’informations, consultez la section Notes de **MapWindowPoints**.

Une autre pratique courante qui peut provoquer des problèmes dans les fenêtres mises en miroir consiste à positionner les objets dans une fenêtre cliente à l’aide de décalages dans les coordonnées d’écran au lieu de coordonnées clientes. Par exemple, le code suivant utilise la différence en coordonnées d’écran comme position x dans les coordonnées clientes pour positionner un contrôle dans une boîte de dialogue.


```
// OK if LTR layout and mapping mode of client is MM_TEXT,
// but WRONG for a mirrored dialog 

RECT rdDialog;
RECT rcControl;

HWND hControl = GetDlgItem(hDlg, IDD_CONTROL);
GetWindowRect(hDlg, &rcDialog);             // gets rect in screen coordinates
GetWindowRect(hControl, &rcControl);
MoveWindow(hControl,
           rcControl.left - rcDialog.left,  // uses x position in client coords
           rcControl.top - rcDialog.top,
           nWidth,
           nHeight,
           FALSE);
```



Ce code est parfait quand la fenêtre de boîte de dialogue a une disposition de gauche à droite (LTR) et que le mode de mappage du client est de MM de \_ texte, car la nouvelle position x dans les coordonnées clientes correspond à la différence dans les bords gauches du contrôle et à la boîte de dialogue en coordonnées d’écran. Toutefois, dans une boîte de dialogue mise en miroir, les gauche et droit sont inversés. vous devez donc utiliser [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) comme suit :


```
RECT rcDialog;
RECT rcControl;

HWND hControl - GetDlgItem(hDlg, IDD_CONTROL);
GetWindowRect(hControl, &rcControl);

// MapWindowPoints works correctly in both mirrored and non-mirrored windows.
MapWindowPoints(NULL, hDlg, (LPPOINT) &rcControl, 2);

// Now rcControl is in client coordinates.
MoveWindow(hControl, rcControl.left, rcControl.top, nWidth, nHeight, FALSE)
```



### <a name="mirroring-dialog-boxes-and-message-boxes"></a>Boîtes de dialogue de mise en miroir et boîtes de message

Les boîtes de dialogue et les boîtes de message n’héritent pas de la disposition. vous devez donc définir explicitement la disposition. Pour mettre en miroir une boîte de message, appelez [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) ou [**MessageBoxEx**](/windows/win32/api/winuser/nf-winuser-messageboxexa) avec l’option **MB \_ RTLREADING** . Pour mettre en forme une boîte de dialogue de droite à gauche, utilisez le style étendu WS \_ ex \_ LAYOUTRTL dans la structure de modèle de boîte de dialogue [**DLGTEMPLATEEX**](../dlgbox/dlgtemplateex.md). Les feuilles de propriétés sont un cas particulier de boîtes de dialogue. Chaque onglet étant traité comme une boîte de dialogue distincte, vous devez inclure le style WS \_ ex \_ LAYOUTRTL dans chaque onglet que vous souhaitez mettre en miroir.

### <a name="mirroring-device-contexts-not-associated-with-a-window"></a>Mise en miroir de contextes de périphérique non associés à une fenêtre

Les contrôleurs de schéma qui ne sont pas associés à une fenêtre, tels que des DC de métafichier ou d’imprimante, n’héritent pas de la disposition. vous devez donc définir explicitement la disposition. Pour modifier la disposition du contexte de périphérique, utilisez la fonction [**setLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout) .

La fonction [**setLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout) est rarement utilisée avec Windows. En général, Windows reçoit un contrôleur de périphérique associé uniquement dans le traitement d’un message de [**\_ peinture WM**](../gdi/wm-paint.md) . Parfois, un programme crée un contrôleur de périphérique pour une fenêtre en appelant [**GetDC**](/windows/win32/api/winuser/nf-winuser-getdc). Dans les deux cas, la disposition initiale du DC est définie par [**BeginPaint**](/windows/win32/api/winuser/nf-winuser-beginpaint) ou **GetDC** en fonction de l’indicateur WS ex LAYOUTRTL de la fenêtre \_ \_ .

Les valeurs retournées par [**GetWindowOrgEx**](/windows/win32/api/wingdi/nf-wingdi-getwindoworgex), [**GetWindowExtEx**](/windows/win32/api/wingdi/nf-wingdi-getwindowextex), [**GetViewportOrgEx**](/windows/win32/api/wingdi/nf-wingdi-getviewportorgex) et [**GetViewportExtEx**](/windows/win32/api/wingdi/nf-wingdi-getviewportextex) ne sont pas affectées par l’appel à [**setLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout).

Lorsque la disposition est RTL, [**GetMapMode**](/windows/win32/api/wingdi/nf-wingdi-getmapmode) retourne mm \_ anisotrope au lieu de mm de \_ texte. L’appel de [**SetMapMode**](/windows/win32/api/wingdi/nf-wingdi-setmapmode) avec \_ le texte de mm fonctionne correctement ; seule la valeur de retour de **GetMapMode** est affectée. De même, l’appel de [**setLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout)(HDC, disposition \_ RTL) quand le mode de mappage est de mm de \_ texte entraîne la modification du mode de mappage signalé en mm \_ anisotrope.

## <a name="window-destruction"></a>Destruction de fenêtre

En général, une application doit détruire toutes les fenêtres qu’elle crée. Pour ce faire, il utilise la fonction [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) . Quand une fenêtre est détruite, le système masque la fenêtre, si elle est visible, puis supprime toutes les données internes associées à la fenêtre. Cela invalide le handle de fenêtre, qui ne peut plus être utilisé par l’application.

Une application détruit un grand nombre des fenêtres qu’elle crée peu après les avoir créées. Par exemple, une application détruit généralement une fenêtre de boîte de dialogue dès que l’application a suffisamment d’entrées de la part de l’utilisateur pour poursuivre sa tâche. Une application détruit finalement la fenêtre principale de l’application (avant de se terminer).

Avant de détruire une fenêtre, une application doit enregistrer ou supprimer toutes les données associées à la fenêtre, et elle doit libérer toutes les ressources système allouées pour la fenêtre. Si l’application ne libère pas les ressources, le système libère toutes les ressources qui ne sont pas libérées par l’application.

La destruction d’une fenêtre n’affecte pas la classe de fenêtre à partir de laquelle la fenêtre est créée. De nouvelles fenêtres peuvent toujours être créées à l’aide de cette classe, et toutes les fenêtres existantes de cette classe continuent à fonctionner. La destruction d’une fenêtre détruit également les fenêtres descendantes de la fenêtre. La fonction [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) envoie tout d’abord un message de [**\_ destruction WM**](wm-destroy.md) à la fenêtre, puis à ses fenêtres enfants et fenêtres descendantes. De cette façon, toutes les fenêtres descendantes de la fenêtre détruite sont également détruites.

Une fenêtre avec un menu fenêtre reçoit un message de [**\_ fermeture WM**](wm-close.md) lorsque l’utilisateur clique sur **Fermer**. En traitant ce message, une application peut demander confirmation à l’utilisateur avant de détruire la fenêtre. Si l’utilisateur confirme que la fenêtre doit être détruite, l’application peut appeler la fonction [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) pour détruire la fenêtre.

Si la fenêtre qui est détruite est la fenêtre active, les États actif et actif sont transférés vers une autre fenêtre. La fenêtre qui devient la fenêtre active est la fenêtre suivante, telle que déterminée par la combinaison de touches ALT + ÉCHAP. La nouvelle fenêtre active détermine ensuite la fenêtre qui reçoit le focus clavier.

 

 
