---
title: Barre d’état
description: Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles de barre d’État.
ms.assetid: 77923055-9d00-4528-bda7-b602a26b577f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca6e46f1c573b75439cc10aa27ae3245e47e3de9
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103731492"
---
# <a name="status-bar"></a><span data-ttu-id="d8f75-103">Barre d’état</span><span class="sxs-lookup"><span data-stu-id="d8f75-103">Status Bar</span></span>

<span data-ttu-id="d8f75-104">Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles de barre d’État.</span><span class="sxs-lookup"><span data-stu-id="d8f75-104">This section contains information about the programming elements used with status bar controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="d8f75-105">Vues d'ensemble</span><span class="sxs-lookup"><span data-stu-id="d8f75-105">Overviews</span></span>



| <span data-ttu-id="d8f75-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="d8f75-106">Topic</span></span>                          | <span data-ttu-id="d8f75-107">Contenu</span><span class="sxs-lookup"><span data-stu-id="d8f75-107">Contents</span></span>                                                                                                                                                   |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8f75-108">Barres d’État</span><span class="sxs-lookup"><span data-stu-id="d8f75-108">Status Bars</span></span>](status-bars.md) | <span data-ttu-id="d8f75-109">Une *barre d’État* est une fenêtre horizontale au bas d’une fenêtre parente dans laquelle une application peut afficher différents types d’informations d’État.</span><span class="sxs-lookup"><span data-stu-id="d8f75-109">A *status bar* is a horizontal window at the bottom of a parent window in which an application can display various kinds of status information.</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="d8f75-110">Fonctions</span><span class="sxs-lookup"><span data-stu-id="d8f75-110">Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d8f75-111">Rubrique</span><span class="sxs-lookup"><span data-stu-id="d8f75-111">Topic</span></span></th>
<th><span data-ttu-id="d8f75-112">Contenu</span><span class="sxs-lookup"><span data-stu-id="d8f75-112">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d8f75-113"><a href="/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa"><strong>CreateStatusWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="d8f75-113"><a href="/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa"><strong>CreateStatusWindow</strong></a></span></span></td>
<td><span data-ttu-id="d8f75-114">Crée une fenêtre d’État, qui est généralement utilisée pour afficher l’état d’une application.</span><span class="sxs-lookup"><span data-stu-id="d8f75-114">Creates a status window, which is typically used to display the status of an application.</span></span> <span data-ttu-id="d8f75-115">La fenêtre apparaît généralement au bas de la fenêtre parente et contient le texte spécifié.</span><span class="sxs-lookup"><span data-stu-id="d8f75-115">The window generally appears at the bottom of the parent window, and it contains the specified text.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="d8f75-116">Cette fonction est obsolète.</span><span class="sxs-lookup"><span data-stu-id="d8f75-116">This function is obsolete.</span></span> <span data-ttu-id="d8f75-117">Utilisez <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa"><strong>CreateWindow</strong></a> à la place.</span><span class="sxs-lookup"><span data-stu-id="d8f75-117">Use <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa"><strong>CreateWindow</strong></a> instead.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d8f75-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a></span><span class="sxs-lookup"><span data-stu-id="d8f75-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a></span></span></td>
<td><span data-ttu-id="d8f75-119">La fonction <a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a> dessine le texte spécifié dans le style d’une fenêtre d’État avec des bordures.</span><span class="sxs-lookup"><span data-stu-id="d8f75-119">The <a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a> function draws the specified text in the style of a status window with borders.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d8f75-120"><a href="/windows/desktop/api/Commctrl/nf-commctrl-menuhelp"><strong>MenuHelp</strong></a></span><span class="sxs-lookup"><span data-stu-id="d8f75-120"><a href="/windows/desktop/api/Commctrl/nf-commctrl-menuhelp"><strong>MenuHelp</strong></a></span></span></td>
<td><span data-ttu-id="d8f75-121">Traite les messages <a href="/windows/desktop/menurc/wm-menuselect"><strong>WM_MENUSELECT</strong></a> et <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> et affiche le texte d’aide à propos du menu en cours dans la fenêtre d’état spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d8f75-121">Processes <a href="/windows/desktop/menurc/wm-menuselect"><strong>WM_MENUSELECT</strong></a> and <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> messages and displays Help text about the current menu in the specified status window.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="messages"></a><span data-ttu-id="d8f75-122">Messages</span><span class="sxs-lookup"><span data-stu-id="d8f75-122">Messages</span></span>



