---
title: Message RB_GETUNICODEFORMAT (commctrl. h)
description: 'RB_GETUNICODEFORMAT message : récupère l’indicateur de format de caractère Unicode pour le contrôle.'
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
ms.openlocfilehash: 45e1a4546c9c33e87943d305c85939ab280fa122
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085977"
---
# <a name="rb_getunicodeformat-message"></a><span data-ttu-id="0e93c-104">\_Message GETUNICODEFORMAT RB</span><span class="sxs-lookup"><span data-stu-id="0e93c-104">RB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="0e93c-105">Récupère l’indicateur de format de caractère Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="0e93c-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0e93c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e93c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e93c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0e93c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0e93c-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="0e93c-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0e93c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e93c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0e93c-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="0e93c-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e93c-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0e93c-111">Return value</span></span>

<span data-ttu-id="0e93c-112">Retourne l’indicateur de format Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="0e93c-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="0e93c-113">Si cette valeur est différente de zéro, le contrôle utilise des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="0e93c-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="0e93c-114">Si cette valeur est égale à zéro, le contrôle utilise des caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="0e93c-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e93c-115">Notes </span><span class="sxs-lookup"><span data-stu-id="0e93c-115">Remarks</span></span>

<span data-ttu-id="0e93c-116">Pour plus d’informations sur ce message, consultez les notes relatives à [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="0e93c-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e93c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e93c-117">Requirements</span></span>



| <span data-ttu-id="0e93c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e93c-118">Requirement</span></span> | <span data-ttu-id="0e93c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e93c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e93c-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e93c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0e93c-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e93c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0e93c-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e93c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0e93c-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e93c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0e93c-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e93c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e93c-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e93c-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e93c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e93c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e93c-127">**\_SETUNICODEFORMAT RB**</span><span class="sxs-lookup"><span data-stu-id="0e93c-127">**RB\_SETUNICODEFORMAT**</span></span>](rb-setunicodeformat.md)
</dt> </dl>

 

 





