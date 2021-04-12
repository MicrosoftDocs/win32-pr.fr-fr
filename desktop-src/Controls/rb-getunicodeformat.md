---
title: Message RB_GETUNICODEFORMAT (commctrl. h)
description: Récupère l’indicateur de format de caractère Unicode pour le contrôle.
ms.assetid: 48a4472b-dda4-41a2-b5bc-6f74b1cdc70b
keywords:
- RB_GETUNICODEFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a6ef31c409ddc0570b03a3bcd8bb0dd81e9c722
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464399"
---
# <a name="rb_getunicodeformat-message"></a><span data-ttu-id="93083-104">\_Message GETUNICODEFORMAT RB</span><span class="sxs-lookup"><span data-stu-id="93083-104">RB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="93083-105">Récupère l’indicateur de format de caractère Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="93083-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="93083-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="93083-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93083-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="93083-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="93083-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="93083-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="93083-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="93083-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="93083-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="93083-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93083-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="93083-111">Return value</span></span>

<span data-ttu-id="93083-112">Retourne l’indicateur de format Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="93083-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="93083-113">Si cette valeur est différente de zéro, le contrôle utilise des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="93083-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="93083-114">Si cette valeur est égale à zéro, le contrôle utilise des caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="93083-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="93083-115">Notes</span><span class="sxs-lookup"><span data-stu-id="93083-115">Remarks</span></span>

<span data-ttu-id="93083-116">Pour plus d’informations sur ce message, consultez les notes relatives à [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="93083-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="93083-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93083-117">Requirements</span></span>



| <span data-ttu-id="93083-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93083-118">Requirement</span></span> | <span data-ttu-id="93083-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="93083-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="93083-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93083-120">Minimum supported client</span></span><br/> | <span data-ttu-id="93083-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93083-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="93083-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93083-122">Minimum supported server</span></span><br/> | <span data-ttu-id="93083-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93083-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="93083-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="93083-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="93083-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="93083-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93083-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93083-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93083-127">**\_SETUNICODEFORMAT RB**</span><span class="sxs-lookup"><span data-stu-id="93083-127">**RB\_SETUNICODEFORMAT**</span></span>](rb-setunicodeformat.md)
</dt> </dl>

 

 





