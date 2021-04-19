---
title: Message WM_SYSCOMMAND (winuser. h)
description: Une fenêtre reçoit ce message lorsque l’utilisateur choisit une commande dans le menu fenêtre (anciennement appelé système ou menu contrôle) ou lorsque l’utilisateur choisit le bouton Agrandir, le bouton réduire, le bouton restaurer ou le bouton Fermer.
ms.assetid: 82c7cc95-82d5-4f0f-8c78-ab325561b04e
keywords:
- WM_SYSCOMMAND des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_SYSCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 25596f30457063bc90124f14489963507f85ff70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539292"
---
# <a name="wm_syscommand-message"></a><span data-ttu-id="66124-104">\_Message WM SYSCOMMAND</span><span class="sxs-lookup"><span data-stu-id="66124-104">WM\_SYSCOMMAND message</span></span>

<span data-ttu-id="66124-105">Une fenêtre reçoit ce message lorsque l’utilisateur choisit une commande dans le menu **fenêtre** (anciennement appelé système ou menu contrôle) ou lorsque l’utilisateur choisit le bouton Agrandir, le bouton réduire, le bouton restaurer ou le bouton Fermer.</span><span class="sxs-lookup"><span data-stu-id="66124-105">A window receives this message when the user chooses a command from the **Window** menu (formerly known as the system or control menu) or when the user chooses the maximize button, minimize button, restore button, or close button.</span></span>


```C++
#define WM_SYSCOMMAND                   0x0112
```

## <a name="example"></a><span data-ttu-id="66124-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="66124-106">Example</span></span>

```cpp
 case WM_SYSCOMMAND:
        if (wParam == SC_CLOSE)
        {
            EndDialog (hDlg, TRUE);
            return(TRUE);
        }
        break;

```
<span data-ttu-id="66124-107">Exemple tiré d' [exemples classiques Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/registry/RegExplorer.c) sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="66124-107">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/registry/RegExplorer.c) on GitHub.</span></span>

