---
title: Message WM_NOTIFYFORMAT (winuser. h)
description: Détermine si une fenêtre accepte des structures ANSI ou Unicode dans le \_ message de notification WM Notify. Les \_ messages WM NOTIFYFORMAT sont envoyés à partir d’un contrôle commun à sa fenêtre parente et de la fenêtre parente au contrôle commun.
ms.assetid: 45ddef45-3300-448d-b609-5fe931b08336
keywords:
- WM_NOTIFYFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- WM_NOTIFYFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e9c7d74b21d0f5785273d1b60d612a346f2d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942370"
---
# <a name="wm_notifyformat-message"></a><span data-ttu-id="90c71-105">\_Message WM NOTIFYFORMAT</span><span class="sxs-lookup"><span data-stu-id="90c71-105">WM\_NOTIFYFORMAT message</span></span>

<span data-ttu-id="90c71-106">Détermine si une fenêtre accepte des structures ANSI ou Unicode dans le message de notification [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="90c71-106">Determines if a window accepts ANSI or Unicode structures in the [**WM\_NOTIFY**](wm-notify.md) notification message.</span></span> <span data-ttu-id="90c71-107">**WM \_** Les messages NOTIFYFORMAT sont envoyés à partir d’un contrôle commun à sa fenêtre parente et de la fenêtre parente au contrôle commun.</span><span class="sxs-lookup"><span data-stu-id="90c71-107">**WM\_NOTIFYFORMAT** messages are sent from a common control to its parent window and from the parent window to the common control.</span></span>

## <a name="parameters"></a><span data-ttu-id="90c71-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="90c71-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90c71-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="90c71-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90c71-110">Handle de la fenêtre qui envoie le message **WM \_ NOTIFYFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="90c71-110">A handle to the window that is sending the **WM\_NOTIFYFORMAT** message.</span></span> <span data-ttu-id="90c71-111">Si *lParam* est \_ une requête NF, ce paramètre est le handle d’un contrôle.</span><span class="sxs-lookup"><span data-stu-id="90c71-111">If *lParam* is NF\_QUERY, this parameter is the handle to a control.</span></span> <span data-ttu-id="90c71-112">Si *lParam* est NF \_ Requery, ce paramètre est le handle de la fenêtre parente d’un contrôle.</span><span class="sxs-lookup"><span data-stu-id="90c71-112">If *lParam* is NF\_REQUERY, this parameter is the handle to the parent window of a control.</span></span>

</dd> <dt>

<span data-ttu-id="90c71-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="90c71-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90c71-114">Valeur de commande qui spécifie la nature du message **WM \_ NOTIFYFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="90c71-114">The command value that specifies the nature of the **WM\_NOTIFYFORMAT** message.</span></span> <span data-ttu-id="90c71-115">Il s’agit de l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="90c71-115">This will be one of the following values:</span></span>



| <span data-ttu-id="90c71-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="90c71-116">Value</span></span>                                                                                                                                                | <span data-ttu-id="90c71-117">Signification</span><span class="sxs-lookup"><span data-stu-id="90c71-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NF_QUERY"></span><span id="nf_query"></span><dl> <span data-ttu-id="90c71-118"><dt>**\_requête NF**</dt></span><span class="sxs-lookup"><span data-stu-id="90c71-118"><dt>**NF\_QUERY**</dt></span></span> </dl>       | <span data-ttu-id="90c71-119">Le message est une requête qui détermine si les structures ANSI ou Unicode doivent être utilisées dans les messages de [**\_ notification WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="90c71-119">The message is a query to determine whether ANSI or Unicode structures should be used in [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="90c71-120">Cette commande est envoyée à partir d’un contrôle à sa fenêtre parente pendant la création d’un contrôle et en réponse à une \_ commande de REREQUÊTE NF.</span><span class="sxs-lookup"><span data-stu-id="90c71-120">This command is sent from a control to its parent window during the creation of a control and in response to an NF\_REQUERY command.</span></span><br/>                                                                                                         |
| <span id="NF_REQUERY"></span><span id="nf_requery"></span><dl> <span data-ttu-id="90c71-121"><dt>**rerequête NF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="90c71-121"><dt>**NF\_REQUERY**</dt></span></span> </dl> | <span data-ttu-id="90c71-122">Le message est une demande pour qu’un contrôle envoie un \_ formulaire de requête NF de ce message à sa fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="90c71-122">The message is a request for a control to send an NF\_QUERY form of this message to its parent window.</span></span> <span data-ttu-id="90c71-123">Cette commande est envoyée à partir de la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="90c71-123">This command is sent from the parent window.</span></span> <span data-ttu-id="90c71-124">La fenêtre parente demande au contrôle de le redemander sur le type de structures à utiliser dans les messages [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="90c71-124">The parent window is asking the control to requery it about the type of structures to use in [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="90c71-125">Si *lParam* est NF \_ Requery, la valeur de retour est le résultat de l’opération de rerequête.</span><span class="sxs-lookup"><span data-stu-id="90c71-125">If *lParam* is NF\_REQUERY, the return value is the result of the requery operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90c71-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="90c71-126">Return value</span></span>

<span data-ttu-id="90c71-127">Retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="90c71-127">Returns one of the following values.</span></span>



| <span data-ttu-id="90c71-128">Code de retour</span><span class="sxs-lookup"><span data-stu-id="90c71-128">Return code</span></span>                                                                                 | <span data-ttu-id="90c71-129">Description</span><span class="sxs-lookup"><span data-stu-id="90c71-129">Description</span></span>                                                                                                    |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="90c71-130"><dt>**\_ANSI NFR**</dt></span><span class="sxs-lookup"><span data-stu-id="90c71-130"><dt>**NFR\_ANSI**</dt></span></span> </dl>    | <span data-ttu-id="90c71-131">Les structures ANSI doivent être utilisées dans les messages de [**\_ notification WM**](wm-notify.md) envoyés par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="90c71-131">ANSI structures should be used in [**WM\_NOTIFY**](wm-notify.md) messages sent by the control.</span></span><br/>     |
| <dl> <span data-ttu-id="90c71-132"><dt>**\_Unicode NFR**</dt></span><span class="sxs-lookup"><span data-stu-id="90c71-132"><dt>**NFR\_UNICODE**</dt></span></span> </dl> | <span data-ttu-id="90c71-133">Les structures Unicode doivent être utilisées dans les messages de [**\_ notification WM**](wm-notify.md) envoyés par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="90c71-133">Unicode structures should be used in [**WM\_NOTIFY**](wm-notify.md) messages sent by the control.</span></span> <br/> |
| <dl> <span data-ttu-id="90c71-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="90c71-134"><dt>**0**</dt></span></span> </dl>            | <span data-ttu-id="90c71-135">Une erreur est survenue.</span><span class="sxs-lookup"><span data-stu-id="90c71-135">An error occurred.</span></span><br/>                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="90c71-136">Notes</span><span class="sxs-lookup"><span data-stu-id="90c71-136">Remarks</span></span>

<span data-ttu-id="90c71-137">Lorsqu’un contrôle commun est créé, le contrôle envoie un message **WM \_ NOTIFYFORMAT** à sa fenêtre parente pour déterminer le type de structures à utiliser dans les messages de [**\_ notification WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="90c71-137">When a common control is created, the control sends a **WM\_NOTIFYFORMAT** message to its parent window to determine the type of structures to use in [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="90c71-138">Si la fenêtre parente ne gère pas ce message, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) répond en fonction du type de la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="90c71-138">If the parent window does not handle this message, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function responds according to the type of the parent window.</span></span> <span data-ttu-id="90c71-139">Autrement dit, si la fenêtre parente est une fenêtre Unicode, **DefWindowProc** retourne des \_ Unicode NFR et, si la fenêtre parente est une fenêtre ANSI, **DefWindowProc** retourne NFR \_ ANSI.</span><span class="sxs-lookup"><span data-stu-id="90c71-139">That is, if the parent window is a Unicode window, **DefWindowProc** returns NFR\_UNICODE, and if the parent window is an ANSI window, **DefWindowProc** returns NFR\_ANSI.</span></span> <span data-ttu-id="90c71-140">Si la fenêtre parente est une boîte de dialogue et ne gère pas ce message, la fonction [**DefDlgProc**](/windows/desktop/api/winuser/nf-winuser-defdlgprocw) répond de la même manière en fonction du type de la boîte de dialogue (Unicode ou ANSI).</span><span class="sxs-lookup"><span data-stu-id="90c71-140">If the parent window is a dialog box and does not handle this message, the [**DefDlgProc**](/windows/desktop/api/winuser/nf-winuser-defdlgprocw) function similarly responds according to the type of the dialog box (Unicode or ANSI).</span></span>

<span data-ttu-id="90c71-141">Une fenêtre parente peut modifier le type de structures qu’un contrôle commun utilise dans les messages de [**\_ notification WM**](wm-notify.md) en affectant à *lParam* la valeur NF \_ Requery et en envoyant un message **WM \_ NOTIFYFORMAT** au contrôle.</span><span class="sxs-lookup"><span data-stu-id="90c71-141">A parent window can change the type of structures a common control uses in [**WM\_NOTIFY**](wm-notify.md) messages by setting *lParam* to NF\_REQUERY and sending a **WM\_NOTIFYFORMAT** message to the control.</span></span> <span data-ttu-id="90c71-142">Ainsi, le contrôle envoie un \_ formulaire de requête NF du message **WM \_ NOTIFYFORMAT** à la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="90c71-142">This causes the control to send an NF\_QUERY form of the **WM\_NOTIFYFORMAT** message to the parent window.</span></span>

<span data-ttu-id="90c71-143">Tous les contrôles communs vont envoyer les messages **WM \_ NOTIFYFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="90c71-143">All common controls will send **WM\_NOTIFYFORMAT** messages.</span></span> <span data-ttu-id="90c71-144">Toutefois, ce n’est pas le cas des contrôles Windows standard (contrôles d’édition, zones de liste déroulante, zones de liste, boutons, barres de défilement et contrôles statiques).</span><span class="sxs-lookup"><span data-stu-id="90c71-144">However, the standard Windows controls (edit controls, combo boxes, list boxes, buttons, scroll bars, and static controls) do not.</span></span>

## <a name="requirements"></a><span data-ttu-id="90c71-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90c71-145">Requirements</span></span>



| <span data-ttu-id="90c71-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="90c71-146">Requirement</span></span> | <span data-ttu-id="90c71-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="90c71-147">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="90c71-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90c71-148">Minimum supported client</span></span><br/> | <span data-ttu-id="90c71-149">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="90c71-149">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="90c71-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90c71-150">Minimum supported server</span></span><br/> | <span data-ttu-id="90c71-151">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="90c71-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="90c71-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="90c71-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="90c71-153"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="90c71-153"><dt>Winuser.h</dt></span></span> </dl> |



 

