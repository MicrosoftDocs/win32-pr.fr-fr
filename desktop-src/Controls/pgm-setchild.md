---
title: Message PGM_SETCHILD (commctrl. h)
description: Définit la fenêtre contenue pour le contrôle de pagineur.
ms.assetid: 717e6720-aa42-4ecd-9520-4618a04dc28d
keywords:
- PGM_SETCHILD les contrôles de message Windows
topic_type:
- apiref
api_name:
- PGM_SETCHILD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c934c3c5688ac79b5c5ce67aef68e28ad3627ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103476"
---
# <a name="pgm_setchild-message"></a><span data-ttu-id="9c8f9-104">\_Message SETCHILD PGM</span><span class="sxs-lookup"><span data-stu-id="9c8f9-104">PGM\_SETCHILD message</span></span>

<span data-ttu-id="9c8f9-105">Définit la fenêtre contenue pour le contrôle de pagineur.</span><span class="sxs-lookup"><span data-stu-id="9c8f9-105">Sets the contained window for the pager control.</span></span> <span data-ttu-id="9c8f9-106">Ce message ne change pas le parent de la fenêtre contenue. Il assigne uniquement un handle de fenêtre au contrôle de pagineur pour le défilement.</span><span class="sxs-lookup"><span data-stu-id="9c8f9-106">This message will not change the parent of the contained window; it only assigns a window handle to the pager control for scrolling.</span></span> <span data-ttu-id="9c8f9-107">Dans la plupart des cas, la fenêtre contenue est une fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="9c8f9-107">In most cases, the contained window will be a child window.</span></span> <span data-ttu-id="9c8f9-108">Si c’est le cas, la fenêtre contenue doit être un enfant du contrôle pager.</span><span class="sxs-lookup"><span data-stu-id="9c8f9-108">If this is the case, the contained window should be a child of the pager control.</span></span> <span data-ttu-id="9c8f9-109">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ SetChild**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) .</span><span class="sxs-lookup"><span data-stu-id="9c8f9-109">You can send this message explicitly or use the [**Pager\_SetChild**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9c8f9-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c8f9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c8f9-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c8f9-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9c8f9-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="9c8f9-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9c8f9-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c8f9-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c8f9-114">Handle de la fenêtre à contenu.</span><span class="sxs-lookup"><span data-stu-id="9c8f9-114">Handle to the window to be contained.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c8f9-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9c8f9-115">Return value</span></span>

<span data-ttu-id="9c8f9-116">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="9c8f9-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c8f9-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c8f9-117">Requirements</span></span>



| <span data-ttu-id="9c8f9-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c8f9-118">Requirement</span></span> | <span data-ttu-id="9c8f9-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c8f9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c8f9-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c8f9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9c8f9-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c8f9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9c8f9-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c8f9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9c8f9-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c8f9-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9c8f9-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="9c8f9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c8f9-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c8f9-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





