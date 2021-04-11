---
title: Message EM_SETEXTENDEDSTYLE (commctrl. h)
description: Informe le contrôle d’édition de la définition de styles étendus. Envoyez ce message ou utilisez la macro Edit \_ SetExtendedStyle.
ms.assetid: 4ca010c3-2c70-41e5-ade4-11e1895fda26
keywords:
- EM_SETEXTENDEDSTYLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 560b675927b4497810b8d492fd89b5765aa5a2c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105571"
---
# <a name="em_setextendedstyle-message"></a><span data-ttu-id="0d548-105">\_Message SETEXTENDEDSTYLE em</span><span class="sxs-lookup"><span data-stu-id="0d548-105">EM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="0d548-106">Informe le contrôle d’édition de la définition de styles étendus.</span><span class="sxs-lookup"><span data-stu-id="0d548-106">Informs the edit control to set extended styles.</span></span> <span data-ttu-id="0d548-107">Envoyez ce message ou utilisez la macro [**Edit \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setextendedstyle).</span><span class="sxs-lookup"><span data-stu-id="0d548-107">Send this message or use the macro [**Edit\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setextendedstyle).</span></span>

## <a name="parameters"></a><span data-ttu-id="0d548-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d548-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d548-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d548-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d548-110">Masque utilisé pour sélectionner les styles à définir.</span><span class="sxs-lookup"><span data-stu-id="0d548-110">Mask used to select the styles to be set.</span></span>

</dd> <dt>

<span data-ttu-id="0d548-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d548-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d548-112">Valeur qui indique le style étendu.</span><span class="sxs-lookup"><span data-stu-id="0d548-112">Value that indicates the extended style.</span></span> <span data-ttu-id="0d548-113">Pour plus d’informations sur les styles, consultez [modifier les styles étendus de contrôle](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="0d548-113">For more information on styles, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d548-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0d548-114">Return value</span></span>

<span data-ttu-id="0d548-115">Si ce message est correctement exécuté, il renvoie la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0d548-115">If this message succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0d548-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0d548-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d548-117">Notes</span><span class="sxs-lookup"><span data-stu-id="0d548-117">Remarks</span></span>

<span data-ttu-id="0d548-118">Les styles étendus pour un contrôle d’édition n’ont rien à faire avec les styles étendus utilisés avec la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span><span class="sxs-lookup"><span data-stu-id="0d548-118">The extended styles for an edit control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d548-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d548-119">Requirements</span></span>



| <span data-ttu-id="0d548-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d548-120">Requirement</span></span> | <span data-ttu-id="0d548-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d548-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d548-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d548-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0d548-123">Applications de bureau Windows 10, version 1809 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d548-123">Windows 10, version 1809 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0d548-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d548-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0d548-125">Applications de bureau Windows Server 2019 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d548-125">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0d548-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d548-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d548-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d548-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

