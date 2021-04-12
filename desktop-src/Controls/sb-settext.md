---
title: Message SB_SETTEXT (commctrl. h)
description: Définit le texte dans la partie spécifiée d’une fenêtre d’État.
ms.assetid: 6039a61c-6ec6-42cd-94d5-5f1cf2998586
keywords:
- SB_SETTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- SB_SETTEXT
- SB_SETTEXTA
- SB_SETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a466187b4ccd00a974b992eacec11938f45001da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105067"
---
# <a name="sb_settext-message"></a><span data-ttu-id="1ef70-104">\_Message SB SETTEXT</span><span class="sxs-lookup"><span data-stu-id="1ef70-104">SB\_SETTEXT message</span></span>

<span data-ttu-id="1ef70-105">Définit le texte dans la partie spécifiée d’une fenêtre d’État.</span><span class="sxs-lookup"><span data-stu-id="1ef70-105">Sets the text in the specified part of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="1ef70-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ef70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ef70-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ef70-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ef70-108">Le [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) du mot de poids faible spécifie l’index de base zéro du composant à définir.</span><span class="sxs-lookup"><span data-stu-id="1ef70-108">The [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) of the low-order word specifies the zero-based index of the part to set.</span></span> <span data-ttu-id="1ef70-109">Si **LOBYTE** a la valeur SB \_ SIMPLEID, la fenêtre d’État est supposée être une barre d’état de mode simple ; autrement dit, une barre d’État avec une seule partie.</span><span class="sxs-lookup"><span data-stu-id="1ef70-109">If the **LOBYTE** is set to SB\_SIMPLEID, the status window is assumed to be a simple mode status bar; that is, a status bar with only one part.</span></span>

<span data-ttu-id="1ef70-110">Le [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) du mot de poids faible spécifie le type de l’opération de dessin.</span><span class="sxs-lookup"><span data-stu-id="1ef70-110">The [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) of the low-order word specifies the type of the drawing operation.</span></span> <span data-ttu-id="1ef70-111">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1ef70-111">This parameter can be one of the following values.</span></span>

