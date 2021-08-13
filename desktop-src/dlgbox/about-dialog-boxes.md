---
title: à propos des boîtes de dialogue
description: Cette rubrique décrit l’utilisation de boîtes de dialogue pour créer des interfaces utilisateur pour les applications.
ms.assetid: 51960c28-a178-4ad3-b45e-426fec42a945
keywords:
- boîtes de dialogue, à propos de
- boîtes de dialogue, quand les utiliser
- boîtes de dialogue modales
- boîtes de dialogue non modales
- boîtes de dialogue, modales
- boîtes de dialogue, non modales
- boîtes de dialogue, modèles
- boîtes de dialogue, fenêtres de propriétaire
- boîtes de dialogue, boîtes de message
- procédures de boîte de dialogue
- boîtes de message
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7855ba67a04558e0df8ffad0f63d2bd78856f84829bf029fbf811a4b89eb4b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786807"
---
# <a name="about-dialog-boxes"></a>à propos des boîtes de dialogue

Il existe de nombreuses fonctions, messages et contrôles prédéfinis pour faciliter la création et la gestion des boîtes de dialogue, ce qui facilite le développement de l’interface utilisateur d’une application. Cette vue d’ensemble décrit les fonctions et les messages de la boîte de dialogue et explique comment les utiliser pour créer et utiliser des boîtes de dialogue.

Cette vue d’ensemble comprend les rubriques suivantes :

