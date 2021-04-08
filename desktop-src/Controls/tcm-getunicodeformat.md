---
title: Message TCM_GETUNICODEFORMAT (commctrl. h)
description: Récupère l’indicateur de format de caractère Unicode pour le contrôle. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro TabCtrl GetUnicodeFormat.
ms.assetid: 720e0325-500b-436c-8713-38ed780735bf
keywords:
- TCM_GETUNICODEFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b497f1b2c2b5ac55ee949b498602b50b267fef3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844174"
---
# <a name="tcm_getunicodeformat-message"></a><span data-ttu-id="45575-105">\_Message GETUNICODEFORMAT TCM</span><span class="sxs-lookup"><span data-stu-id="45575-105">TCM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="45575-106">Récupère l’indicateur de format de caractère Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="45575-106">Retrieves the Unicode character format flag for the control.</span></span> <span data-ttu-id="45575-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**TabCtrl \_ GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="45575-107">You can send this message explicitly or use the [**TabCtrl\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="45575-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="45575-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45575-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="45575-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="45575-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="45575-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="45575-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="45575-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="45575-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="45575-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45575-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="45575-113">Return value</span></span>

<span data-ttu-id="45575-114">Retourne l’indicateur de format Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="45575-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="45575-115">Si cette valeur est différente de zéro, le contrôle utilise des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="45575-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="45575-116">Si cette valeur est égale à zéro, le contrôle utilise des caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="45575-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="45575-117">Notes</span><span class="sxs-lookup"><span data-stu-id="45575-117">Remarks</span></span>

<span data-ttu-id="45575-118">Pour plus d’informations sur ce message, consultez les notes relatives à [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="45575-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="45575-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45575-119">Requirements</span></span>



| <span data-ttu-id="45575-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45575-120">Requirement</span></span> | <span data-ttu-id="45575-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="45575-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="45575-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45575-122">Minimum supported client</span></span><br/> | <span data-ttu-id="45575-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="45575-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="45575-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45575-124">Minimum supported server</span></span><br/> | <span data-ttu-id="45575-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="45575-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="45575-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="45575-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="45575-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="45575-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45575-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45575-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45575-129">**\_SETUNICODEFORMAT TCM**</span><span class="sxs-lookup"><span data-stu-id="45575-129">**TCM\_SETUNICODEFORMAT**</span></span>](tcm-setunicodeformat.md)
</dt> </dl>

 

 





