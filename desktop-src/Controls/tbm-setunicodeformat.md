---
title: Message TBM_SETUNICODEFORMAT (commctrl. h)
description: Définit l’indicateur de format de caractère Unicode pour le contrôle. Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle.
ms.assetid: c50a49e8-6042-490d-bb7b-baf917d5c30a
keywords:
- TBM_SETUNICODEFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adb64c8fcb3464067e9522695930f4f9d0771357
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509306"
---
# <a name="tbm_setunicodeformat-message"></a><span data-ttu-id="529dd-105">\_Message TBM SETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="529dd-105">TBM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="529dd-106">Définit l’indicateur de format de caractère Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="529dd-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="529dd-107">Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle.</span><span class="sxs-lookup"><span data-stu-id="529dd-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="529dd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="529dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="529dd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="529dd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="529dd-110">Détermine le jeu de caractères utilisé par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="529dd-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="529dd-111">Si cette valeur est différente de zéro, le contrôle utilise des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="529dd-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="529dd-112">Si cette valeur est égale à zéro, le contrôle utilise des caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="529dd-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="529dd-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="529dd-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="529dd-114">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="529dd-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="529dd-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="529dd-115">Return value</span></span>

<span data-ttu-id="529dd-116">Retourne l’indicateur de format Unicode précédent pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="529dd-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="529dd-117">Notes</span><span class="sxs-lookup"><span data-stu-id="529dd-117">Remarks</span></span>

<span data-ttu-id="529dd-118">Pour plus d’informations sur ce message, consultez les notes relatives à [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="529dd-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="529dd-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="529dd-119">Requirements</span></span>



| <span data-ttu-id="529dd-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="529dd-120">Requirement</span></span> | <span data-ttu-id="529dd-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="529dd-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="529dd-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="529dd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="529dd-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="529dd-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="529dd-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="529dd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="529dd-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="529dd-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="529dd-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="529dd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="529dd-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="529dd-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="529dd-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="529dd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="529dd-129">**TBM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="529dd-129">**TBM\_GETUNICODEFORMAT**</span></span>](tbm-getunicodeformat.md)
</dt> </dl>

 

 





