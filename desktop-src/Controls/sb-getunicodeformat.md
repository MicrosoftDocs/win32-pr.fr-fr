---
title: Message SB_GETUNICODEFORMAT (commctrl. h)
description: 'SB_GETUNICODEFORMAT message : récupère l’indicateur de format de caractère Unicode pour le contrôle.'
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
ms.openlocfilehash: 857af43911a01ffc58b1a878be6e1875a44c76cb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085897"
---
# <a name="sb_getunicodeformat-message"></a><span data-ttu-id="8bb67-104">\_Message SB GETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="8bb67-104">SB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="8bb67-105">Récupère l’indicateur de format de caractère Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="8bb67-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8bb67-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8bb67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bb67-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8bb67-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8bb67-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8bb67-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8bb67-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8bb67-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8bb67-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8bb67-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bb67-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8bb67-111">Return value</span></span>

<span data-ttu-id="8bb67-112">Retourne l’indicateur de format Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="8bb67-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="8bb67-113">Si cette valeur est différente de zéro, le contrôle utilise des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="8bb67-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="8bb67-114">Si cette valeur est égale à zéro, le contrôle utilise des caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="8bb67-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bb67-115">Notes </span><span class="sxs-lookup"><span data-stu-id="8bb67-115">Remarks</span></span>

<span data-ttu-id="8bb67-116">Pour plus d’informations sur ce message, consultez les notes relatives à [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="8bb67-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bb67-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8bb67-117">Requirements</span></span>



| <span data-ttu-id="8bb67-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8bb67-118">Requirement</span></span> | <span data-ttu-id="8bb67-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8bb67-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8bb67-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8bb67-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8bb67-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8bb67-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8bb67-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8bb67-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8bb67-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8bb67-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8bb67-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="8bb67-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bb67-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bb67-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bb67-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8bb67-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bb67-127">**\_SETUNICODEFORMAT SB**</span><span class="sxs-lookup"><span data-stu-id="8bb67-127">**SB\_SETUNICODEFORMAT**</span></span>](sb-setunicodeformat.md)
</dt> </dl>

 

 





