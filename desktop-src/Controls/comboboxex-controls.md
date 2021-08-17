---
title: À propos des contrôles ComboBoxEx
description: Les contrôles ComboBoxEx sont des contrôles de zone de liste déroulante qui fournissent une prise en charge native des images d’élément.
ms.assetid: a4b1aa79-40c4-4eff-801c-4f308d86fb35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993fa8db73246c62f8ceee805e767c13ffdcc15a12d0222e09f308324cc97bab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831835"
---
# <a name="about-comboboxex-controls"></a>À propos des contrôles ComboBoxEx

Les contrôles ComboBoxEx sont des contrôles de zone de liste déroulante qui fournissent une prise en charge native des images d’élément. Pour faciliter l’accès aux images d’élément, le contrôle fournit la prise en charge de la liste d’images. À l’aide de ce contrôle, vous pouvez fournir les fonctionnalités d’une zone de liste déroulante sans avoir à dessiner manuellement les graphiques d’éléments.

Cette rubrique contient les sections suivantes.

-   [Création de contrôles ComboBoxEx](#creating-comboboxex-controls)
-   [Styles de contrôle ComboBoxEx](#comboboxex-control-styles)
-   [Éléments de contrôle ComboBoxEx](#comboboxex-control-items)
-   [Éléments de rappel](#callback-items)
-   [Listes d’images de contrôle ComboBoxEx](#comboboxex-control-image-lists)
-   [À propos des messages de notification de contrôle ComboBoxEx](#about-comboboxex-control-notification-messages)
-   [ComboBoxEx le transfert des messages de contrôle](#comboboxex-control-message-forwarding)

## <a name="creating-comboboxex-controls"></a>Création de contrôles ComboBoxEx

En fait, un contrôle ComboBoxEx crée une zone de liste déroulante enfant et effectue Owner Draw tâches pour vous en fonction d’une liste d’images affectée. Par conséquent, le style [**CBS \_ OWNERDRAWFIXED**](combo-box-styles.md) est implicite et il n’est pas nécessaire de l’utiliser lors de la création du contrôle. Étant donné que les listes d’images sont utilisées pour fournir des graphiques d’élément, le style [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) ne peut pas être utilisé.

Un contrôle ComboBoxEx doit être initialisé en appelant la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , en spécifiant \_ les \_ classes USEREX ICC dans la structure [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) associée.

Vous pouvez créer un contrôle ComboBoxEx à l’aide de la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) et en spécifiant [**WC \_ ComboBoxEx**](common-control-window-classes.md) comme classe de fenêtre. La classe est inscrite lorsque la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) est appelée, comme expliqué ci-dessus.

Les contrôles ComboBoxEx sont créés sans liste d’images par défaut. Pour utiliser des images d’élément, vous devez créer une liste d’images pour le contrôle ComboBoxEx et l’assigner au contrôle à l’aide du message [**CBEM \_ SETIMAGELIST**](cbem-setimagelist.md) . Si vous n’assignez pas de liste d’images au contrôle ComboBoxEx, le contrôle affiche uniquement le texte de l’élément.

## <a name="comboboxex-control-styles"></a>Styles de contrôle ComboBoxEx

Les contrôles ComboBoxEx prennent uniquement en charge les styles de zone de liste modifiable suivants :

-   CBS \_ simple
-   \_liste déroulante CBS
-   \_DropDownList SCC
-   \_enfant WS

Il existe également plusieurs [styles étendus de contrôle ComboBoxEx](comboboxex-control-extended-styles.md) qui sont utilisés uniquement par ComboBoxEx.

> [!Note]  
> Le [**style \_ simple CBS**](combo-box-styles.md) peut ne pas fonctionner correctement dans certains cas.

 

Étant donné que le contrôle ComboBoxEx effectue Owner Draw tâches pour vous en fonction d’une liste d’images affectée, le style [**CBS \_ OWNERDRAWFIXED**](combo-box-styles.md) est implicite ; vous n’avez pas besoin de l’utiliser lors de la création du contrôle. Étant donné que les listes d’images sont utilisées pour fournir des graphiques d’élément, le style [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) ne peut pas être utilisé. Le contrôle ComboBoxEx prend également en charge les [styles étendus de contrôle ComboBoxEx](comboboxex-control-extended-styles.md) qui fournissent des fonctionnalités supplémentaires.

## <a name="comboboxex-control-items"></a>Éléments de contrôle ComboBoxEx

Les contrôles ComboBoxEx gèrent les informations d’élément à l’aide d’une structure [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) . Cette structure comprend des membres pour les index d’éléments, les index d’images (normal, état de sélection et superposition), les valeurs de mise en retrait, les chaînes de texte et les valeurs spécifiques aux éléments.

Le contrôle ComboBoxEx permet d’accéder facilement aux éléments et de les manipuler par le biais de la messagerie. Pour ajouter ou supprimer un élément, envoyez le message [**CBEM \_ INSERTITEM**](cbem-insertitem.md) ou [**CBEM \_ DELETEITEM**](cbem-deleteitem.md) . Vous pouvez modifier les éléments qui se trouvent actuellement dans le contrôle à l’aide du message [**CBEM \_ SETITEM**](cbem-setitem.md) .

## <a name="callback-items"></a>Éléments de rappel

Les contrôles ComboBoxEx prennent en charge les attributs d’élément de rappel. Vous pouvez spécifier un élément en tant qu’élément de rappel lorsque vous l’ajoutez au contrôle à l’aide de [**CBEM \_ INSERTITEM**](cbem-insertitem.md). Lorsque vous assignez des valeurs à la structure [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) d’un élément, vous devez spécifier les valeurs d’indicateur de rappel appropriées. Voici les membres de la structure **COMBOBOXEXITEM** et leurs valeurs d’indicateur de rappel correspondantes.



| Membre             | Valeur de rappel      |
|--------------------|---------------------|
| **pszText**        | LPSTR \_ TEXTCALLBACK |
| **iImage**         | Je \_ IMAGECALLBACK    |
| **iSelectedImage** | Je \_ IMAGECALLBACK    |
| **iOverlay**       | Je \_ IMAGECALLBACK    |
| **iIndent**        | Je \_ INDENTCALLBACK   |



 

Le contrôle demande des informations sur les éléments de rappel en envoyant des codes de notification [CBEN \_ GETDISPINFO](cben-getdispinfo.md) . Cette notification est envoyée sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . Lorsque votre application traite ce message, elle doit fournir les informations demandées pour le contrôle. Si vous définissez le membre **Mask** de la structure [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) associée sur CBEIF \_ di \_ SETITEM, le contrôle stocke les données d’élément et ne les redemande pas.

## <a name="comboboxex-control-image-lists"></a>Listes d’images de contrôle ComboBoxEx

Si vous souhaitez qu’un contrôle ComboBoxEx affiche des icônes avec des éléments, vous devez fournir une liste d’images. Les contrôles ComboBoxEx prennent en charge jusqu’à trois images pour un élément : une pour son état sélectionné, une pour son état non sélectionné et une pour une image de superposition. Affectez une liste d’images existante à un contrôle ComboBoxEx à l’aide du message [**CBEM \_ SETIMAGELIST**](cbem-setimagelist.md) .

La structure [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) contient des membres qui représentent les index d’images pour chaque liste d’images (sélectionnée, désélectionnée et superposée). Pour chaque élément, définissez ces membres de façon à afficher les images souhaitées. Il n’est pas nécessaire de spécifier des index d’images pour chaque type d’image. Vous pouvez mélanger et faire correspondre les types d’images comme vous le souhaitez, mais vous devez toujours définir le membre **Mask** de la structure **COMBOBOXEXITEM** pour indiquer les membres qui sont utilisés. Le contrôle ignore les membres qui n’ont pas été marqués comme étant valides.

> [!Note]  
> Si vous utilisez le [**style \_ simple CBS**](combo-box-styles.md) , les icônes ne sont pas affichées.

 

## <a name="about-comboboxex-control-notification-messages"></a>À propos des messages de notification de contrôle ComboBoxEx

Un contrôle ComboBoxEx envoie des messages de notification pour signaler les modifications dans lui-même ou pour demander des informations sur les éléments de rappel. Le parent du contrôle reçoit tous les messages de [**\_ commande WM**](/windows/desktop/menurc/wm-command) de la zone de liste déroulante contenue dans le contrôle ComboBoxEx. Le contrôle ComboBoxEx envoie ses propres notifications à l’aide de messages de [**\_ notification WM**](wm-notify.md) . Par conséquent, le propriétaire du contrôle doit être préparé à traiter les deux formes de message de notification.

Voici les codes de notification spécifiques à ComboBoxEx qui sont envoyés par le biais de messages de notification [**WM \_**](wm-notify.md) .



| Notification                              | **Description**                                                                                                            |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [CBEN \_ BEGINEDIT](cben-beginedit.md)     | Signale que l’utilisateur a activé la liste déroulante ou qu’il a cliqué dans la zone d’édition du contrôle.                               |
| [CBEN \_ ENDEDIT](cben-endedit.md)         | Signale que l’utilisateur a sélectionné un élément dans la liste déroulante ou a terminé une opération de modification dans la zone d’édition. |
| [CBEN \_ DELETEITEM](cben-deleteitem.md)   | Signale qu’un élément a été supprimé.                                                                                          |
| [CBEN \_ GETDISPINFO](cben-getdispinfo.md) | Demande des informations sur les attributs d’un élément.                                                                           |
| [CBEN \_ INSERTITEM](cben-insertitem.md)   | Signale qu’un élément a été inséré dans le contrôle.                                                                          |



 

## <a name="comboboxex-control-message-forwarding"></a>ComboBoxEx le transfert des messages de contrôle

Voici les messages de zone de liste déroulante standard qu’un contrôle ComboBoxEx transmet à sa zone de liste déroulante enfant. Certains de ces messages peuvent être traités par le contrôle ComboBoxEx avant ou après le transfert du message.

-   [**\_DELETESTRING CB**](cb-deletestring.md)
-   [**\_FINDEXACTSTRING CB**](cb-findstringexact.md)
-   [**CB \_ GETCOUNT**](cb-getcount.md)
-   [**\_GETCURSEL CB**](cb-getcursel.md)
-   [**\_GETDROPPEDCONTROLRECT CB**](cb-getdroppedcontrolrect.md)
-   [**\_GETDROPPEDSTATE CB**](cb-getdroppedstate.md)
-   [**\_GETITEMDATA CB**](cb-getitemdata.md)
-   [**\_GETITEMHEIGHT CB**](cb-getitemheight.md)
-   [**\_GETLBTEXT CB**](cb-getlbtext.md)
-   [**\_GETLBTEXTLEN CB**](cb-getlbtextlen.md)
-   [**\_GETEXTENDEDUI CB**](cb-getextendedui.md)
-   [**\_LIMITTEXT CB**](cb-limittext.md)
-   [**\_RESETCONTENT CB**](cb-resetcontent.md)
-   [**\_SETCURSEL CB**](cb-setcursel.md)
-   [**\_SETDROPPEDWIDTH CB**](cb-setdroppedwidth.md)
-   [**\_SETEXTENDEDUI CB**](cb-setextendedui.md)
-   [**\_SETITEMDATA CB**](cb-setitemdata.md)
-   [**\_SETITEMHEIGHT CB**](cb-setitemheight.md)
-   [**\_SHOWDROPDOWN CB**](cb-showdropdown.md)

Voici les messages Windows qu’un contrôle ComboBoxEx transmet à sa fenêtre parente :

-   [**WM \_ COMMANDE**](/windows/desktop/menurc/wm-command) (y compris toutes les \_ notifications CBN.)
-   [**\_notification WM**](wm-notify.md)

 

 