---
title: Message LVM_GETUNICODEFORMAT (commctrl. h)
description: Récupère l’indicateur de format de caractère UNICODE pour le contrôle. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView GetUnicodeFormat.
ms.assetid: b0598b60-4d0e-4c68-b63a-e614c6268129
keywords:
- LVM_GETUNICODEFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 720a65baab8ec9c1ec3b311e49fe3672c97a0fba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844089"
---
# <a name="lvm_getunicodeformat-message"></a><span data-ttu-id="36b0f-105">\_Message GETUNICODEFORMAT LVM</span><span class="sxs-lookup"><span data-stu-id="36b0f-105">LVM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="36b0f-106">Récupère l’indicateur de format de caractère UNICODE pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="36b0f-106">Retrieves the UNICODE character format flag for the control.</span></span> <span data-ttu-id="36b0f-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="36b0f-107">You can send this message explicitly or use the [**ListView\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="36b0f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36b0f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36b0f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36b0f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="36b0f-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="36b0f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="36b0f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36b0f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="36b0f-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="36b0f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36b0f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="36b0f-113">Return value</span></span>

<span data-ttu-id="36b0f-114">Retourne l’indicateur de format Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="36b0f-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="36b0f-115">Si cette valeur est différente de zéro, le contrôle utilise des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="36b0f-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="36b0f-116">Si cette valeur est égale à zéro, le contrôle utilise des caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="36b0f-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="36b0f-117">Notes</span><span class="sxs-lookup"><span data-stu-id="36b0f-117">Remarks</span></span>

<span data-ttu-id="36b0f-118">Pour plus d’informations sur ce message, consultez les notes relatives à [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="36b0f-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="36b0f-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36b0f-119">Requirements</span></span>



| <span data-ttu-id="36b0f-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36b0f-120">Requirement</span></span> | <span data-ttu-id="36b0f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="36b0f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="36b0f-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36b0f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="36b0f-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36b0f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="36b0f-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36b0f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="36b0f-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36b0f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="36b0f-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="36b0f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="36b0f-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="36b0f-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36b0f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36b0f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36b0f-129">**\_SETUNICODEFORMAT LVM**</span><span class="sxs-lookup"><span data-stu-id="36b0f-129">**LVM\_SETUNICODEFORMAT**</span></span>](lvm-setunicodeformat.md)
</dt> </dl>

 

 





