---
title: Message SB_SETUNICODEFORMAT (commctrl. h)
description: 'SB_SETUNICODEFORMAT message : définit l’indicateur de format de caractère Unicode pour le contrôle. Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle.'
ms.assetid: 022e7138-c12f-4c59-82da-2ac6d276fa77
keywords:
- SB_SETUNICODEFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- SB_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 278a5645928a51732b87c12447bb2524bfadfbcd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085887"
---
# <a name="sb_setunicodeformat-message"></a><span data-ttu-id="60ca1-105">\_Message SB SETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="60ca1-105">SB\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="60ca1-106">Définit l’indicateur de format de caractère Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="60ca1-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="60ca1-107">Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle.</span><span class="sxs-lookup"><span data-stu-id="60ca1-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="60ca1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60ca1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60ca1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="60ca1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="60ca1-110">Détermine le jeu de caractères utilisé par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="60ca1-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="60ca1-111">Si cette valeur est **true**, le contrôle utilise des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="60ca1-111">If this value is **TRUE**, the control will use Unicode characters.</span></span> <span data-ttu-id="60ca1-112">Si cette valeur est **false**, le contrôle utilise des caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="60ca1-112">If this value is **FALSE**, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="60ca1-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="60ca1-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="60ca1-114">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="60ca1-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60ca1-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="60ca1-115">Return value</span></span>

<span data-ttu-id="60ca1-116">Retourne l’indicateur de format Unicode précédent pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="60ca1-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="60ca1-117">Notes </span><span class="sxs-lookup"><span data-stu-id="60ca1-117">Remarks</span></span>

<span data-ttu-id="60ca1-118">Pour plus d’informations sur ce message, consultez les notes relatives à [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="60ca1-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="60ca1-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60ca1-119">Requirements</span></span>



| <span data-ttu-id="60ca1-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60ca1-120">Requirement</span></span> | <span data-ttu-id="60ca1-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="60ca1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60ca1-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60ca1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="60ca1-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="60ca1-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="60ca1-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60ca1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="60ca1-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="60ca1-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="60ca1-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="60ca1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="60ca1-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="60ca1-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60ca1-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60ca1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60ca1-129">**\_GETUNICODEFORMAT SB**</span><span class="sxs-lookup"><span data-stu-id="60ca1-129">**SB\_GETUNICODEFORMAT**</span></span>](sb-getunicodeformat.md)
</dt> </dl>

 

 





