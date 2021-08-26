---
title: Messages de contrôle
description: cette section contient des informations sur la façon dont les messages de Windows sont utilisés pour communiquer avec les contrôles.
ms.assetid: 94d34132-25c2-4a1a-bd0e-35e5a666bbfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed60ebb66341332b6248b8427045abc5b62a2311427d56e46b25fe93b3d899ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921099"
---
# <a name="control-messages"></a>Messages de contrôle

cette section contient des informations sur la façon dont les messages de Windows sont utilisés pour communiquer avec les contrôles.

Les rubriques suivantes sont présentées.

-   [Messages aux contrôles communs](#messages-to-common-controls)
-   [Notifications à partir de contrôles](#notifications-from-controls)
-   [Rubriques connexes](#related-topics)

## <a name="messages-to-common-controls"></a>Messages aux contrôles communs

Étant donné que les contrôles communs sont des fenêtres, une application peut communiquer avec elles à l’aide de messages Microsoft Win32 communs tels que [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont) ou [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext). En outre, la classe de fenêtre de chaque contrôle commun prend en charge un ensemble de messages spécifiques au contrôle. En règle générale, une application utilise [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) ou [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) pour transmettre des messages au contrôle (souvent en recevant des informations dans la valeur de retour).

Certains contrôles courants disposent également d’un ensemble de macros qu’une application peut utiliser au lieu de [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage). Les macros sont généralement plus faciles à utiliser que les fonctions. L’exemple de code suivant récupère le texte de l’élément d’arborescence sélectionné, en utilisant d’abord les messages bruts, et en utilisant les macros équivalentes. Supposons que *HWND* est le handle de la fenêtre de contrôle.


```
BOOL fSuccess;
WCHAR itemText[99];
TVITEM tvItem = { 0 };
tvItem.mask = TVIF_TEXT;
tvItem.cchTextMax = ARRAYSIZE(itemText);
tvItem.pszText = itemText;

// This...
tvItem.hItem = (HTREEITEM)SendMessage(hwnd, TVM_GETNEXTITEM, TVGN_CARET, NULL);
fSuccess = SendMessage(hwnd, TVM_GETITEM, 0, (LPARAM)&tvItem);

// ... is equivalent to this.
tvItem.hItem = TreeView_GetSelection(hwnd);
fSuccess = TreeView_GetItem(hwnd, &tvItem);
```



quand une modification est apportée aux paramètres de couleur système, Windows envoie un message [**WM \_ SYSCOLORCHANGE**](/windows/desktop/gdi/wm-syscolorchange) à toutes les fenêtres de niveau supérieur. Votre fenêtre de niveau supérieur doit transférer le message **WM \_ SYSCOLORCHANGE** à ses contrôles communs ; dans le cas contraire, les contrôles ne seront pas notifiés de la modification de la couleur. Le transfert du message permet de s’assurer que les couleurs utilisées par vos contrôles communs sont cohérentes avec celles utilisées par d’autres objets de l’interface utilisateur. Par exemple, un contrôle ToolBar utilise la couleur « objets 3D » pour dessiner ses boutons. Si l’utilisateur modifie la couleur de l’objet 3D, mais que le message **WM \_ SYSCOLORCHANGE** n’est pas transféré à la barre d’outils, les boutons de la barre d’outils restent dans leur couleur d’origine (ou même sont modifiés en une combinaison de couleurs anciennes et nouvelles), tandis que la couleur des autres boutons du système change.

## <a name="notifications-from-controls"></a>Notifications à partir de contrôles

Les contrôles sont des fenêtres enfants qui envoient des messages de notification à la fenêtre parente lorsque des événements, généralement déclenchés par une entrée de l’utilisateur, se produisent dans le contrôle. L’application s’appuie sur ces messages de notification pour déterminer l’action que l’utilisateur souhaite effectuer. À l’exception de trackbars, qui utilisent les messages [**WM \_ HSCROLL**](wm-hscroll.md) et [**WM \_ VSCROLL**](wm-vscroll.md) pour notifier leur parent de modifications, les contrôles communs envoient des notifications en tant que [**\_ commandes WM**](/windows/desktop/menurc/wm-command) ou messages de [**\_ notification WM**](wm-notify.md) , comme indiqué dans la rubrique de référence pour la notification. En général, les notifications plus anciennes (celles qui se trouvent dans l’API pendant une longue période) utilisent la **\_ commande WM**.

Le paramètre *lParam* de [**WM \_ Notify**](wm-notify.md) est l’adresse d’une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) ou l’adresse d’une structure plus grande qui comprend **NMHDR** comme premier membre. La structure contient le code de notification et identifie le contrôle commun qui a envoyé le message de notification. La signification des autres membres de la structure, le cas échéant, varie selon le code de notification.

Chaque type de contrôle commun possède un ensemble de codes de notification correspondant. La bibliothèque de contrôles communs fournit également des codes de notification qui peuvent être envoyés par plus d’un type de contrôle commun. Consultez la documentation sur le contrôle qui vous intéresse pour déterminer les codes de notification qu’il enverra et le format qu’ils prennent.

Pour obtenir un exemple de code illustrant la gestion des messages de [**\_ notification WM**](wm-notify.md) , consultez la rubrique de référence pour ce message.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de contrôle générale](common-control-reference.md)
</dt> </dl>

 

 
