---
title: Contrôles personnalisés
description: Cette section contient des informations sur les contrôles personnalisés ou définis par l’application.
ms.assetid: 220f7058-db04-46d0-acee-ed5e676790b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d1a31a44f1f71d99088f7729c2de6d5fdb597e14507f5f994dfaca1b96613d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059709"
---
# <a name="custom-controls"></a>Contrôles personnalisés

Cette section contient des informations sur les contrôles personnalisés ou définis par l’application.

Les rubriques suivantes sont présentées.

-   [Création de contrôles Owner-Drawn](#creating-owner-drawn-controls)
-   [Sous-classement de la classe de fenêtre d’un contrôle existant](#subclassing-the-window-class-of-an-existing-control)
-   [Implémentation d’une classe de fenêtre Application-Defined](#implementing-an-application-defined-window-class)
-   [Envoi de notifications à partir d’un contrôle](#sending-notifications-from-a-control)
-   [Accessibilité](#accessibility)
-   [Rubriques connexes](#related-topics)

## <a name="creating-owner-drawn-controls"></a>Création de contrôles Owner-Drawn

Les boutons, les menus, les contrôles de texte statiques, les zones de liste et les zones de liste modifiable peuvent être créés avec un indicateur de style owner-drawn. Lorsqu’un contrôle a le style owner-drawn, le système gère l’interaction de l’utilisateur avec le contrôle comme d’habitude, en effectuant des tâches telles que la détection lorsqu’un utilisateur a choisi un bouton et avertit le propriétaire de l’événement du bouton. Toutefois, étant donné que le contrôle est owner-drawn, la fenêtre parente du contrôle est responsable de l’apparence visuelle du contrôle. La fenêtre parente reçoit un message chaque fois que le contrôle doit être dessiné.

Pour les boutons et les contrôles de texte statique, le style owner-drawn affecte la façon dont le système dessine l’ensemble du contrôle. Pour les zones de liste et les zones de liste modifiable, la fenêtre parente dessine les éléments dans le contrôle et le contrôle dessine son propre plan. Par exemple, une application peut personnaliser une zone de liste pour qu’elle affiche une petite bitmap en regard de chaque élément de la liste.

L’exemple de code suivant montre comment créer un contrôle de texte statique owner-drawn. Supposons que Unicode est défini.


```
// g_myStatic is a global HWND variable.
g_myStatic = CreateWindowEx(0, L"STATIC", L"Some static text", 
            WS_CHILD | WS_VISIBLE | SS_OWNERDRAW, 
            25, 125, 150, 20, hDlg, 0, 0, 0);
```



Dans l’exemple suivant, dans la procédure de fenêtre pour la boîte de dialogue qui contient le contrôle créé dans l’exemple précédent, le message [**WM \_ DRAWITEM**](wm-drawitem.md) est géré en affichant le texte dans une couleur personnalisée, à l’aide de la police par défaut. Notez que vous n’avez pas besoin d’appeler [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) et [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) lors du traitement de **WM \_ DRAWITEM**.


```
case WM_DRAWITEM:
{
    LPDRAWITEMSTRUCT pDIS = (LPDRAWITEMSTRUCT)lParam;
    if (pDIS->hwndItem == g_myStatic)
    {
        SetTextColor(pDIS->hDC, RGB(100, 0, 100));
        WCHAR staticText[99];
        int len = SendMessage(myStatic, WM_GETTEXT, 
            ARRAYSIZE(staticText), (LPARAM)staticText);
        TextOut(pDIS->hDC, pDIS->rcItem.left, pDIS->rcItem.top, staticText, len);
    }
    return TRUE;
}
```



Pour plus d’informations sur les contrôles owner-drawn, consultez [création d’une zone de liste owner-drawn](using-list-boxes.md) et de zones de liste [déroulante owner drawn](about-combo-boxes.md).

## <a name="subclassing-the-window-class-of-an-existing-control"></a>Sous-classement de la classe de fenêtre d’un contrôle existant

Le sous-classement d’un contrôle existant est une autre façon de créer un contrôle personnalisé. La procédure de sous-classe peut modifier les comportements sélectionnés du contrôle en traitant les messages qui affectent les comportements sélectionnés. Tous les autres messages passent à la procédure de fenêtre d’origine pour le contrôle. Par exemple, une application peut afficher une petite bitmap en regard du texte d’un contrôle d’édition en lecture seule sur une seule ligne en sous-classant le contrôle et en traitant le message de [**\_ peinture WM**](/windows/desktop/gdi/wm-paint) . Pour plus d’informations, consultez [à propos des procédures de fenêtre](/windows/desktop/winmsg/about-window-procedures) et des contrôles de sous- [classe](subclassing-overview.md).

## <a name="implementing-an-application-defined-window-class"></a>Implémentation d’une classe de fenêtre Application-Defined

Pour créer un contrôle qui n’est pas explicitement basé sur un contrôle existant, l’application doit créer et inscrire une classe de fenêtre. Le processus d’inscription d’une classe de fenêtre définie par l’application pour un contrôle personnalisé est identique à l’inscription d’une classe pour une fenêtre ordinaire. Pour créer un contrôle personnalisé, spécifiez le nom de la classe de fenêtre dans la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou dans un modèle de boîte de dialogue. Chaque classe doit avoir un nom unique, une procédure de fenêtre correspondante et d’autres informations.

Au minimum, la procédure de fenêtre dessine le contrôle. Si une application utilise le contrôle pour permettre à l’utilisateur de taper des informations, la procédure de fenêtre traite également les messages d’entrée à partir du clavier et de la souris et envoie des messages de notification à la fenêtre parente. En outre, si le contrôle prend en charge les messages de contrôle, la procédure de fenêtre traite les messages qui lui sont envoyés par la fenêtre parente ou d’autres fenêtres. Par exemple, les contrôles traitent souvent le message [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode) envoyé par les boîtes de dialogue pour indiquer à une boîte de dialogue de traiter l’entrée au clavier d’une manière donnée.

La procédure de fenêtre pour un contrôle défini par l’application doit traiter n’importe quel message de contrôle prédéfini dans le tableau suivant si le message affecte le fonctionnement du contrôle.



| Message                                          | Recommandation                                                                                                                                                                                                                                  |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_GETDLGCODE WM**](/windows/desktop/dlgbox/wm-getdlgcode)       | Processus si le contrôle utilise les touches entrée, ÉCHAP, TAB ou flèche. La fonction [**IsDialogMessage**](/windows/desktop/api/winuser/nf-winuser-isdialogmessagea) envoie ce message aux contrôles dans une boîte de dialogue pour déterminer s’il faut traiter les clés ou les passer au contrôle. |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)             | Processus si le message [**WM \_ SetFont**](/windows/desktop/winmsg/wm-setfont) est également traité.                                                                                                                                                                  |
| [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)             | Processus si le texte du contrôle n’est pas le même que le titre spécifié par la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .                                                                                                                 |
| [**\_GETTEXTLENGTH WM**](/windows/desktop/winmsg/wm-gettextlength) | Processus si le texte du contrôle n’est pas le même que le titre spécifié par la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .                                                                                                                 |
| [**\_KILLFOCUS WM**](/windows/desktop/inputdev/wm-killfocus)       | Processus si le contrôle affiche un signe insertion, un rectangle de focus ou un autre élément pour indiquer qu’il a le focus d’entrée.                                                                                                                            |
| [**WM \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus)         | Processus si le contrôle affiche un signe insertion, un rectangle de focus ou un autre élément pour indiquer qu’il a le focus d’entrée.                                                                                                                            |
| [**WM, \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)             | Processus si le texte du contrôle n’est pas le même que le titre spécifié par la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .                                                                                                                 |
| [**\_SetFont WM**](/windows/desktop/winmsg/wm-setfont)             | Processus si le contrôle affiche du texte. Le système envoie ce message lors de la création d’une boîte de dialogue avec le \_ style DS setfont.                                                                                                                  |



 

Les messages de contrôle définis par l’application sont spécifiques au contrôle donné et doivent être envoyés explicitement au contrôle à l’aide d’une fonction [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) ou [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) . La valeur numérique de chaque message doit être unique et ne doit pas être en conflit avec les valeurs d’autres messages de fenêtre. Pour s’assurer que les valeurs des messages définis par l’application ne sont pas en conflit, une application doit créer chaque valeur en ajoutant un numéro unique à la valeur de l' [**\_ utilisateur WM**](/windows/desktop/winmsg/wm-user) .

## <a name="sending-notifications-from-a-control"></a>Envoi de notifications à partir d’un contrôle

Des contrôles personnalisés peuvent être nécessaires pour envoyer des notifications d’événements à la fenêtre parente afin que l’application hôte puisse répondre à ces événements. Par exemple, un affichage de liste personnalisé peut envoyer une notification lorsque l’utilisateur sélectionne un élément et une autre notification lors d’un double-clic sur un élément.

Les notifications sont envoyées en tant que [**\_ commandes WM**](/windows/desktop/menurc/wm-command) ou messages de [**\_ notification WM**](wm-notify.md) . **WM \_** Les messages de notification contiennent plus d’informations que les messages de **\_ commande WM** .

L’identificateur de contrôle est un nombre unique que l’application utilise pour identifier le contrôle qui envoie le message. L’application définit l’identificateur d’un contrôle lorsqu’il crée le contrôle. L’application spécifie l’identificateur dans le paramètre *HMENU* de la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou dans le membre **ID** de la structure [**DLGITEMTEMPLATEEX**](/windows/desktop/dlgbox/dlgitemtemplateex) .

Étant donné que le contrôle lui-même ne définit pas l’identificateur de contrôle, le contrôle doit récupérer l’identificateur avant de pouvoir envoyer des messages de notification. Un contrôle doit utiliser la fonction [**GetDlgCtrlID**](/windows/desktop/api/winuser/nf-winuser-getdlgctrlid) pour récupérer son propre identificateur de contrôle. Bien que l’identificateur de contrôle soit spécifié comme handle de menu lorsque le contrôle est créé, la fonction [**GetMenu**](/windows/desktop/api/winuser/nf-winuser-getmenu) ne peut pas être utilisée pour récupérer l’identificateur. Un contrôle peut également récupérer l’identificateur du membre **HMENU** dans la structure [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) lors du traitement du message [**WM \_ Create**](/windows/desktop/winmsg/wm-create) .

Les exemples suivants, où *hwndControl* est le descripteur de la fenêtre de contrôle et que la définition de la \_ notification CN est une définition de notification personnalisée, illustrent les deux façons d’envoyer une notification spécifique au contrôle.


```
 // Send as WM_COMMAND.
SendMessage(GetParent(hwndControl), 
    WM_COMMAND,
    MAKEWPARAM(GetDlgCtrlID(hwndControl), CN_VALUECHANGED),
    (LPARAM)hwndControl);

// Send as WM_NOTIFY.           
NMHDR nmh;
nmh.code = CN_VALUECHANGED;
nmh.idFrom = GetDlgCtrlID(hwndControl);
nmh.hwndFrom = hwndControl;
SendMessage(GetParent(hwndControl), 
    WM_NOTIFY, 
    (WPARAM)hwndControl, 
    (LPARAM)&nmh);
```



Notez que la structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) peut faire partie d’une plus grande structure définie par le contrôle qui contient des informations supplémentaires. Dans l’exemple, les valeurs anciennes et nouvelles du contrôle peuvent être contenues dans cette structure. (Ces structures étendues sont utilisées avec de nombreuses notifications standard ; par exemple, consultez [LVN \_ INSERTITEM](lvn-insertitem.md), qui utilise la structure [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .)

## <a name="accessibility"></a>Accessibilité

Tous les contrôles communs prennent en charge Microsoft Active Accessibility (MSAA), qui permet l’accès par programme aux applications de technologie accessibles telles que les lecteurs d’écran. MSAA permet également l’automatisation d’interface utilisateur, une technologie plus récente, pour interagir avec les contrôles.

Les contrôles personnalisés doivent implémenter l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (pour prendre en charge MSAA) ou les interfaces UI Automation, ou les deux. Dans le cas contraire, les produits de technologie accessible ne pourront obtenir que des informations très limitées sur la fenêtre de contrôle, n’auront pas accès aux propriétés du contrôle et ne pourront pas déclencher d’événements dans le contrôle.

pour plus d’informations sur la mise à disposition de votre contrôle, consultez [Windows API Automation](/windows/desktop/WinAuto/windows-automation-api-portal).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Référence de contrôle générale](common-control-reference.md)
</dt> <dt>

[Personnalisation de l’apparence d’un contrôle à l’aide d’un dessin personnalisé](custom-draw.md)
</dt> <dt>

[Messages de contrôle](control-messages.md)
</dt> <dt>

[Utilisation de styles visuels avec des contrôles Owner-Drawn](using-visual-styles.md)
</dt> </dl>

 

 