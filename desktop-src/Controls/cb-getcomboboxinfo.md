---
title: Message CB_GETCOMBOBOXINFO (winuser. h)
description: Obtient des informations sur la zone de liste déroulante spécifiée.
ms.assetid: 3239dfa8-7301-48e3-ba8e-29c5d5f43b39
keywords:
- CB_GETCOMBOBOXINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_GETCOMBOBOXINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd7052ef4feca8a8704258c7c34d6516c7cd6cd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464435"
---
# <a name="cb_getcomboboxinfo-message"></a><span data-ttu-id="884cd-104">\_Message GETCOMBOBOXINFO CB</span><span class="sxs-lookup"><span data-stu-id="884cd-104">CB\_GETCOMBOBOXINFO message</span></span>

<span data-ttu-id="884cd-105">Obtient des informations sur la zone de liste déroulante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="884cd-105">Gets information about the specified combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="884cd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="884cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="884cd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="884cd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="884cd-108">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="884cd-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="884cd-109">*lParam* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="884cd-109">*lParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="884cd-110">Pointeur vers une structure [**COMBOBOXINFO**](/windows/win32/api/winuser/ns-winuser-comboboxinfo) qui reçoit les informations.</span><span class="sxs-lookup"><span data-stu-id="884cd-110">A pointer to a [**COMBOBOXINFO**](/windows/win32/api/winuser/ns-winuser-comboboxinfo) structure that receives the information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="884cd-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="884cd-111">Return value</span></span>

<span data-ttu-id="884cd-112">Si la fonction réussit, la valeur de retour est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="884cd-112">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="884cd-113">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="884cd-113">If the function fails, the return value is zero.</span></span> <span data-ttu-id="884cd-114">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="884cd-114">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="884cd-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="884cd-115">Remarks</span></span>

<span data-ttu-id="884cd-116">Ce message est équivalent à [**GetComboBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo).</span><span class="sxs-lookup"><span data-stu-id="884cd-116">This message is equivalent to [**GetComboBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo).</span></span>

## <a name="requirements"></a><span data-ttu-id="884cd-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="884cd-117">Requirements</span></span>



| <span data-ttu-id="884cd-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="884cd-118">Requirement</span></span> | <span data-ttu-id="884cd-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="884cd-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="884cd-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="884cd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="884cd-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="884cd-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="884cd-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="884cd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="884cd-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="884cd-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="884cd-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="884cd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="884cd-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="884cd-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="884cd-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="884cd-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="884cd-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="884cd-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="884cd-128">**COMBOBOXINFO**</span><span class="sxs-lookup"><span data-stu-id="884cd-128">**COMBOBOXINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-comboboxinfo)
</dt> <dt>

[<span data-ttu-id="884cd-129">**GetComboBoxInfo**</span><span class="sxs-lookup"><span data-stu-id="884cd-129">**GetComboBoxInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo)
</dt> </dl>

 

