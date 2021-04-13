---
title: Message RB_BEGINDRAG (commctrl. h)
description: Place le contrôle rebar en mode glisser-déplacer. Ce message n’entraîne pas l' \_ envoi d’une notification BEGINDRAG RBN.
ms.assetid: 1e3e4928-cb84-4fd4-8056-84de1f791d1c
keywords:
- RB_BEGINDRAG les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41865baa2bf6c640595296be9c157201d0cc16d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466090"
---
# <a name="rb_begindrag-message"></a><span data-ttu-id="313c1-105">\_Message BEGINDRAG RB</span><span class="sxs-lookup"><span data-stu-id="313c1-105">RB\_BEGINDRAG message</span></span>

<span data-ttu-id="313c1-106">Place le contrôle rebar en mode glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="313c1-106">Puts the rebar control in drag-and-drop mode.</span></span> <span data-ttu-id="313c1-107">Ce message n’entraîne pas l’envoi d’une notification [ \_ BEGINDRAG RBN](rbn-begindrag.md) .</span><span class="sxs-lookup"><span data-stu-id="313c1-107">This message does not cause a [RBN\_BEGINDRAG](rbn-begindrag.md) notification to be sent.</span></span>

## <a name="parameters"></a><span data-ttu-id="313c1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="313c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="313c1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="313c1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="313c1-110">Index de base zéro de la bande affecté par l’opération de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="313c1-110">Zero-based index of the band that the drag-and-drop operation will affect.</span></span>

</dd> <dt>

<span data-ttu-id="313c1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="313c1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="313c1-112">Valeur **DWORD** qui contient les coordonnées de début de la souris.</span><span class="sxs-lookup"><span data-stu-id="313c1-112">**DWORD** value that contains the starting mouse coordinates.</span></span> <span data-ttu-id="313c1-113">La coordonnée horizontale est contenue dans le LOWORD et la coordonnée verticale est contenue dans le HIWORD.</span><span class="sxs-lookup"><span data-stu-id="313c1-113">The horizontal coordinate is contained in the LOWORD and the vertical coordinate is contained in the HIWORD.</span></span> <span data-ttu-id="313c1-114">Si vous transmettez (**DWORD**)-1, le contrôle rebar utilise la position de la souris la dernière fois que le thread du contrôle a appelé [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea).</span><span class="sxs-lookup"><span data-stu-id="313c1-114">If you pass (**DWORD**)-1, the rebar control will use the position of the mouse the last time the control's thread called [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="313c1-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="313c1-115">Return value</span></span>

<span data-ttu-id="313c1-116">La valeur de retour de ce message n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="313c1-116">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="313c1-117">Notes</span><span class="sxs-lookup"><span data-stu-id="313c1-117">Remarks</span></span>

<span data-ttu-id="313c1-118">Les **messages \_ RB BEGINDRAG**, [**RB \_ DRAGMOVE**](rb-dragmove.md)et [**RB \_ ENDDRAG**](rb-enddrag.md) vous permettent d’implémenter une interface [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) pour un contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="313c1-118">The **RB\_BEGINDRAG**, [**RB\_DRAGMOVE**](rb-dragmove.md), and [**RB\_ENDDRAG**](rb-enddrag.md) messages allow you to implement an [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) interface for a rebar control.</span></span> <span data-ttu-id="313c1-119">Vous envoyez le **message \_ RB BEGINDRAG** en réponse à [**IDropTarget ::D ragenter**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter), envoyez le message **RB \_ DRAGMOVE** en réponse à [**IDropTarget ::D Ragover**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover)et au message **RB \_ ENDDRAG** en réponse à [**IDropTarget ::D ROP**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop) et [**IDropTarget ::D ragleave**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave).</span><span class="sxs-lookup"><span data-stu-id="313c1-119">You send the **RB\_BEGINDRAG** message in response to [**IDropTarget::DragEnter**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter), send the **RB\_DRAGMOVE** message in response to [**IDropTarget::DragOver**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover), and the **RB\_ENDDRAG** message in response to [**IDropTarget::Drop**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop) and [**IDropTarget::DragLeave**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave).</span></span>

## <a name="requirements"></a><span data-ttu-id="313c1-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="313c1-120">Requirements</span></span>



| <span data-ttu-id="313c1-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="313c1-121">Requirement</span></span> | <span data-ttu-id="313c1-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="313c1-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="313c1-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="313c1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="313c1-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="313c1-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="313c1-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="313c1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="313c1-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="313c1-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="313c1-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="313c1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="313c1-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="313c1-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