## <a name="parameters"></a><span data-ttu-id="66124-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66124-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66124-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="66124-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66124-110">Type de commande système demandée.</span><span class="sxs-lookup"><span data-stu-id="66124-110">The type of system command requested.</span></span> <span data-ttu-id="66124-111">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="66124-111">This parameter can be one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="66124-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="66124-112">Value</span></span></th>
<th><span data-ttu-id="66124-113">Signification</span><span class="sxs-lookup"><span data-stu-id="66124-113">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="SC_CLOSE"></span><span id="sc_close"></span><dl> <span data-ttu-id="66124-114"><dt><strong>SC_CLOSE</strong></dt> <dt>0xF060</dt> </span><span class="sxs-lookup"><span data-stu-id="66124-114"><dt><strong>SC_CLOSE</strong></dt> <dt>0xF060</dt> </span></span></dl></td>
<td><span data-ttu-id="66124-115">Ferme la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="66124-115">Closes the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_CONTEXTHELP"></span><span id="sc_contexthelp"></span><dl> <span data-ttu-id="66124-116"><dt><strong>SC_CONTEXTHELP</strong></dt> <dt>0xF180</dt> </span><span class="sxs-lookup"><span data-stu-id="66124-116"><dt><strong>SC_CONTEXTHELP</strong></dt> <dt>0xF180</dt> </span></span></dl></td>
<td><span data-ttu-id="66124-117">Remplace le curseur par un point d’interrogation par un pointeur.</span><span class="sxs-lookup"><span data-stu-id="66124-117">Changes the cursor to a question mark with a pointer.</span></span> <span data-ttu-id="66124-118">Si l’utilisateur clique ensuite sur un contrôle dans la boîte de dialogue, le contrôle reçoit un message de <a href="/windows/desktop/shell/wm-help"><strong>WM_HELP</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="66124-118">If the user then clicks a control in the dialog box, the control receives a <a href="/windows/desktop/shell/wm-help"><strong>WM_HELP</strong></a> message.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_DEFAULT"></span><span id="sc_default"></span><dl> <span data-ttu-id="66124-119"><dt><strong>SC_DEFAULT</strong></dt> <dt>0xF160</dt> </span><span class="sxs-lookup"><span data-stu-id="66124-119"><dt><strong>SC_DEFAULT</strong></dt> <dt>0xF160</dt> </span></span></dl></td>
<td><span data-ttu-id="66124-120">Sélectionne l’élément par défaut ; l’utilisateur a double-cliqué dans le menu fenêtre.</span><span class="sxs-lookup"><span data-stu-id="66124-120">Selects the default item; the user double-clicked the window menu.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_HOTKEY"></span><span id="sc_hotkey"></span><dl> <span data-ttu-id="66124-121"><dt><strong>SC_HOTKEY</strong></dt> <dt>0xF150</dt> </span><span class="sxs-lookup"><span data-stu-id="66124-121"><dt><strong>SC_HOTKEY</strong></dt> <dt>0xF150</dt> </span></span></dl></td>
<td><span data-ttu-id="66124-122">Active la fenêtre associée à la touche d’accès rapide spécifiée par l’application.</span><span class="sxs-lookup"><span data-stu-id="66124-122">Activates the window associated with the application-specified hot key.</span></span> <span data-ttu-id="66124-123">Le paramètre <em>lParam</em> identifie la fenêtre à activer.</span><span class="sxs-lookup"><span data-stu-id="66124-123">The <em>lParam</em> parameter identifies the window to activate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_HSCROLL"></span><span id="sc_hscroll"></span><dl> <span data-ttu-id="66124-124"><dt><strong>SC_HSCROLL</strong></dt> <dt>0xF080</dt> </span><span class="sxs-lookup"><span data-stu-id="66124-124"><dt><strong>SC_HSCROLL</strong></dt> <dt>0xF080</dt> </span></span></dl></td>
<td><span data-ttu-id="66124-125">Fait défiler horizontalement.</span><span class="sxs-lookup"><span data-stu-id="66124-125">Scrolls horizontally.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SCF_ISSECURE"></span><span id="scf_issecure"></span><dl> <span data-ttu-id="66124-126"><dt><strong>SCF_ISSECURE</strong></dt> <dt>0x00000001</dt> </span><span class="sxs-lookup"><span data-stu-id="66124-126"><dt><strong>SCF_ISSECURE</strong></dt> <dt>0x00000001</dt> </span></span></dl></td>
<td><span data-ttu-id="66124-127">Indique si l’économiseur d’écran est sécurisé.</span><span class="sxs-lookup"><span data-stu-id="66124-127">Indicates whether the screen saver is secure.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="SC_KEYMENU"></span><span id="sc_keymenu"></span><dl> <span data-ttu-id="66124-128"><dt><strong>SC_KEYMENU</strong></dt> <dt>0xF100</dt> </span><span class="sxs-lookup"><span data-stu-id="66124-128"><dt><strong>SC_KEYMENU</strong></dt> <dt>0xF100</dt> </span></span></dl></td>
<td><span data-ttu-id="66124-129">Récupère le menu fenêtre à la suite d’une séquence de touches.</span><span class="sxs-lookup"><span data-stu-id="66124-129">Retrieves the window menu as a result of a keystroke.</span></span> <span data-ttu-id="66124-130">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="66124-130">For more information, see the Remarks section.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_MAXIMIZE"></span><span id="sc_maximize"></span><dl> <span data-ttu-id="66124-131"><dt><strong>SC_MAXIMIZE</strong></dt> <dt>0xF030</dt> </span><span class="sxs-lookup"><span data-stu-id="66124-131"><dt><strong>SC_MAXIMIZE</strong></dt> <dt>0xF030</dt> </span></span></dl></td>
<td><span data-ttu-id="66124-132">Agrandit la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="66124-132">Maximizes the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_MINIMIZE"></span><span id="sc_minimize"></span><dl> <span data-ttu-id="66124-133"><dt><strong>SC_MINIMIZE</strong></dt> <dt>0xF020</dt> </span><span class="sxs-lookup"><span data-stu-id="66124-133"><dt><strong>SC_MINIMIZE</strong></dt> <dt>0xF020</dt> </span></span></dl></td>
<td><span data-ttu-id="66124-134">Réduit la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="66124-134">Minimizes the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_MONITORPOWER"></span><span id="sc_monitorpower"></span><dl> <span data-ttu-id="66124-135"><dt><strong>SC_MONITORPOWER</strong></dt> <dt>0xF170</dt> </span><span class="sxs-lookup"><span data-stu-id="66124-135"><dt><strong>SC_MONITORPOWER</strong></dt> <dt>0xF170</dt> </span></span></dl></td>
<td><span data-ttu-id="66124-136">Définit l’état de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="66124-136">Sets the state of the display.</span></span> <span data-ttu-id="66124-137">Cette commande prend en charge les appareils qui ont des fonctionnalités d’économie d’énergie, comme un ordinateur personnel alimenté par batterie.</span><span class="sxs-lookup"><span data-stu-id="66124-137">This command supports devices that have power-saving features, such as a battery-powered personal computer.</span></span> <br/> <span data-ttu-id="66124-138">Le paramètre <em>lParam</em> peut avoir les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="66124-138">The <em>lParam</em> parameter can have the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="66124-139">-1 (l’affichage est sous tension)</span><span class="sxs-lookup"><span data-stu-id="66124-139">-1 (the display is powering on)</span></span></li>
<li><span data-ttu-id="66124-140">1 (l’affichage est faible puissance)</span><span class="sxs-lookup"><span data-stu-id="66124-140">1 (the display is going to low power)</span></span></li>
<li><span data-ttu-id="66124-141">2 (l’affichage est en cours d’arrêt)</span><span class="sxs-lookup"><span data-stu-id="66124-141">2 (the display is being shut off)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="SC_MOUSEMENU"></span><span id="sc_mousemenu"></span><dl> <span data-ttu-id="66124-142"><dt><strong>SC_MOUSEMENU</strong></dt> <dt>0xF090</dt> </span><span class="sxs-lookup"><span data-stu-id="66124-142"><dt><strong>SC_MOUSEMENU</strong></dt> <dt>0xF090</dt> </span></span></dl></td>
<td><span data-ttu-id="66124-143">Récupère le menu fenêtre à la suite d’un clic de souris.</span><span class="sxs-lookup"><span data-stu-id="66124-143">Retrieves the window menu as a result of a mouse click.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_MOVE"></span><span id="sc_move"></span><dl> <span data-ttu-id="66124-144"><dt><strong>SC_MOVE</strong></dt> <dt>0xF010</dt> </span><span class="sxs-lookup"><span data-stu-id="66124-144"><dt><strong>SC_MOVE</strong></dt> <dt>0xF010</dt> </span></span></dl></td>
<td><span data-ttu-id="66124-145">Déplace la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="66124-145">Moves the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_NEXTWINDOW"></span><span id="sc_nextwindow"></span><dl> <span data-ttu-id="66124-146"><dt><strong>SC_NEXTWINDOW</strong></dt> <dt>0xF040</dt> </span><span class="sxs-lookup"><span data-stu-id="66124-146"><dt><strong>SC_NEXTWINDOW</strong></dt> <dt>0xF040</dt> </span></span></dl></td>
<td><span data-ttu-id="66124-147">Passe à la fenêtre suivante.</span><span class="sxs-lookup"><span data-stu-id="66124-147">Moves to the next window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_PREVWINDOW"></span><span id="sc_prevwindow"></span><dl> <span data-ttu-id="66124-148"><dt><strong>SC_PREVWINDOW</strong></dt> <dt>0xF050</dt> </span><span class="sxs-lookup"><span data-stu-id="66124-148"><dt><strong>SC_PREVWINDOW</strong></dt> <dt>0xF050</dt> </span></span></dl></td>
<td><span data-ttu-id="66124-149">Passe à la fenêtre précédente.</span><span class="sxs-lookup"><span data-stu-id="66124-149">Moves to the previous window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_RESTORE"></span><span id="sc_restore"></span><dl> <span data-ttu-id="66124-150"><dt><strong>SC_RESTORE</strong></dt> <dt>0xF120</dt> </span><span class="sxs-lookup"><span data-stu-id="66124-150"><dt><strong>SC_RESTORE</strong></dt> <dt>0xF120</dt> </span></span></dl></td>
<td><span data-ttu-id="66124-151">Rétablit la position et la taille normales de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="66124-151">Restores the window to its normal position and size.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_SCREENSAVE"></span><span id="sc_screensave"></span><dl> <span data-ttu-id="66124-152"><dt><strong>SC_SCREENSAVE</strong></dt> <dt>0xF140</dt> </span><span class="sxs-lookup"><span data-stu-id="66124-152"><dt><strong>SC_SCREENSAVE</strong></dt> <dt>0xF140</dt> </span></span></dl></td>
<td><span data-ttu-id="66124-153">Exécute l’application d’écran de veille spécifiée dans la section [boot] du fichier System.ini.</span><span class="sxs-lookup"><span data-stu-id="66124-153">Executes the screen saver application specified in the [boot] section of the System.ini file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_SIZE"></span><span id="sc_size"></span><dl> <span data-ttu-id="66124-154"><dt><strong>SC_SIZE</strong></dt> <dt>0xF000</dt> </span><span class="sxs-lookup"><span data-stu-id="66124-154"><dt><strong>SC_SIZE</strong></dt> <dt>0xF000</dt> </span></span></dl></td>
<td><span data-ttu-id="66124-155">Dimensionne la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="66124-155">Sizes the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_TASKLIST"></span><span id="sc_tasklist"></span><dl> <span data-ttu-id="66124-156"><dt><strong>SC_TASKLIST</strong></dt> <dt>0xF130</dt> </span><span class="sxs-lookup"><span data-stu-id="66124-156"><dt><strong>SC_TASKLIST</strong></dt> <dt>0xF130</dt> </span></span></dl></td>
<td><span data-ttu-id="66124-157">Active le menu <strong>Démarrer</strong> .</span><span class="sxs-lookup"><span data-stu-id="66124-157">Activates the <strong>Start</strong> menu.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_VSCROLL"></span><span id="sc_vscroll"></span><dl> <span data-ttu-id="66124-158"><dt><strong>SC_VSCROLL</strong></dt> <dt>0xF070</dt> </span><span class="sxs-lookup"><span data-stu-id="66124-158"><dt><strong>SC_VSCROLL</strong></dt> <dt>0xF070</dt> </span></span></dl></td>
<td><span data-ttu-id="66124-159">Fait défiler verticalement.</span><span class="sxs-lookup"><span data-stu-id="66124-159">Scrolls vertically.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="66124-160">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66124-160">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66124-161">Le mot de poids faible spécifie la position horizontale du curseur, en coordonnées d’écran, si une commande de menu fenêtre est sélectionnée avec la souris.</span><span class="sxs-lookup"><span data-stu-id="66124-161">The low-order word specifies the horizontal position of the cursor, in screen coordinates, if a window menu command is chosen with the mouse.</span></span> <span data-ttu-id="66124-162">Dans le cas contraire, ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="66124-162">Otherwise, this parameter is not used.</span></span>

