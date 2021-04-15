---
title: Implémentation d’un affichage des dossiers
description: Le shell Windows fournit une implémentation par défaut de l’affichage des dossiers, connu sous le nom de DefView, ce qui vous permet d’éviter une grande partie du travail d’implémentation de votre propre extension d’espace de noms.
ms.assetid: 8c6712d8-c3cb-4450-8277-3a8675622651
keywords:
- objet de l’affichage des dossiers
- IShellView
- IShellBrowser, objets de vue de dossier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c7b86d587154a034f276d4bdab903e5337ed4b
ms.sourcegitcommit: 469b6de41e2a565b7ead231d7f282ec4071ac158
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/11/2020
ms.locfileid: "104383152"
---
# <a name="implementing-a-folder-view"></a>Implémentation d’un affichage des dossiers

Le shell Windows fournit une implémentation par défaut de l’affichage des dossiers, connu sous le nom de DefView, ce qui vous permet d’éviter une grande partie du travail d’implémentation de votre propre extension d’espace de noms. Étant donné que certaines fonctionnalités de vue ne peuvent pas être obtenues par le biais de vues personnalisées, il est souvent recommandé d’utiliser l’objet de vue de dossier système par défaut à la place d’une vue personnalisée. Pour plus d’informations, consultez [**SHCreateShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview). Le reste de cette rubrique traite de l’implémentation d’une vue de dossier personnalisée qui ne prend pas en charge les fonctionnalités d’affichage plus récentes.

Contrairement à l’arborescence, l’Explorateur Windows ne gère pas le contenu d’une vue de dossier. Au lieu de cela, la fenêtre d’affichage des dossiers héberge une fenêtre enfant qui est fournie par l’objet dossier. L’objet Folder est chargé de créer un objet d’affichage des dossiers pour afficher le contenu du dossier dans la fenêtre enfant.

La clé de l’implémentation d’un objet de vue de dossier est l’interface [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) . Cette interface est utilisée par l’Explorateur Windows pour communiquer avec l’objet de vue de dossier. Avant d’afficher un affichage des dossiers, l’Explorateur Windows appelle la méthode [**IShellFolder :: CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) de l’objet Folder avec *riid* défini sur IID \_ IShellView. Créez un objet de vue de dossier et retournez son interface **IShellView** . L’objet de vue de dossier doit ensuite créer une fenêtre enfant de la fenêtre d’affichage des dossiers et utiliser la fenêtre enfant pour afficher des informations sur le contenu du dossier.

Outre le contrôle de l’affichage des données, les extensions peuvent également personnaliser un certain nombre de fonctionnalités de l’Explorateur Windows. Par exemple, une extension peut ajouter des éléments à la barre d’outils ou à la barre de menus, ou afficher des informations sur la barre d’État.

