---
title: Personnalisation des boîtes de dialogue courantes
description: Cette rubrique explique comment utiliser les boîtes de dialogue courantes.
ms.assetid: 31ba9deb-32e6-455c-be0e-ff8bcc691c80
keywords:
- Bibliothèque de boîtes de dialogue communes, personnalisation
- boîtes de dialogue communes, personnalisation
- personnalisation des boîtes de dialogue courantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7eaa71c4f6fc6aa038ef150eb53935f6b3ec280
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292639"
---
# <a name="customizing-common-dialog-boxes"></a>Personnalisation des boîtes de dialogue courantes

Vous pouvez utiliser les boîtes de dialogue communes dans leur forme standard, ou vous pouvez les personnaliser. Du point de vue de l’utilisateur, le principal avantage de la boîte de dialogue commune est son apparence et sa fonctionnalité cohérentes de l’application à l’application. Par conséquent, il est important de personnaliser une boîte de dialogue courante uniquement lorsqu’elle est absolument nécessaire pour une application. Dans le cas contraire, l’apparence cohérente et l’interface de codage simple sont perdues. Les personnalisations appropriées laissent intacts autant de contrôles originaux que possible. L’augmentation de la taille de la boîte de dialogue ou l’ajout de nouveaux contrôles dans l’espace déjà disponible dans la boîte de dialogue est une personnalisation appropriée. Le masquage des contrôles d’origine ou la modification de la fonctionnalité prévue des contrôles d’origine est une personnalisation moins appropriée.

Cette section décrit les méthodes suivantes pour personnaliser une boîte de dialogue commune :