<span data-ttu-id="66124-163">Le mot de poids fort spécifie la position verticale du curseur, en coordonnées d’écran, si une commande de menu fenêtre est sélectionnée avec la souris.</span><span class="sxs-lookup"><span data-stu-id="66124-163">The high-order word specifies the vertical position of the cursor, in screen coordinates, if a window menu command is chosen with the mouse.</span></span> <span data-ttu-id="66124-164">Ce paramètre a la valeur 1 si la commande est choisie à l’aide d’un accélérateur système, ou zéro si vous utilisez un mnémonique.</span><span class="sxs-lookup"><span data-stu-id="66124-164">This parameter is  1 if the command is chosen using a system accelerator, or zero if using a mnemonic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66124-165">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="66124-165">Return value</span></span>

<span data-ttu-id="66124-166">Une application doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="66124-166">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="66124-167">Notes</span><span class="sxs-lookup"><span data-stu-id="66124-167">Remarks</span></span>

<span data-ttu-id="66124-168">Pour obtenir les coordonnées de position en coordonnées d’écran, utilisez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="66124-168">To obtain the position coordinates in screen coordinates, use the following code:</span></span>


```
xPos = GET_X_LPARAM(lParam);    // horizontal position 
yPos = GET_Y_LPARAM(lParam);    // vertical position
```