| <span data-ttu-id="d8f75-123">Rubrique</span><span class="sxs-lookup"><span data-stu-id="d8f75-123">Topic</span></span>                                               | <span data-ttu-id="d8f75-124">Contenu</span><span class="sxs-lookup"><span data-stu-id="d8f75-124">Contents</span></span>                                                                                                                                                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8f75-125">**\_GETBORDERS SB**</span><span class="sxs-lookup"><span data-stu-id="d8f75-125">**SB\_GETBORDERS**</span></span>](sb-getborders.md)             | <span data-ttu-id="d8f75-126">Récupère les largeurs actuelles des bordures horizontale et verticale d’une fenêtre d’État.</span><span class="sxs-lookup"><span data-stu-id="d8f75-126">Retrieves the current widths of the horizontal and vertical borders of a status window.</span></span> <br/>                                                                                                  |
| [<span data-ttu-id="d8f75-127">**\_GETICON SB**</span><span class="sxs-lookup"><span data-stu-id="d8f75-127">**SB\_GETICON**</span></span>](sb-geticon.md)                   | <span data-ttu-id="d8f75-128">Récupère l’icône pour un composant dans une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="d8f75-128">Retrieves the icon for a part in a status bar.</span></span> <br/>                                                                                                                                           |
| [<span data-ttu-id="d8f75-129">**\_GETPARTS SB**</span><span class="sxs-lookup"><span data-stu-id="d8f75-129">**SB\_GETPARTS**</span></span>](sb-getparts.md)                 | <span data-ttu-id="d8f75-130">Récupère le nombre de parties dans une fenêtre d’État.</span><span class="sxs-lookup"><span data-stu-id="d8f75-130">Retrieves a count of the parts in a status window.</span></span> <span data-ttu-id="d8f75-131">Le message récupère également la coordonnée du bord droit du nombre spécifié de parties.</span><span class="sxs-lookup"><span data-stu-id="d8f75-131">The message also retrieves the coordinate of the right edge of the specified number of parts.</span></span> <br/>                                         |
| [<span data-ttu-id="d8f75-132">**\_GETRECT SB**</span><span class="sxs-lookup"><span data-stu-id="d8f75-132">**SB\_GETRECT**</span></span>](sb-getrect.md)                   | <span data-ttu-id="d8f75-133">Récupère le rectangle englobant d’un composant dans une fenêtre d’État.</span><span class="sxs-lookup"><span data-stu-id="d8f75-133">Retrieves the bounding rectangle of a part in a status window.</span></span> <br/>                                                                                                                           |
| [<span data-ttu-id="d8f75-134">**SB \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="d8f75-134">**SB\_GETTEXT**</span></span>](sb-gettext.md)                   | <span data-ttu-id="d8f75-135">Le message [**SB \_ GETTEXT**](sb-gettext.md) récupère le texte à partir de la partie spécifiée d’une fenêtre d’État.</span><span class="sxs-lookup"><span data-stu-id="d8f75-135">The [**SB\_GETTEXT**](sb-gettext.md) message retrieves the text from the specified part of a status window.</span></span> <br/>                                                                             |
| [<span data-ttu-id="d8f75-136">**\_GETTEXTLENGTH SB**</span><span class="sxs-lookup"><span data-stu-id="d8f75-136">**SB\_GETTEXTLENGTH**</span></span>](sb-gettextlength.md)       | <span data-ttu-id="d8f75-137">Le message [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) récupère la longueur, en caractères, du texte à partir de la partie spécifiée d’une fenêtre d’État.</span><span class="sxs-lookup"><span data-stu-id="d8f75-137">The [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) message retrieves the length, in characters, of the text from the specified part of a status window.</span></span> <br/>                                   |
| [<span data-ttu-id="d8f75-138">**\_GETTIPTEXT SB**</span><span class="sxs-lookup"><span data-stu-id="d8f75-138">**SB\_GETTIPTEXT**</span></span>](sb-gettiptext.md)             | <span data-ttu-id="d8f75-139">Récupère le texte d’info-bulle pour un composant dans une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="d8f75-139">Retrieves the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="d8f75-140">La barre d’État doit être créée avec le style [**\_ info-bulles SBT**](status-bar-styles.md) pour activer les info-bulles.</span><span class="sxs-lookup"><span data-stu-id="d8f75-140">The status bar must be created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span> <br/>         |
| [<span data-ttu-id="d8f75-141">**\_GETUNICODEFORMAT SB**</span><span class="sxs-lookup"><span data-stu-id="d8f75-141">**SB\_GETUNICODEFORMAT**</span></span>](sb-getunicodeformat.md) | <span data-ttu-id="d8f75-142">Récupère l’indicateur de format de caractère Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="d8f75-142">Retrieves the Unicode character format flag for the control.</span></span> <br/>                                                                                                                             |
| [<span data-ttu-id="d8f75-143">**\_ISSIMPLE SB**</span><span class="sxs-lookup"><span data-stu-id="d8f75-143">**SB\_ISSIMPLE**</span></span>](sb-issimple.md)                 | <span data-ttu-id="d8f75-144">Vérifie un contrôle de barre d’État pour déterminer s’il est en mode simple.</span><span class="sxs-lookup"><span data-stu-id="d8f75-144">Checks a status bar control to determine if it is in simple mode.</span></span> <br/>                                                                                                                        |
| [<span data-ttu-id="d8f75-145">**\_SETBKCOLOR SB**</span><span class="sxs-lookup"><span data-stu-id="d8f75-145">**SB\_SETBKCOLOR**</span></span>](sb-setbkcolor.md)             | <span data-ttu-id="d8f75-146">Définit la couleur d’arrière-plan dans une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="d8f75-146">Sets the background color in a status bar.</span></span> <br/>                                                                                                                                               |
| [<span data-ttu-id="d8f75-147">**\_SETICON SB**</span><span class="sxs-lookup"><span data-stu-id="d8f75-147">**SB\_SETICON**</span></span>](sb-seticon.md)                   | <span data-ttu-id="d8f75-148">Définit l’icône d’un composant dans une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="d8f75-148">Sets the icon for a part in a status bar.</span></span> <br/>                                                                                                                                                |
| [<span data-ttu-id="d8f75-149">**\_SETMINHEIGHT SB**</span><span class="sxs-lookup"><span data-stu-id="d8f75-149">**SB\_SETMINHEIGHT**</span></span>](sb-setminheight.md)         | <span data-ttu-id="d8f75-150">Définit la hauteur minimale de la zone de dessin d’une fenêtre d’État.</span><span class="sxs-lookup"><span data-stu-id="d8f75-150">Sets the minimum height of a status window's drawing area.</span></span> <br/>                                                                                                                               |
| [<span data-ttu-id="d8f75-151">**\_SETPARTS SB**</span><span class="sxs-lookup"><span data-stu-id="d8f75-151">**SB\_SETPARTS**</span></span>](sb-setparts.md)                 | <span data-ttu-id="d8f75-152">Définit le nombre de parties dans une fenêtre d’État et la coordonnée du bord droit de chaque partie.</span><span class="sxs-lookup"><span data-stu-id="d8f75-152">Sets the number of parts in a status window and the coordinate of the right edge of each part.</span></span> <br/>                                                                                           |
| [<span data-ttu-id="d8f75-153">**unisettext SB \_**</span><span class="sxs-lookup"><span data-stu-id="d8f75-153">**SB\_SETTEXT**</span></span>](sb-settext.md)                   | <span data-ttu-id="d8f75-154">Le \_ message SB SETTEXT définit le texte dans la partie spécifiée d’une fenêtre d’État.</span><span class="sxs-lookup"><span data-stu-id="d8f75-154">The SB\_SETTEXT message sets the text in the specified part of a status window.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="d8f75-155">**\_SETTIPTEXT SB**</span><span class="sxs-lookup"><span data-stu-id="d8f75-155">**SB\_SETTIPTEXT**</span></span>](sb-settiptext.md)             | <span data-ttu-id="d8f75-156">Définit le texte d’info-bulle pour un composant dans une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="d8f75-156">Sets the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="d8f75-157">La barre d’État doit avoir été créée avec le style [**\_ info-bulles SBT**](status-bar-styles.md) pour activer les info-bulles.</span><span class="sxs-lookup"><span data-stu-id="d8f75-157">The status bar must have been created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span><br/>        |
| [<span data-ttu-id="d8f75-158">**\_SETUNICODEFORMAT SB**</span><span class="sxs-lookup"><span data-stu-id="d8f75-158">**SB\_SETUNICODEFORMAT**</span></span>](sb-setunicodeformat.md) | <span data-ttu-id="d8f75-159">Définit l’indicateur de format de caractère Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="d8f75-159">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="d8f75-160">Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle.</span><span class="sxs-lookup"><span data-stu-id="d8f75-160">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <br/> |
| [<span data-ttu-id="d8f75-161">**\_simple SB**</span><span class="sxs-lookup"><span data-stu-id="d8f75-161">**SB\_SIMPLE**</span></span>](sb-simple.md)                     | <span data-ttu-id="d8f75-162">Spécifie si une fenêtre d’état affiche du texte simple ou affiche toutes les parties de fenêtre définies par un message [**SB \_ SETPARTS**](sb-setparts.md) précédent.</span><span class="sxs-lookup"><span data-stu-id="d8f75-162">Specifies whether a status window displays simple text or displays all window parts set by a previous [**SB\_SETPARTS**](sb-setparts.md) message.</span></span> <br/>                                       |



 

