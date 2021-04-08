---
title: Message TB_SETPARENT (commctrl. h)
description: Définit la fenêtre à laquelle le contrôle de barre d’outils envoie des messages de notification.
ms.assetid: 4863bd9f-021b-4295-9483-459fc19325d9
keywords:
- TB_SETPARENT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETPARENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8137406c8e6854f86ed81d8d6b96293074ae67b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844194"
---
# <a name="tb_setparent-message"></a><span data-ttu-id="6b054-104">TO \_ SetParent, message</span><span class="sxs-lookup"><span data-stu-id="6b054-104">TB\_SETPARENT message</span></span>

<span data-ttu-id="6b054-105">Définit la fenêtre à laquelle le contrôle de barre d’outils envoie des messages de notification.</span><span class="sxs-lookup"><span data-stu-id="6b054-105">Sets the window to which the toolbar control sends notification messages.</span></span>

## <a name="parameters"></a><span data-ttu-id="6b054-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6b054-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b054-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b054-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b054-108">Handle de la fenêtre pour recevoir des messages de notification.</span><span class="sxs-lookup"><span data-stu-id="6b054-108">Handle to the window to receive notification messages.</span></span>

</dd> <dt>

<span data-ttu-id="6b054-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b054-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6b054-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="6b054-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b054-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6b054-111">Return value</span></span>

<span data-ttu-id="6b054-112">La valeur de retour est un handle vers la fenêtre de notification précédente, ou **null** s’il n’existe aucune fenêtre de notification précédente.</span><span class="sxs-lookup"><span data-stu-id="6b054-112">The return value is a handle to the previous notification window, or **NULL** if there is no previous notification window.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b054-113">Notes</span><span class="sxs-lookup"><span data-stu-id="6b054-113">Remarks</span></span>

<span data-ttu-id="6b054-114">Le message **to \_ SetParent,** ne modifie pas la fenêtre parente qui a été spécifiée lors de la création du contrôle.</span><span class="sxs-lookup"><span data-stu-id="6b054-114">The **TB\_SETPARENT** message does not change the parent window that was specified when the control was created.</span></span> <span data-ttu-id="6b054-115">L’appel de la fonction [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) pour un contrôle ToolBar retourne la fenêtre parente réelle, et non la fenêtre spécifiée dans **to \_ SetParent,**.</span><span class="sxs-lookup"><span data-stu-id="6b054-115">Calling the [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) function for a toolbar control will return the actual parent window, not the window specified in **TB\_SETPARENT**.</span></span> <span data-ttu-id="6b054-116">Pour modifier la fenêtre parente du contrôle, appelez la fonction [**SetParent,**](/windows/desktop/api/winuser/nf-winuser-setparent) .</span><span class="sxs-lookup"><span data-stu-id="6b054-116">To change the control's parent window, call the [**SetParent**](/windows/desktop/api/winuser/nf-winuser-setparent) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b054-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b054-117">Requirements</span></span>



| <span data-ttu-id="6b054-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b054-118">Requirement</span></span> | <span data-ttu-id="6b054-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b054-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b054-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b054-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6b054-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b054-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6b054-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b054-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6b054-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b054-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b054-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="6b054-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b054-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b054-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

