---
title: Message TVM_SETEXTENDEDSTYLE (commctrl. h)
description: Informe le contrôle d’arborescence pour définir des styles étendus. Envoyez ce message ou utilisez la macro TreeView \_ SetExtendedStyle.
ms.assetid: 35cb6ac8-1c1e-4ecd-88b2-878d3f6ccaa5
keywords:
- TVM_SETEXTENDEDSTYLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c450f72f85e40514c35f08284428feec4f7caf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508694"
---
# <a name="tvm_setextendedstyle-message"></a><span data-ttu-id="d0cd0-105">TVM \_ SETEXTENDEDSTYLE message</span><span class="sxs-lookup"><span data-stu-id="d0cd0-105">TVM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="d0cd0-106">Informe le contrôle d’arborescence pour définir des styles étendus.</span><span class="sxs-lookup"><span data-stu-id="d0cd0-106">Informs the tree-view control to set extended styles.</span></span> <span data-ttu-id="d0cd0-107">Envoyez ce message ou utilisez la macro [**TreeView \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle).</span><span class="sxs-lookup"><span data-stu-id="d0cd0-107">Send this message or use the macro [**TreeView\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle).</span></span>

## <a name="parameters"></a><span data-ttu-id="d0cd0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0cd0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0cd0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d0cd0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0cd0-110">Masque utilisé pour sélectionner les styles à définir.</span><span class="sxs-lookup"><span data-stu-id="d0cd0-110">Mask used to select the styles to be set.</span></span>

</dd> <dt>

<span data-ttu-id="d0cd0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d0cd0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0cd0-112">Valeur qui indique le style étendu.</span><span class="sxs-lookup"><span data-stu-id="d0cd0-112">Value that indicates the extended style.</span></span> <span data-ttu-id="d0cd0-113">Pour plus d’informations sur les styles, consultez [styles étendus de contrôle d’arborescence](tree-view-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="d0cd0-113">For more information on styles, see [Tree-View Control Extended Styles](tree-view-control-window-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0cd0-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d0cd0-114">Return value</span></span>

<span data-ttu-id="d0cd0-115">Si ce message est correctement exécuté, il renvoie la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d0cd0-115">If this message succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d0cd0-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d0cd0-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0cd0-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d0cd0-117">Remarks</span></span>

<span data-ttu-id="d0cd0-118">Les styles étendus pour un contrôle d’arborescence n’ont rien à voir avec les styles étendus utilisés avec la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span><span class="sxs-lookup"><span data-stu-id="d0cd0-118">The extended styles for a tree-view control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0cd0-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0cd0-119">Requirements</span></span>



| <span data-ttu-id="d0cd0-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0cd0-120">Requirement</span></span> | <span data-ttu-id="d0cd0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0cd0-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0cd0-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0cd0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d0cd0-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0cd0-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d0cd0-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0cd0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d0cd0-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0cd0-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d0cd0-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="d0cd0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0cd0-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0cd0-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

