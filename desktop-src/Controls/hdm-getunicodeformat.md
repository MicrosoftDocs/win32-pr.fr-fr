---
title: Message HDM_GETUNICODEFORMAT (commctrl. h)
description: Obtient l’indicateur de format de caractère Unicode pour le contrôle. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ GetUnicodeFormat.
ms.assetid: 2b36265a-023c-4083-a755-769461f3804b
keywords:
- HDM_GETUNICODEFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce625cc9d4c0ede0c4ce9b54dc852025b22d4870
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103768"
---
# <a name="hdm_getunicodeformat-message"></a><span data-ttu-id="4c9e3-105">\_Message HDM GETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="4c9e3-105">HDM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="4c9e3-106">Obtient l’indicateur de format de caractère Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="4c9e3-106">Gets the Unicode character format flag for the control.</span></span> <span data-ttu-id="4c9e3-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro d' [**en-tête \_ GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-header_getunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="4c9e3-107">You can send this message explicitly or use the [**Header\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-header_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4c9e3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c9e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c9e3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4c9e3-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4c9e3-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="4c9e3-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4c9e3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4c9e3-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4c9e3-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="4c9e3-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c9e3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4c9e3-113">Return value</span></span>

<span data-ttu-id="4c9e3-114">Retourne l’indicateur de format Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="4c9e3-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="4c9e3-115">Si cette valeur est différente de zéro, le contrôle utilise des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="4c9e3-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="4c9e3-116">Si cette valeur est égale à zéro, le contrôle utilise des caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="4c9e3-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c9e3-117">Notes</span><span class="sxs-lookup"><span data-stu-id="4c9e3-117">Remarks</span></span>

<span data-ttu-id="4c9e3-118">Pour plus d’informations sur ce message, consultez les notes relatives à [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="4c9e3-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c9e3-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c9e3-119">Requirements</span></span>



| <span data-ttu-id="4c9e3-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c9e3-120">Requirement</span></span> | <span data-ttu-id="4c9e3-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c9e3-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c9e3-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c9e3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4c9e3-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c9e3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4c9e3-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c9e3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4c9e3-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c9e3-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4c9e3-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="4c9e3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c9e3-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c9e3-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c9e3-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c9e3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c9e3-129">**HDM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="4c9e3-129">**HDM\_SETUNICODEFORMAT**</span></span>](hdm-setunicodeformat.md)
</dt> </dl>

 

 





