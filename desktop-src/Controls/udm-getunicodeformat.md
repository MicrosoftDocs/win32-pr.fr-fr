---
title: Message UDM_GETUNICODEFORMAT (commctrl. h)
description: Récupère l’indicateur de format de caractère Unicode pour le contrôle.
ms.assetid: 8c09d37b-95a2-49cd-b578-919f9c39fa8b
keywords:
- UDM_GETUNICODEFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- UDM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2f9eef604af6cf5dfcefbf1e3e03dec561ac21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942872"
---
# <a name="udm_getunicodeformat-message"></a><span data-ttu-id="dc5e3-104">\_Message GETUNICODEFORMAT UDM</span><span class="sxs-lookup"><span data-stu-id="dc5e3-104">UDM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="dc5e3-105">Récupère l’indicateur de format de caractère Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="dc5e3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc5e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc5e3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dc5e3-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="dc5e3-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="dc5e3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dc5e3-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="dc5e3-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc5e3-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dc5e3-111">Return value</span></span>

<span data-ttu-id="dc5e3-112">Retourne l’indicateur de format Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="dc5e3-113">Si cette valeur est différente de zéro, le contrôle utilise des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="dc5e3-114">Si cette valeur est égale à zéro, le contrôle utilise des caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc5e3-115">Notes</span><span class="sxs-lookup"><span data-stu-id="dc5e3-115">Remarks</span></span>

<span data-ttu-id="dc5e3-116">Pour plus d’informations sur ce message, consultez les notes relatives à [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="dc5e3-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc5e3-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc5e3-117">Requirements</span></span>



| <span data-ttu-id="dc5e3-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc5e3-118">Requirement</span></span> | <span data-ttu-id="dc5e3-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc5e3-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc5e3-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc5e3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dc5e3-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc5e3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dc5e3-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc5e3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dc5e3-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc5e3-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dc5e3-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc5e3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc5e3-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc5e3-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc5e3-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc5e3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc5e3-127">**\_SETUNICODEFORMAT UDM**</span><span class="sxs-lookup"><span data-stu-id="dc5e3-127">**UDM\_SETUNICODEFORMAT**</span></span>](udm-setunicodeformat.md)
</dt> </dl>

 

 





