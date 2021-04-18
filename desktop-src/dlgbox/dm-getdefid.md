---
title: Message DM_GETDEFID (winuser. h)
description: Récupère l’identificateur du contrôle de bouton de commande par défaut d’une boîte de dialogue.
ms.assetid: 9f00a494-f5a2-4c4e-a9fc-2220d9326eb9
keywords:
- Boîtes de dialogue de DM_GETDEFID message
topic_type:
- apiref
api_name:
- DM_GETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fdcdfc2cd278ab452d48ecb1c254bdb00ffbb7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509310"
---
# <a name="dm_getdefid-message"></a><span data-ttu-id="ba553-104">\_Message GETDEFID DM</span><span class="sxs-lookup"><span data-stu-id="ba553-104">DM\_GETDEFID message</span></span>

<span data-ttu-id="ba553-105">Récupère l’identificateur du contrôle de bouton de commande par défaut d’une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ba553-105">Retrieves the identifier of the default push button control for a dialog box.</span></span>


```C++
#define WM_USER              0x0400
#define DM_GETDEFID         (WM_USER+0)
```



## <a name="parameters"></a><span data-ttu-id="ba553-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba553-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba553-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ba553-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba553-108">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="ba553-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ba553-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ba553-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba553-110">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="ba553-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba553-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ba553-111">Return value</span></span>

<span data-ttu-id="ba553-112">Si un bouton de commande par défaut existe, le mot de poids fort de la valeur de retour contient la valeur **DC \_ HASDEFID** et le mot de poids faible contient l’identificateur de contrôle.</span><span class="sxs-lookup"><span data-stu-id="ba553-112">If a default push button exists, the high-order word of the return value contains the value **DC\_HASDEFID** and the low-order word contains the control identifier.</span></span> <span data-ttu-id="ba553-113">Sinon, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="ba553-113">Otherwise, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba553-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ba553-114">Remarks</span></span>

<span data-ttu-id="ba553-115">La fonction [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) traite ce message.</span><span class="sxs-lookup"><span data-stu-id="ba553-115">The [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) function processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba553-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba553-116">Requirements</span></span>



| <span data-ttu-id="ba553-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba553-117">Requirement</span></span> | <span data-ttu-id="ba553-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba553-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba553-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba553-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ba553-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba553-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ba553-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba553-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ba553-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba553-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ba553-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="ba553-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba553-124"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba553-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba553-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba553-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="ba553-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="ba553-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ba553-127">**DefDlgProc**</span><span class="sxs-lookup"><span data-stu-id="ba553-127">**DefDlgProc**</span></span>](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[<span data-ttu-id="ba553-128">**DM \_ SETDEFID**</span><span class="sxs-lookup"><span data-stu-id="ba553-128">**DM\_SETDEFID**</span></span>](dm-setdefid.md)
</dt> <dt>

<span data-ttu-id="ba553-129">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="ba553-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ba553-130">Boîtes de dialogue</span><span class="sxs-lookup"><span data-stu-id="ba553-130">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 

 