<span data-ttu-id="66124-169">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) exécute la demande du menu fenêtre pour les actions prédéfinies spécifiées dans le tableau précédent.</span><span class="sxs-lookup"><span data-stu-id="66124-169">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function carries out the window menu request for the predefined actions specified in the previous table.</span></span>

<span data-ttu-id="66124-170">Dans les messages **WM \_ SYSCOMMAND** , les quatre bits de poids faible du paramètre *wParam* sont utilisés en interne par le système.</span><span class="sxs-lookup"><span data-stu-id="66124-170">In **WM\_SYSCOMMAND** messages, the four low-order bits of the *wParam* parameter are used internally by the system.</span></span> <span data-ttu-id="66124-171">Pour obtenir le résultat correct lors du test de la valeur de *wParam*, une application doit combiner la valeur 0xFFF0 avec la valeur *wParam* à l’aide de l’opérateur de bits and.</span><span class="sxs-lookup"><span data-stu-id="66124-171">To obtain the correct result when testing the value of *wParam*, an application must combine the value 0xFFF0 with the *wParam* value by using the bitwise AND operator.</span></span>

<span data-ttu-id="66124-172">Les éléments de menu d’un menu fenêtre peuvent être modifiés à l’aide des fonctions [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu), [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)et [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="66124-172">The menu items in a window menu can be modified by using the [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu), [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema), and [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) functions.</span></span> <span data-ttu-id="66124-173">Les applications qui modifient le menu fenêtre doivent traiter les messages **WM \_ SYSCOMMAND** .</span><span class="sxs-lookup"><span data-stu-id="66124-173">Applications that modify the window menu must process **WM\_SYSCOMMAND** messages.</span></span>

<span data-ttu-id="66124-174">Une application peut exécuter n’importe quelle commande système à tout moment en transmettant un message **WM \_ SYSCOMMAND** à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="66124-174">An application can carry out any system command at any time by passing a **WM\_SYSCOMMAND** message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="66124-175">Tous les messages **WM \_ SYSCOMMAND** non gérés par l’application doivent être passés à **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="66124-175">Any **WM\_SYSCOMMAND** messages not handled by the application must be passed to **DefWindowProc**.</span></span> <span data-ttu-id="66124-176">Toutes les valeurs de commande ajoutées par une application doivent être traitées par l’application et ne peuvent pas être passées à **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="66124-176">Any command values added by an application must be processed by the application and cannot be passed to **DefWindowProc**.</span></span>

<span data-ttu-id="66124-177">Si la protection par mot de passe est activée par la stratégie, l’économiseur d’écran est démarré indépendamment de ce qu’une application utilise avec la notification **SC \_ SCREENSAVE** même si ne parvient pas à la passer à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="66124-177">If password protection is enabled by policy, the screen saver is started regardless of what an application does with the **SC\_SCREENSAVE** notification even if fails to pass it to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="66124-178">Les touches d’accès rapide définies pour choisir des éléments dans le menu fenêtre sont traduites en messages **WM \_ SYSCOMMAND** ; toutes les autres séquences de touches d’accélérateur sont traduites en messages de [**\_ commande WM**](wm-command.md) .</span><span class="sxs-lookup"><span data-stu-id="66124-178">Accelerator keys that are defined to choose items from the window menu are translated into **WM\_SYSCOMMAND** messages; all other accelerator keystrokes are translated into [**WM\_COMMAND**](wm-command.md) messages.</span></span>

<span data-ttu-id="66124-179">Si le *wParam* est **le \_ keymenu SC**, *lParam* contient le code de caractère de la clé utilisée avec la touche Alt pour afficher le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="66124-179">If the *wParam* is **SC\_KEYMENU**, *lParam* contains the character code of the key that is used with the ALT key to display the popup menu.</span></span> <span data-ttu-id="66124-180">Par exemple, si vous appuyez sur ALT + F pour afficher la fenêtre contextuelle du fichier, un **\_ SYSCOMMAND WM** avec *wParam* égal à **SC \_ keymenu** et *lParam* est égal à’F'.</span><span class="sxs-lookup"><span data-stu-id="66124-180">For example, pressing ALT+F to display the File popup will cause a **WM\_SYSCOMMAND** with *wParam* equal to **SC\_KEYMENU** and *lParam* equal to 'f'.</span></span>

## <a name="requirements"></a><span data-ttu-id="66124-181">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66124-181">Requirements</span></span>



| <span data-ttu-id="66124-182">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66124-182">Requirement</span></span> | <span data-ttu-id="66124-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="66124-183">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66124-184">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66124-184">Minimum supported client</span></span><br/> | <span data-ttu-id="66124-185">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66124-185">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="66124-186">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66124-186">Minimum supported server</span></span><br/> | <span data-ttu-id="66124-187">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66124-187">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="66124-188">En-tête</span><span class="sxs-lookup"><span data-stu-id="66124-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="66124-189"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66124-189"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66124-190">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66124-190">See also</span></span>

<dl> <dt>

<span data-ttu-id="66124-191">**Référence**</span><span class="sxs-lookup"><span data-stu-id="66124-191">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="66124-192">**AppendMenu**</span><span class="sxs-lookup"><span data-stu-id="66124-192">**AppendMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-appendmenua)
</dt> <dt>

[<span data-ttu-id="66124-193">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="66124-193">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="66124-194">**Obtient \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="66124-194">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="66124-195">**Obtient \_ le \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="66124-195">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="66124-196">**GetSystemMenu**</span><span class="sxs-lookup"><span data-stu-id="66124-196">**GetSystemMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)
</dt> <dt>

[<span data-ttu-id="66124-197">**InsertMenu**</span><span class="sxs-lookup"><span data-stu-id="66124-197">**InsertMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-insertmenua)
</dt> <dt>

[<span data-ttu-id="66124-198">**ModifyMenu**</span><span class="sxs-lookup"><span data-stu-id="66124-198">**ModifyMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-modifymenua)
</dt> <dt>

[<span data-ttu-id="66124-199">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="66124-199">**WM\_COMMAND**</span></span>](wm-command.md)
</dt> <dt>

<span data-ttu-id="66124-200">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="66124-200">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="66124-201">Raccourcis clavier</span><span class="sxs-lookup"><span data-stu-id="66124-201">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

