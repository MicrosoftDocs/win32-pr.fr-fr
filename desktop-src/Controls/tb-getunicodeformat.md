---
title: Message TB_GETUNICODEFORMAT (commctrl. h)
description: 'TB_GETUNICODEFORMAT message : récupère l’indicateur de format de caractère Unicode pour le contrôle.'
ms.assetid: aadce646-daf1-4f1e-9171-2aeac12d3484
keywords:
- TB_GETUNICODEFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4beb5a5ff0b71dd76c85db2788d9dc91aa9f4957
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106787"
---
# <a name="tb_getunicodeformat-message"></a><span data-ttu-id="df756-104">TO \_ GETUNICODEFORMAT message</span><span class="sxs-lookup"><span data-stu-id="df756-104">TB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="df756-105">Récupère l’indicateur de format de caractère Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="df756-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="df756-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df756-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df756-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="df756-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="df756-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="df756-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="df756-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="df756-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="df756-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="df756-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df756-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="df756-111">Return value</span></span>

<span data-ttu-id="df756-112">Retourne l’indicateur de format Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="df756-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="df756-113">Si cette valeur est différente de zéro, le contrôle utilise des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="df756-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="df756-114">Si cette valeur est égale à zéro, le contrôle utilise des caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="df756-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="df756-115">Notes </span><span class="sxs-lookup"><span data-stu-id="df756-115">Remarks</span></span>

<span data-ttu-id="df756-116">Pour plus d’informations sur ce message, consultez les notes relatives à [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="df756-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="df756-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df756-117">Requirements</span></span>



| <span data-ttu-id="df756-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df756-118">Requirement</span></span> | <span data-ttu-id="df756-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="df756-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df756-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df756-120">Minimum supported client</span></span><br/> | <span data-ttu-id="df756-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df756-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="df756-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df756-122">Minimum supported server</span></span><br/> | <span data-ttu-id="df756-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df756-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="df756-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="df756-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="df756-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="df756-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df756-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df756-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df756-127">**TO \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="df756-127">**TB\_SETUNICODEFORMAT**</span></span>](tb-setunicodeformat.md)
</dt> </dl>

 

 