### <a name="notifications"></a><span data-ttu-id="d8f75-163">Notifications</span><span class="sxs-lookup"><span data-stu-id="d8f75-163">Notifications</span></span>



| <span data-ttu-id="d8f75-164">Rubrique</span><span class="sxs-lookup"><span data-stu-id="d8f75-164">Topic</span></span>                                                 | <span data-ttu-id="d8f75-165">Contenu</span><span class="sxs-lookup"><span data-stu-id="d8f75-165">Contents</span></span>                                                                                                                                                                                                                                                           |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8f75-166">NM- \_ cliquer (barre d’État)</span><span class="sxs-lookup"><span data-stu-id="d8f75-166">NM\_CLICK (status bar)</span></span>](nm-click-status-bar.md)     | <span data-ttu-id="d8f75-167">Notifie la fenêtre parente d’un contrôle de barre d’État que l’utilisateur a cliqué avec le bouton gauche de la souris dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="d8f75-167">Notifies the parent window of a status bar control that the user has clicked the left mouse button within the control.</span></span> <span data-ttu-id="d8f75-168">[Nm \_ Cliquez (barre d’État)](nm-click-status-bar.md) est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d8f75-168">[NM\_CLICK (status bar)](nm-click-status-bar.md) is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/>              |
| [<span data-ttu-id="d8f75-169">\_DBLCLK nm (barre d’État)</span><span class="sxs-lookup"><span data-stu-id="d8f75-169">NM\_DBLCLK (status bar)</span></span>](nm-dblclk-status-bar.md)   | <span data-ttu-id="d8f75-170">Notifie la fenêtre parente d’un contrôle de barre d’État que l’utilisateur a double-cliqué dans le contrôle avec le bouton gauche de la souris.</span><span class="sxs-lookup"><span data-stu-id="d8f75-170">Notifies the parent window of a status bar control that the user has double-clicked the left mouse button within the control.</span></span> <span data-ttu-id="d8f75-171">Cette notification est envoyée sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d8f75-171">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/>                                       |
| [<span data-ttu-id="d8f75-172">\_RCLICK nm (barre d’État)</span><span class="sxs-lookup"><span data-stu-id="d8f75-172">NM\_RCLICK (status bar)</span></span>](nm-rclick-status-bar.md)   | <span data-ttu-id="d8f75-173">Notifie la fenêtre parente d’un contrôle de barre d’État sur lequel l’utilisateur a cliqué avec le bouton droit de la souris dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="d8f75-173">Notifies the parent window of a status bar control that the user has clicked the right mouse button within the control.</span></span> <span data-ttu-id="d8f75-174">Cette notification est envoyée sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d8f75-174">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/>                                             |
| [<span data-ttu-id="d8f75-175">\_RDBLCLK nm (barre d’État)</span><span class="sxs-lookup"><span data-stu-id="d8f75-175">NM\_RDBLCLK (status bar)</span></span>](nm-rdblclk-status-bar.md) | <span data-ttu-id="d8f75-176">Avertit les fenêtres parentes d’un contrôle de barre d’État que l’utilisateur a double-cliqué sur le bouton droit de la souris dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="d8f75-176">Notifies the parent windows of a status bar control that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="d8f75-177">[Nm \_ RDBLCLK (barre d’État)](nm-rdblclk-status-bar.md) est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d8f75-177">[NM\_RDBLCLK (status bar)](nm-rdblclk-status-bar.md) is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/> |
| [<span data-ttu-id="d8f75-178">SBN \_ SIMPLEMODECHANGE</span><span class="sxs-lookup"><span data-stu-id="d8f75-178">SBN\_SIMPLEMODECHANGE</span></span>](sbn-simplemodechange.md)     | <span data-ttu-id="d8f75-179">Envoyé par un contrôle de barre d’État lorsque le mode simple change en raison d’un message [**SB \_ simple**](sb-simple.md) .</span><span class="sxs-lookup"><span data-stu-id="d8f75-179">Sent by a status bar control when the simple mode changes due to a [**SB\_SIMPLE**](sb-simple.md) message.</span></span> <span data-ttu-id="d8f75-180">Cette notification est envoyée sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d8f75-180">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/>                                                        |



 

### <a name="constants"></a><span data-ttu-id="d8f75-181">Constantes</span><span class="sxs-lookup"><span data-stu-id="d8f75-181">Constants</span></span>



| <span data-ttu-id="d8f75-182">Rubrique</span><span class="sxs-lookup"><span data-stu-id="d8f75-182">Topic</span></span>                                      | <span data-ttu-id="d8f75-183">Contenu</span><span class="sxs-lookup"><span data-stu-id="d8f75-183">Contents</span></span>                                                                                                              |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8f75-184">Styles de barre d’État</span><span class="sxs-lookup"><span data-stu-id="d8f75-184">Status Bar Styles</span></span>](status-bar-styles.md) | <span data-ttu-id="d8f75-185">Cette section répertorie les styles, en plus des styles de fenêtre standard, pris en charge par les contrôles de *barre d’État* .</span><span class="sxs-lookup"><span data-stu-id="d8f75-185">This section lists the styles, in addition to standard window styles, supported by *status bar* controls.</span></span> <br/> |



 

 