-   [Modèles personnalisés](#custom-templates)
-   [Procédures de Hook pour les boîtes de dialogue communes](#hook-procedures-for-common-dialog-boxes)
-   [Messages de boîte de dialogue communs](#common-dialog-messages)
-   [Support technique](#help-support)
    -   [Aide contextuelle](#context-sensitive-help)
    -   [Bouton d'aide](#the-help-button)

## <a name="custom-templates"></a>Modèles personnalisés

Les boîtes de dialogue communes possèdent des modèles par défaut qui définissent le nombre, le type et la position des contrôles standard dans la boîte de dialogue. Vous pouvez définir un modèle personnalisé pour permettre aux utilisateurs d’accéder à des contrôles supplémentaires qui sont propres à votre application.

Pour toutes les boîtes de dialogue courantes, à l’exception des boîtes de dialogue **ouvrir** et **Enregistrer sous** de style Explorateur, vous modifiez le modèle par défaut pour créer un modèle personnalisé qui remplace le modèle par défaut. Le modèle personnalisé définit le type et la position des contrôles standard, ainsi que des contrôles supplémentaires.

Quand vous créez un modèle de boîte de dialogue personnalisé en modifiant le modèle de boîte de dialogue par défaut, assurez-vous que les identificateurs de tous les contrôles ajoutés sont uniques et n’entrent pas en conflit avec les identificateurs des contrôles standard. Le tableau suivant répertorie le nom du fichier de modèle par défaut et le fichier include pour chacun des types de boîtes de dialogue courantes.



| Type de boîte de dialogue               | Fichier de modèle | Fichier include |
|-------------------------------|---------------|--------------|
| **Couleur**                     | Color. DLG     | ColorDlg. h   |
| **Rechercher**                      | FindText. DLG  | Dlgs. h       |
| **Font**                      | Font. DLG      | Dlgs. h       |
| **Ouvrir** (sélection multiple) | FileOpen. DLG  | Dlgs. h       |
| **Ouvrir** (sélection unique)   | FileOpen. DLG  | Dlgs. h       |
| **Mise en page**                | Prnsetup. DLG  | Dlgs. h       |
| **Imprimer**                     | Prnsetup. DLG  | Dlgs. h       |
| **Configuration** de l’impression (obsolète)    | Prnsetup. DLG  | Dlgs. h       |
| **Replace**                   | FindText. DLG  | Dlgs. h       |



 

Pour activer un modèle personnalisé, vous devez définir un indicateur dans le membre **Flags** de la structure correspondante de la boîte de dialogue. Si le modèle est une ressource d’une application ou d’une bibliothèque de liens dynamiques, définissez un indicateur **ENABLETEMPLATE** dans le membre **Flags** et utilisez les membres **HINSTANCE** et **lpTemplateName** de la structure pour identifier le nom du module et de la ressource. Si le modèle est déjà en mémoire, définissez un indicateur **ENABLETEMPLATEHANDLE** dans le membre **Flags** et utilisez le membre **HINSTANCE** pour identifier l’objet mémoire qui contient le modèle.

Dans la plupart des cas, vous devez également activer une procédure de Hook pour que la boîte de dialogue prenne en charge et traite les entrées pour les contrôles supplémentaires dans votre modèle personnalisé.

Pour les boîtes de dialogue **ouvrir** et **Enregistrer sous** de type Explorateur, les modèles par défaut ne peuvent pas être modifiés. Au lieu de cela, votre modèle personnalisé définit une boîte de dialogue enfant qui comprend uniquement les éléments à ajouter à la boîte de dialogue standard. Le modèle personnalisé peut également définir un contrôle statique qui spécifie l’emplacement du cluster de contrôles standard dans la boîte de dialogue enfant. Pour plus d’informations, consultez [modèles personnalisés de style Explorateur](open-and-save-as-dialog-boxes.md).

## <a name="hook-procedures-for-common-dialog-boxes"></a>Procédures de Hook pour les boîtes de dialogue communes

Pour chacune des boîtes de dialogue courantes, vous pouvez activer une procédure de Hook pour traiter les messages à partir de la procédure de la boîte de dialogue par défaut. Il existe deux types généraux de procédures de hook de dialogue courantes :

-   Procédure de raccordement standard utilisée avec les boîtes de dialogue les plus courantes
-   Procédure de raccordement de style Explorateur prise en charge par les boîtes de dialogue **ouvrir** et **Enregistrer sous**

Lorsque vous fournissez une procédure de raccordement standard pour l’une des boîtes de dialogue courantes, la procédure de boîte de dialogue par défaut gère ses messages comme suit.



| Message                                 | Gestion                                                                                                                                                                                                             |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_INITDIALOG WM**](wm-initdialog.md) | La procédure de boîte de dialogue par défaut traite le message avant de le passer à la procédure de raccordement. Le paramètre *lParam* du message est un pointeur vers la structure d’initialisation spécifiée lors de la création de la boîte de dialogue. |
| Tous les autres messages                      | La procédure de hook reçoit d’abord le message. Ensuite, la valeur de retour de la procédure de raccordement détermine si la procédure de dialogue par défaut traite le message ou l’ignore.                                     |



 

Pour les boîtes de dialogue **ouvrir** et **Enregistrer sous** de type Explorateur, la procédure de hook ne reçoit pas les messages destinés aux contrôles standard de la boîte de dialogue. Au lieu de cela, elle reçoit des messages de notification de la boîte de dialogue et des messages pour tous les contrôles supplémentaires que vous avez définis dans un modèle personnalisé. Pour plus d’informations, consultez [procédures de raccordement de style Explorateur](open-and-save-as-dialog-boxes.md).

Pour activer une procédure de Hook, définissez une valeur **ENABLEHOOK** dans le membre **Flags** de la structure correspondante de la boîte de dialogue. Si un indicateur **ENABLEHOOK** est défini, un membre **lpfnHook** de la structure doit spécifier l’adresse de la procédure de raccordement.

Le tableau suivant indique le type de procédure de raccordement à fournir pour chacune des boîtes de dialogue courantes.



| Type de boîte de dialogue                          | Procédure de Hook                                      |
|------------------------------------------|-----------------------------------------------------|
| **Couleur**                                | [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc)                      |
| **Rechercher** ou **remplacer**                  | [*FRHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpfrhookproc)                      |
| **Font**                                 | [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)                      |
| **Ouvrir** ou **Enregistrer sous** (style Explorateur) | [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)                    |
| **Ouvrir** ou **Enregistrer sous** (ancien style)      | [*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) |
| **Imprimer**                                | [*PrintHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpprinthookproc)                |
| **Mise en page**                           | [*PageSetupHook*](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook)                |



 

Pour la boîte de dialogue **mise en page** , vous pouvez également spécifier une procédure de hook [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) . Il s’agit d’une procédure de raccordement spéciale que vous pouvez utiliser pour personnaliser l’apparence de la page d’exemple affichée par la boîte de dialogue **mise en page** .

> [!Note]  
> La boîte de dialogue Configuration de l' **impression** a été remplacée par la boîte de dialogue **mise en page** . Les applications doivent utiliser la boîte de dialogue **mise en page** . Toutefois, pour des cas de compatibilité, la fonction [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) continue de prendre en charge l’affichage de la boîte de dialogue Configuration de l' **impression** . Vous pouvez fournir une procédure de hook [*SetupHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpsetuphookproc) pour la boîte de dialogue Configuration de l' **impression** .

 

## <a name="common-dialog-messages"></a>Messages de boîte de dialogue communs

Les boîtes de dialogue courantes utilisent des messages pour notifier votre procédure de fenêtre ou votre procédure de hook lorsque certains événements se produisent. En outre, il existe des messages que vous pouvez envoyer à une boîte de dialogue commune pour récupérer des informations ou pour contrôler le comportement ou l’apparence de la boîte de dialogue. Cette section décrit les messages de boîte de dialogue communs inscrits par la fonction [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) , les messages utilisés par la boîte de dialogue **police** et la boîte de dialogue **mise en page** , ainsi que les messages utilisés par les boîtes de dialogue **ouvrir** et **Enregistrer sous** de style Explorateur.

La bibliothèque de boîtes de dialogue communes définit un ensemble de chaînes de message. Vous pouvez transmettre une constante associée à l’une de ces chaînes de message à [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) pour obtenir un identificateur de message. Vous pouvez ensuite utiliser l’identificateur pour détecter et traiter les messages envoyés à partir d’une boîte de dialogue commune, ou pour envoyer des messages à une boîte de dialogue commune. Le tableau suivant présente les constantes de message et décrit leur utilisation.



| Constantes                               | Utilisation                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COLOROKSTRING**](colorokstring.md) | Une boîte de dialogue de **couleur** envoie ce message à la procédure de hook lorsque l’utilisateur sélectionne une couleur et clique sur le bouton **OK** . La procédure de raccordement peut accepter la couleur ou la rejeter et forcer la boîte de dialogue à rester ouverte.                                                                                                                                                                                             |
| [**FILEOKSTRING**](fileokstring.md)   | Une boîte de dialogue **ouvrir** ou **Enregistrer sous** envoie ce message à la procédure de hook lorsque l’utilisateur sélectionne un nom de fichier et clique sur le bouton **OK** . La procédure de raccordement peut accepter le nom de fichier ou la rejeter et forcer la boîte de dialogue à rester ouverte. pour les boîtes de dialogue **ouvrir** et **enregistrer sous** d’un navigateur, ce message a été remplacé par le message de notification [**CDN \_ FILEOK**](cdn-fileok.md) .<br/> |
| [**FINDMSGSTRING**](findmsgstring.md) | Une boîte de dialogue **Rechercher** ou **remplacer** envoie ce message à la procédure de fenêtre de sa fenêtre parente lorsque l’utilisateur clique sur **Rechercher suivant**, **remplacer** ou **remplacer tout**, ou ferme la boîte de dialogue. Le paramètre *lParam* du message est un pointeur vers une structure [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) contenant l’entrée de l’utilisateur.                                                                               |
| [**HELPMSGSTRING**](helpmsgstring.md) | Toutes les boîtes de dialogue courantes envoient ce message à la procédure de fenêtre de la fenêtre parente quand l’utilisateur clique sur le bouton **aide** . pour les boîtes de dialogue **ouvrir** et **enregistrer sous** d’un navigateur, ce message a été remplacé par le message de notification [**\_ d’aide CDN**](cdn-help.md) .<br/>                                                                                                                    |
| [**LBSELCHSTRING**](lbselchstring.md) | Une boîte de dialogue **ouvrir** ou **Enregistrer sous** envoie ce message à la procédure de hook lorsque l’utilisateur modifie la sélection dans la zone de liste **nom de fichier** . pour les boîtes de dialogue **ouvrir** et **enregistrer sous** d’un navigateur, ce message a été remplacé par le message de notification [**CDN \_ SELCHANGE**](cdn-selchange.md) .<br/>                                                                                           |
| [**SETRGBSTRING**](setrgbstring.md)   | Une procédure de raccordement peut envoyer ce message à une boîte de dialogue de **couleur** pour définir la sélection de couleur actuelle.                                                                                                                                                                                                                                                                                                                   |
| [**SHAREVISTRING**](sharevistring.md) | Une boîte de dialogue **ouvrir** ou **Enregistrer sous** envoie ce message à la procédure de hook si une violation de partage se produit pour le fichier sélectionné quand l’utilisateur clique sur le bouton **OK** . pour les boîtes de dialogue **ouvrir** et **enregistrer sous** d’un navigateur, ce message a été remplacé par le message de notification [**CDN \_ SHAREVIOLATION**](cdn-shareviolation.md) .<br/>                                                        |



 

Certaines boîtes de dialogue courantes envoient et reçoivent d’autres messages de fenêtre. La procédure de raccordement d’une boîte de dialogue de **police** peut envoyer n’importe quel **\_ message WM CHOOSEFONT \_ \* *_ à la boîte de dialogue _* font** . Pour plus d’informations, consultez [boîte de dialogue police](font-dialog-box.md). La boîte de dialogue **mise en page** envoie les messages **WM \_ PSD \_ \** _ si vous avez activé une procédure de hook [_PagePaintHook *](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) . Pour plus d’informations, consultez [boîte de dialogue mise en page](page-setup-dialog-box.md).

Les boîtes de dialogue **ouvrir** et **Enregistrer sous** de style Explorateur prennent en charge un ensemble de messages prédéfinis. Celles-ci incluent les messages de notification envoyés sous la forme d’un message [**WM \_ Notify**](../controls/wm-notify.md) à votre procédure de raccordement, ainsi que les messages que votre procédure de raccordement peut envoyer à la boîte de dialogue. Pour obtenir la liste complète de ces messages, consultez [procédures de hook de style Explorateur](open-and-save-as-dialog-boxes.md).

## <a name="help-support"></a>Support technique

Les boîtes de dialogue courantes fournissent une aide contextuelle pour les contrôles standard de la boîte de dialogue. Pour fournir une aide supplémentaire pour une boîte de dialogue commune, vous pouvez afficher un bouton **aide** et traiter les messages générés lorsque l’utilisateur clique sur le bouton. Le bouton **aide** est un complément de l’aide contextuelle par défaut. Le bouton **aide** est utile pour décrire l’usage général de la boîte de dialogue telle qu’elle s’applique à votre application.

-   [Aide contextuelle](#context-sensitive-help)
-   [Bouton d'aide](#the-help-button)

### <a name="context-sensitive-help"></a>Aide Context-Sensitive

Toutes les boîtes de dialogue courantes fournissent une aide contextuelle pour les contrôles standard de la boîte de dialogue. L’utilisateur peut afficher l’aide pour des contrôles individuels à l’aide de l’une des méthodes suivantes :

-   Sélectionnant le contrôle et en appuyant sur la touche F1.
-   Cliquant sur le bouton **?** dans la barre de titre et en cliquant ensuite sur un contrôle.
-   Cliquer sur le bouton droit de la souris sur un contrôle.

Si vous personnalisez une boîte de dialogue en ajoutant de nouveaux contrôles, vous devez également étendre la prise en charge de l’aide pour ces contrôles en traitant les demandes d’aide dans la procédure de raccordement. La procédure de raccordement reçoit les messages suivants lorsque l’utilisateur demande de l’aide.



| Action requise                                                           | Message                                      |
|-----------------------------------------------------------------------|----------------------------------------------|
| Cliquez avec le bouton droit de la souris sur un contrôle.                          | [**WM \_ CONTEXTMENU**](/windows/desktop/menurc/wm-contextmenu) |
| Appuyez sur la touche F1.                                                   | [**\_aide WM**](../shell/wm-help.md)               |
| Vous avez cliqué sur le **?** sur la barre de titre, puis sur un contrôle. | [**\_aide WM**](../shell/wm-help.md)               |



 

Vous devez traiter ces messages pour les contrôles que vous avez ajoutés, mais laisser la procédure de boîte de dialogue par défaut traitera les messages pour les contrôles standard. Pour plus d’informations sur le traitement de ces messages, consultez [l’aide](/previous-versions/windows/desktop/legacy/bb776786(v=vs.85))de.

### <a name="the-help-button"></a>Bouton d'aide

Vous pouvez afficher un bouton d' **aide** dans toutes les boîtes de dialogue courantes en définissant une valeur **SHOWHELP** dans le membre **Flags** de la structure d’initialisation de la boîte de dialogue. Si vous affichez le bouton **aide** , vous devez traiter la demande d’aide de l’utilisateur. Le traitement peut être effectué dans l’une des procédures de fenêtre de votre application ou dans une procédure de Hook pour la boîte de dialogue. En règle générale, vous devez traiter la demande d’aide en appelant la fonction [**WinHelp**](/windows/win32/api/winuser/nf-winuser-winhelpa) .

Pour traiter les messages d’aide dans l’une de vos procédures de fenêtre, vous devez obtenir un identificateur de message pour la chaîne définie par la valeur [**HELPMSGSTRING**](helpmsgstring.md) et identifier la fenêtre de réception des messages. Pour obtenir l’identificateur de message, spécifiez **HELPMSGSTRING** en tant que paramètre dans un appel à la fonction [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) . Lorsque vous créez la boîte de dialogue, utilisez le membre **hwndOwner** de la structure d’initialisation de la boîte de dialogue pour identifier la fenêtre qui doit recevoir les messages. La procédure de boîte de dialogue envoie le message à la procédure de fenêtre chaque fois que l’utilisateur clique sur le bouton **aide** .

Pour traiter les messages d’aide dans une procédure de Hook, vous devez traiter le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) . La procédure de raccordement fournit de l’aide si le paramètre *wParam* de ce message indique que l’utilisateur a cliqué sur le bouton **aide** . L’identificateur du bouton **d’aide** est la constante **pshHelp** définie dans le fichier Dlgs. h.

Les procédures de Hook pour les boîtes de dialogue **ouvrir** et **Enregistrer sous** de type Explorateur ne reçoivent pas les messages de [**\_ commande WM**](/windows/desktop/menurc/wm-command) pour le bouton **aide** . au lieu de cela, la boîte de dialogue envoie un message de notification d' [**\_ aide CDN**](cdn-help.md) à la procédure de hook lorsque l’utilisateur clique sur le bouton **aide** .

 