<span data-ttu-id="1ef70-112">Le mot de poids fort de *wParam* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="1ef70-112">The high-order word of *wParam* is ignored.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1ef70-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ef70-113">Value</span></span></th>
<th><span data-ttu-id="1ef70-114">Signification</span><span class="sxs-lookup"><span data-stu-id="1ef70-114">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="0"></span><dl> <span data-ttu-id="1ef70-115"><dt><strong>entre</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1ef70-115"><dt><strong>0</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="1ef70-116">Le texte est dessiné avec une bordure qui apparaît plus bas que le plan de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="1ef70-116">The text is drawn with a border to appear lower than the plane of the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOBORDERS"></span><span id="sbt_noborders"></span><dl> <span data-ttu-id="1ef70-117"><dt><strong>SBT_NOBORDERS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1ef70-117"><dt><strong>SBT_NOBORDERS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="1ef70-118">Le texte est dessiné sans bordures.</span><span class="sxs-lookup"><span data-stu-id="1ef70-118">The text is drawn without borders.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_OWNERDRAW"></span><span id="sbt_ownerdraw"></span><dl> <span data-ttu-id="1ef70-119"><dt><strong>SBT_OWNERDRAW</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1ef70-119"><dt><strong>SBT_OWNERDRAW</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="1ef70-120">Le texte est dessiné par la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="1ef70-120">The text is drawn by the parent window.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1ef70-121">Une barre d’état de mode simple ne prend pas en charge le dessin owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="1ef70-121">A simple mode status bar does not support owner drawing.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_POPOUT"></span><span id="sbt_popout"></span><dl> <span data-ttu-id="1ef70-122"><dt><strong>SBT_POPOUT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1ef70-122"><dt><strong>SBT_POPOUT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="1ef70-123">Le texte est dessiné avec une bordure qui doit apparaître plus haut que le plan de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="1ef70-123">The text is drawn with a border to appear higher than the plane of the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_RTLREADING"></span><span id="sbt_rtlreading"></span><dl> <span data-ttu-id="1ef70-124"><dt><strong>SBT_RTLREADING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1ef70-124"><dt><strong>SBT_RTLREADING</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="1ef70-125">Le texte s’affiche dans le sens inverse du texte de la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="1ef70-125">The text will be displayed in the opposite direction to the text in the parent window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOTABPARSING"></span><span id="sbt_notabparsing"></span><dl> <span data-ttu-id="1ef70-126"><dt><strong>SBT_NOTABPARSING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1ef70-126"><dt><strong>SBT_NOTABPARSING</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="1ef70-127">Les caractères de tabulation sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="1ef70-127">Tab characters are ignored.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="1ef70-128">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ef70-128">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ef70-129">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le texte à définir.</span><span class="sxs-lookup"><span data-stu-id="1ef70-129">Pointer to a null-terminated string that specifies the text to set.</span></span> <span data-ttu-id="1ef70-130">Si *wParam* est SBT \_ OwnerDraw, ce paramètre représente 32 bits de données.</span><span class="sxs-lookup"><span data-stu-id="1ef70-130">If *wParam* is SBT\_OWNERDRAW, this parameter represents 32 bits of data.</span></span> <span data-ttu-id="1ef70-131">La fenêtre parente doit interpréter les données et dessiner le texte lorsqu’il reçoit le message [**WM \_ DRAWITEM**](wm-drawitem.md) .</span><span class="sxs-lookup"><span data-stu-id="1ef70-131">The parent window must interpret the data and draw the text when it receives the [**WM\_DRAWITEM**](wm-drawitem.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ef70-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1ef70-132">Return value</span></span>

<span data-ttu-id="1ef70-133">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="1ef70-133">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ef70-134">Notes</span><span class="sxs-lookup"><span data-stu-id="1ef70-134">Remarks</span></span>

<span data-ttu-id="1ef70-135">Le message invalide la partie de la fenêtre qui a changé, provoquant l’affichage du nouveau texte lorsque la fenêtre reçoit le message de [**\_ peinture WM**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="1ef70-135">The message invalidates the portion of the window that has changed, causing it to display the new text when the window next receives the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span>

<span data-ttu-id="1ef70-136">Les fenêtres normales affichent le texte de gauche à droite (LTR).</span><span class="sxs-lookup"><span data-stu-id="1ef70-136">Normal windows display text left-to-right (LTR).</span></span> <span data-ttu-id="1ef70-137">Les fenêtres peuvent être *mises en miroir* pour afficher des langues telles que l’hébreu ou l’arabe, qui sont lues de droite à gauche (RTL).</span><span class="sxs-lookup"><span data-stu-id="1ef70-137">Windows can be *mirrored* to display languages such as Hebrew or Arabic that read right-to-left (RTL).</span></span> <span data-ttu-id="1ef70-138">Si SBT \_ RTLREADING est défini, la chaîne *lParam* lira dans le sens inverse du texte de la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="1ef70-138">If SBT\_RTLREADING is set, the *lParam* string will read in the opposite direction from the text in the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ef70-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ef70-139">Requirements</span></span>



| <span data-ttu-id="1ef70-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ef70-140">Requirement</span></span> | <span data-ttu-id="1ef70-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ef70-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ef70-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ef70-142">Minimum supported client</span></span><br/> | <span data-ttu-id="1ef70-143">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1ef70-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ef70-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ef70-144">Minimum supported server</span></span><br/> | <span data-ttu-id="1ef70-145">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1ef70-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ef70-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="1ef70-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ef70-147"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ef70-147"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="1ef70-148">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="1ef70-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1ef70-149">**SB \_ SETTEXTW** (Unicode) et **SB \_ SETTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1ef70-149">**SB\_SETTEXTW** (Unicode) and **SB\_SETTEXTA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="1ef70-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ef70-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ef70-151">**SB \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="1ef70-151">**SB\_GETTEXT**</span></span>](sb-gettext.md)
</dt> </dl>

 

