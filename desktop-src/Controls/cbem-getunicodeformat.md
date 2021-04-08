---
title: Message CBEM_GETUNICODEFORMAT (commctrl. h)
description: Obtient l’indicateur de format de caractère UNICODE pour le contrôle.
ms.assetid: 854ff8d5-6e2f-4918-a6c5-91356a4454af
keywords:
- CBEM_GETUNICODEFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- CBEM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b77bb0daabe6ef14d4be1b5e2de6bb1dd63248d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844350"
---
# <a name="cbem_getunicodeformat-message"></a><span data-ttu-id="3da58-104">\_Message CBEM GETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="3da58-104">CBEM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="3da58-105">Obtient l’indicateur de format de caractère UNICODE pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="3da58-105">Gets the UNICODE character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3da58-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3da58-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3da58-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3da58-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3da58-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="3da58-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3da58-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3da58-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3da58-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="3da58-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3da58-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3da58-111">Return value</span></span>

<span data-ttu-id="3da58-112">Retourne l’indicateur de format Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="3da58-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="3da58-113">Si cette valeur est différente de zéro, le contrôle utilise des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="3da58-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="3da58-114">Si cette valeur est égale à zéro, le contrôle utilise des caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="3da58-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="3da58-115">Notes</span><span class="sxs-lookup"><span data-stu-id="3da58-115">Remarks</span></span>

<span data-ttu-id="3da58-116">Pour plus d’informations sur ce message, consultez les notes relatives à [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="3da58-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3da58-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3da58-117">Requirements</span></span>



| <span data-ttu-id="3da58-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3da58-118">Requirement</span></span> | <span data-ttu-id="3da58-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="3da58-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3da58-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3da58-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3da58-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3da58-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3da58-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3da58-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3da58-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3da58-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3da58-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="3da58-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3da58-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3da58-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3da58-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3da58-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3da58-127">**CBEM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="3da58-127">**CBEM\_SETUNICODEFORMAT**</span></span>](cbem-setunicodeformat.md)
</dt> </dl>

 

 





