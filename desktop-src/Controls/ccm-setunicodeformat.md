---
title: Message CCM_SETUNICODEFORMAT (commctrl. h)
description: Définit l’indicateur de format de caractère Unicode pour le contrôle. Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle.
ms.assetid: 8028b7d7-30d2-4154-81c7-ba1ed095ef02
keywords:
- CCM_SETUNICODEFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- CCM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffbe9f5032c193cb612f68ca8ed6ec6b04ce8094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465915"
---
# <a name="ccm_setunicodeformat-message"></a><span data-ttu-id="decc0-105">\_Message CCM SETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="decc0-105">CCM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="decc0-106">Définit l’indicateur de format de caractère Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="decc0-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="decc0-107">Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle.</span><span class="sxs-lookup"><span data-stu-id="decc0-107">This message enables you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="decc0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="decc0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="decc0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="decc0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="decc0-110">Valeur qui détermine le jeu de caractères utilisé par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="decc0-110">A value that determines the character set that is used by the control.</span></span> <span data-ttu-id="decc0-111">Si cette valeur est **true**, le contrôle utilise des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="decc0-111">If this value is **TRUE**, the control will use Unicode characters.</span></span> <span data-ttu-id="decc0-112">Si cette valeur est **false**, le contrôle utilise des caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="decc0-112">If this value is **FALSE**, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="decc0-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="decc0-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="decc0-114">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="decc0-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="decc0-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="decc0-115">Return value</span></span>

<span data-ttu-id="decc0-116">Retourne l’indicateur de format Unicode précédent pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="decc0-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="decc0-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="decc0-117">Requirements</span></span>



| <span data-ttu-id="decc0-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="decc0-118">Requirement</span></span> | <span data-ttu-id="decc0-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="decc0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="decc0-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="decc0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="decc0-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="decc0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="decc0-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="decc0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="decc0-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="decc0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="decc0-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="decc0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="decc0-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="decc0-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="decc0-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="decc0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="decc0-127">**CCM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="decc0-127">**CCM\_GETUNICODEFORMAT**</span></span>](ccm-getunicodeformat.md)
</dt> </dl>

 

 