-   [Quand utiliser une boîte de dialogue](#when-to-use-a-dialog-box)
-   [Fenêtre propriétaire de la boîte de dialogue](#dialog-box-owner-window)
-   [Boîtes de message](#message-boxes)
-   [Boîtes de dialogue modales](#modal-dialog-boxes)
-   [Boîtes de dialogue non modales](#modeless-dialog-boxes)
-   [Modèles de boîte de dialogue](#dialog-box-templates)
    -   [Styles de modèles de boîte de dialogue](#dialog-box-template-styles)
    -   [Mesures de la boîte de dialogue](#dialog-box-measurements)
    -   [Contrôles de boîte de dialogue](#dialog-box-controls)
    -   [Menu de la boîte de dialogue](#dialog-box-window-menu)
    -   [Polices de boîte de dialogue](#dialog-box-fonts)
    -   [Modèles en mémoire](#templates-in-memory)

Pour plus d’informations sur les boîtes de dialogue communes, consultez Bibliothèque de boîtes de [dialogue communes](common-dialog-box-library.md).

## <a name="when-to-use-a-dialog-box"></a>Quand utiliser une boîte de dialogue

La plupart des applications utilisent des boîtes de dialogue pour demander des informations supplémentaires pour les éléments de menu qui nécessitent une entrée d’utilisateur. L’utilisation d’une boîte de dialogue est la seule méthode recommandée pour qu’une application récupère l’entrée. Par exemple, un élément de menu **ouvert** classique requiert le nom d’un fichier à ouvrir, de sorte qu’une application doit utiliser une boîte de dialogue pour inviter l’utilisateur à entrer le nom. Dans ce cas, l’application crée la boîte de dialogue lorsque l’utilisateur clique sur l’élément de menu et détruit la boîte de dialogue immédiatement après que l’utilisateur a fourni les informations.

De nombreuses applications utilisent également des boîtes de dialogue pour afficher des informations ou des options lorsque l’utilisateur travaille dans une autre fenêtre. Par exemple, les applications de traitement de texte utilisent souvent une boîte de dialogue avec une option de recherche de texte. Lorsque l’application recherche le texte, la boîte de dialogue reste à l’écran. L’utilisateur peut ensuite revenir à la boîte de dialogue et rechercher le même mot. ou l’utilisateur peut modifier l’entrée dans la boîte de dialogue et Rechercher un nouveau mot. En général, les applications qui utilisent des boîtes de dialogue en créent une lorsque l’utilisateur clique sur l’élément de menu et continuent à l’afficher tant que l’application s’exécute ou jusqu’à ce que l’utilisateur ferme explicitement la boîte de dialogue.

Pour prendre en charge les différents modes d’utilisation des boîtes de dialogue par les applications, il existe deux types de boîte de dialogue : modal et non modal. Une *boîte de dialogue modale* demande à l’utilisateur de fournir des informations ou d’annuler la boîte de dialogue avant de permettre à l’application de continuer. Les applications utilisent des boîtes de dialogue modales conjointement avec les éléments de menu qui requièrent des informations supplémentaires avant de pouvoir continuer. Une *boîte de dialogue non modale* permet à l’utilisateur de fournir des informations et de revenir à la tâche précédente sans fermer la boîte de dialogue. Les boîtes de dialogue modales sont plus simples à gérer que les boîtes de dialogue non modales, car elles sont créées, exécutent leur tâche et sont détruites en appelant une fonction unique.

Pour créer une boîte de dialogue modale ou non modale, une application doit fournir un modèle de boîte de dialogue pour décrire le style et le contenu de la boîte de dialogue ; l’application doit également fournir une procédure de boîte de dialogue pour effectuer des tâches. Le *modèle de boîte de dialogue* est une description binaire de la boîte de dialogue et des contrôles qu’il contient. Le développeur peut créer ce modèle en tant que ressource à charger à partir du fichier exécutable de l’application, ou créé en mémoire pendant l’exécution de l’application. La *procédure de boîte de dialogue* est une fonction de rappel définie par l’application que le système appelle lorsqu’il a une entrée pour la boîte de dialogue ou les tâches de la boîte de dialogue à exécuter. Bien qu’une procédure de boîte de dialogue soit similaire à une procédure de fenêtre, elle n’a pas les mêmes responsabilités.

Une application crée généralement une boîte de dialogue à l’aide de la fonction [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) ou [**createDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) . **DialogBox** crée une boîte de dialogue modale. **CreateDialog** crée une boîte de dialogue non modale. Ces deux fonctions chargent un modèle de boîte de dialogue à partir du fichier exécutable de l’application et créent une fenêtre indépendante qui correspond aux spécifications du modèle. D’autres fonctions créent une boîte de dialogue à l’aide de modèles en mémoire ; ils transmettent des informations supplémentaires à la procédure de boîte de dialogue lors de la création de la boîte de dialogue.

Les boîtes de dialogue appartiennent généralement à une classe de fenêtre exclusive prédéfinie. Le système utilise cette classe de fenêtre et la procédure de fenêtre correspondante pour les boîtes de dialogue modales et non modales. Lorsque la fonction est appelée, elle crée la fenêtre pour la boîte de dialogue, ainsi que les fenêtres pour les contrôles de la boîte de dialogue, puis envoie les messages sélectionnés à la procédure de la boîte de dialogue. Lorsque la boîte de dialogue est visible, la procédure de fenêtre prédéfinie gère tous les messages, en traitant certains messages et en passant d’autres à la procédure de la boîte de dialogue afin que la procédure puisse effectuer des tâches. Les applications n’ont pas d’accès direct à la classe de fenêtre prédéfinie ou à la procédure de fenêtre, mais elles peuvent utiliser le modèle de boîte de dialogue et la procédure de boîte de dialogue pour modifier le style et le comportement d’une boîte de dialogue.

## <a name="dialog-box-owner-window"></a>Fenêtre propriétaire de la boîte de dialogue

La plupart des boîtes de dialogue ont une fenêtre propriétaire (ou plus simplement un propriétaire). Lors de la création de la boîte de dialogue, l’application définit le propriétaire en spécifiant le descripteur de fenêtre du propriétaire. Le système utilise le propriétaire pour déterminer la position de la boîte de dialogue dans l’ordre décroissant afin que la boîte de dialogue soit toujours positionnée au-dessus de son propriétaire. En outre, le système peut envoyer des messages à la procédure de fenêtre du propriétaire, en l’avertissant des événements dans la boîte de dialogue.

Le système masque ou détruit automatiquement la boîte de dialogue chaque fois que son propriétaire est masqué ou détruit. Cela signifie que la procédure de la boîte de dialogue ne nécessite aucun traitement spécial pour détecter les modifications apportées à l’état de la fenêtre propriétaire.

Étant donné que la boîte de dialogue standard est utilisée conjointement avec un élément de menu, la fenêtre propriétaire correspond généralement à la fenêtre qui contient le menu. Bien qu’il soit possible de créer une boîte de dialogue qui n’a pas de propriétaire, cela n’est pas recommandé. Par exemple, lorsqu’une boîte de dialogue modale n’a pas de propriétaire, le système ne désactive aucune des autres fenêtres de l’application et permet à l’utilisateur de continuer à effectuer des tâches dans les autres fenêtres, en désactivant l’objectif de la boîte de dialogue modale.

Quand une boîte de dialogue non modale n’a pas de propriétaire, le système ne masque pas et ne détruit pas la boîte de dialogue lorsque d’autres fenêtres de l’application sont masquées ou détruites. Bien que cela n’annule pas l’objectif de la boîte de dialogue non modale, elle nécessite que l’application exécute un traitement spécial pour s’assurer que la boîte de dialogue est masquée et détruite aux moments opportuns.

## <a name="message-boxes"></a>Boîtes de message

Une boîte de message est une boîte de dialogue spéciale qu’une application peut utiliser pour afficher des messages et demander une entrée simple. Une boîte de message contient généralement un message texte et un ou plusieurs boutons. Une application crée la boîte de message à l’aide de la fonction [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) ou [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) , en spécifiant le texte et le nombre et les types de boutons à afficher. Notez qu’il n’y a actuellement aucune différence entre la façon dont **MessageBox** et **MessageBoxEx** fonctionnent.

Bien que la boîte de message soit une boîte de dialogue, le système prend le contrôle total de la création et de la gestion de la boîte de message. Cela signifie que l’application ne fournit pas de modèle de boîte de dialogue et de procédure de boîte de dialogue. Le système crée son propre modèle en fonction du texte et des boutons spécifiés pour la boîte de message et fournit sa propre procédure de boîte de dialogue.

Une boîte de message est une boîte de dialogue modale et le système la crée à l’aide des fonctions internes utilisées par [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) . Si l’application spécifie une fenêtre propriétaire lors de l’appel de [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) ou de [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa), le système désactive le propriétaire. Une application peut également demander au système de désactiver toutes les fenêtres de niveau supérieur appartenant au thread actuel en spécifiant la valeur de **\_ TASKMODAL Mo** lors de la création de la boîte de dialogue.

Le système peut envoyer des messages au propriétaire, tels que [**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) et [**WM \_ Enable**](/windows/desktop/winmsg/wm-enable), comme c’est le cas lors de la création d’une boîte de dialogue modale. La fenêtre propriétaire doit exécuter toutes les actions demandées par ces messages.

## <a name="modal-dialog-boxes"></a>Boîtes de dialogue modales

Une boîte de dialogue modale doit être une fenêtre indépendante contenant un menu fenêtre, une barre de titre et une bordure épaisse. autrement dit, le modèle de boîte de dialogue doit spécifier les styles **WS \_ Popup**, **WS \_ SYSMENU**, **WS \_ Caption** et **DS \_ MODALFRAME** . Bien qu’une application puisse désigner le style **\_ visible WS** , le système affiche toujours une boîte de dialogue modale, que le modèle de boîte de dialogue spécifie ou non le style **\_ visible WS** . Une application ne doit pas créer une boîte de dialogue modale avec le style **WS \_ enfant** . Une boîte de dialogue modale avec ce style est désactivée, empêchant toute entrée ultérieure d’atteindre l’application.

Une application crée une boîte de dialogue modale à l’aide de la fonction [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) ou [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) . **DialogBox** requiert le nom ou l’identificateur d’une ressource contenant un modèle de boîte de dialogue ; **DialogBoxIndirect** requiert un handle vers un objet mémoire contenant un modèle de boîte de dialogue. Les fonctions [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) et [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama) créent également des boîtes de dialogue modales. ils sont identiques aux fonctions mentionnées précédemment, mais transmettent un paramètre spécifié à la procédure de boîte de dialogue lors de la création de la boîte de dialogue.

Lors de la création de la boîte de dialogue modale, le système en fait la fenêtre active. La boîte de dialogue reste active jusqu’à ce que la procédure de la boîte de dialogue appelle la fonction [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) ou que le système active une fenêtre dans une autre application. L’utilisateur et l’application ne peuvent pas activer la fenêtre propriétaire tant que la boîte de dialogue modale n’a pas été détruite.

Lorsque la fenêtre propriétaire n’est pas encore désactivée, le système désactive automatiquement la fenêtre et toutes les fenêtres enfants qui lui appartiennent lors de la création de la boîte de dialogue modale. La fenêtre propriétaire reste désactivée jusqu’à ce que la boîte de dialogue soit détruite. Bien qu’une procédure de boîte de dialogue puisse potentiellement activer la fenêtre propriétaire à tout moment, l’activation du propriétaire dégrade l’objectif de la boîte de dialogue modale et n’est pas recommandée. Lorsque la procédure de la boîte de dialogue est détruite, le système active à nouveau la fenêtre propriétaire, mais uniquement si la boîte de dialogue modale a provoqué la désactivation du propriétaire.

Au fur et à mesure que le système crée la boîte de dialogue modale, il envoie le message [**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) à la fenêtre (le cas échéant) qui capture actuellement l’entrée de la souris. Une application qui reçoit ce message doit libérer la capture de la souris afin que l’utilisateur puisse déplacer la souris dans la boîte de dialogue modale. Étant donné que le système désactive la fenêtre propriétaire, toutes les entrées de la souris sont perdues si le propriétaire ne parvient pas à libérer la souris lors de la réception de ce message.

Pour traiter les messages de la boîte de dialogue modale, le système démarre sa propre boucle de message, en tenant le contrôle temporaire de la file d’attente de messages pour l’application entière. Lorsque le système récupère un message qui n’est pas explicitement pour la boîte de dialogue, il distribue le message à la fenêtre appropriée. S’il récupère un message [**WM \_ Quit**](/windows/desktop/winmsg/wm-quit) , il publie le message dans la file d’attente de messages d’application afin que la boucle de message principale de l’application puisse récupérer le message.

Le système envoie le message [**WM \_ ENTERIDLE**](wm-enteridle.md) à la fenêtre propriétaire chaque fois que la file d’attente de messages d’application est vide. L’application peut utiliser ce message pour effectuer une tâche en arrière-plan pendant que la boîte de dialogue reste à l’écran. Quand une application utilise le message de cette manière, l’application doit souvent obtenir le contrôle (par exemple, à l’aide de la fonction [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) ) afin que la boîte de dialogue modale puisse recevoir toute entrée d’utilisateur. Pour empêcher la boîte de dialogue modale d’envoyer les messages **WM \_ ENTERIDLE** , l’application peut spécifier le \_ style DS NOIDLEMSG lors de la création de la boîte de dialogue.

Une application détruit une boîte de dialogue modale à l’aide de la fonction [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) . Dans la plupart des cas, la procédure de la boîte de dialogue appelle **EndDialog** lorsque l’utilisateur clique sur **Fermer** dans le menu fenêtre de la boîte de dialogue ou clique sur le bouton **OK** ou **Annuler** dans la boîte de dialogue. La boîte de dialogue peut retourner une valeur par le biais de la fonction [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) (ou d’autres fonctions de création) en spécifiant une valeur lors de l’appel de la fonction **EndDialog** . Le système retourne cette valeur après avoir détruit la boîte de dialogue. La plupart des applications utilisent cette valeur de retour pour déterminer si la boîte de dialogue a réussi sa tâche ou a été annulée par l’utilisateur. Le système ne retourne pas le contrôle à partir de la fonction qui crée la boîte de dialogue tant que la procédure de la boîte de dialogue n’a pas appelé la fonction **EndDialog** .

## <a name="modeless-dialog-boxes"></a>Boîtes de dialogue non modales

Une boîte de dialogue non modale doit être une fenêtre indépendante contenant un menu fenêtre, une barre de titre et une bordure fine. autrement dit, le modèle de boîte de dialogue doit spécifier les styles **WS \_ Popup**, **WS \_ Caption**, **WS \_ Border** et **WS \_ SYSMENU** . Le système n’affiche pas automatiquement la boîte de dialogue, sauf si le modèle spécifie le style **WS \_ visible** .

Une application crée une boîte de dialogue non modale à l’aide de la fonction [**createDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) ou [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta) . **CreateDialog** requiert le nom ou l’identificateur d’une ressource contenant un modèle de boîte de dialogue ; **CreateDialogIndirect** requiert un handle vers un objet mémoire contenant un modèle de boîte de dialogue. Deux autres fonctions, [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama) et [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), créent également des boîtes de dialogue non modales. ils transmettent un paramètre spécifié à la procédure de boîte de dialogue lors de la création de la boîte de dialogue.

[**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) et d’autres fonctions de création retournent un handle de fenêtre à la boîte de dialogue. L’application et la procédure de boîte de dialogue peuvent utiliser ce handle pour gérer la boîte de dialogue. Par exemple, si **WS \_ visible** n’est pas spécifié dans le modèle de boîte de dialogue, l’application peut afficher la boîte de dialogue en passant le handle de fenêtre à la fonction [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) .

Une boîte de dialogue non modale ne désactive pas la fenêtre propriétaire et n’envoie pas de messages à celle-ci. Lors de la création de la boîte de dialogue, le système en fait la fenêtre active, mais l’utilisateur ou l’application peut modifier la fenêtre active à tout moment. Si la boîte de dialogue devient inactive, elle reste au-dessus de la fenêtre propriétaire dans l’ordre de plan, même si la fenêtre propriétaire est active.

L’application est responsable de la récupération et de la distribution des messages d’entrée à la boîte de dialogue. La plupart des applications utilisent la boucle de messages principale pour cela. Toutefois, pour permettre à l’utilisateur de déplacer et de sélectionner des contrôles à l’aide du clavier, l’application doit appeler la fonction [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) . Pour plus d’informations sur cette fonction, consultez [interface de clavier de la boîte de dialogue](dlgbox-programming-considerations.md).

Une boîte de dialogue non modale ne peut pas retourner de valeur à l’application sous forme de boîte de dialogue modale, mais la procédure de la boîte de dialogue peut envoyer des informations à la fenêtre propriétaire à l’aide de la fonction [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) .

Une application doit détruire toutes les boîtes de dialogue non modales avant de se terminer. Il peut détruire une boîte de dialogue non modale à l’aide de la fonction [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) . Dans la plupart des cas, la procédure de la boîte de dialogue appelle **DestroyWindow** en réponse à une entrée utilisateur, par exemple en cliquant sur le bouton **Annuler** . Si l’utilisateur ne ferme jamais la boîte de dialogue de cette manière, l’application doit appeler **DestroyWindow**.

[**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) invalide le handle de fenêtre de la boîte de dialogue, donc tous les appels suivants aux fonctions qui utilisent le handle retournent des valeurs d’erreur. Pour éviter les erreurs, la procédure de la boîte de dialogue doit informer le propriétaire que la boîte de dialogue a été détruite. De nombreuses applications conservent une variable globale contenant le descripteur de la boîte de dialogue. Lorsque la procédure de la boîte de dialogue détruit la boîte de dialogue, elle définit également la variable globale sur la **valeur null**, ce qui indique que la boîte de dialogue n’est plus valide.

La procédure de la boîte de dialogue ne doit pas appeler la fonction [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) pour détruire une boîte de dialogue non modale.

## <a name="dialog-box-templates"></a>Modèles de boîte de dialogue

Un modèle de boîte de dialogue contient des données binaires qui décrivent la boîte de dialogue, définissant sa hauteur, sa largeur, son style et les contrôles qu’elle contient. Pour créer une boîte de dialogue, le système charge un modèle de boîte de dialogue à partir des ressources du fichier exécutable de l’application ou utilise le modèle qui lui est passé dans la mémoire globale par l’application. Dans les deux cas, l’application doit fournir un modèle lors de la création d’une boîte de dialogue.

Un développeur crée des ressources de modèle à l’aide d’un compilateur de ressources ou d’un éditeur de boîtes de dialogue. Un compilateur de ressources convertit une description de texte en ressource binaire, et un éditeur de boîtes de dialogue enregistre une boîte de dialogue construite de manière interactive en tant que ressource binaire.

> [!Note]  
> Une explication de la manière de créer des ressources de modèle et de les ajouter au fichier exécutable de l’application dépasse le cadre de cette vue d’ensemble. Pour plus d’informations sur la création de ressources de modèle et leur ajout à un fichier exécutable, consultez la documentation fournie avec vos outils de développement d’applications.

 

Pour créer une boîte de dialogue sans utiliser de ressources de modèle, vous devez créer un modèle en mémoire et le passer à la fonction [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama) ou [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama) , ou à la macro [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta) ou [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) .

Un modèle de boîte de dialogue en mémoire se compose d’un en-tête qui décrit la boîte de dialogue, suivie d’un ou de plusieurs blocs de données supplémentaires qui décrivent chacun des contrôles de la boîte de dialogue. Le modèle peut utiliser le format standard ou le format étendu. Dans un modèle standard, l’en-tête est une structure [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) suivie de tableaux de longueur variable supplémentaires. et les données de chaque contrôle se composent d’une structure [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) suivie de tableaux de longueur variable supplémentaires. Dans un modèle de boîte de dialogue étendue, l’en-tête utilise le format [**DLGTEMPLATEEX**](dlgtemplateex.md) et les définitions de contrôle utilisent le format [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) .

Vous pouvez créer un modèle de mémoire en allouant un objet mémoire global et en le remplissant avec les définitions d’en-tête standard ou étendu et de contrôle. Un modèle de mémoire est identique au format et au contenu d’une ressource de modèle. De nombreuses applications qui utilisent des modèles de mémoire utilisent d’abord la fonction [**LoadResource**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadresource) pour charger une ressource de modèle en mémoire, puis modifier la ressource chargée pour créer un nouveau modèle de mémoire. Pour plus d’informations sur la création d’un modèle de boîte de dialogue en mémoire, consultez [modèles en mémoire](#templates-in-memory).

Les sections suivantes décrivent les styles, les mesures et les autres valeurs utilisées dans un modèle de boîte de dialogue.

-   [Styles de modèles de boîte de dialogue](#dialog-box-template-styles)
-   [Mesures de la boîte de dialogue](#dialog-box-measurements)
-   [Contrôles de boîte de dialogue](#dialog-box-controls)
-   [Menu de la boîte de dialogue](#dialog-box-window-menu)
-   [Polices de boîte de dialogue](#dialog-box-fonts)
-   [Modèles en mémoire](#templates-in-memory)

### <a name="dialog-box-template-styles"></a>Styles de modèles de boîte de dialogue

Chaque modèle de boîte de dialogue spécifie une combinaison de valeurs de style qui définissent l’apparence et les fonctionnalités de la boîte de dialogue. Les valeurs de style peuvent être des styles de fenêtre, tels que **WS \_ Popup** et **WS \_ SYSMENU**, et des styles de boîte de dialogue, tels que **DS \_ MODALFRAME**. Le nombre et le type de styles d’un modèle dépendent du type et de l’objectif de la boîte de dialogue. Pour obtenir la liste des valeurs, consultez [**styles de boîte de dialogue**](dialog-box-styles.md).

Le système passe tous les styles de fenêtre spécifiés dans le modèle à la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) lors de la création de la boîte de dialogue. Le système peut passer un ou plusieurs styles étendus selon les styles de boîte de dialogue spécifiés. Par exemple, lorsque le modèle spécifie **DS \_ MODALFRAME**, le système utilise **WS \_ ex \_ DLGMODALFRAME** lors de la création de la boîte de dialogue.

La plupart des boîtes de dialogue sont des fenêtres indépendantes qui comportent un menu fenêtre et une barre de titre. Par conséquent, le modèle standard spécifie les styles **WS \_ Popup**, **WS \_ SYSMENU** et **WS \_ Caption** . Le modèle spécifie également un style de bordure : **WS \_ Border** pour les boîtes de dialogue non modales et **DS \_ MODALFRAME** pour les boîtes de dialogue modales. Un modèle peut spécifier un type de fenêtre autre que Popup (par exemple, **WS \_ OVERLAPPED**) s’il crée une fenêtre personnalisée au lieu d’une boîte de dialogue.

Le système affiche toujours une boîte de dialogue modale, que le style **\_ visible WS** soit spécifié ou non. Lorsque le modèle d’une boîte de dialogue non modale spécifie le style **WS \_ visible** , le système affiche automatiquement la boîte de dialogue lors de sa création. Dans le cas contraire, l’application est responsable de l’affichage de la boîte de dialogue à l’aide de la fonction [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) .

### <a name="dialog-box-measurements"></a>Mesures de la boîte de dialogue

Chaque modèle de boîte de dialogue contient des mesures qui spécifient la position, la largeur et la hauteur de la boîte de dialogue et les contrôles qu’elle contient. Ces mesures étant indépendantes des appareils, une application peut utiliser un modèle unique pour créer la même boîte de dialogue pour tous les types de périphériques d’affichage. Cela permet de s’assurer qu’une boîte de dialogue aura les mêmes proportions et apparences sur tous les écrans en dépit des résolutions et des ratios d’aspect entre les écrans différents.

Les mesures d’un modèle de boîte de dialogue sont spécifiées dans les unités du modèle de boîte de dialogue. Pour convertir des mesures à partir d’unités de modèle de boîte de dialogue en unités d’écran (pixels), utilisez la fonction [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) , qui prend en compte la police utilisée par la boîte de dialogue et convertit correctement un rectangle à partir d’unités de modèle de boîte de dialogue en pixels. Pour les boîtes de dialogue qui utilisent la police système, vous pouvez utiliser la fonction [**GetDialogBaseUnits**](/windows/desktop/api/Winuser/nf-winuser-getdialogbaseunits) pour effectuer vous-même les calculs de conversion, bien que l’utilisation de **MapDialogRect** soit plus simple.

Le modèle doit spécifier les coordonnées initiales de l’angle supérieur gauche de la boîte de dialogue. En général, les coordonnées sont relatives au coin supérieur gauche de la zone cliente de la fenêtre propriétaire. Lorsque le modèle spécifie le \_ style DS ABSALIGN ou si la boîte de dialogue n’a pas de propriétaire, la position est relative à l’angle supérieur gauche de l’écran. Le système définit cette position initiale lors de la création de la boîte de dialogue, mais permet à une application d’ajuster la position avant d’afficher la boîte de dialogue. Par exemple, une application peut récupérer les dimensions de la fenêtre propriétaire, calculer une nouvelle position qui centre la boîte de dialogue dans la fenêtre propriétaire, puis définir la position à l’aide de la fonction [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) .

Le modèle doit spécifier une largeur et une hauteur de boîte de dialogue qui ne dépassent pas la largeur et la hauteur de l’écran et garantit que tous les contrôles se trouvent dans la zone cliente de la boîte de dialogue. Bien que le système permette à une boîte de dialogue d’avoir n’importe quelle taille, la création d’une boîte de dialogue qui est trop petite ou trop grande peut empêcher l’utilisateur de fournir une entrée, ce qui a pour effet de mettre en application la boîte de dialogue. De nombreuses applications utilisent plusieurs boîtes de dialogue lorsqu’il y a un grand nombre de contrôles. Dans ce cas, la boîte de dialogue initiale contient généralement un ou plusieurs boutons que l’utilisateur peut choisir d’afficher dans la boîte de dialogue suivante.

### <a name="dialog-box-controls"></a>Contrôles de boîte de dialogue

Le modèle spécifie la position, la largeur, la hauteur, le style, l’identificateur et la classe de fenêtre pour chaque contrôle de la boîte de dialogue. Le système crée chaque contrôle en passant ces données à la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) . Les contrôles sont créés dans l’ordre dans lequel ils sont spécifiés dans le modèle. Le modèle doit spécifier le nombre, le type et l’ordre de contrôles appropriés pour s’assurer que l’utilisateur peut entrer l’entrée nécessaire pour exécuter la tâche associée à la boîte de dialogue.

Pour chaque contrôle, le modèle spécifie des valeurs de style qui définissent l’apparence et le fonctionnement du contrôle. Chaque contrôle est une fenêtre enfant et doit donc avoir le style **WS \_ enfant** . Pour vous assurer que le contrôle est visible lorsque la boîte de dialogue est affichée, chaque contrôle doit également avoir le style **\_ visible WS** . Les autres styles de fenêtre couramment utilisés sont **WS \_ Border** pour les contrôles qui ont des bordures facultatives, **WS \_ désactivé** pour les contrôles qui doivent être désactivés lors de la création de la boîte de dialogue, et **WS \_ TABSTOP** et **WS \_ Group** pour les contrôles accessibles à l’aide du clavier. Les styles **WS \_ TABSTOP** et **WS \_ Group** sont utilisés conjointement avec l’interface de clavier de boîte de dialogue décrite plus loin dans cette rubrique.

Le modèle peut également spécifier des styles de contrôle spécifiques à la classe de fenêtre du contrôle. Par exemple, un modèle qui spécifie un contrôle Button doit fournir un style de contrôle Button comme **BS \_ PUSHBUTTON** ou **BS \_ case à cocher**. Le système passe les styles de contrôle à la procédure de fenêtre de contrôle par le biais du message [**WM \_ Create**](/windows/desktop/winmsg/wm-create) , ce qui permet à la procédure d’adapter l’apparence et le fonctionnement du contrôle.

Le système convertit les coordonnées de position et les mesures de largeur et de hauteur des unités de base de dialogue en pixels, avant de les passer à [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Lorsque le système crée un contrôle, il spécifie la boîte de dialogue en tant que fenêtre parente. Cela signifie que le système interprète toujours les coordonnées de position du contrôle en tant que coordonnées clientes, par rapport au coin supérieur gauche de la zone cliente de la boîte de dialogue.

Le modèle spécifie la classe de fenêtre pour chaque contrôle. Une boîte de dialogue classique contient des contrôles appartenant aux classes de fenêtres de contrôle prédéfinies, telles que les classes de fenêtre de contrôle Button et Edit. Dans ce cas, le modèle spécifie des classes de fenêtre en fournissant les valeurs Atom prédéfinies correspondantes pour les classes. Lorsqu’une boîte de dialogue contient un contrôle appartenant à une classe de fenêtre de contrôle personnalisée, le modèle donne le nom de la classe de fenêtre inscrite ou la valeur Atom actuellement associée au nom.

Chaque contrôle d’une boîte de dialogue doit avoir un identificateur unique pour le distinguer des autres contrôles. Les contrôles envoient des informations à la procédure de boîte de dialogue par le biais de messages de [**\_ commande WM**](/windows/desktop/menurc/wm-command) . par conséquent, les identificateurs de contrôle sont essentiels pour que la procédure détermine le contrôle qui a envoyé un message spécifié. La seule exception à cette règle est les identificateurs de contrôle pour les contrôles statiques. Les contrôles statiques ne nécessitent pas d’identificateurs uniques, car ils n’envoient aucun message de **\_ commande WM** .

Pour permettre à l’utilisateur de fermer la boîte de dialogue, le modèle doit spécifier au moins un bouton de commande et lui donner l’identificateur de contrôle **IDCANCEL**. Pour permettre à l’utilisateur de choisir entre l’exécution ou l’annulation de la tâche associée à la boîte de dialogue, le modèle doit spécifier deux boutons de commande, étiquetés **OK** et **Annuler**, avec les identificateurs de contrôle de **IDOK** et **IDCANCEL**, respectivement.

Un modèle spécifie également un texte facultatif et des données de création pour un contrôle. Le texte fournit généralement des étiquettes pour les contrôles Button ou spécifie le contenu initial d’un contrôle de texte statique. Les données de création sont un ou plusieurs octets de données que le système passe à la procédure de fenêtre de contrôle lors de la création du contrôle. Les données de création sont utiles pour les contrôles qui requièrent plus d’informations sur leur contenu initial ou leur style que celui spécifié par d’autres données. Par exemple, une application peut utiliser les données de création pour définir le paramètre et la plage initiaux pour un contrôle de barre de défilement.

### <a name="dialog-box-window-menu"></a>Menu de la boîte de dialogue

Le système affiche une boîte de dialogue dans un menu fenêtre lorsque le modèle spécifie le style **WS \_ SYSMENU** . Pour empêcher une entrée inappropriée, le système désactive automatiquement tous les éléments dans le menu, à l’exception de **déplacer** et **Fermer**. L’utilisateur peut cliquer sur **déplacer** pour déplacer la boîte de dialogue. Quand l’utilisateur clique sur **Fermer**, le système envoie un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) à la procédure de boîte de dialogue avec le paramètre *wParam* défini sur **IDCANCEL**. Il est identique au message envoyé par le bouton **Annuler** lorsque l’utilisateur clique dessus. L’action recommandée pour ce message est de fermer la boîte de dialogue et d’annuler la tâche demandée.

Bien qu’il ne soit pas recommandé d’utiliser d’autres menus dans les boîtes de dialogue, un modèle de boîte de dialogue peut spécifier un menu en fournissant l’identificateur ou le nom d’une ressource de menu. Dans ce cas, le système charge la ressource et crée le menu de la boîte de dialogue. Les applications utilisent généralement des identificateurs de menu ou des noms dans des modèles lors de l’utilisation de modèles pour créer des fenêtres personnalisées plutôt que des boîtes de dialogue.

### <a name="dialog-box-fonts"></a>Polices de boîte de dialogue

Le système utilise la largeur moyenne des caractères de la police de la boîte de dialogue pour calculer la position et les dimensions de la boîte de dialogue. Par défaut, le système dessine tout le texte dans une boîte de dialogue à l’aide de la police du **système \_** .

Pour spécifier une police pour une boîte de dialogue autre que celle par défaut, vous devez créer la boîte de dialogue à l’aide d’un modèle de boîte de dialogue. Dans une ressource de modèle, utilisez l' [instruction font](../menurc/font-statement.md). Dans un modèle de boîte de dialogue, définissez le style **DS \_ SetFont** ou **DS \_ SHELLFONT** et spécifiez une taille de point et un nom de police. Même si un modèle de boîte de dialogue spécifie une police de cette manière, le système utilise toujours la police système pour les menus du titre et de la boîte de dialogue de la boîte de dialogue.

Quand la boîte de dialogue a le style **DS \_ SetFont** ou **DS \_ SHELLFONT** , le système envoie un message [**WM \_ SetFont**](/windows/desktop/winmsg/wm-setfont) à la procédure de la boîte de dialogue et à chaque contrôle au fur et à mesure qu’il crée le contrôle. La procédure de boîte de dialogue est responsable de l’enregistrement du handle de police passé avec le message **WM \_ SetFont** et de la sélection du handle dans le contexte de périphérique d’affichage chaque fois qu’il écrit du texte dans la fenêtre. Les contrôles prédéfinis le font par défaut.

La police système peut varier d’une version à l’autre de Windows. Pour que votre application utilise la police système quel que soit le système sur lequel elle s’exécute, utilisez **DS \_ SHELLFONT** avec la police MS Shell Dlg et utilisez la [ressource DIALOGEX](../menurc/dialogex-resource.md) au lieu de la [ressource de boîte de dialogue](../menurc/dialog-resource.md). Le système mappe ce caractère afin que votre boîte de dialogue utilise la police Tahoma. Notez que **le \_ SHELLFONT DS** n’a aucun effet si le type de caractères n’est pas MS Shell Dlg.

### <a name="templates-in-memory"></a>Modèles en mémoire

Un modèle de boîte de dialogue en mémoire se compose d’un en-tête qui décrit la boîte de dialogue, suivie d’un ou de plusieurs blocs de données supplémentaires qui décrivent chacun des contrôles de la boîte de dialogue. Le modèle peut utiliser le format standard ou le format étendu. Dans un modèle standard, l’en-tête est une structure [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) suivie de tableaux de longueur variable supplémentaires. Les données de chaque contrôle se composent d’une structure [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) suivie de tableaux de longueur variable supplémentaires. Dans un modèle de boîte de dialogue étendue, l’en-tête utilise le format [**DLGTEMPLATEEX**](dlgtemplateex.md) et les définitions de contrôle utilisent le format [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) .

Pour faire la distinction entre un modèle standard et un modèle étendu, vérifiez les 16 premiers bits d’un modèle de boîte de dialogue. Dans un modèle étendu, le premier **mot** est 0xFFFF ; toute autre valeur indique un modèle standard.

Si vous créez un modèle de boîte de dialogue en mémoire, vous devez vous assurer que chacune des définitions de contrôle [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) ou [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) est alignée sur les limites **DWORD** . En outre, toutes les données de création qui suivent une définition de contrôle doivent être alignées sur une limite **DWORD** . Tous les autres tableaux de longueur variable d’un modèle de boîte de dialogue doivent être alignés sur les limites de **mots** .

### <a name="template-header"></a>En-tête de modèle

Dans les modèles standard et étendus pour les boîtes de dialogue, l’en-tête contient les informations générales suivantes :

-   L’emplacement et les dimensions de la boîte de dialogue
-   Les styles de fenêtre et de boîte de dialogue pour la boîte de dialogue
-   Nombre de contrôles dans la boîte de dialogue. Cette valeur détermine le nombre de définitions de contrôle [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) ou [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) dans le modèle.
-   Ressource de menu facultative pour la boîte de dialogue. Le modèle peut indiquer que la boîte de dialogue n’a pas de menu, ou elle peut spécifier une valeur ordinale ou une chaîne Unicode terminée par le caractère null qui identifie une ressource de menu dans un fichier exécutable.
-   Classe de fenêtre de la boîte de dialogue. Il peut s’agir de la classe de boîte de dialogue prédéfinie ou d’une valeur ordinale ou d’une chaîne Unicode terminée par le caractère null qui identifie une classe de fenêtre inscrite.
-   Chaîne Unicode terminée par le caractère null qui spécifie le titre de la fenêtre de la boîte de dialogue. Si la chaîne est vide, la barre de titre de la boîte de dialogue est vide. Si la boîte de dialogue n’a pas le style de **\_ légende WS** , le système définit le titre sur la chaîne spécifiée, mais ne l’affiche pas.
-   Si la boîte de dialogue contient le style **DS \_ SetFont** , l’en-tête spécifie la taille du point et le nom de la police à utiliser pour le texte dans la zone cliente et les contrôles de la boîte de dialogue.

Dans un modèle étendu, l’en-tête [**DLGTEMPLATEEX**](dlgtemplateex.md) spécifie également les informations supplémentaires suivantes :

-   L’identificateur de contexte d’aide de la fenêtre de boîte de dialogue lorsque le système envoie un message [**\_ d’aide WM**](../shell/wm-help.md) .
-   Si la boîte de dialogue a le style **DS \_ SetFont** ou **DS \_ SHELLFONT** , l’en-tête spécifie l’épaisseur de la police et indique si la police est en italique.

### <a name="control-definitions"></a>Définitions de contrôles

Après l’en-tête de modèle se trouve une ou plusieurs définitions de contrôle qui décrivent les contrôles de la boîte de dialogue. Dans les modèles standard et étendus, l’en-tête de boîte de dialogue a un membre qui indique le nombre de définitions de contrôle dans le modèle. Dans un modèle standard, chaque définition de contrôle se compose d’une structure [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) suivie de tableaux de longueur variable supplémentaires. Dans un modèle étendu, les définitions de contrôle utilisent le format [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) .

Dans les modèles standard et étendus, la définition de contrôle comprend les informations suivantes :

-   Emplacement et dimensions du contrôle.
-   Les styles de fenêtre et de contrôle pour le contrôle.
-   Identificateur du contrôle.
-   Classe de fenêtre du contrôle. Il peut s’agir de la valeur ordinale d’une classe système prédéfinie ou d’une chaîne Unicode terminée par le caractère null qui spécifie le nom d’une classe de fenêtre inscrite.
-   Chaîne Unicode terminée par le caractère null qui spécifie le texte initial du contrôle, ou valeur ordinale qui identifie une ressource, telle qu’une icône, dans un fichier exécutable.
-   Bloc de données de création facultatives de longueur variable. Lorsque le système crée le contrôle, il passe un pointeur vers ces données dans le paramètre *lParam* du message [**WM \_ Create**](/windows/desktop/winmsg/wm-create) qu’il envoie au contrôle.

Dans un modèle étendu, la définition de contrôle spécifie également un identificateur de contexte d’aide pour le contrôle lorsque le système envoie un message [**\_ d’aide WM**](../shell/wm-help.md) .

 

 