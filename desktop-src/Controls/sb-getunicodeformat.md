---
title: Message SB_GETUNICODEFORMAT (commctrl. h)
description: Récupère l’indicateur de format de caractère Unicode pour le contrôle.
ms.assetid: 0b2b543a-b1ef-452c-9b34-c5fbbac4aaa9
keywords:
- SB_GETUNICODEFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- SB_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dbb639a04f0a40d9d5e11b938aaadbcc8b4c730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509018"
---
# <a name="sb_getunicodeformat-message"></a><span data-ttu-id="c5d44-104">\_Message SB GETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="c5d44-104">SB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="c5d44-105">Récupère l’indicateur de format de caractère Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="c5d44-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c5d44-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5d44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5d44-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c5d44-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c5d44-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c5d44-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c5d44-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c5d44-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c5d44-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c5d44-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5d44-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c5d44-111">Return value</span></span>

<span data-ttu-id="c5d44-112">Retourne l’indicateur de format Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="c5d44-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="c5d44-113">Si cette valeur est différente de zéro, le contrôle utilise des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="c5d44-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="c5d44-114">Si cette valeur est égale à zéro, le contrôle utilise des caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="c5d44-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5d44-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c5d44-115">Remarks</span></span>

<span data-ttu-id="c5d44-116">Pour plus d’informations sur ce message, consultez les notes relatives à [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="c5d44-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5d44-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5d44-117">Requirements</span></span>



| <span data-ttu-id="c5d44-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5d44-118">Requirement</span></span> | <span data-ttu-id="c5d44-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5d44-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5d44-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5d44-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c5d44-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5d44-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c5d44-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5d44-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c5d44-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5d44-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c5d44-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5d44-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5d44-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5d44-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5d44-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5d44-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5d44-127">**\_SETUNICODEFORMAT SB**</span><span class="sxs-lookup"><span data-stu-id="c5d44-127">**SB\_SETUNICODEFORMAT**</span></span>](sb-setunicodeformat.md)
</dt> </dl>

 

 





