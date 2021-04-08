---
title: Messages de contrôle
description: Cette section contient des informations sur l’utilisation des messages Windows pour communiquer avec les contrôles.
ms.assetid: 94d34132-25c2-4a1a-bd0e-35e5a666bbfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923a1b47d625a2797a900a6c582d00c5169097f3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103842945"
---
# <a name="control-messages"></a><span data-ttu-id="ffe35-103">Messages de contrôle</span><span class="sxs-lookup"><span data-stu-id="ffe35-103">Control Messages</span></span>

<span data-ttu-id="ffe35-104">Cette section contient des informations sur l’utilisation des messages Windows pour communiquer avec les contrôles.</span><span class="sxs-lookup"><span data-stu-id="ffe35-104">This section contains information about how Windows messages are used to communicate with controls.</span></span>

<span data-ttu-id="ffe35-105">Les rubriques suivantes sont présentées.</span><span class="sxs-lookup"><span data-stu-id="ffe35-105">The following topics are discussed.</span></span>

-   [<span data-ttu-id="ffe35-106">Messages aux contrôles communs</span><span class="sxs-lookup"><span data-stu-id="ffe35-106">Messages to Common Controls</span></span>](#messages-to-common-controls)
-   [<span data-ttu-id="ffe35-107">Notifications à partir de contrôles</span><span class="sxs-lookup"><span data-stu-id="ffe35-107">Notifications from Controls</span></span>](#notifications-from-controls)
-   [<span data-ttu-id="ffe35-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ffe35-108">Related topics</span></span>](#related-topics)

## <a name="messages-to-common-controls"></a><span data-ttu-id="ffe35-109">Messages aux contrôles communs</span><span class="sxs-lookup"><span data-stu-id="ffe35-109">Messages to Common Controls</span></span>

<span data-ttu-id="ffe35-110">Étant donné que les contrôles communs sont des fenêtres, une application peut communiquer avec elles à l’aide de messages Microsoft Win32 communs tels que [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont) ou [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext).</span><span class="sxs-lookup"><span data-stu-id="ffe35-110">Because common controls are windows, an application can communicate with them by using common Microsoft Win32 messages such as [**WM\_GETFONT**](/windows/desktop/winmsg/wm-getfont) or [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext).</span></span> <span data-ttu-id="ffe35-111">En outre, la classe de fenêtre de chaque contrôle commun prend en charge un ensemble de messages spécifiques au contrôle.</span><span class="sxs-lookup"><span data-stu-id="ffe35-111">In addition, the window class of each common control supports a set of control-specific messages.</span></span> <span data-ttu-id="ffe35-112">En règle générale, une application utilise [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) ou [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) pour transmettre des messages au contrôle (souvent en recevant des informations dans la valeur de retour).</span><span class="sxs-lookup"><span data-stu-id="ffe35-112">Typically, an application uses [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) or [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) to pass messages to the control (often receiving information in the return value).</span></span>

<span data-ttu-id="ffe35-113">Certains contrôles courants disposent également d’un ensemble de macros qu’une application peut utiliser au lieu de [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="ffe35-113">Some common controls also have a set of macros that an application can use instead of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span></span> <span data-ttu-id="ffe35-114">Les macros sont généralement plus faciles à utiliser que les fonctions.</span><span class="sxs-lookup"><span data-stu-id="ffe35-114">The macros are typically easier to use than the functions.</span></span> <span data-ttu-id="ffe35-115">L’exemple de code suivant récupère le texte de l’élément d’arborescence sélectionné, en utilisant d’abord les messages bruts, et en utilisant les macros équivalentes.</span><span class="sxs-lookup"><span data-stu-id="ffe35-115">The following example code retrieves the text of the selected tree-view item, first by using the raw messages, and second by using the equivalent macros.</span></span> <span data-ttu-id="ffe35-116">Supposons que *HWND* est le handle de la fenêtre de contrôle.</span><span class="sxs-lookup"><span data-stu-id="ffe35-116">Assume that *hwnd* is the handle of the control window.</span></span>


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



<span data-ttu-id="ffe35-117">Quand une modification est apportée aux paramètres de couleur système, Windows envoie un message [**WM \_ SYSCOLORCHANGE**](/windows/desktop/gdi/wm-syscolorchange) à toutes les fenêtres de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="ffe35-117">When a change is made to the system color settings, Windows sends a [**WM\_SYSCOLORCHANGE**](/windows/desktop/gdi/wm-syscolorchange) message to all top-level windows.</span></span> <span data-ttu-id="ffe35-118">Votre fenêtre de niveau supérieur doit transférer le message **WM \_ SYSCOLORCHANGE** à ses contrôles communs ; dans le cas contraire, les contrôles ne seront pas notifiés de la modification de la couleur.</span><span class="sxs-lookup"><span data-stu-id="ffe35-118">Your top-level window must forward the **WM\_SYSCOLORCHANGE** message to its common controls; otherwise, the controls will not be notified of the color change.</span></span> <span data-ttu-id="ffe35-119">Le transfert du message permet de s’assurer que les couleurs utilisées par vos contrôles communs sont cohérentes avec celles utilisées par d’autres objets de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ffe35-119">Forwarding the message ensures that the colors used by your common controls are consistent with those used by other user interface objects.</span></span> <span data-ttu-id="ffe35-120">Par exemple, un contrôle ToolBar utilise la couleur « objets 3D » pour dessiner ses boutons.</span><span class="sxs-lookup"><span data-stu-id="ffe35-120">For example, a toolbar control uses the "3-D Objects" color to draw its buttons.</span></span> <span data-ttu-id="ffe35-121">Si l’utilisateur modifie la couleur de l’objet 3D, mais que le message **WM \_ SYSCOLORCHANGE** n’est pas transféré à la barre d’outils, les boutons de la barre d’outils restent dans leur couleur d’origine (ou même sont modifiés en une combinaison de couleurs anciennes et nouvelles), tandis que la couleur des autres boutons du système change.</span><span class="sxs-lookup"><span data-stu-id="ffe35-121">If the user changes the 3-D Object's color but the **WM\_SYSCOLORCHANGE** message is not forwarded to the toolbar, the toolbar buttons will remain in their original color (or even change to a combination of old and new colors) while the color of other buttons in the system changes.</span></span>

## <a name="notifications-from-controls"></a><span data-ttu-id="ffe35-122">Notifications à partir de contrôles</span><span class="sxs-lookup"><span data-stu-id="ffe35-122">Notifications from Controls</span></span>

<span data-ttu-id="ffe35-123">Les contrôles sont des fenêtres enfants qui envoient des messages de notification à la fenêtre parente lorsque des événements, généralement déclenchés par une entrée de l’utilisateur, se produisent dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="ffe35-123">Controls are child windows that send notification messages to the parent window when events, usually triggered by input from the user, occur in the control.</span></span> <span data-ttu-id="ffe35-124">L’application s’appuie sur ces messages de notification pour déterminer l’action que l’utilisateur souhaite effectuer.</span><span class="sxs-lookup"><span data-stu-id="ffe35-124">The application relies on these notification messages to determine what action the user wants it to take.</span></span> <span data-ttu-id="ffe35-125">À l’exception de trackbars, qui utilisent les messages [**WM \_ HSCROLL**](wm-hscroll.md) et [**WM \_ VSCROLL**](wm-vscroll.md) pour notifier leur parent de modifications, les contrôles communs envoient des notifications en tant que [**\_ commandes WM**](/windows/desktop/menurc/wm-command) ou messages de [**\_ notification WM**](wm-notify.md) , comme indiqué dans la rubrique de référence pour la notification.</span><span class="sxs-lookup"><span data-stu-id="ffe35-125">Except for trackbars, which use the [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md) messages to notify their parent of changes, common controls send notifications as either [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) or [**WM\_NOTIFY**](wm-notify.md) messages, as specified in the reference topic for the notification.</span></span> <span data-ttu-id="ffe35-126">En général, les notifications plus anciennes (celles qui se trouvent dans l’API pendant une longue période) utilisent la **\_ commande WM**.</span><span class="sxs-lookup"><span data-stu-id="ffe35-126">Typically, older notifications (those that have been in the API for a long time) use **WM\_COMMAND**.</span></span>

<span data-ttu-id="ffe35-127">Le paramètre *lParam* de [**WM \_ Notify**](wm-notify.md) est l’adresse d’une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) ou l’adresse d’une structure plus grande qui comprend **NMHDR** comme premier membre.</span><span class="sxs-lookup"><span data-stu-id="ffe35-127">The *lParam* parameter of [**WM\_NOTIFY**](wm-notify.md) is either the address of an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure or the address of a larger structure that includes **NMHDR** as its first member.</span></span> <span data-ttu-id="ffe35-128">La structure contient le code de notification et identifie le contrôle commun qui a envoyé le message de notification.</span><span class="sxs-lookup"><span data-stu-id="ffe35-128">The structure contains the notification code and identifies the common control that sent the notification message.</span></span> <span data-ttu-id="ffe35-129">La signification des autres membres de la structure, le cas échéant, varie selon le code de notification.</span><span class="sxs-lookup"><span data-stu-id="ffe35-129">The meaning of the remaining structure members, if any, varies depending on the notification code.</span></span>

<span data-ttu-id="ffe35-130">Chaque type de contrôle commun possède un ensemble de codes de notification correspondant.</span><span class="sxs-lookup"><span data-stu-id="ffe35-130">Each type of common control has a corresponding set of notification codes.</span></span> <span data-ttu-id="ffe35-131">La bibliothèque de contrôles communs fournit également des codes de notification qui peuvent être envoyés par plus d’un type de contrôle commun.</span><span class="sxs-lookup"><span data-stu-id="ffe35-131">The common control library also provides notification codes that can be sent by more than one type of common control.</span></span> <span data-ttu-id="ffe35-132">Consultez la documentation sur le contrôle qui vous intéresse pour déterminer les codes de notification qu’il enverra et le format qu’ils prennent.</span><span class="sxs-lookup"><span data-stu-id="ffe35-132">See the documentation for the control of interest to determine which notification codes it will send and what format they take.</span></span>

<span data-ttu-id="ffe35-133">Pour obtenir un exemple de code illustrant la gestion des messages de [**\_ notification WM**](wm-notify.md) , consultez la rubrique de référence pour ce message.</span><span class="sxs-lookup"><span data-stu-id="ffe35-133">For example code showing how to handle [**WM\_NOTIFY**](wm-notify.md) messages, see the reference topic for that message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ffe35-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ffe35-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffe35-135">Référence de contrôle générale</span><span class="sxs-lookup"><span data-stu-id="ffe35-135">General Control Reference</span></span>](common-control-reference.md)
</dt> </dl>

 

 
