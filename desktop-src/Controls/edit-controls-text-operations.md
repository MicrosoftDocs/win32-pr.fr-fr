---
title: Modifier les opérations de texte de contrôle
description: Le système traite automatiquement toutes les opérations de texte initiées par l’utilisateur et notifie l’application lorsque les opérations sont terminées.
ms.assetid: 9af3a1bc-4c87-4cc9-966d-50742be7c811
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8698fbd38241a0e5c3f40e69f7ab401fc22e3982e2bc70001733bc71daf49689
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826369"
---
# <a name="edit-control-text-operations"></a>Modifier les opérations de texte de contrôle

Le système traite automatiquement toutes les opérations de texte initiées par l’utilisateur et notifie l’application lorsque les opérations sont terminées.

Les rubriques suivantes traitent des opérations de texte initiées par l’utilisateur et de la réponse de l’application :

-   [Sélection d’un contrôle d’édition](#selecting-an-edit-control)
-   [Définition et récupération de texte](#setting-and-retrieving-text)
-   [Sélection de texte](#selecting-text)
-   [Remplacer du texte](#replacing-text)
-   [Modification de la police utilisée par un contrôle d’édition](#changing-the-font-used-by-an-edit-control)
-   [Opérations couper coller et effacer copier](#cut-copy-paste-and-clear-operations)
-   [Modification du texte](#modifying-text)
-   [Limitation du texte entré par l’utilisateur](#limiting-user-entered-text)
-   [Opérations de caractère et de ligne](#character-and-line-operations)
-   [Défilement du texte dans un contrôle d’édition](#scrolling-text-in-an-edit-control)
-   [Définition des taquets de tabulation et des marges](#setting-tab-stops-and-margins)
-   [Masquage de l’entrée utilisateur](#concealing-user-input)
-   [Utilisation d’entiers](#using-integers)
-   [Annuler des opérations de texte](#undoing-text-operations)
-   [Gestion des retours de ligne et des sauts de ligne](#handling-wordwrap-and-line-breaks)
-   [Récupération des points et des caractères](#retrieving-points-and-characters)
-   [Saisie semi-automatique de chaînes](#autocompletion-of-strings)
-   [Script complexe dans les contrôles d’édition](#complex-script-in-edit-controls)

## <a name="selecting-an-edit-control"></a>Sélection d’un contrôle d’édition

L’utilisateur peut sélectionner un contrôle d’édition en cliquant dessus avec la souris ou en appuyant sur la touche TAB pour y accéder. La méthode de tabulation fait partie d’une interface clavier prédéfinie fournie par le système. Pour obtenir une description complète de cette interface, consultez [boîtes de dialogue](/windows/desktop/dlgbox/dialog-boxes). Lorsque l’utilisateur sélectionne un contrôle d’édition, le système lui donne le focus clavier (voir « focus clavier et activation » dans [à propos](/windows/desktop/inputdev/about-keyboard-input)de l’entrée au clavier) et met en surbrillance le texte à l’aide de la vidéo inversée.

## <a name="setting-and-retrieving-text"></a>Définition et récupération de texte

Une application peut définir le texte d’un contrôle d’édition à l’aide de la fonction [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) , de la fonction [**SetDlgItemText**](/windows/desktop/DevNotes/-setdlgitemtext) ou en envoyant le contrôle à un message [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) .

Pour récupérer tout le texte d’un contrôle d’édition, utilisez d’abord la fonction [**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) ou le message [**WM \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength) pour déterminer la taille de la mémoire tampon nécessaire pour contenir le texte. Ensuite, récupérez le texte à l’aide de la fonction [**GetWindowText**](/windows/desktop/DevNotes/-getwindowtext) , de la fonction [**GetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-getdlgitemtexta) ou du message [**WM \_**](/windows/desktop/winmsg/wm-gettext) .

## <a name="selecting-text"></a>Sélection de texte

Après avoir sélectionné un contrôle d’édition, l’utilisateur peut sélectionner du texte dans le contrôle à l’aide de la souris ou du clavier. Une application peut récupérer les positions des caractères de début et de fin de la sélection actuelle dans un contrôle d’édition en envoyant le contrôle à un message [**em \_ GETSEL**](em-getsel.md) . La valeur de retour de la position de fin est supérieure d’une unité au dernier caractère de la sélection (autrement dit, la position du premier caractère qui suit le dernier caractère sélectionné).

Une application peut également sélectionner du texte dans un contrôle d’édition en envoyant au contrôle un message [**em \_ SETSEL**](em-setsel.md) avec les index de caractères de début et de fin pour la sélection. Par exemple, l’application peut utiliser **em \_ SETSEL** avec [**em \_ REPLACESEL**](em-replacesel.md) pour supprimer du texte d’un contrôle d’édition.

Ces trois messages s’appliquent aux contrôles d’édition à une seule ligne et à plusieurs lignes.

## <a name="replacing-text"></a>Remplacer du texte

Une application peut remplacer le texte sélectionné dans un contrôle d’édition en lui envoyant un message [**em \_ REPLACESEL**](em-replacesel.md) avec un pointeur vers le texte de remplacement. S’il n’y a aucune sélection actuelle, **em \_ REPLACESEL** insère le texte de remplacement au niveau du point d’insertion. L’application peut recevoir un code de notification en [ \_ ERRSPACE](en-errspace.md) si le texte de remplacement dépasse la mémoire disponible. Ce message s’applique aux contrôles d’édition à une seule ligne et à plusieurs lignes.

Une application peut utiliser [**em \_ REPLACESEL**](em-replacesel.md) pour remplacer une partie du texte d’un contrôle d’édition ou la fonction [**SetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta) pour la remplacer.

## <a name="changing-the-font-used-by-an-edit-control"></a>Modification de la police utilisée par un contrôle d’édition

Une application peut modifier la police utilisée par un contrôle d’édition en envoyant le message [**WM \_ SetFont**](/windows/desktop/winmsg/wm-setfont) . La plupart des applications le font lors du traitement du message [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) . La modification de la police ne modifie pas la taille du contrôle d’édition ; les applications qui envoient le message **WM \_ SetFont** peuvent avoir à récupérer les métriques de police du texte et recalculer la taille du contrôle d’édition. Pour plus d’informations sur les polices et les métriques de police, consultez [polices et texte](/windows/desktop/gdi/fonts-and-text).

## <a name="cut-copy-paste-and-clear-operations"></a>Opérations couper coller et effacer copier

Il y a quatre messages pour déplacer du texte entre un contrôle d’édition et le presse-papiers. Le message de [**\_ copie WM**](/windows/desktop/dataxchg/wm-copy) copie la sélection actuelle (le cas échéant) d’un contrôle d’édition dans le presse-papiers sans la supprimer du contrôle d’édition. Le message [**WM \_ Cut**](/windows/desktop/dataxchg/wm-cut) supprime la sélection actuelle (le cas échéant) dans le contrôle d’édition et copie le texte supprimé dans le presse-papiers. Le message [**WM \_ Clear**](/windows/desktop/dataxchg/wm-clear) supprime la sélection actuelle (le cas échéant) d’un contrôle d’édition, mais ne la copie pas dans le presse-papiers (sauf si l’utilisateur a appuyé sur la touche Maj). Le message [**WM \_ Paste**](/windows/desktop/dataxchg/wm-paste) copie le texte du presse-papiers dans un contrôle d’édition au niveau du point d’insertion. Ces quatre messages s’appliquent aux contrôles d’édition à une seule ligne et à plusieurs lignes.

Microsoft Windows NT 4,0 et versions ultérieures : un contrôle d’édition comprend un menu contextuel intégré qui permet à l’utilisateur de déplacer facilement du texte entre le contrôle d’édition et le presse-papiers. Le menu contextuel s’affiche lorsque l’utilisateur clique avec le bouton droit sur le contrôle. Les commandes du menu contextuel incluent **Annuler**, **couper**, **copier**, **coller**, **supprimer** et **Sélectionner tout**.

## <a name="modifying-text"></a>Modification du texte

L’utilisateur peut sélectionner, supprimer ou déplacer du texte dans un contrôle d’édition. Le système gère un indicateur interne pour chaque contrôle d’édition, indiquant si le contenu du contrôle a été modifié. Le système efface cet indicateur lorsqu’il crée le contrôle et définit l’indicateur chaque fois que le texte du contrôle est modifié. Une application peut récupérer l’indicateur de modification en envoyant un message au contrôle en [**em \_ GETMODIFY**](em-getmodify.md) . L’application peut ensuite définir ou effacer l’indicateur de modification en envoyant le contrôle à un message [**em \_ SETMODIFY**](em-setmodify.md) . Ces messages s’appliquent aux contrôles d’édition à une seule ligne et à plusieurs lignes.

## <a name="limiting-user-entered-text"></a>Limitation du texte entré par l’utilisateur

La limite par défaut de la quantité de texte qu’un utilisateur peut entrer dans un contrôle d’édition est de 32 Ko. Une application peut modifier la limite par défaut en envoyant un message au contrôle en [**em \_ SETLIMITTEXT**](em-setlimittext.md) . Ce message définit une limite inconditionnelle sur le nombre d’octets que l’utilisateur peut entrer dans un contrôle d’édition, mais n’affecte ni le texte qui se trouve déjà dans le contrôle lorsque le message a été envoyé, ni le texte copié dans le contrôle par la fonction [**SetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta) ou le message [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) . Par exemple, supposons que l’application utilise la fonction **SetDlgItemText** pour placer 500 octets dans un contrôle d’édition, et que l’utilisateur entre également 500 octets (1 000 octets au total). Si l’application envoie ensuite un **message \_ SETLIMITTEXT em** pour limiter le texte entré par l’utilisateur à 300 octets, les 1 000 octets déjà présents dans le contrôle d’édition restent là et l’utilisateur ne peut pas ajouter de texte supplémentaire. En revanche, si l’application envoie un message **\_ SETLIMITTEXT em** qui limite le texte entré par l’utilisateur à 1 300 octets, les 1 000 octets sont conservés, mais l’utilisateur peut ajouter 300 octets de plus.

Lorsque l’utilisateur atteint la limite de caractères d’un contrôle d’édition, le système envoie à l’application un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) contenant un code de notification en [ \_ MAXTEXT](en-maxtext.md) . Ce code de notification ne signifie pas que la mémoire est épuisée, mais que la limite pour le texte entré par l’utilisateur a été atteinte. l’utilisateur ne peut pas entrer de texte supplémentaire. Pour modifier cette limite, une application doit envoyer au contrôle un nouveau message [**em \_ SETLIMITTEXT**](em-setlimittext.md) avec une limite supérieure.

À titre d’exemple d’utilisation de [**em \_ SETLIMITTEXT**](em-setlimittext.md) et [en \_ MAXTEXT](en-maxtext.md), supposez que l’application doit limiter l’utilisateur à quatre caractères au maximum dans un contrôle d’édition. L’application utilise **em \_ SETLIMITTEXT** pour spécifier une limite de quatre caractères. Si l’utilisateur a tenté d’entrer un cinquième caractère, le système envoie un \_ Code de notification en MAXTEXT à l’application.

## <a name="character-and-line-operations"></a>Opérations de caractère et de ligne

Il existe plusieurs messages qui retournent des informations sur les caractères et les lignes d’un contrôle d’édition. La plupart des messages retournent un index, généralement un nombre de base zéro, pour faire référence à un caractère ou à une ligne. Par exemple, dans un contrôle d’édition sur une seule ligne qui contient n caractères, l’index de ligne est égal à zéro et les caractères sont indexés de zéro à n-1. Dans un contrôle d’édition multiligne qui contient m lignes et n caractères, les lignes sont indexées de zéro à m-1, et les caractères sont indexés de zéro à n-1. Notez que l’indexation de caractères ignore les sauts de ligne.

Une application peut déterminer le nombre de caractères dans un contrôle d’édition en envoyant le message [**WM \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength) au contrôle d’édition. Ce message retourne la longueur, en caractères (à l’exclusion du caractère null de fin), du texte dans un contrôle d’édition sur une seule ligne ou multiligne. Le message [**em \_ LINELENGTH**](em-linelength.md) retourne la longueur, en caractères, d’une ligne spécifiée par l’index de caractère d’un caractère dans la ligne. La longueur retournée n’inclut pas les caractères sélectionnés. Une application peut utiliser ces messages dans un contrôle d’édition à ligne unique ou multiligne.

Le message [**em \_ GETFIRSTVISIBLELINE**](em-getfirstvisibleline.md) retourne l’index de base zéro de la ligne visible supérieure dans un contrôle d’édition multiligne, ou l’index de base zéro du premier caractère visible dans un contrôle d’édition sur une seule ligne. Une application peut copier une ligne d’un contrôle d’édition dans une mémoire tampon en envoyant le message [**em \_ GETLINE**](em-getline.md) au contrôle d’édition. La ligne est spécifiée par son index de ligne et le premier mot de la mémoire tampon de réception contient le nombre maximal d’octets à copier dans la mémoire tampon. La valeur de retour est le nombre d’octets copiés. Ce message peut également être utilisé dans un contrôle d’édition à ligne unique ou multiligne.

Des messages uniques sont disponibles pour retourner les informations relatives à une ligne dans un contrôle d’édition multiligne. Le message [**em \_ GETLINECOUNT**](em-getlinecount.md) retourne le nombre de lignes dans un contrôle d’édition. Le message [**em \_ LINEFROMCHAR**](em-linefromchar.md) retourne l’index de la ligne contenant un index de caractère spécifié. Le message [**em \_ LINEINDEX**](em-lineindex.md) retourne l’index du premier caractère d’une ligne spécifiée.

## <a name="scrolling-text-in-an-edit-control"></a>Défilement du texte dans un contrôle d’édition

Pour implémenter le défilement dans un contrôle d’édition, vous pouvez utiliser les styles de défilement automatique décrits dans [modifier les types et les styles de contrôle](about-edit-controls.md), ou vous pouvez ajouter explicitement des barres de défilement au contrôle d’édition. Pour ajouter une barre de défilement horizontale, utilisez le style WS \_ HSCROLL ; pour ajouter une barre de défilement verticale, utilisez le style [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles). Un contrôle d’édition avec des barres de défilement traite ses propres messages de barre de défilement. Pour plus d’informations sur l’ajout de barres de défilement aux contrôles d’édition, consultez [barres de défilement](scroll-bars.md).

Le système fournit trois messages qu’une application peut envoyer à un contrôle d’édition avec des barres de défilement. Le [**message \_ LINESCROLL em**](em-linescroll.md) peut faire défiler un contrôle d’édition multiligne à la fois verticalement et horizontalement. Le paramètre *lParam* spécifie le nombre de lignes à faire défiler verticalement à partir de la ligne active et le paramètre *wParam* spécifie le nombre de caractères à faire défiler horizontalement, en commençant par le caractère actuel. Le contrôle d’édition n’accuse pas réception des messages de défilement horizontal s’il a le style de [**\_ droite**](edit-control-styles.md) du [**\_ Centre des e**](edit-control-styles.md) /s. Le **message \_ LINESCROLL em** s’applique uniquement aux contrôles d’édition multiligne.

Le message de [**\_ défilement em**](em-scroll.md) fait défiler verticalement un contrôle d’édition multiligne. Le paramètre *wParam* spécifie l’action de défilement. Le message de **\_ défilement em** s’applique uniquement aux contrôles d’édition multiligne. **Em \_ Le défilement** a le même effet que le message [**WM \_ VSCROLL**](wm-vscroll.md) .

Le [**message \_ SCROLLCARET em**](em-scrollcaret.md) fait défiler le signe insertion dans un contrôle d’édition.

## <a name="setting-tab-stops-and-margins"></a>Définition des taquets de tabulation et des marges

Une application peut définir des taquets de tabulation dans un contrôle d’édition multiligne à l’aide du message [**em \_ SETTABSTOPS**](em-settabstops.md) . (La valeur par défaut d’un taquet de tabulation est de huit caractères.) Quand une application ajoute du texte au contrôle d’édition, les caractères de tabulation dans le texte génèrent automatiquement l’espace jusqu’au taquet de tabulation suivant. Le **message \_ SETTABSTOPS em** n’entraîne pas automatiquement le redessin du texte par le système. Pour ce faire, une application peut appeler la fonction [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) . Le **message \_ SETTABSTOPS em** s’applique uniquement aux contrôles d’édition multiligne.

Une application peut définir la largeur des marges gauche et droite d’un contrôle d’édition à l’aide du message [**em \_ setMargins**](em-setmargins.md) . Après l’envoi de ce message, le système redessine le contrôle d’édition pour refléter les nouveaux paramètres de marge. Une application peut récupérer la largeur de la marge de gauche ou de droite en envoyant le message [**em \_ GETMARGINS**](em-getmargins.md) . Par défaut, les marges du contrôle d’édition sont définies sur une valeur suffisamment grande pour accueillir le plus grand dépassement horizontal de caractère horizontal (largeur ABC négative) pour la police actuelle utilisée dans le contrôle d’édition.

## <a name="concealing-user-input"></a>Masquage de l’entrée utilisateur

Une application peut utiliser un caractère de mot de passe dans un contrôle d’édition pour masquer l’entrée d’utilisateur. Lorsqu’un caractère de mot de passe est défini, il est affiché à la place de chaque caractère que l’utilisateur tape. Lorsqu’un caractère de mot de passe est supprimé, le contrôle affiche les caractères que l’utilisateur tape. Si l’application crée un contrôle d’édition sur une seule ligne à l’aide du [**\_ mot de passe style es**](edit-control-styles.md), le caractère de mot de passe par défaut est un astérisque ( \* ). Une application peut utiliser le message [**em \_ SETPASSWORDCHAR**](em-setpasswordchar.md) pour supprimer ou définir un caractère de mot de passe différent et le message [**em \_ GETPASSWORDCHAR**](em-getpasswordchar.md) pour récupérer le caractère de mot de passe actuel. Ces messages s’appliquent uniquement aux contrôles d’édition sur une seule ligne.

## <a name="using-integers"></a>Utilisation d’entiers

Il existe deux fonctions de conversion d’entiers pour les contrôles d’édition conçus pour contenir uniquement des nombres. La fonction [**SetDlgItemInt**](/windows/desktop/api/winuser/nf-winuser-setdlgitemint) crée la représentation sous forme de chaîne d’un entier spécifié (signé ou non signé) et envoie la chaîne à un contrôle d’édition. **SetDlgItemInt** ne retourne aucune valeur. La fonction [**GetDlgItemInt**](/windows/desktop/api/winuser/nf-winuser-getdlgitemint) crée un entier (signé ou non signé) à partir de sa représentation sous forme de chaîne dans un contrôle d’édition. **GetDlgItemInt** retourne l’entier (ou une valeur d’erreur).

## <a name="undoing-text-operations"></a>Annuler des opérations de texte

Chaque contrôle d’édition gère un indicateur d’annulation qui indique si une application peut inverser ou annuler l’opération la plus récente dans le contrôle d’édition (annulation de la suppression du texte, par exemple). Le contrôle d’édition définit l’indicateur d’annulation pour indiquer que l’opération peut être annulée et la réinitialise pour indiquer que l’opération ne peut pas être annulée. Une application peut déterminer le paramètre de l’indicateur d’annulation en envoyant le contrôle à un message [**em \_ CANUNDO**](em-canundo.md) .

Une application peut annuler l’opération la plus récente en envoyant le contrôle à un message d' [**\_ annulation em**](em-undo.md) . Une opération peut être annulée si aucune autre opération de contrôle d’édition ne se produit en premier. Par exemple, l’utilisateur peut supprimer du texte, remplacer le texte (annuler la suppression), puis supprimer le texte (annuler le remplacement). Le message d' **\_ annulation em** s’applique aux contrôles d’édition à une seule ligne et à plusieurs lignes, et fonctionne toujours pour les contrôles d’édition sur une seule ligne.

Une application peut réinitialiser l’indicateur d’annulation d’un contrôle d’édition en envoyant le contrôle à un message [**em \_ EMPTYUNDOBUFFER**](em-emptyundobuffer.md) . Le système réinitialise automatiquement l’indicateur d’annulation chaque fois qu’un contrôle d’édition reçoit un message [**em \_ SETHANDLE**](em-sethandle.md) ou [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) . La fonction [**SetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta) envoie un message **WM \_ SETTEXT** .

## <a name="handling-wordwrap-and-line-breaks"></a>Gestion des retours de ligne et des sauts de ligne

Une application peut utiliser des fonctions WordWrap avec des contrôles d’édition multiligne pour localiser le mot ou le fragment de mot qui doit être renvoyé à la ligne suivante. À l’aide de la fonction de WordWrap par défaut fournie par le système, les lignes se terminent toujours par les espaces entre les mots. Une application peut spécifier sa propre fonction WordWrap en fournissant une fonction WordWrap [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) et en envoyant le contrôle Edit à un message [**em \_ SETWORDBREAKPROC**](em-setwordbreakproc.md) . Une application peut récupérer l’adresse de la fonction WordWrap actuelle en envoyant le contrôle à un message [**em \_ GETWORDBREAKPROC**](em-getwordbreakproc.md) .

Une application peut diriger un contrôle d’édition multiligne pour ajouter ou supprimer un caractère de saut de ligne conditionnel (deux retours chariot et un saut de ligne) automatiquement à la fin des lignes de texte renvoyées à la ligne. Une application peut activer ou désactiver cette fonctionnalité en envoyant le contrôle d’édition à un message [**em \_ FMTLINES**](em-fmtlines.md) . Ce message s’applique uniquement aux contrôles d’édition multiligne et n’affecte pas une ligne qui se termine par un saut de ligne matériel (un retour chariot et un saut de ligne entré par l’utilisateur). En outre, dans les contrôles d’édition multiligne, une application peut spécifier le style [**es \_ WANTRETURN**](edit-control-styles.md) pour demander que le système insère un retour chariot lorsque l’utilisateur appuie sur la touche entrée dans le contrôle d’édition.

## <a name="retrieving-points-and-characters"></a>Récupération des points et des caractères

Pour déterminer le caractère le plus proche d’un point spécifié dans la zone cliente d’un contrôle d’édition, envoyez le message [**em \_ CHARFROMPOS**](em-charfrompos.md) au contrôle. Le message retourne l’index de caractère et l’index de ligne du caractère le plus proche du point. De même, vous pouvez récupérer les coordonnées de la zone cliente d’un caractère spécifié en envoyant le message [**em \_ POSFROMCHAR**](em-posfromchar.md) . Le message retourne les coordonnées x et y de l’angle supérieur gauche du caractère spécifié.

## <a name="autocompletion-of-strings"></a>Saisie semi-automatique de chaînes

La saisie semi-automatique développe des chaînes qui ont été entrées partiellement dans un contrôle d’édition dans des chaînes complètes. par exemple, lorsqu’un utilisateur commence à entrer une URL dans le contrôle d’édition d’adresse qui est incorporé dans la Windows barre d’outils Internet Explorer, la saisie semi-automatique développe la chaîne en une ou plusieurs url complètes qui sont cohérentes avec la chaîne partielle existante. Une chaîne d’URL partielle telle que « MIC » peut être développée en « https://www.microsoft.com » ou «» https://www.microsoft.com/windows . La saisie semi-automatique est généralement utilisée avec les contrôles d’édition ou avec les contrôles dotés d’un contrôle d’édition incorporé.

Pour plus d’informations, consultez la documentation de l’interface [**IAutoComplete**](/windows/desktop/api/shldisp/nn-shldisp-iautocomplete) et [**IAutoComplete2**](/windows/desktop/api/shldisp/nn-shldisp-iautocomplete2) .

## <a name="complex-script-in-edit-controls"></a>Script complexe dans les contrôles d’édition

Un *script complexe* est un langage dont le formulaire imprimé n’est pas disposé de manière simple. Par exemple, un script complexe peut permettre un rendu bidirectionnel, une mise en forme contextuelle de glyphes ou une combinaison de caractères. Les contrôles d’édition standard ont été étendus pour prendre en charge le texte multilingue et les scripts complexes. Cela comprend non seulement l’entrée et l’affichage, mais également le déplacement du curseur sur les clusters de caractères (par exemple, dans le script thaï et DÉVANÂGARÎ).

Une application bien écrite reçoit cette prise en charge automatiquement, sans modification. Là encore, vous devez envisager d’ajouter la prise en charge pour l’ordre de lecture de droite à gauche et l’alignement à droite. Dans ce cas, basculez les indicateurs de style étendus de la fenêtre Modifier le contrôle pour contrôler ces attributs, comme indiqué dans l’exemple suivant.


```
// ID_EDITCONTROL is the control ID in the resource file.
HANDLE hWndEdit = GetDlgItem(hDlg, ID_EDITCONTROL);
LONG lAlign = GetWindowLong(hWndEdit, GWL_EXSTYLE) ;

// To toggle alignment
lAlign ^= WS_EX_RIGHT ;

// To toggle reading order
lAlign ^= WS_EX_RTLREADING ;
```



Après avoir défini la valeur **lAlign** , activez le nouvel affichage en définissant le style étendu de la fenêtre Modifier le contrôle comme suit.


```
// This assumes your edit control is in a dialog box. If not, 
// get the edit control handle from another source.

SetWindowLong(hWndEdit, GWL_EXSTYLE, lAlign);
InvalidateRect(hWndEdit, NULL, FALSE);
```



Uniscribe est un autre ensemble de fonctions qui permettent de contrôler précisément le traitement des scripts complexes. Pour plus d’informations, consultez [Uniscribe](/windows/desktop/Intl/uniscribe).

 

 