-   [Objet de l’affichage des dossiers](#the-folder-view-object)
-   [Initialisation de l’objet de vue de dossier](#initializing-the-folder-view-object)
-   [Affichage de l’affichage des dossiers](#displaying-the-folder-view)
-   [Implémentation de IShellView](#implementing-ishellview)
    -   [AddPropertySheetPages](#addpropertysheetpages)
    -   [GetCurrentInfo](#getcurrentinfo)
    -   [Actualiser](#refresh)
    -   [SaveViewState](#saveviewstate)
    -   [TranslateAcelerator](#translateacelerator)
-   [Utilisation de IShellBrowser pour communiquer avec l’Explorateur Windows](#using-ishellbrowser-to-communicate-with-windows-explorer)
    -   [Modification de la barre de menus de l’Explorateur Windows](#modifying-the-windows-explorer-menu-bar)
    -   [Modification de la barre d’outils de l’Explorateur Windows](#modifying-the-windows-explorer-toolbar)
    -   [Modification de la barre d’état de l’Explorateur Windows](#modifying-the-windows-explorer-status-bar)
    -   [Stockage des informations spécifiques à la vue](#storing-view-specific-information)

## <a name="the-folder-view-object"></a>Objet de l’affichage des dossiers

Un objet de vue de dossier est un objet COM (Component Object Model) qui expose une interface [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) . Cet objet est chargé des opérations suivantes :

-   Création d’une fenêtre enfant de la fenêtre d’affichage des dossiers et utilisation de celle-ci pour afficher le contenu du dossier.
-   Gestion de la communication avec l’Explorateur Windows.
-   Ajout de commandes spécifiques aux dossiers à la barre de menus et à la barre d’outils de l’Explorateur Windows et gestion de ces commandes lorsqu’elles sont sélectionnées.
-   Gestion de l’interaction de l’utilisateur à l’aide de la fenêtre d’affichage des dossiers, telle que l’affichage des menus contextuels ou la gestion des opérations de glisser-déplacer.

Ce document traite des trois premières rubriques. Étant donné que l’interaction de l’utilisateur avec l’affichage des dossiers s’effectue dans votre fenêtre enfant, votre objet de vue de dossier est chargé de le gérer comme n’importe quelle autre fenêtre.

L’Explorateur Windows demande un objet de vue de dossier en appelant le [**IShellFolder :: CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) de l’objet Folder avec *riid* défini sur IID \_ IShellView. La procédure de création d’un affichage des dossiers est la suivante :

1.  Votre objet Folder crée une nouvelle instance de votre objet de vue de dossier et retourne un pointeur vers son interface [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) .
2.  L’Explorateur Windows initialise l’objet d’affichage des dossiers en appelant la méthode [**IShellView :: CreateViewWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) . Crée une fenêtre enfant de la fenêtre d’affichage des dossiers et retourne son handle à l’Explorateur Windows.
3.  L’objet d’affichage des dossiers utilise l’interface [**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) de l’Explorateur Windows pour personnaliser la barre d’outils de l’Explorateur Windows, la barre de menus et la barre d’État.
4.  L’objet d’affichage des dossiers affiche le contenu du dossier dans la fenêtre enfant.
5.  L’objet d’affichage des dossiers gère l’interaction de l’utilisateur avec l’affichage des dossiers et les éléments de barre de menus ou de barre d’outils spécifiques aux dossiers.

## <a name="initializing-the-folder-view-object"></a>Initialisation de l’objet de vue de dossier

L’Explorateur Windows initialise l’objet d’affichage des dossiers en appelant la méthode [**IShellView :: CreateViewWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) . Les paramètres de la méthode fournissent à l’objet de vue de dossier les informations dont il a besoin pour créer la fenêtre enfant qui sera utilisée pour afficher le contenu du dossier :

-   Pointeur vers l’interface [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) de l’objet d’affichage du dossier précédent. Ce paramètre peut avoir la valeur **null**.
-   Structure [**FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) qui contient les paramètres de la vue de dossier précédente.
-   Pointeur vers l’interface [**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) de l’Explorateur Windows.
-   Une structure [Rect](/previous-versions//ms536136(v=vs.85)) avec les dimensions de la fenêtre d’affichage des dossiers.

La méthode [**IShellView :: CreateViewWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) est appelée avant la destruction de l’objet de vue de dossier précédent. Le pointeur d’interface [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) vous permet donc de communiquer avec l’objet d’affichage de dossier précédent. Cette interface est surtout utile si le dossier précédent appartenait à votre extension et utilisait le même schéma d’affichage. Dans ce cas, vous pouvez communiquer avec l’objet d’affichage de dossier précédent à des fins telles que l’échange de paramètres privés.

Un moyen simple de déterminer si le pointeur [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) appartient à votre extension est de faire en sorte que tous vos objets de vue de dossier exposent une interface privée. Appelez [IShellView :: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour demander l’interface privée, puis examinez la valeur de retour pour déterminer si l’objet de la vue du dossier est l’un des vôtres. Vous pouvez ensuite utiliser une méthode privée sur cette interface pour échanger des informations.

La structure [**FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) contient les paramètres d’affichage du dossier précédent. Le paramètre principal est le mode d’affichage : grande icône, petite icône, liste ou détails. Il y a également un indicateur qui contient les paramètres d’une variété d’options d’affichage, par exemple si la vue doit être alignée à gauche. L’affichage de vos dossiers doit respecter ces paramètres dans la mesure du possible, afin de fournir aux utilisateurs une expérience cohérente lorsqu’ils passent d’un dossier à un autre. Vous devez stocker cette structure et la mettre à jour en fonction des modifications apportées aux paramètres. L’Explorateur Windows appelle [**IShellView :: GetCurrentInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-getcurrentinfo) pour obtenir la valeur la plus récente de cette structure avant d’ouvrir l’affichage suivant du dossier.

L’interface [**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) est exposée par l’Explorateur Windows. Cette interface est associée à [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) et permet à un objet de vue de dossier de communiquer avec l’Explorateur Windows. Il n’existe aucune autre façon de récupérer ce pointeur d’interface, votre objet de vue de dossier doit donc le stocker pour une utilisation ultérieure. En particulier, vous devez appeler [IShellBrowser :: GetWindow](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) pour récupérer la fenêtre d’affichage du dossier parent que vous allez utiliser pour créer votre fenêtre enfant. Notez que la méthode IShellBrowser :: GetWindow n’est pas incluse dans la documentation **IShellBrowser** , car elle est héritée de [IOleWindow](/windows/win32/api/oleidl/nn-oleidl-iolewindow). Après avoir stocké le pointeur d’interface, n’oubliez pas d’appeler [IShellBrowser :: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) pour incrémenter le décompte de références de l’interface. Lorsque vous n’avez plus besoin de l’interface, appelez [IShellBrowser :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

Pour créer votre fenêtre enfant :

1.  Examinez les structures [**FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) et [Rect](/previous-versions//ms536136(v=vs.85)) .
2.  Si nécessaire, obtenez des paramètres privés à partir de l’objet d’affichage du dossier précédent.
3.  Appelez [IShellBrowser :: GetWindow](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) pour récupérer la fenêtre d’affichage du dossier parent.
4.  Créez un enfant de la fenêtre d’affichage des dossiers obtenue à l’étape précédente et renvoyez-le à l’Explorateur Windows.

## <a name="displaying-the-folder-view"></a>Affichage de l’affichage des dossiers

Une fois que vous avez créé la fenêtre enfant et que vous l’avez retournée à l’Explorateur Windows, vous pouvez afficher le contenu du dossier. En règle générale, les extensions affichent leurs informations en faisant en sorte que la fenêtre enfant héberge soit un [contrôle List View](../controls/list-view-control-reference.md) , soit un **contrôle WebBrowser**. Le contrôle List View vous permet de répliquer l' [affichage classique](web-view.md)de l’Explorateur Windows. Le contrôle WebBrowser vous permet d’utiliser un document DHTML (Dynamic HTML) pour afficher vos informations, de la même façon que l’affichage Web de l’Explorateur Windows. Pour plus d’informations, reportez-vous à la documentation de ces contrôles.

La fenêtre d’affichage des dossiers existe toujours, même si elle n’a pas le focus. Vous devez donc conserver trois États pour votre fenêtre enfant :

-   Activé avec focus. L’affichage des dossiers a été créé et a le focus. Définissez la barre de menus ou les éléments de barre d’outils qui conviennent à un État ciblé.
-   Activé sans focus. L’affichage des dossiers a été créé et est actif, mais il n’a pas le focus. Définissez la barre de menus ou les éléments de barre d’outils qui conviennent à un État sans focus. Omettez tous les éléments qui s’appliquent à la sélection d’éléments dans l’affichage des dossiers.
-   Désactivé. L’affichage des dossiers va être détruit. Supprimer tous les éléments de menu spécifiques au dossier.

L’Explorateur Windows avertit votre objet de vue de dossier lorsque l’état de la fenêtre change en appelant [**IShellView :: UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate). À son tour, l’objet d’affichage des dossiers doit notifier l’Explorateur Windows lorsqu’un utilisateur active la fenêtre d’affichage des dossiers en appelant [**IShellBrowser :: OnViewWindowActive**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-onviewwindowactive). Pour plus d’informations sur cette interface, consultez [utilisation de IShellBrowser pour communiquer avec l’Explorateur Windows](#using-ishellbrowser-to-communicate-with-windows-explorer).

Lorsque l’affichage des dossiers est actif, vous devez traiter tous les messages Windows, tels que la [ \_ taille du WM](../winmsg/wm-size.md), qui appartiennent à votre fenêtre enfant. Votre procédure de fenêtre recevra également les messages de [ \_ commande WM](../menurc/wm-command.md) pour tous les éléments que vous avez ajoutés à la barre de menus ou à la barre d’outils de l’Explorateur Windows.

Après la création de l’affichage des dossiers, l’Explorateur Windows appelle l’interface [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) de l’objet affichage des dossiers pour lui transmettre de nombreuses informations. Votre objet doit modifier son affichage en conséquence. Lorsque l’affichage des dossiers va être détruit, l’Explorateur Windows avertit l’objet de la vue du dossier en appelant sa méthode [**IShellView ::D estroyviewwindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-destroyviewwindow) .

## <a name="implementing-ishellview"></a>Implémentation de IShellView

Une fois l’objet dossier créé, l’Explorateur Windows appelle différentes méthodes [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) pour demander des informations ou notifier l’objet d’une modification de l’état de l’Explorateur Windows. Cette section décrit comment implémenter ces méthodes **IShellView** . Les méthodes restantes sont utilisées à des fins plus spécialisées, telles que la boîte de dialogue Ouvrir un fichier commun. Pour plus d’informations, consultez la documentation **IShellView** .

### <a name="addpropertysheetpages"></a>AddPropertySheetPages

Quand un utilisateur sélectionne des **options de dossier** dans le menu **Outils** de l’Explorateur Windows, une feuille de propriétés s’affiche et permet à l’utilisateur de modifier les options des dossiers. L’Explorateur Windows appelle la méthode [**IShellView :: AddPropertySheetPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-addpropertysheetpages) de l’objet affichage des dossiers pour vous permettre d’ajouter une page à cette feuille de propriétés.

L’Explorateur Windows passe un pointeur vers une fonction de rappel [AddPropSheetPageProc](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) dans le paramètre *lpfn* de [**IShellView :: AddPropertySheetPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-addpropertysheetpages). Appelez [CreatePropertySheetPage](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) pour créer la page, puis appelez AddPropSheetPageProc pour l’ajouter à la feuille de propriétés. Pour plus d’informations sur la façon de gérer les feuilles de propriétés, consultez [feuilles de propriétés](../controls/property-sheets.md).

### <a name="getcurrentinfo"></a>GetCurrentInfo

Lorsque l’utilisateur passe d’un dossier à un autre, l’Explorateur Windows tente de maintenir un affichage de dossiers similaire. Par exemple, si l’affichage du dossier précédent affichait de grandes icônes, le prochain devrait également. Lorsque l’Explorateur Windows appelle [**IShellView :: CreateViewWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) pour initialiser votre objet de vue de dossier, la méthode reçoit une structure [**FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) . Cette structure contient des informations qui vous permettent de rendre votre affichage des dossiers cohérent avec l’affichage du dossier précédent.

Pour vous assurer que la vue suivante est cohérente avec la vue actuelle, stockez la structure [**FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) . Si la vue change, par exemple de grande taille à petite icône, mettez à jour la structure en conséquence. Avant de basculer entre les vues, l’Explorateur Windows appelle [**IShellView :: GetCurrentInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-getcurrentinfo) pour demander les valeurs **FOLDERSETTINGS** actuelles pour les passer à l’objet de vue de dossier suivant.

### <a name="refresh"></a>Actualiser

L’utilisateur peut s’assurer que l’affichage des dossiers reflète l’état actuel du dossier en sélectionnant **Actualiser** dans le menu **affichage** ou en appuyant sur la touche F5. Lorsque l’utilisateur le fait, l’Explorateur Windows appelle la méthode [**IShellView :: Refresh**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-refresh) . Votre objet de vue de dossier doit immédiatement mettre à jour l’affichage du dossier.

### <a name="saveviewstate"></a>SaveViewState

L’Explorateur Windows appelle la méthode [**IShellView :: SaveViewState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-saveviewstate) pour inviter votre objet de vue de dossier à enregistrer son état d’affichage. Vous pouvez ensuite récupérer l’état lors de la prochaine consultation du dossier. Pour enregistrer un état d’affichage, il est préférable d’appeler la méthode [**IShellBrowser :: GetViewStateStream**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-getviewstatestream) . Cette méthode retourne une interface [IStream](/windows/win32/api/objidl/nn-objidl-istream) que votre objet d’affichage des dossiers peut utiliser pour enregistrer son état. Lorsque vous créez un autre affichage des dossiers, vous pouvez appeler la même méthode **IShellBrowser :: GetViewStateStream** pour obtenir un pointeur IStream qui vous permet de lire les paramètres enregistrés par les affichages des dossiers précédents.

### <a name="translateacelerator"></a>TranslateAcelerator

Quand l’utilisateur appuie sur une touche de raccourci, l’Explorateur Windows transmet le message à l’objet d’affichage des dossiers en appelant [**IShellView :: TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-translateaccelerator). Retourne \_ la valeur false pour que l’Explorateur Windows traite le message. Si votre objet de vue de dossier a traité le message, renvoyez \_ OK.

Lorsque la fenêtre d’affichage des dossiers a le focus, l’Explorateur Windows appelle [**IShellView :: TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-translateaccelerator) avant de traiter le message. Étant donné que la plupart des messages sont généralement associés à des commandes de barre de menus ou de barre d’outils de l’Explorateur Windows, votre objet de vue de dossier doit normalement retourner S \_ false. L’Explorateur Windows peut ensuite traiter le message normalement. Retourne \_ la valeur OK uniquement si le message est spécifique à un dossier et que vous ne souhaitez pas que l’Explorateur Windows effectue un traitement supplémentaire. Si l’affichage des dossiers n’a pas le focus, l’Explorateur Windows traite le message en premier. Elle appelle [**IShellBrowser :: TranslateAcceleratorSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-translateacceleratorsb) uniquement si elle ne gère pas le message.

## <a name="using-ishellbrowser-to-communicate-with-windows-explorer"></a>Utilisation de IShellBrowser pour communiquer avec l’Explorateur Windows

L’interface [**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) est utilisée par l’objet d’affichage des dossiers pour communiquer avec l’Explorateur Windows à diverses fins, notamment :

-   [Modification de la barre de menus de l’Explorateur Windows](#modifying-the-windows-explorer-menu-bar)
-   [Modification de la barre d’outils de l’Explorateur Windows](#modifying-the-windows-explorer-toolbar)
-   [Modification de la barre d’état de l’Explorateur Windows](#modifying-the-windows-explorer-status-bar)
-   [Stockage des informations spécifiques à la vue](#storing-view-specific-information)

### <a name="modifying-the-windows-explorer-menu-bar"></a>Modification de la barre de menus de l’Explorateur Windows

La barre de menus de l’Explorateur Windows permet à l’utilisateur de lancer une série de commandes. Par défaut, la barre de menus ne prend en charge que les commandes spécifiques à l’Explorateur Windows. Les messages [de \_ commande WM](../menurc/wm-command.md) associés sont traités par l’Explorateur Windows et ne sont pas transmis à votre objet de vue de dossier. Toutefois, vous pouvez modifier la barre de menus pour inclure un ou plusieurs éléments de menu spécifiques à un dossier avec [**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser). L’Explorateur Windows transmet les \_ messages de commande WM associés à ces éléments à la procédure de fenêtre de votre objet dossier pour traitement. Vous pouvez également supprimer ou désactiver toutes les commandes standard qui ne s’appliquent pas à votre application.

Les objets d’affichage des dossiers modifient généralement la barre de menus avant l’affichage du dossier. Ils doivent retourner la barre de menus à son état d’origine lorsque l’affichage des dossiers est détruit. Vous devrez peut-être également modifier la barre de menus chaque fois que votre vue de dossier gagne ou perd le focus.

Étant donné que l’Explorateur Windows appelle [**IShellView :: UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) chaque fois que l’état de la fenêtre d’affichage des dossiers change, la modification de la barre de menus est normalement incluse dans l’implémentation de cette méthode. La procédure de base pour modifier la barre de menus de l’Explorateur Windows est la suivante :

1.  Appelez [CreateMenu](/windows/win32/api/winuser/nf-winuser-createmenu) pour créer un handle de menu.
2.  Transmettez ce handle de menu à l’Explorateur Windows en appelant [**IShellBrowser :: InsertMenusSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb). L’Explorateur Windows renseigne ses informations de menu.
3.  Modifiez le menu en fonction des besoins.
4.  Appelez [**IShellBrowser :: SetMenuSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) pour que l’Explorateur Windows affiche la barre de menus modifiée.

L’Explorateur Windows possède six menus contextuels dans sa barre de menus. Comme avec tous les conteneurs OLE, le menu de l’Explorateur Windows est divisé en six groupes : fichier, modifier, conteneur, objet, fenêtre et aide. Le tableau suivant répertorie les menus contextuels de l’Explorateur Windows et le groupe qui leur est associé, ainsi que les ID de menu.



| Menu contextuel | id                     | Group     |
|-------------|------------------------|-----------|
| Fichier        | \_fichier de menu FCIDM \_      | Fichier      |
| Modifier        | FCIDM \_ menu \_ Edition      | Fichier      |
| Affichage        | \_affichage du menu FCIDM \_      | Conteneur |
| Favoris   | FCIDM \_ menu \_ favoris | Conteneur |
| Outils       | \_outils de menu FCIDM \_     | Conteneur |
| Aide        | \_aide du menu FCIDM \_      | Fenêtre    |



 

Quand vous transmettez le descripteur de menu à l’Explorateur Windows en appelant [**IShellBrowser :: InsertMenusSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb), vous devez également passer un pointeur vers une structure [OLEMENUGROUPWIDTHS](/windows/win32/api/oleidl/ns-oleidl-olemenugroupwidths) dont les membres ont été initialisés à zéro.

Quand [**IShellBrowser :: InsertMenusSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) est retourné, l’Explorateur Windows a ajouté ses éléments de menu. Vous pouvez ensuite utiliser le descripteur de menu retourné avec les fonctions de menu Windows standard, telles que [InsertMenuItem](/windows/win32/api/winuser/nf-winuser-insertmenuitema) , pour :

-   Ajoutez des éléments aux menus contextuels de l’Explorateur Windows.
-   Modifiez ou supprimez des éléments existants dans les menus contextuels de l’Explorateur Windows.
-   Ajoutez de nouveaux menus contextuels.

Utilisez les ID figurant dans le tableau pour identifier les différents menus contextuels de l’Explorateur Windows.

> [!Note]  
> Pour éviter les conflits avec les ID de commande de l’Explorateur Windows, les ID des éléments de menu que vous ajoutez doivent être compris entre FCIDM \_ SHVIEWFIRST et FCIDM \_ SHVIEWLAST. Ces deux valeurs sont définies dans shlobj. h.

 

Une fois que vous avez fini de modifier le menu, appelez [**IShellBrowser :: SetMenuSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) pour que l’Explorateur Windows affiche la nouvelle barre de menus.

Une fois l’affichage des dossiers initialement affiché, l’Explorateur Windows appelle [**IShellView :: UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) chaque fois que l’affichage des dossiers gagne ou perd le focus. Si vous avez des éléments de menu qui sont sensibles à l’état de l’affichage des dossiers, vous devez modifier le menu en conséquence, chaque fois que l’état change. Par exemple, vous pouvez avoir un élément de menu qui agit sur un élément dans l’affichage des dossiers qui a été sélectionné par l’utilisateur. Vous devez désactiver ou supprimer cet élément de menu lorsque l’affichage des dossiers perd le focus.

Lorsque l’Explorateur Windows appelle [**IShellView :: UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) pour indiquer que l’affichage des dossiers est désactivé, restaurez la barre de menus à son état d’origine en appelant [**IShellBrowser :: RemoveMenusSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-removemenussb).

### <a name="modifying-the-windows-explorer-toolbar"></a>Modification de la barre d’outils de l’Explorateur Windows

Outre la modification de la barre de menus de l’Explorateur Windows, vous pouvez également ajouter des boutons à la barre d’outils. Comme avec la barre de menus, la modification de la barre d’outils fait généralement partie de l’implémentation de [**IShellView :: UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) . La procédure d’ajout de boutons à la barre d’outils de l’Explorateur Windows est la suivante :

1.  Ajoutez l’image bitmap du bouton à la liste d’images de la barre d’outils.
2.  Définissez la chaîne de texte du bouton.
3.  Ajoutez le bouton à la barre d’outils.

Pour ajouter une image bitmap à la liste d’images d’une barre d’outils, envoyez la barre d’outils à un message [ \_ ADDBITMAP to](../controls/tb-addbitmap.md) en appelant [**IShellBrowser :: SendControlMsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg). Pour spécifier le contrôle ToolBar, définissez le paramètre *ID* de la méthode sur la **\_ barre d’outils FCW**. Définissez *wParam* sur le nombre d’images de bouton dans l’image bitmap et *lParam* sur l’adresse d’une structure [TBADDBITMAP](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap) . L’index d’image est retourné dans le paramètre *pret* .

Il existe deux façons de définir une chaîne pour le bouton :

-   Assignez la chaîne au membre **iString** de la structure [TBBUTTON](/windows/win32/api/commctrl/ns-commctrl-tbbutton) du bouton.
-   Appelez [**IShellBrowser :: SendControlMsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg) pour envoyer le contrôle de barre d’outils à un message [ \_ ADDSTRING to](../controls/tb-addstring.md) . Le paramètre *wParam* doit être défini sur zéro et le paramètre *lParam* sur la chaîne. L’index de chaîne est retourné dans le paramètre *pret* .

Pour ajouter le bouton à la barre d’outils, remplissez une structure [TBBUTTON](/windows/win32/api/commctrl/ns-commctrl-tbbutton) et transmettez-la à [**IShellBrowser :: SetToolbarItems**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-settoolbaritems). Comme avec le menu, votre ID de commande doit se situer entre FCIDM \_ SHVIEWFIRST et FCIDM \_ SHVIEWLAST. La barre d’outils ajoute ensuite le bouton à droite des boutons existants.

Par exemple, le fragment de code suivant ajoute un bouton standard à la barre d’outils de l’Explorateur Windows avec l’ID de commande IDB \_ MYBUTTON.


```
TBADDBITMAP tbadbm;
int iButtonIndex;
TBBUTTON tbb;

tbadbm.hInst = g_hInstance;    // The module's instance handle
tbadbm.nID = IDB_BUTTONIMAGE;  // The bitmap's resource ID

psb->SendControlMsg(FCW_TOOLBAR, TB_ADDBITMAP, 1,
                    reinterpret_cast<LPARAM>(&tbadbm), &iButtonIndex);

psb->SendControlMsg(FCW_TOOLBAR, TB_ADDSTRING, NULL,
                    reinterpret_cast<LPARAM>(szLabel), &iStringIndex);

ZeroMemory(&tbb, sizeof(TBBUTTON));
tbb.iBitmap = iButtonIndex;
tbb.iCommand = IDB_MYBUTTON;
tbb.iString = iStringIndex;
tbb.fsState = TBSTATE_ENABLED;
tbb.fsStyle = TBSTYLE_BUTTON;

psb->SetToolbarItems(&tbb, 1, FCT_MERGE);
```



Pour plus d’informations sur la gestion des contrôles ToolBar, consultez [Toolbar Controls](../controls/toolbar-control-reference.md).

### <a name="modifying-the-windows-explorer-status-bar"></a>Modification de la barre d’état de l’Explorateur Windows

Vous pouvez utiliser la barre d’état de l’Explorateur Windows pour afficher une variété d’informations utiles. Il existe deux façons d’utiliser la barre d’État :

-   Utilisez [**IShellBrowser :: SetStatusTextSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setstatustextsb) pour afficher une chaîne de texte dans la barre d’État.
-   Envoyer des messages directement au contrôle de barre d’État avec [**IShellBrowser :: SendControlMsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg).

La première méthode est simple, mais suffisante pour de nombreuses raisons. Pour une plus grande flexibilité, vous pouvez envoyer des messages directement au contrôle de barre d’État en appelant [**IShellBrowser :: SendControlMsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg) avec le paramètre *ID* défini sur **FCW \_ Status**. Pour plus d’informations sur les contrôles de barre d’État, consultez [barres d’État](../controls/status-bars.md).

### <a name="storing-view-specific-information"></a>Stockage des informations spécifiques à la vue

Quand une vue va être détruite, il est souvent utile de stocker des informations telles que l’État ou les paramètres de la vue. L’Explorateur Windows vous invite à effectuer cette tâche en appelant [**IShellView :: SaveViewState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-saveviewstate). La méthode recommandée pour enregistrer des informations spécifiques à une vue consiste à appeler [**IShellBrowser :: GetViewStateStream**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-getviewstatestream). Cette méthode vous fournit une interface [IStream](/windows/win32/api/objidl/nn-objidl-istream) que vous pouvez utiliser pour stocker les informations. Vous êtes libre d’utiliser n’importe quel format de données approprié.

 

 
