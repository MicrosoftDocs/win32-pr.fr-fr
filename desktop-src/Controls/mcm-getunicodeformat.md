---
title: Message MCM_GETUNICODEFORMAT (commctrl. h)
description: Récupère l’indicateur de format de caractère Unicode pour le contrôle. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro calendrier monthcal GetUnicodeFormat.
ms.assetid: 28261e11-0fd0-407e-9f62-446536d62460
keywords:
- MCM_GETUNICODEFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4be573923f154958e1defd0be2adb02068076950
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743573"
---
# <a name="mcm_getunicodeformat-message"></a><span data-ttu-id="b4f91-105">\_Message GETUNICODEFORMAT MCM</span><span class="sxs-lookup"><span data-stu-id="b4f91-105">MCM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="b4f91-106">Récupère l’indicateur de format de caractère Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="b4f91-106">Retrieves the Unicode character format flag for the control.</span></span> <span data-ttu-id="b4f91-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**calendrier monthcal \_ GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="b4f91-107">You can send this message explicitly or use the [**MonthCal\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b4f91-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4f91-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4f91-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b4f91-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b4f91-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="b4f91-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b4f91-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b4f91-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b4f91-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="b4f91-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4f91-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b4f91-113">Return value</span></span>

<span data-ttu-id="b4f91-114">Retourne l’indicateur de format Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="b4f91-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="b4f91-115">Si cette valeur est différente de zéro, le contrôle utilise des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="b4f91-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="b4f91-116">Si cette valeur est égale à zéro, le contrôle utilise des caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="b4f91-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4f91-117">Notes</span><span class="sxs-lookup"><span data-stu-id="b4f91-117">Remarks</span></span>

<span data-ttu-id="b4f91-118">Pour plus d’informations sur ce message, consultez les notes relatives à [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="b4f91-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4f91-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4f91-119">Requirements</span></span>



| <span data-ttu-id="b4f91-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4f91-120">Requirement</span></span> | <span data-ttu-id="b4f91-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4f91-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f91-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4f91-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b4f91-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4f91-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b4f91-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4f91-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b4f91-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4f91-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b4f91-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4f91-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4f91-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4f91-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4f91-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4f91-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4f91-129">**MCM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="b4f91-129">**MCM\_SETUNICODEFORMAT**</span></span>](mcm-setunicodeformat.md)
</dt> </dl>

 

 





