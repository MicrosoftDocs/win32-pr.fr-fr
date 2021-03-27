---
description: Présente les nouvelles fonctionnalités de la barre des tâches, notamment la consolidation du lancement et du basculement, les fonctionnalités améliorées des boutons de la barre des tâches, telles que l’accès par un simple clic à des documents et des tâches spécifiques aux applications, les contrôles de transport et les notifications d’État, les représentations de miniatures et les cibles de commutateur à l’aide d’un glisser-déplacer
ms.assetid: cbf2b07d-d67c-4755-888c-d40692d13cae
title: Extensions de la barre des tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4df308d8045301b98937eb03af595d2e800921b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867742"
---
# <a name="taskbar-extensions"></a>Extensions de la barre des tâches

À compter de Windows 7, la barre des tâches a été étendue de manière significative sous le principe de l’optimisation des utilisateurs là où ils se dépasseront aussi rapidement et efficacement que possible. À cette fin, les fenêtres d’application, les fichiers et les commandes que l’utilisateur doit accomplir et sont désormais centralisés dans un bouton de barre des tâches unique qui consolide les sources d’informations et les contrôles précédemment éparpillés. Un utilisateur peut désormais trouver des tâches courantes, des fichiers récents et fréquents, des alertes, des notifications de progression et des miniatures pour des documents individuels ou des onglets dans un même emplacement.

