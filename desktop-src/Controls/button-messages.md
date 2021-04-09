---
title: Messages de bouton
description: Un bouton peut envoyer des messages à sa fenêtre parente et une fenêtre parente peut envoyer des messages à un bouton.
ms.assetid: 2d2358fb-b17d-48a9-8def-15ae8bad9162
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1601f269ec1242a10579d2ace812723d3ead7f84
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103734044"
---
# <a name="button-messages"></a><span data-ttu-id="739ac-103">Messages de bouton</span><span class="sxs-lookup"><span data-stu-id="739ac-103">Button Messages</span></span>

<span data-ttu-id="739ac-104">Un bouton peut envoyer des messages à sa fenêtre parente et une fenêtre parente peut envoyer des messages à un bouton.</span><span class="sxs-lookup"><span data-stu-id="739ac-104">A button can send messages to its parent window, and a parent window can send messages to a button.</span></span>

<span data-ttu-id="739ac-105">Les rubriques suivantes sont présentées dans cette section.</span><span class="sxs-lookup"><span data-stu-id="739ac-105">The following topics are discussed in this section.</span></span>

-   [<span data-ttu-id="739ac-106">Envoi de messages à des boutons</span><span class="sxs-lookup"><span data-stu-id="739ac-106">Sending Messages to Buttons</span></span>](#sending-messages-to-buttons)
-   [<span data-ttu-id="739ac-107">Gestion des messages à partir d’un bouton</span><span class="sxs-lookup"><span data-stu-id="739ac-107">Handling Messages from a Button</span></span>](#handling-messages-from-a-button)
-   [<span data-ttu-id="739ac-108">Messages de notification à partir de boutons</span><span class="sxs-lookup"><span data-stu-id="739ac-108">Notification Messages from Buttons</span></span>](#notification-messages-from-buttons)
-   [<span data-ttu-id="739ac-109">Messages de couleur de bouton</span><span class="sxs-lookup"><span data-stu-id="739ac-109">Button Color Messages</span></span>](#button-color-messages)
-   [<span data-ttu-id="739ac-110">Traitement du message par défaut du bouton</span><span class="sxs-lookup"><span data-stu-id="739ac-110">Button Default Message Processing</span></span>](#button-default-message-processing)
-   [<span data-ttu-id="739ac-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="739ac-111">Related topics</span></span>](#related-topics)

## <a name="sending-messages-to-buttons"></a><span data-ttu-id="739ac-112">Envoi de messages à des boutons</span><span class="sxs-lookup"><span data-stu-id="739ac-112">Sending Messages to Buttons</span></span>

<span data-ttu-id="739ac-113">Une fenêtre parente peut envoyer des messages à un bouton dans une fenêtre superposée ou enfant à l’aide de la fonction [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , ou elle peut envoyer des messages à un bouton dans une boîte de dialogue à l’aide des fonctions [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea), [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton), [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton)et [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) .</span><span class="sxs-lookup"><span data-stu-id="739ac-113">A parent window can send messages to a button in an overlapped or child window by using the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function, or it can send messages to a button in a dialog box by using the [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea), [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton), [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton), and [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) functions.</span></span>

<span data-ttu-id="739ac-114">Une application peut utiliser le [**message \_ GETCHECK BM**](bm-getcheck.md) pour récupérer l’état d’activation d’une case à cocher ou d’une case d’option.</span><span class="sxs-lookup"><span data-stu-id="739ac-114">An application can use the [**BM\_GETCHECK**](bm-getcheck.md) message to retrieve the check state of a check box or radio button.</span></span> <span data-ttu-id="739ac-115">Une application peut également utiliser le [**message \_ GETSTATE BM**](bm-getstate.md) pour récupérer les États actuels du bouton (l’état d’activation, de transmission et de focus).</span><span class="sxs-lookup"><span data-stu-id="739ac-115">An application can also use the [**BM\_GETSTATE**](bm-getstate.md) message to retrieve the button's current states (the check state, push state, and focus state).</span></span> <span data-ttu-id="739ac-116">Pour obtenir des informations sur un état spécifique, utilisez un masque de données sur la valeur d’État retournée.</span><span class="sxs-lookup"><span data-stu-id="739ac-116">To get information about a specific state, use a bitmask on the returned state value.</span></span>

<span data-ttu-id="739ac-117">Le message [**BM \_ SETCHECK**](bm-setcheck.md) définit l’état d’activation d’une case à cocher ou d’une case d’option ; le message retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="739ac-117">The [**BM\_SETCHECK**](bm-setcheck.md) message sets the check state of a check box or radio button; the message returns zero.</span></span> <span data-ttu-id="739ac-118">Le message de [**BM \_ SETSTATE**](bm-setstate.md) définit l’état de transmission d’un bouton ; ce message retourne également zéro.</span><span class="sxs-lookup"><span data-stu-id="739ac-118">The [**BM\_SETSTATE**](bm-setstate.md) message sets the push state of a button; this message also returns zero.</span></span> <span data-ttu-id="739ac-119">Le message [**BM \_ SETSTYLE**](bm-setstyle.md) change le style d’un bouton.</span><span class="sxs-lookup"><span data-stu-id="739ac-119">The [**BM\_SETSTYLE**](bm-setstyle.md) message changes the style of a button.</span></span> <span data-ttu-id="739ac-120">Il est conçu pour modifier les styles de bouton dans un type (par exemple, en remplaçant une case à cocher par une case à cocher automatique).</span><span class="sxs-lookup"><span data-stu-id="739ac-120">It is designed for changing button styles within a type (for example, changing a check box to an automatic check box).</span></span> <span data-ttu-id="739ac-121">Elle n’est pas conçue pour changer entre les types (par exemple, en remplaçant une case à cocher par une case d’option).</span><span class="sxs-lookup"><span data-stu-id="739ac-121">It is not designed for changing between types (for example, changing a check box to a radio button).</span></span> <span data-ttu-id="739ac-122">Une application ne doit pas modifier un bouton d’un type à un autre.</span><span class="sxs-lookup"><span data-stu-id="739ac-122">An application should not change a button from one type to another.</span></span>

<span data-ttu-id="739ac-123">Un bouton du style de la [**\_ bitmap BS**](button-styles.md) ou de l' [**\_ icône BS**](button-styles.md) affiche une bitmap ou une icône au lieu de texte.</span><span class="sxs-lookup"><span data-stu-id="739ac-123">A button of the [**BS\_BITMAP**](button-styles.md) or [**BS\_ICON**](button-styles.md) style displays a bitmap or icon instead of text.</span></span> <span data-ttu-id="739ac-124">Le [**message \_ SETIMAGE BM**](bm-setimage.md) associe un handle à une image bitmap ou à une icône avec un bouton.</span><span class="sxs-lookup"><span data-stu-id="739ac-124">The [**BM\_SETIMAGE**](bm-setimage.md) message associates a handle to a bitmap or icon with a button.</span></span> <span data-ttu-id="739ac-125">Le [**message \_ GETIMAGE de BM**](bm-getimage.md) récupère un handle vers l’image bitmap ou l’icône associée à un bouton.</span><span class="sxs-lookup"><span data-stu-id="739ac-125">The [**BM\_GETIMAGE**](bm-getimage.md) message retrieves a handle to the bitmap or icon associated with a button.</span></span>

<span data-ttu-id="739ac-126">Une application peut également utiliser le message [**DM \_ GETDEFID**](/windows/desktop/dlgbox/dm-getdefid) pour récupérer l’identificateur du contrôle bouton de commande par défaut dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="739ac-126">An application can also use the [**DM\_GETDEFID**](/windows/desktop/dlgbox/dm-getdefid) message to retrieve the identifier of the default push button control in a dialog box.</span></span> <span data-ttu-id="739ac-127">Une application peut utiliser le message [**DM \_ SETDEFID**](/windows/desktop/dlgbox/dm-setdefid) pour définir le bouton de commande par défaut d’une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="739ac-127">An application can use the [**DM\_SETDEFID**](/windows/desktop/dlgbox/dm-setdefid) message to set the default push button for a dialog box.</span></span>

<span data-ttu-id="739ac-128">L’appel de la fonction [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton) ou [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton) équivaut à l’envoi d’un message [**\_ SETCHECK BM**](bm-setcheck.md) .</span><span class="sxs-lookup"><span data-stu-id="739ac-128">Calling the [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton) or [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton) function is equivalent to sending a [**BM\_SETCHECK**](bm-setcheck.md) message.</span></span> <span data-ttu-id="739ac-129">L’appel de la fonction [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) revient à envoyer un message [**\_ GETCHECK BM**](bm-getcheck.md) .</span><span class="sxs-lookup"><span data-stu-id="739ac-129">Calling the [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) function is equivalent to sending a [**BM\_GETCHECK**](bm-getcheck.md) message.</span></span>

## <a name="handling-messages-from-a-button"></a><span data-ttu-id="739ac-130">Gestion des messages à partir d’un bouton</span><span class="sxs-lookup"><span data-stu-id="739ac-130">Handling Messages from a Button</span></span>

<span data-ttu-id="739ac-131">Les notifications d’un bouton sont envoyées en tant que [**\_ commandes WM**](/windows/desktop/menurc/wm-command) ou messages de [**\_ notification WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="739ac-131">Notifications from a button are sent as either [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) or [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="739ac-132">Vous trouverez des informations sur le message qui est utilisé dans la page de référence de chaque notification.</span><span class="sxs-lookup"><span data-stu-id="739ac-132">Information about which message is used can be found on the reference page for each notification.</span></span>

<span data-ttu-id="739ac-133">Pour plus d’informations sur la gestion des messages, consultez [contrôle des messages](control-messages.md).</span><span class="sxs-lookup"><span data-stu-id="739ac-133">For more information on how to handle messages, see [Control Messages](control-messages.md).</span></span> <span data-ttu-id="739ac-134">Voir aussi messages de bouton.</span><span class="sxs-lookup"><span data-stu-id="739ac-134">See also Button Messages.</span></span>

## <a name="notification-messages-from-buttons"></a><span data-ttu-id="739ac-135">Messages de notification à partir de boutons</span><span class="sxs-lookup"><span data-stu-id="739ac-135">Notification Messages from Buttons</span></span>

<span data-ttu-id="739ac-136">Lorsque l’utilisateur clique sur un bouton, son état change et le bouton envoie des codes de notification, sous la forme de messages de [**\_ commande WM**](/windows/desktop/menurc/wm-command) , à sa fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="739ac-136">When the user clicks a button, its state changes, and the button sends notification codes, in the form of [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages, to its parent window.</span></span> <span data-ttu-id="739ac-137">Par exemple, un contrôle de bouton de commande envoie le code de notification sur lequel l’utilisateur a [ \_ cliqué](bn-clicked.md) chaque fois que l’utilisateur choisit le bouton.</span><span class="sxs-lookup"><span data-stu-id="739ac-137">For example, a push button control sends the [BN\_CLICKED](bn-clicked.md) notification code whenever the user chooses the button.</span></span> <span data-ttu-id="739ac-138">Dans tous les cas (à l’exception de [BCN \_ HOTITEMCHANGE](bcn-hotitemchange.md)), le mot de poids faible du paramètre *wParam* contient l’identificateur de contrôle, le mot de poids fort de *wParam* contient le code de notification et le paramètre *lParam* contient le handle de fenêtre de contrôle.</span><span class="sxs-lookup"><span data-stu-id="739ac-138">In all cases (except for [BCN\_HOTITEMCHANGE](bcn-hotitemchange.md)), the low-order word of the *wParam* parameter contains the control identifier, the high-order word of *wParam* contains the notification code, and the *lParam* parameter contains the control window handle.</span></span>

<span data-ttu-id="739ac-139">Le message et la réponse de la fenêtre parente dépendent du type, du style et de l’état actuel du bouton.</span><span class="sxs-lookup"><span data-stu-id="739ac-139">Both the message and the parent window's response depend on the type, style, and current state of the button.</span></span> <span data-ttu-id="739ac-140">Voici les codes de notification de bouton qu’une application doit surveiller et traiter.</span><span class="sxs-lookup"><span data-stu-id="739ac-140">Following are the button notification codes an application should monitor and process.</span></span>



| <span data-ttu-id="739ac-141">Code de notification</span><span class="sxs-lookup"><span data-stu-id="739ac-141">Notification code</span></span>                                                        | <span data-ttu-id="739ac-142">Description</span><span class="sxs-lookup"><span data-stu-id="739ac-142">Description</span></span>                                            |
|--------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="739ac-143">BCN \_ HOTITEMCHANGE</span><span class="sxs-lookup"><span data-stu-id="739ac-143">BCN\_HOTITEMCHANGE</span></span>](bcn-hotitemchange.md)                              | <span data-ttu-id="739ac-144">Souris entrée ou gauche de la zone cliente d’un bouton.</span><span class="sxs-lookup"><span data-stu-id="739ac-144">The mouse entered or left the client area of a button.</span></span> |
| [<span data-ttu-id="739ac-145">sur lequel l' \_ utilisateur a cliqué</span><span class="sxs-lookup"><span data-stu-id="739ac-145">BN\_CLICKED</span></span>](bn-clicked.md)                                            | <span data-ttu-id="739ac-146">L’utilisateur a cliqué sur un bouton.</span><span class="sxs-lookup"><span data-stu-id="739ac-146">The user clicked a button.</span></span>                             |
| <span data-ttu-id="739ac-147">De la [ \_ DBLCLK](bn-dblclk.md) ou [un \_ ](bn-doubleclicked.md)</span><span class="sxs-lookup"><span data-stu-id="739ac-147">[BN\_DBLCLK](bn-dblclk.md) or [BN\_DOUBLECLICKED](bn-doubleclicked.md)</span></span> | <span data-ttu-id="739ac-148">L’utilisateur a double-cliqué sur un bouton.</span><span class="sxs-lookup"><span data-stu-id="739ac-148">The user double-clicked a button.</span></span>                      |
| [<span data-ttu-id="739ac-149">désactivation de la \_ coche</span><span class="sxs-lookup"><span data-stu-id="739ac-149">BN\_DISABLE</span></span>](bn-disable.md)                                            | <span data-ttu-id="739ac-150">Un bouton est désactivé.</span><span class="sxs-lookup"><span data-stu-id="739ac-150">A button is disabled.</span></span>                                  |
| <span data-ttu-id="739ac-151">De la [ \_ Push](bn-pushed.md) ou [ \_ HiLite](bn-hilite.md)</span><span class="sxs-lookup"><span data-stu-id="739ac-151">[BN\_PUSHED](bn-pushed.md) or [BN\_HILITE](bn-hilite.md)</span></span>               | <span data-ttu-id="739ac-152">L’utilisateur a appuyé sur un bouton.</span><span class="sxs-lookup"><span data-stu-id="739ac-152">The user pushed a button.</span></span>                              |
| [<span data-ttu-id="739ac-153">\_KILLFOCUS.</span><span class="sxs-lookup"><span data-stu-id="739ac-153">BN\_KILLFOCUS</span></span>](bn-killfocus.md)                                        | <span data-ttu-id="739ac-154">Le bouton a perdu le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="739ac-154">The button lost the keyboard focus.</span></span>                    |
| [<span data-ttu-id="739ac-155">peinture de la \_ bosse</span><span class="sxs-lookup"><span data-stu-id="739ac-155">BN\_PAINT</span></span>](bn-paint.md)                                                | <span data-ttu-id="739ac-156">Le bouton doit être peint.</span><span class="sxs-lookup"><span data-stu-id="739ac-156">The button should be painted.</span></span>                          |
| [<span data-ttu-id="739ac-157">-e \_ SetFocus</span><span class="sxs-lookup"><span data-stu-id="739ac-157">BN\_SETFOCUS</span></span>](bn-setfocus.md)                                          | <span data-ttu-id="739ac-158">Le bouton a obtenu le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="739ac-158">The button gained the keyboard focus.</span></span>                  |
| <span data-ttu-id="739ac-159">De la [ \_ ](bn-unpushed.md) [ \_ UNHILITE](bn-unhilite.md) de type push</span><span class="sxs-lookup"><span data-stu-id="739ac-159">[BN\_UNPUSHED](bn-unpushed.md) or [BN\_UNHILITE](bn-unhilite.md)</span></span>       | <span data-ttu-id="739ac-160">Le bouton n’est plus poussé.</span><span class="sxs-lookup"><span data-stu-id="739ac-160">The button is no longer pushed.</span></span>                        |



 

<span data-ttu-id="739ac-161">Un bouton envoie les codes de notification de la part de [ \_ désactivation](bn-disable.md), de la cale, de l' [ \_ KILLFOCUS](bn-killfocus.md) [, \_ du](bn-pushed.md)type de ligne et de la ligne de commande [**de la part de la ligne \_**](button-styles.md) de [ \_ commande](bn-unpushed.md) . [ \_](bn-paint.md) [ \_](bn-setfocus.md)</span><span class="sxs-lookup"><span data-stu-id="739ac-161">A button sends the [BN\_DISABLE](bn-disable.md), [BN\_PUSHED](bn-pushed.md), [BN\_KILLFOCUS](bn-killfocus.md), [BN\_PAINT](bn-paint.md), [BN\_SETFOCUS](bn-setfocus.md), and [BN\_UNPUSHED](bn-unpushed.md) notification codes only if it has the [**BS\_NOTIFY**](button-styles.md) style.</span></span> <span data-ttu-id="739ac-162">De la [ \_](bn-dblclk.md)Les codes de notification DBLCLK sont automatiquement envoyés pour les boutons [**BS \_ UserButton**](button-styles.md), [**BS \_ RadioButton**](button-styles.md)et [**BS \_ OwnerDraw**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="739ac-162">[BN\_DBLCLK](bn-dblclk.md) notification codes are sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="739ac-163">Les autres types de bouton envoient \_ l’DBLCLK de l’adresse de l’utilisateur uniquement s’ils ont le style **BS \_ Notify** .</span><span class="sxs-lookup"><span data-stu-id="739ac-163">Other button types send BN\_DBLCLK only if they have the **BS\_NOTIFY** style.</span></span> <span data-ttu-id="739ac-164">Tous les boutons envoient le code de notification [ \_ sur lequel vous avez cliqué](bn-clicked.md) , quels que soient les styles de bouton.</span><span class="sxs-lookup"><span data-stu-id="739ac-164">All buttons send the [BN\_CLICKED](bn-clicked.md) notification code regardless of their button styles.</span></span>

<span data-ttu-id="739ac-165">Pour les boutons automatiques, le système modifie l’état de transmission et peint le bouton.</span><span class="sxs-lookup"><span data-stu-id="739ac-165">For automatic buttons, the system changes the push state and paints the button.</span></span> <span data-ttu-id="739ac-166">Dans ce cas, l’application traite généralement uniquement les codes de notification « en [ \_ un clic](bn-clicked.md) » et « [ \_ DBLCLK](bn-dblclk.md) ».</span><span class="sxs-lookup"><span data-stu-id="739ac-166">In this case, the application typically processes only the [BN\_CLICKED](bn-clicked.md) and [BN\_DBLCLK](bn-dblclk.md) notification codes.</span></span> <span data-ttu-id="739ac-167">Pour les boutons qui ne sont pas automatiques, l’application répond généralement au code de notification en envoyant un message pour modifier l’état du bouton.</span><span class="sxs-lookup"><span data-stu-id="739ac-167">For buttons that are not automatic, the application typically responds to the notification code by sending a message to change the state of the button.</span></span> <span data-ttu-id="739ac-168">Pour plus d’informations sur l’envoi de messages à des boutons, consultez [envoi de messages à des boutons](#sending-messages-to-buttons).</span><span class="sxs-lookup"><span data-stu-id="739ac-168">For information about sending messages to buttons, see [Sending Messages to Buttons](#sending-messages-to-buttons).</span></span>

<span data-ttu-id="739ac-169">Lorsque l’utilisateur sélectionne un bouton owner-drawn, le bouton envoie à sa fenêtre parente un message [**WM \_ DRAWITEM**](wm-drawitem.md) contenant l’identificateur du contrôle à dessiner et des informations sur ses dimensions et son état.</span><span class="sxs-lookup"><span data-stu-id="739ac-169">When the user selects an owner-drawn button, the button sends its parent window a [**WM\_DRAWITEM**](wm-drawitem.md) message containing the identifier of the control to be drawn and information about its dimensions and state.</span></span>

## <a name="button-color-messages"></a><span data-ttu-id="739ac-170">Messages de couleur de bouton</span><span class="sxs-lookup"><span data-stu-id="739ac-170">Button Color Messages</span></span>

<span data-ttu-id="739ac-171">Le système fournit des valeurs de couleur par défaut pour les boutons.</span><span class="sxs-lookup"><span data-stu-id="739ac-171">The system provides default color values for buttons.</span></span> <span data-ttu-id="739ac-172">Une application peut récupérer les valeurs par défaut de ces couleurs en appelant la fonction [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) ou définir les valeurs en appelant la fonction [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) .</span><span class="sxs-lookup"><span data-stu-id="739ac-172">An application can retrieve the default values for these colors by calling the [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) function, or set the values by calling the [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) function.</span></span> <span data-ttu-id="739ac-173">Le tableau suivant indique les valeurs de couleur de bouton par défaut.</span><span class="sxs-lookup"><span data-stu-id="739ac-173">The following table shows the default button-color values.</span></span>



| <span data-ttu-id="739ac-174">Valeur</span><span class="sxs-lookup"><span data-stu-id="739ac-174">Value</span></span>               | <span data-ttu-id="739ac-175">Élément coloré</span><span class="sxs-lookup"><span data-stu-id="739ac-175">Element colored</span></span>                                                                                                            |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="739ac-176">BTNFACE de couleurs \_</span><span class="sxs-lookup"><span data-stu-id="739ac-176">COLOR\_BTNFACE</span></span>      | <span data-ttu-id="739ac-177">Visages de bouton.</span><span class="sxs-lookup"><span data-stu-id="739ac-177">Button faces.</span></span>                                                                                                              |
| <span data-ttu-id="739ac-178">BTNHIGHLIGHT de couleurs \_</span><span class="sxs-lookup"><span data-stu-id="739ac-178">COLOR\_BTNHIGHLIGHT</span></span> | <span data-ttu-id="739ac-179">Zone de surbrillance (bords supérieur et gauche) d’un bouton.</span><span class="sxs-lookup"><span data-stu-id="739ac-179">Highlight area (the top and left edges) of a button.</span></span>                                                                       |
| <span data-ttu-id="739ac-180">BTNSHADOW de couleurs \_</span><span class="sxs-lookup"><span data-stu-id="739ac-180">COLOR\_BTNSHADOW</span></span>    | <span data-ttu-id="739ac-181">Zone ombrée (bords inférieur et droit) d’un bouton.</span><span class="sxs-lookup"><span data-stu-id="739ac-181">Shadow area (the bottom and right edges) of a button.</span></span>                                                                      |
| <span data-ttu-id="739ac-182">BTNTEXT de couleurs \_</span><span class="sxs-lookup"><span data-stu-id="739ac-182">COLOR\_BTNTEXT</span></span>      | <span data-ttu-id="739ac-183">Texte normal (qui n’est pas grisé) dans les boutons.</span><span class="sxs-lookup"><span data-stu-id="739ac-183">Regular (nongrayed) text in buttons.</span></span>                                                                                       |
| <span data-ttu-id="739ac-184">GRAYTEXT de couleurs \_</span><span class="sxs-lookup"><span data-stu-id="739ac-184">COLOR\_GRAYTEXT</span></span>     | <span data-ttu-id="739ac-185">Texte désactivé (gris) dans les boutons.</span><span class="sxs-lookup"><span data-stu-id="739ac-185">Disabled (gray) text in buttons.</span></span> <span data-ttu-id="739ac-186">Cette couleur est définie sur 0 si le pilote d’affichage actuel ne prend pas en charge une couleur grise unie.</span><span class="sxs-lookup"><span data-stu-id="739ac-186">This color is set to 0 if the current display driver does not support a solid gray color.</span></span> |
| <span data-ttu-id="739ac-187">fenêtre de couleur \_</span><span class="sxs-lookup"><span data-stu-id="739ac-187">COLOR\_WINDOW</span></span>       | <span data-ttu-id="739ac-188">Arrière-plan des fenêtres.</span><span class="sxs-lookup"><span data-stu-id="739ac-188">Window backgrounds.</span></span>                                                                                                        |
| <span data-ttu-id="739ac-189">WINDOWFRAME de couleurs \_</span><span class="sxs-lookup"><span data-stu-id="739ac-189">COLOR\_WINDOWFRAME</span></span>  | <span data-ttu-id="739ac-190">Frames de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="739ac-190">Window frames.</span></span>                                                                                                             |
| <span data-ttu-id="739ac-191">WINDOWTEXT de couleurs \_</span><span class="sxs-lookup"><span data-stu-id="739ac-191">COLOR\_WINDOWTEXT</span></span>   | <span data-ttu-id="739ac-192">Texte dans Windows.</span><span class="sxs-lookup"><span data-stu-id="739ac-192">Text in windows.</span></span>                                                                                                           |



 

<span data-ttu-id="739ac-193">Toutefois, l’appel de [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) affecte toutes les applications. par conséquent, vous ne devez pas appeler cette fonction pour personnaliser des boutons pour votre application.</span><span class="sxs-lookup"><span data-stu-id="739ac-193">However, calling [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) affects all applications, so you should not call this function to customize buttons for your application.</span></span>

<span data-ttu-id="739ac-194">Le système envoie un message [**WM \_ CTLCOLORBTN**](wm-ctlcolorbtn.md) à la fenêtre parente d’un bouton avant de dessiner un bouton.</span><span class="sxs-lookup"><span data-stu-id="739ac-194">The system sends a [**WM\_CTLCOLORBTN**](wm-ctlcolorbtn.md) message to a button's parent window before drawing a button.</span></span> <span data-ttu-id="739ac-195">Ce message contient un handle vers le contexte de périphérique du bouton et un handle vers la fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="739ac-195">This message contains a handle to the button's device context and a handle to the child window.</span></span> <span data-ttu-id="739ac-196">La fenêtre parente peut utiliser ces poignées pour modifier le texte du bouton et les couleurs d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="739ac-196">The parent window can use these handles to change the button's text and background colors.</span></span> <span data-ttu-id="739ac-197">Toutefois, seuls les boutons owner-drawn répondent à la fenêtre parente qui traite le message.</span><span class="sxs-lookup"><span data-stu-id="739ac-197">However, only owner-drawn buttons respond to the parent window processing the message.</span></span>

## <a name="button-default-message-processing"></a><span data-ttu-id="739ac-198">Traitement du message par défaut du bouton</span><span class="sxs-lookup"><span data-stu-id="739ac-198">Button Default Message Processing</span></span>

<span data-ttu-id="739ac-199">La procédure de fenêtre pour la classe de fenêtre de contrôle de bouton prédéfinie effectue le traitement par défaut pour tous les messages que la procédure de contrôle de bouton ne traite pas.</span><span class="sxs-lookup"><span data-stu-id="739ac-199">The window procedure for the predefined button control window class carries out default processing for all messages that the button control procedure does not process.</span></span> <span data-ttu-id="739ac-200">Lorsque la procédure de contrôle Button retourne la **valeur false** pour un message, la procédure de fenêtre prédéfinie vérifie les messages et exécute les actions par défaut indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="739ac-200">When the button control procedure returns **FALSE** for any message, the predefined window procedure checks the messages and performs the default actions listed in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="739ac-201">Message</span><span class="sxs-lookup"><span data-stu-id="739ac-201">Message</span></span></th>
<th><span data-ttu-id="739ac-202">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="739ac-202">Default action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="739ac-203"><a href="bm-click.md"><strong>BM_CLICK</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-203"><a href="bm-click.md"><strong>BM_CLICK</strong></a></span></span></td>
<td><span data-ttu-id="739ac-204">Envoie le bouton une <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> et un message <a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a> , puis envoie la fenêtre parente à un code de notification <a href="bn-clicked.md">BN_CLICKED</a> .</span><span class="sxs-lookup"><span data-stu-id="739ac-204">Sends the button a <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> and a <a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a> message, and sends the parent window a <a href="bn-clicked.md">BN_CLICKED</a> notification code.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="739ac-205"><a href="bm-getcheck.md"><strong>BM_GETCHECK</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-205"><a href="bm-getcheck.md"><strong>BM_GETCHECK</strong></a></span></span></td>
<td><span data-ttu-id="739ac-206">Retourne l’état d’activation du bouton.</span><span class="sxs-lookup"><span data-stu-id="739ac-206">Returns the check state of the button.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="739ac-207"><a href="bm-getimage.md"><strong>BM_GETIMAGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-207"><a href="bm-getimage.md"><strong>BM_GETIMAGE</strong></a></span></span></td>
<td><span data-ttu-id="739ac-208">Retourne un handle vers la bitmap ou l’icône associée au bouton, ou <strong>null</strong> si le bouton n’a aucune bitmap ou icône.</span><span class="sxs-lookup"><span data-stu-id="739ac-208">Returns a handle to the bitmap or icon associated with the button or <strong>NULL</strong> if the button has no bitmap or icon.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="739ac-209"><a href="bm-getstate.md"><strong>BM_GETSTATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-209"><a href="bm-getstate.md"><strong>BM_GETSTATE</strong></a></span></span></td>
<td><span data-ttu-id="739ac-210">Retourne l’état d’activation actuel, l’état de push et l’état de focus du bouton.</span><span class="sxs-lookup"><span data-stu-id="739ac-210">Returns the current check state, push state, and focus state of the button.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="739ac-211"><a href="bm-setcheck.md"><strong>BM_SETCHECK</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-211"><a href="bm-setcheck.md"><strong>BM_SETCHECK</strong></a></span></span></td>
<td><span data-ttu-id="739ac-212">Définit l’état d’activation de tous les styles des cases d’option et des cases à cocher.</span><span class="sxs-lookup"><span data-stu-id="739ac-212">Sets the check state for all styles of radio buttons and check boxes.</span></span> <span data-ttu-id="739ac-213">Si le paramètre <em>wParam</em> est supérieur à zéro pour les cases d’option, le bouton se voit attribuer le style <a href="/windows/desktop/winmsg/window-styles"><strong>WS_TABSTOP</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="739ac-213">If the <em>wParam</em> parameter is greater than zero for radio buttons, the button is given the <a href="/windows/desktop/winmsg/window-styles"><strong>WS_TABSTOP</strong></a> style.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="739ac-214"><a href="bm-setimage.md"><strong>BM_SETIMAGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-214"><a href="bm-setimage.md"><strong>BM_SETIMAGE</strong></a></span></span></td>
<td><span data-ttu-id="739ac-215">Associe la bitmap ou la poignée d’icône spécifiée au bouton et retourne un handle vers la bitmap ou l’icône précédente.</span><span class="sxs-lookup"><span data-stu-id="739ac-215">Associates the specified bitmap or icon handle with the button and returns a handle to the previous bitmap or icon.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="739ac-216"><a href="bm-setstate.md"><strong>BM_SETSTATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-216"><a href="bm-setstate.md"><strong>BM_SETSTATE</strong></a></span></span></td>
<td><span data-ttu-id="739ac-217">Définit l’état de transmission (push) du bouton.</span><span class="sxs-lookup"><span data-stu-id="739ac-217">Sets the push state of the button.</span></span> <span data-ttu-id="739ac-218">Pour les boutons owner-drawn, un <a href="wm-drawitem.md"><strong>WM_DRAWITEM</strong></a> message est envoyé à la fenêtre parente si l’état du bouton a changé.</span><span class="sxs-lookup"><span data-stu-id="739ac-218">For owner-drawn buttons, a <a href="wm-drawitem.md"><strong>WM_DRAWITEM</strong></a> message is sent to the parent window if the state of the button has changed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="739ac-219"><a href="bm-setstyle.md"><strong>BM_SETSTYLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-219"><a href="bm-setstyle.md"><strong>BM_SETSTYLE</strong></a></span></span></td>
<td><span data-ttu-id="739ac-220">Définit le style du bouton.</span><span class="sxs-lookup"><span data-stu-id="739ac-220">Sets the button style.</span></span> <span data-ttu-id="739ac-221">Si le mot de poids faible du paramètre <em>lParam</em> a la <strong>valeur true</strong>, le bouton est redessiné.</span><span class="sxs-lookup"><span data-stu-id="739ac-221">If the low-order word of the <em>lParam</em> parameter is <strong>TRUE</strong>, the button is redrawn.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="739ac-222"><a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-222"><a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a></span></span></td>
<td><span data-ttu-id="739ac-223">Active une case à cocher ou une case à cocher automatique lorsque l’utilisateur appuie sur les touches plus (+) ou égales (=).</span><span class="sxs-lookup"><span data-stu-id="739ac-223">Checks a check box or automatic check box when the user presses the plus (+) or equal (=) keys.</span></span> <span data-ttu-id="739ac-224">Désactive une case à cocher ou une case à cocher automatique lorsque l’utilisateur appuie sur la touche moins (–).</span><span class="sxs-lookup"><span data-stu-id="739ac-224">Clears a check box or automatic check box when the user presses the minus (–) key.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="739ac-225"><a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-225"><a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a></span></span></td>
<td><span data-ttu-id="739ac-226">Peint le bouton.</span><span class="sxs-lookup"><span data-stu-id="739ac-226">Paints the button.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="739ac-227"><a href="/windows/desktop/winmsg/wm-erasebkgnd"><strong>WM_ERASEBKGND</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-227"><a href="/windows/desktop/winmsg/wm-erasebkgnd"><strong>WM_ERASEBKGND</strong></a></span></span></td>
<td><span data-ttu-id="739ac-228">Efface l’arrière-plan des boutons owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="739ac-228">Erases the background for owner-drawn buttons.</span></span> <span data-ttu-id="739ac-229">Les arrière-plans des autres boutons sont effacés dans le cadre de la <a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a> et <a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a> traitement.</span><span class="sxs-lookup"><span data-stu-id="739ac-229">The backgrounds of other buttons are erased as part of the <a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a> and <a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a> processing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="739ac-230"><a href="/windows/desktop/dlgbox/wm-getdlgcode"><strong>WM_GETDLGCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-230"><a href="/windows/desktop/dlgbox/wm-getdlgcode"><strong>WM_GETDLGCODE</strong></a></span></span></td>
<td><span data-ttu-id="739ac-231">Retourne des valeurs qui indiquent le type d’entrée traité par la procédure de bouton par défaut, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="739ac-231">Returns values that indicate the type of input processed by the default button procedure, as shown in the following table.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="739ac-232">Style de bouton</span><span class="sxs-lookup"><span data-stu-id="739ac-232">Button style</span></span></th>
<th><span data-ttu-id="739ac-233">Retours</span><span class="sxs-lookup"><span data-stu-id="739ac-233">Returns</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="739ac-234"><a href="button-styles.md"><strong>BS_AUTOCHECKBOX</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-234"><a href="button-styles.md"><strong>BS_AUTOCHECKBOX</strong></a></span></span></td>
<td><span data-ttu-id="739ac-235">DLGC_WANTCHARS | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="739ac-235">DLGC_WANTCHARS | DLGC_BUTTON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="739ac-236"><a href="button-styles.md"><strong>BS_AUTORADIOBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-236"><a href="button-styles.md"><strong>BS_AUTORADIOBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="739ac-237">DLGC_RADIOBUTTON | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="739ac-237">DLGC_RADIOBUTTON | DLGC_BUTTON</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="739ac-238"><a href="button-styles.md"><strong>BS_CHECKBOX</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-238"><a href="button-styles.md"><strong>BS_CHECKBOX</strong></a></span></span></td>
<td><span data-ttu-id="739ac-239">DLGC_WANTCHARS | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="739ac-239">DLGC_WANTCHARS | DLGC_BUTTON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="739ac-240"><a href="button-styles.md"><strong>BS_DEFPUSHBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-240"><a href="button-styles.md"><strong>BS_DEFPUSHBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="739ac-241">DLGC_DEFPUSHBUTTON | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="739ac-241">DLGC_DEFPUSHBUTTON | DLGC_BUTTON</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="739ac-242"><a href="button-styles.md"><strong>BS_GROUPBOX</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-242"><a href="button-styles.md"><strong>BS_GROUPBOX</strong></a></span></span></td>
<td><span data-ttu-id="739ac-243">DLGC_STATIC</span><span class="sxs-lookup"><span data-stu-id="739ac-243">DLGC_STATIC</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="739ac-244"><a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-244"><a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="739ac-245">DLGC_UNDEFPUSHBUTTON | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="739ac-245">DLGC_UNDEFPUSHBUTTON | DLGC_BUTTON</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="739ac-246"><a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-246"><a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="739ac-247">DLGC_RADIOBUTTON | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="739ac-247">DLGC_RADIOBUTTON | DLGC_BUTTON</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="739ac-248"><a href="/windows/desktop/winmsg/wm-getfont"><strong>WM_GETFONT</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-248"><a href="/windows/desktop/winmsg/wm-getfont"><strong>WM_GETFONT</strong></a></span></span></td>
<td><span data-ttu-id="739ac-249">Retourne un handle vers la police actuelle.</span><span class="sxs-lookup"><span data-stu-id="739ac-249">Returns a handle to the current font.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="739ac-250"><a href="/windows/desktop/inputdev/wm-keydown"><strong>WM_KEYDOWN</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-250"><a href="/windows/desktop/inputdev/wm-keydown"><strong>WM_KEYDOWN</strong></a></span></span></td>
<td><span data-ttu-id="739ac-251">Exécute un push du bouton si l’utilisateur appuie sur la barre d’espace.</span><span class="sxs-lookup"><span data-stu-id="739ac-251">Pushes the button if the user presses the SPACEBAR.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="739ac-252"><a href="/windows/desktop/inputdev/wm-keyup"><strong>WM_KEYUP</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-252"><a href="/windows/desktop/inputdev/wm-keyup"><strong>WM_KEYUP</strong></a></span></span></td>
<td><span data-ttu-id="739ac-253">Libère la capture de la souris pour tous les cas, à l’exception de la touche TAB.</span><span class="sxs-lookup"><span data-stu-id="739ac-253">Releases the mouse capture for all cases except the TAB key.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="739ac-254"><a href="/windows/desktop/inputdev/wm-killfocus"><strong>WM_KILLFOCUS</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-254"><a href="/windows/desktop/inputdev/wm-killfocus"><strong>WM_KILLFOCUS</strong></a></span></span></td>
<td><span data-ttu-id="739ac-255">Supprime le rectangle de focus d’un bouton.</span><span class="sxs-lookup"><span data-stu-id="739ac-255">Removes the focus rectangle from a button.</span></span> <span data-ttu-id="739ac-256">Pour les boutons de commande et les boutons de commande par défaut, le rectangle de focus est invalidé.</span><span class="sxs-lookup"><span data-stu-id="739ac-256">For push buttons and default push buttons, the focus rectangle is invalidated.</span></span> <span data-ttu-id="739ac-257">Si le bouton a la capture de la souris, la capture est libérée, le bouton n’est pas cliqué et tout état de transmission est supprimé.</span><span class="sxs-lookup"><span data-stu-id="739ac-257">If the button has the mouse capture, the capture is released, the button is not clicked, and any push state is removed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="739ac-258"><a href="/windows/desktop/inputdev/wm-lbuttondblclk"><strong>WM_LBUTTONDBLCLK</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-258"><a href="/windows/desktop/inputdev/wm-lbuttondblclk"><strong>WM_LBUTTONDBLCLK</strong></a></span></span></td>
<td><span data-ttu-id="739ac-259">Envoie un <a href="bn-dblclk.md">BN_DBLCLK</a> code de notification à la fenêtre parente pour les cases d’option et les boutons owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="739ac-259">Sends a <a href="bn-dblclk.md">BN_DBLCLK</a> notification code to the parent window for radio buttons and owner-drawn buttons.</span></span> <span data-ttu-id="739ac-260">Pour les autres boutons, un double-clic est traité comme un message de <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="739ac-260">For other buttons, a double-click is processed as a <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> message.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="739ac-261"><a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-261"><a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a></span></span></td>
<td><span data-ttu-id="739ac-262">Met en surbrillance le bouton si la position du curseur de la souris se trouve dans le rectangle client du bouton.</span><span class="sxs-lookup"><span data-stu-id="739ac-262">Highlights the button if the position of the mouse cursor is within the button's client rectangle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="739ac-263"><a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-263"><a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a></span></span></td>
<td><span data-ttu-id="739ac-264">Libère la capture de la souris si le bouton avait la capture de la souris.</span><span class="sxs-lookup"><span data-stu-id="739ac-264">Releases the mouse capture if the button had the mouse capture.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="739ac-265"><a href="/windows/desktop/inputdev/wm-mousemove"><strong>WM_MOUSEMOVE</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-265"><a href="/windows/desktop/inputdev/wm-mousemove"><strong>WM_MOUSEMOVE</strong></a></span></span></td>
<td><span data-ttu-id="739ac-266">Effectue la même action que <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a>, si le bouton a la capture de la souris.</span><span class="sxs-lookup"><span data-stu-id="739ac-266">Performs the same action as <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a>, if the button has the mouse capture.</span></span> <span data-ttu-id="739ac-267">Dans le cas contraire, aucune action n’est effectuée.</span><span class="sxs-lookup"><span data-stu-id="739ac-267">Otherwise, no action is performed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="739ac-268"><a href="/windows/desktop/winmsg/wm-nccreate"><strong>WM_NCCREATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-268"><a href="/windows/desktop/winmsg/wm-nccreate"><strong>WM_NCCREATE</strong></a></span></span></td>
<td><span data-ttu-id="739ac-269">Active un bouton de <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> dans un bouton de <a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="739ac-269">Turns any <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> button into a <a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a> button.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="739ac-270"><a href="/windows/desktop/inputdev/wm-nchittest"><strong>WM_NCHITTEST</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-270"><a href="/windows/desktop/inputdev/wm-nchittest"><strong>WM_NCHITTEST</strong></a></span></span></td>
<td><span data-ttu-id="739ac-271">Retourne HTTRANSPARENT, si le contrôle bouton est une zone de groupe.</span><span class="sxs-lookup"><span data-stu-id="739ac-271">Returns HTTRANSPARENT, if the button control is a group box.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="739ac-272"><a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-272"><a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a></span></span></td>
<td><span data-ttu-id="739ac-273">Dessine le bouton en fonction de son style et de son état actuel.</span><span class="sxs-lookup"><span data-stu-id="739ac-273">Draws the button according to its style and current state.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="739ac-274"><a href="/windows/desktop/inputdev/wm-setfocus"><strong>WM_SETFOCUS</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-274"><a href="/windows/desktop/inputdev/wm-setfocus"><strong>WM_SETFOCUS</strong></a></span></span></td>
<td><span data-ttu-id="739ac-275">Dessine un rectangle de focus sur le bouton qui obtient le focus.</span><span class="sxs-lookup"><span data-stu-id="739ac-275">Draws a focus rectangle on the button getting the focus.</span></span> <span data-ttu-id="739ac-276">Pour les cases d’option et les cases d’option automatiques, la fenêtre parente reçoit un code de notification <a href="bn-clicked.md">BN_CLICKED</a> .</span><span class="sxs-lookup"><span data-stu-id="739ac-276">For radio buttons and automatic radio buttons, the parent window is sent a <a href="bn-clicked.md">BN_CLICKED</a> notification code.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="739ac-277"><a href="/windows/desktop/winmsg/wm-setfont"><strong>WM_SETFONT</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-277"><a href="/windows/desktop/winmsg/wm-setfont"><strong>WM_SETFONT</strong></a></span></span></td>
<td><span data-ttu-id="739ac-278">Définit une nouvelle police et éventuellement met à jour la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="739ac-278">Sets a new font and optionally updates the window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="739ac-279"><a href="/windows/desktop/winmsg/wm-settext"><strong>WM_SETTEXT</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-279"><a href="/windows/desktop/winmsg/wm-settext"><strong>WM_SETTEXT</strong></a></span></span></td>
<td><span data-ttu-id="739ac-280">Définit le texte du bouton.</span><span class="sxs-lookup"><span data-stu-id="739ac-280">Sets the text of the button.</span></span> <span data-ttu-id="739ac-281">Dans le cas d’une zone de groupe, le message est peint sur le texte préexistant avant de repeindre la zone de groupe avec le nouveau texte.</span><span class="sxs-lookup"><span data-stu-id="739ac-281">In the case of a group box, the message paints over the preexisting text before repainting the group box with the new text.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="739ac-282"><a href="/windows/desktop/inputdev/wm-syskeyup"><strong>WM_SYSKEYUP</strong></a></span><span class="sxs-lookup"><span data-stu-id="739ac-282"><a href="/windows/desktop/inputdev/wm-syskeyup"><strong>WM_SYSKEYUP</strong></a></span></span></td>
<td><span data-ttu-id="739ac-283">Libère la capture de la souris pour tous les cas, à l’exception de la touche TAB.</span><span class="sxs-lookup"><span data-stu-id="739ac-283">Releases the mouse capture for all cases except the TAB key.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="739ac-284">La procédure de fenêtre prédéfinie transmet tous les autres messages à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour le traitement par défaut.</span><span class="sxs-lookup"><span data-stu-id="739ac-284">The predefined window procedure passes all other messages to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function for default processing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="739ac-285">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="739ac-285">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="739ac-286">Messages de contrôle</span><span class="sxs-lookup"><span data-stu-id="739ac-286">Control Messages</span></span>](control-messages.md)
</dt> </dl>

 

 