-   [Lancement et commutation unifiés](#unified-launching-and-switching)
-   [Listes de raccourcis](#jump-lists)
-   [Destinations](#destinations)
-   [Tâches](#tasks)
-   [Personnalisation des listes de raccourcis](#customizing-jump-lists)
-   [Barres d’outils miniatures](#thumbnail-toolbars)
-   [Superpositions d’icône](#icon-overlays)
-   [Barres de progression](#progress-bars)
-   [Deskbands](#deskbands)
-   [Zone de notification](#notification-area)
-   [Miniatures](#thumbnails)
-   [Rubriques connexes](#related-topics)

## <a name="unified-launching-and-switching"></a>Lancement et commutation unifiés

À partir de la barre des tâches de Windows 7, le lancement rapide n’est plus une barre d’outils distincte. Les raccourcis du lanceur que le lancement rapide contient généralement sont maintenant épinglés à la barre des tâches proprement dite, mélangés à des boutons pour les applications en cours d’exécution. Quand un utilisateur démarre une application à partir d’un raccourci de lancement épinglé, l’icône se transforme en bouton de la barre des tâches de l’application tant que l’application est en cours d’exécution. Lorsque l’utilisateur ferme l’application, le bouton revient à l’icône. Toutefois, le raccourci du lanceur et le bouton pour l’application en cours d’exécution sont simplement des formes différentes du bouton de la barre des tâches de Windows 7.

![barre des tâches Windows 7](images/taskbar/taskbar.png)

Un petit ensemble d’applications est épinglé par défaut pour les nouvelles installations. Outre celles-ci, seul l’utilisateur peut épingler d’autres applications. l’épinglage par programmation par une application n’est pas autorisé.

La fonctionnalité afficher le Bureau à partir de lancement rapide se trouve désormais à l’extrême droite de la barre des tâches. Si vous pointez sur cette zone, toutes les fenêtres actives deviennent transparentes et affichent le bureau. Cliquez sur la zone pour exécuter l’action familière de minimisation de toutes les fenêtres et de basculement vers le bureau.

Pendant que l’application est en cours d’exécution, son bouton de la barre des tâches devient l’emplacement unique pour accéder à toutes les fonctionnalités suivantes, chacune étant traitée en détail ci-dessous.

-   [Tâches](#tasks): commandes d’application courantes, présentes même lorsque l’application n’est pas en cours d’exécution.
-   [Destinations](#destinations): fichiers récemment et fréquemment consultés spécifiques à l’application.
-   [Miniatures](#thumbnails): changement de fenêtre, y compris les cibles de commutateur pour des onglets et des documents individuels.
-   [Barres d’outils miniatures](#thumbnail-toolbars): contrôle d’application de base à partir de la miniature elle-même.
-   [Barres de progression](#progress-bars) et [superpositions d’icône](#icon-overlays): notifications d’État.

Le bouton de la barre des tâches peut représenter un lanceur, une fenêtre d’application unique ou un groupe. Un identificateur connu sous le nom d’ID de modèle d’utilisateur d’application (AppUserModelID) est attribué à chaque groupe. Une valeur AppUserModelID peut être spécifiée pour remplacer le regroupement de la barre des tâches standard, ce qui permet à Windows de devenir membres du même groupe lorsqu’ils ne peuvent pas être considérés comme tels. Chaque membre d’un groupe reçoit un aperçu séparé dans le menu volant miniature qui s’affiche lorsque la souris pointe sur le bouton de la barre des tâches du groupe. Notez que le regroupement lui-même reste facultatif.

À compter de Windows 7, les boutons de la barre des tâches peuvent désormais être réorganisés par l’utilisateur par le biais d’opérations de glisser-déplacer.

> [!Note]  
> Le dossier lancement rapide ([* * * * FOLDERID \_ QuickLaunch * *](knownfolderid.md)* *) est toujours disponible à des fins de compatibilité descendante, bien qu’il n’y ait plus d’interface utilisateur de lancement rapide. Toutefois, les nouvelles applications ne doivent pas demander à d’ajouter une icône au lancement rapide lors de l’installation.

 

Pour plus d’informations, consultez [ID de modèle d’utilisateur d’application (AppUserModelIDs)](appids.md).

## <a name="jump-lists"></a>Listes de raccourcis

Un utilisateur lance généralement un programme avec l’intention d’accéder à un document ou d’effectuer des tâches au sein du programme. L’utilisateur d’un programme de jeu peut vouloir accéder à un jeu enregistré ou le lancer sous la forme d’un caractère spécifique plutôt que de redémarrer un jeu depuis le début. Pour obtenir des utilisateurs plus efficacement à leur objectif final, une liste de [destinations](#destinations) et de [tâches](#tasks) courantes associées à une application est attachée au bouton de la barre des tâches de cette application (ainsi qu’à l’entrée de menu **Démarrer** équivalente). Il s’agit de la liste de raccourcis de l’application. La liste de raccourcis est disponible si le bouton de la barre des tâches est dans un état de lancement (l’application n’est pas en cours d’exécution) ou si elle représente une ou plusieurs fenêtres. Cliquez avec le bouton droit sur le bouton de la barre des tâches pour afficher la liste de raccourcis de l’application, comme indiqué dans l’illustration suivante.

![liste de raccourcis avec les catégories épinglé, fréquent et tâches](images/taskbar/jumplist.png)

Par défaut, une liste de raccourcis standard contient deux catégories : éléments récents et éléments épinglés, bien que seules les catégories avec du contenu soient affichées dans l’interface utilisateur, aucune de ces catégories n’est affichée au premier lancement. Toujours présent sont une icône de lancement d’application (pour lancer davantage d’instances de l’application), une option pour épingler ou détacher l’application de la barre des tâches et une commande **Fermer** pour les fenêtres ouvertes.

## <a name="destinations"></a>Destinations

Les catégories **récentes** et **fréquentes** sont considérées comme contenant des destinations. Une destination, généralement un fichier, un document ou une URL, est une valeur qui peut être modifiée, parcourue, affichée, et ainsi de suite. Imaginez une destination comme un élément plutôt qu’une action. En règle générale, une destination est un élément de l’espace de noms Shell, représenté par un [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) ou un [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka). Ces parties de la liste de destination sont analogues à la liste des documents utilisés récemment du menu **Démarrer** (qui n’est plus affichée par défaut) et à la liste des applications fréquemment utilisées, mais elles sont spécifiques à une application et sont donc plus précises et utiles à l’utilisateur. Les résultats utilisés dans la liste de destination sont calculés par le biais d’appels à [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs). Notez que lorsque l’utilisateur ouvre un fichier à partir de l’Explorateur Windows ou utilise la boîte de dialogue de fichier commune pour ouvrir, enregistrer ou créer un fichier, **SHAddToRecentDocs** est appelé automatiquement pour vous, ce qui a pour effet que de nombreuses applications obtiennent leurs éléments récents dans la liste de destination sans aucune action de leur part.

Le lancement d’une destination est semblable au lancement d’un élément à l’aide de la commande **Ouvrir avec** . L’application démarre avec cette destination chargée et prête à l’emploi. Vous pouvez également faire glisser des éléments de la liste de destination à partir de la liste vers une destination de dépôt telle qu’un message électronique. En faisant en sorte que ces éléments soient centralisés dans une liste de destination, il obtient des utilisateurs où ils souhaitent aller plus rapidement, ce qui est l’objectif.

Comme les éléments apparaissent dans la catégorie **récente** d’une liste de destination (ou la catégorie **fréquente** ou une [catégorie personnalisée](#customizing-jump-lists) comme indiqué dans une section ultérieure), un utilisateur peut vouloir s’assurer que l’élément est toujours dans la liste pour y accéder rapidement. Pour ce faire, il peut épingler cet élément à la liste, ce qui ajoute l’élément à la catégorie **épinglée** . Lorsqu’un utilisateur travaille activement avec une destination, il souhaite le faire facilement à la main et l’épingler à la liste de destination de l’application. Une fois le travail de l’utilisateur terminé, il lui suffit de désépingler l’élément. Ce contrôle utilisateur conserve la liste inencombrée et pertinente.

Une liste de destination peut être considérée comme une version propre à l’application du menu **Démarrer** . Une liste de destination n’est pas un menu contextuel. Vous pouvez cliquer avec le bouton droit sur chaque élément dans une liste de destination pour son propre menu contextuel.

### <a name="apis"></a>API

-   [**IApplicationDestinations::RemoveDestination**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-removedestination)
-   [**IApplicationDestinations::RemoveAllDestinations**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-removealldestinations)
-   [**IApplicationDocumentLists :: GetList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist)
-   [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)

## <a name="tasks"></a>Tâches

Une autre partie intégrée d’une liste de raccourcis est la catégorie **tâches** . Alors qu’une destination est un élément, une tâche est une action, et dans ce cas, il s’agit d’une action propre à l’application. En d’autres termes, une destination est un substantif et une tâche est un verbe. En règle générale, les tâches sont des éléments [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) avec des arguments de ligne de commande qui indiquent une fonctionnalité particulière qui peut être déclenchée par une application. Là encore, l’idée est de centraliser autant d’informations relatives à une application que possible.

Les applications définissent des tâches basées sur les fonctionnalités du programme et sur les éléments clés qu’un utilisateur est censé faire. Les tâches doivent être sans contexte, dans le fait que l’application n’a pas besoin d’être en cours d’exécution pour fonctionner. Ils doivent également correspondre aux actions statistiquement les plus courantes qu’un utilisateur normal effectuerait dans une application, telles que composer un message électronique ou ouvrir le calendrier dans un programme de messagerie, créer un nouveau document dans un traitement de texte, lancer une application dans un mode spécifique ou lancer l’une de ses sous-commandes. Une application ne doit pas encombrer le menu avec des fonctionnalités avancées dont les utilisateurs standard n’ont pas besoin ou des actions ponctuelles, telles que l’inscription. N’utilisez pas de tâches pour des éléments promotionnels, tels que des mises à niveau ou des offres spéciales.

Il est fortement recommandé que la liste des tâches soit statique. Elle doit rester la même, quel que soit l’État ou l’état de l’application. Bien qu’il soit possible de faire varier la liste de manière dynamique, vous devez considérer que cela peut dérouter l’utilisateur qui ne s’attend pas à ce que la partie de la liste de destination change.

### <a name="apis"></a>API

-   [**ICustomDestinationList::AddUserTasks**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-addusertasks)

## <a name="customizing-jump-lists"></a>Personnalisation des listes de raccourcis

Une application peut définir ses propres catégories et les ajouter en plus ou à la place des catégories standard **récentes** et **fréquentes** dans une liste de raccourcis. L’application peut contrôler ses propres destinations dans ces catégories personnalisées en fonction de l’architecture de l’application et de l’utilisation prévue. La capture d’écran suivante montre une liste de raccourcis personnalisée avec une catégorie d’historique.

![liste de raccourcis personnalisée](images/taskbar/customjumplist.png)

Si une application décide de fournir une catégorie personnalisée, cette application assume la responsabilité de son remplissage. Le contenu de la catégorie doit toujours être spécifique à l’utilisateur et dépend de l’historique de l’utilisateur, des actions, ou des deux, mais par le biais d’une catégorie personnalisée, une application peut déterminer ce qu’elle souhaite suivre et ce qu’elle veut ignorer, peut-être en fonction d’une option d’application. Par exemple, un programme audio peut choisir d’inclure uniquement les albums récemment lus et d’ignorer les pistes individuelles jouées récemment.

Si un utilisateur a supprimé un élément de la liste, qui est toujours une option utilisateur, l’application doit le respecter. L’application doit également s’assurer que les éléments de la liste sont valides ou qu’ils échouent correctement s’ils ont été supprimés. Les éléments individuels ou le contenu entier de la liste peuvent être supprimés par programmation.

Le nombre maximal d’éléments dans une liste de destination est déterminé par le système en fonction de divers facteurs tels que la résolution de l’affichage et la taille de la police. S’il n’y a pas suffisamment d’espace pour tous les éléments de toutes les catégories, ils sont tronqués du bas vers le haut.

### <a name="apis"></a>API

-   [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)
-   [**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations)
-   [**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)

## <a name="thumbnail-toolbars"></a>Barres d’outils miniatures

Pour fournir l’accès aux commandes de clé d’une fenêtre particulière sans effectuer la restauration de l’utilisateur ou activer la fenêtre de l’application, un contrôle de barre d’outils actif peut être incorporé dans la miniature de cette fenêtre. Par exemple, le lecteur Windows Media peut proposer des contrôles de transport multimédia standard tels que lecture, pause, muet et arrêt. L’interface utilisateur affiche cette barre d’outils directement sous la miniature, comme indiqué dans l’illustration suivante : elle ne couvre aucune partie de celle-ci.

![barre des tâches miniature pour Windows Media Player, avec trois boutons : précédent, lire et transférer](images/taskbar/thumbbar.png)

Cette barre d’outils est simplement le contrôle commun de barre d’outils standard. Il a un maximum de sept boutons. L’ID, l’image, l’info-bulle et l’état de chaque bouton sont définis dans une structure, qui est ensuite transmise à la barre des tâches. L’application peut afficher, activer, désactiver ou masquer les boutons de la barre d’outils miniatures, selon les besoins de son état actuel.

Étant donné qu’il y a une salle limitée pour afficher des miniatures et un nombre variable de miniatures à afficher, les applications ne sont pas assurées d’une taille de barre d’outils donnée. Si l’espace est restreint, les boutons de la barre d’outils sont tronqués de droite à gauche. Par conséquent, lorsque vous concevez votre barre d’outils, vous devez classer par ordre de priorité les commandes associées à vos boutons et vous assurer que les plus importantes sont les plus importantes et qu’elles sont moins susceptibles d’être supprimées en raison de problèmes d’espace.

> [!Note]  
> Quand une application affiche une fenêtre, son bouton de la barre des tâches est créé par le système. Lorsque le bouton est en place, la barre des tâches envoie un message **TaskbarButtonCreated** à la fenêtre. Sa valeur est calculée en appelant [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)(L ("TaskbarButtonCreated")). Ce message doit être reçu par votre application avant d’appeler une méthode [**ITaskbarList3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3) .

 

### <a name="api"></a>API

-   [**ITaskbarList3 :: ThumbBarAddButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons)
-   [**ITaskbarList3 :: ThumbBarSetImageList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist)
-   [**ITaskbarList3 :: ThumbBarUpdateButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarupdatebuttons)
-   [**THUMBBUTTON**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton)

## <a name="icon-overlays"></a>Superpositions d’icône

Une application peut communiquer certaines notifications et certains États à l’utilisateur par le biais de son bouton de la barre des tâches en affichant de petites superpositions sur le bouton. Ces superpositions sont similaires au type de superposition existante utilisé pour les raccourcis ou les notifications de sécurité, affichée dans le coin inférieur droit du bouton. Pour afficher une icône de superposition, la barre des tâches doit être en mode grandes icônes par défaut, comme illustré dans la capture d’écran suivante.

![bouton de la barre des tâches Windows Messenger avec une superposition pour indiquer un état disponible](images/taskbar/taskbaroverlay.png)

Les superpositions d’icône servent de notification contextuelle de l’État et sont destinées à annuler la nécessité d’une autre icône d’état de la zone de notification pour communiquer ces informations à l’utilisateur. Par exemple, le nouvel État du courrier dans Microsoft Outlook, actuellement affiché dans la zone de notification, peut maintenant être indiqué par une superposition sur le bouton de la barre des tâches. Là encore, vous devez décider au cours de votre cycle de développement de la méthode la mieux adaptée à votre application. Les icônes de superposition sont destinées à fournir des notifications importantes et de longue durée, telles que l’état du réseau, l’état de Messenger ou le nouveau courrier. L’utilisateur ne doit pas être présenté avec des superpositions ou animations constamment modifiées.

Comme une superposition unique est superposée sur le bouton de la barre des tâches et non sur les miniatures de fenêtre individuelles, il s’agit d’une fonctionnalité par groupe plutôt que par fenêtre. Les demandes d’icônes de superposition peuvent être reçues à partir de fenêtres individuelles dans un groupe de la barre des tâches, mais elles ne sont pas mises en file d’attente. La dernière superposition reçue est la superposition affichée.

### <a name="apis"></a>API

-   [**ITaskbarList3 :: SetOverlayIcon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon)

## <a name="progress-bars"></a>Barres de progression

Un bouton de barre des tâches peut être utilisé pour afficher une barre de progression. Cela permet à une fenêtre de fournir des informations de progression à l’utilisateur sans que cet utilisateur ait à basculer vers la fenêtre elle-même. L’utilisateur peut rester productif dans une autre application tout en regardant en un clin d’œil la progression d’une ou plusieurs opérations qui se produisent dans d’autres fenêtres. Il est prévu qu’une barre de progression dans un bouton de la barre des tâches reflète un indicateur de progression plus détaillé dans la fenêtre elle-même. Cette fonctionnalité peut être utilisée pour effectuer le suivi des copies de fichiers, des téléchargements, des installations, de la gravure de supports ou de toute opération qui va prendre un certain temps. Cette fonctionnalité n’est pas destinée à être utilisée avec des actions de périphérique normalement, telles que le chargement d’une page Web ou l’impression d’un document. Ce type de progression doit continuer à s’afficher dans la barre d’état d’une fenêtre.

La barre de progression du bouton de la barre des tâches est une expérience similaire au contrôle de barre de progression familier. Il peut afficher la progression de l’arrêt en fonction d’un pourcentage terminé de l’opération ou une progression indéterminée du style Marquee pour indiquer que l’opération est en cours sans prédiction de temps restant. Il peut également indiquer que l’opération est suspendue ou a rencontré une erreur et nécessite une intervention de l’utilisateur.

### <a name="apis"></a>API

-   [**ITaskbarList3 :: SetProgressState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate)
-   [**ITaskbarList3 :: SetProgressValue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue)

## <a name="deskbands"></a>Deskbands

Dans les versions de Windows antérieures à Windows 7, il était possible d’obtenir des fonctionnalités similaires à celles de la barre d’outils miniatures à l’aide d’un Deskband, une barre d’outils hébergée dans la barre des tâches. Par exemple, le lecteur Windows Media peut réduire la barre des tâches en tant qu’ensemble de contrôles de transport plutôt qu’en tant que bouton standard. Dans Windows 7, deskbands peut toujours être implémenté et les barres d’outils miniatures ne sont pas destinées à les remplacer toutes. Toutes les applications ne se prêtent pas à une barre d’outils miniatures, et une autre solution comme Deskband ou une tâche dans une liste de destination peut être la bonne réponse pour votre application ; vous devez choisir la solution qui convient le mieux à votre application dans le cadre de votre cycle de développement. Toutefois, sachez que deskbands doit prendre en charge Windows Aero avec translucidité (« Glass ») activé et l’interface [**IDeskBand2**](/windows/desktop/api/Shobjidl/nn-shobjidl-ideskband2) .

### <a name="apis"></a>API

-   [**IDeskBand2**](/windows/desktop/api/Shobjidl/nn-shobjidl-ideskband2)

## <a name="notification-area"></a>Zone de notification

Des modifications ont été apportées à la zone de notification pour permettre à l’utilisateur de mieux contrôler les icônes qui apparaissent dans la barre des tâches. Toutes les icônes de notification sont désormais masquées par défaut et la visibilité ne peut pas être contrôlée par programmation. Seul l’utilisateur est autorisé à choisir les icônes de notification qui s’affichent dans la barre des tâches. Quand une bulle de notification s’affiche, l’icône devient temporairement visible, mais même un utilisateur peut choisir de la faire disparaître. Une superposition d’icône sur un bouton de la barre des tâches devient donc un choix attrayant lorsque vous souhaitez que votre application communique ces informations à vos utilisateurs.

## <a name="thumbnails"></a>Miniatures

Dans Windows Vista, si vous pointez sur le bouton de la barre des tâches d’une application, vous affichez une miniature qui représente la fenêtre en cours d’exécution. Si la barre des tâches a réduit les fenêtres de l’application, la miniature la représente en s’affichant sous forme de pile, mais seule la fenêtre active est affichée dans la miniature elle-même.

Dans Windows 7, chaque membre d’un groupe est affiché sous la forme d’une miniature distincte et est maintenant également une cible de commutateur. Une application peut définir ses enfants (tels que des véritables fenêtres enfants, des documents individuels ou des onglets) et fournir des miniatures correspondantes pour chacune de ces fenêtres, même si elles n’apparaissent pas normalement dans la barre des tâches. Cela permet aux utilisateurs de basculer directement vers l’affichage de l’application qu’ils souhaitent, plutôt que de basculer vers l’application, puis de basculer vers leur destination. Par exemple, les applications d’interface/tabbed-document (TDI) d’interface multidocument (MDI) peuvent avoir chaque document ou onglet affiché sous la forme d’une miniature distincte et d’un commutateur cible lorsque la souris pointe sur le bouton de la barre des tâches d’un groupe.

![trois miniatures de la barre des tâches qui représentent des onglets individuels dans Windows Internet Explorer](images/taskbar/taskbarthumbnails.png)

> [!Note]  
> Comme dans Windows Vista, Aero doit être actif pour afficher les miniatures.

 

### <a name="api"></a>API

-   [**ITaskbarList3 :: RegisterTab**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-registertab)
-   [**ITaskbarList3 :: SetTabActive**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settabactive)
-   [**ITaskbarList3 :: SetTabOrder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settaborder)
-   [**ITaskbarList3 :: UnregisterTab**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-unregistertab)
-   [**ITaskbarList4::SetTabProperties**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist4-settabproperties)

Les représentations miniatures pour Windows sont généralement automatiques, mais dans les cas où le résultat n’est pas optimal, la miniature peut être explicitement spécifiée. Par défaut, seules les fenêtres de niveau supérieur ont une miniature automatiquement générée, et les miniatures des fenêtres enfants apparaissent comme une représentation générique. Cela peut se traduire par une expérience plus ou moins claire pour l’utilisateur final. Par exemple, une miniature de cible de commutateur spécifique pour chaque fenêtre enfant offre une expérience utilisateur bien meilleure.

### <a name="api"></a>API

-   [**DwmSetWindowAttribute**](/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)
-   [**DwmSetIconicThumbnail**](/windows/win32/api/dwmapi/nf-dwmapi-dwmseticonicthumbnail)
-   [**DwmSetIconicLivePreviewBitmap**](/windows/win32/api/dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap)
-   [**DwmInvalidateIconicBitmaps**](/windows/win32/api/dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
-   [**\_DWMSENDICONICTHUMBNAIL WM**](../dwm/wm-dwmsendiconicthumbnail.md)
-   [**\_DWMSENDICONICLIVEPREVIEWBITMAP WM**](../dwm/wm-dwmsendiconiclivepreviewbitmap.md)

Vous pouvez sélectionner une zone particulière de la fenêtre à utiliser comme miniature. Cela peut s’avérer utile lorsqu’une application sait que ses documents ou ses onglets apparaîtront comme s’ils étaient affichés à la taille de la miniature. L’application peut ensuite choisir d’afficher uniquement la partie de sa zone cliente que l’utilisateur peut utiliser pour faire la distinction entre les miniatures. Toutefois, si vous placez le curseur sur une miniature, vous affichez une vue de la fenêtre complète en arrière-plan afin que l’utilisateur puisse rapidement en faire un coup d’œil.

S’il y a plus de miniatures qu’il n’est possible d’afficher, l’aperçu revient à la miniature héritée ou à une icône standard.

### <a name="api"></a>API

-   [**ITaskbarList3 :: SetThumbnailClip**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setthumbnailclip)

Pour ajouter **Épingler à la barre des tâches** au menu contextuel d’un élément, qui est normalement requis uniquement pour les types de fichiers qui incluent l’entrée [IsShortCut](./links.md) , s’effectue en inscrivant le gestionnaire de menu contextuel approprié. Cela s’applique également à **Épingler au menu Démarrer**. Pour plus d’informations, consultez [inscription de gestionnaires d’extension de Shell](reg-shell-exts.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[La barre des tâches](taskbar.md)
</dt> <dt>

[ID de modèle d’utilisateur d’application (AppUserModelIDs)](appids.md)
</dt> <dt>

[Notifications et zone de notification](notification-area.md)
</dt> </dl>

 

 
