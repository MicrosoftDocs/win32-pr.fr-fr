---
title: Message TCM_SETUNICODEFORMAT (commctrl. h)
description: Définit l’indicateur de format de caractère Unicode pour le contrôle.
ms.assetid: 4a9bacfc-d1b7-432a-9b61-b0fe18576679
keywords:
- TCM_SETUNICODEFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 033851411f95811f202ea6d87e23717d39141c04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383859"
---
# <a name="tcm_setunicodeformat-message"></a><span data-ttu-id="ea1e7-104">\_Message SETUNICODEFORMAT TCM</span><span class="sxs-lookup"><span data-stu-id="ea1e7-104">TCM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="ea1e7-105">Définit l’indicateur de format de caractère Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="ea1e7-105">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="ea1e7-106">Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle.</span><span class="sxs-lookup"><span data-stu-id="ea1e7-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="ea1e7-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**TabCtrl \_ SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="ea1e7-107">You can send this message explicitly or use the [**TabCtrl\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea1e7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea1e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea1e7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea1e7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea1e7-110">Détermine le jeu de caractères utilisé par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="ea1e7-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="ea1e7-111">Si cette valeur est différente de zéro, le contrôle utilise des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="ea1e7-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="ea1e7-112">Si cette valeur est égale à zéro, le contrôle utilise des caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="ea1e7-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="ea1e7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea1e7-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ea1e7-114">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="ea1e7-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea1e7-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea1e7-115">Return value</span></span>

<span data-ttu-id="ea1e7-116">Retourne l’indicateur de format Unicode précédent pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="ea1e7-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea1e7-117">Notes</span><span class="sxs-lookup"><span data-stu-id="ea1e7-117">Remarks</span></span>

<span data-ttu-id="ea1e7-118">Pour plus d’informations sur ce message, consultez les notes relatives à [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="ea1e7-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea1e7-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea1e7-119">Requirements</span></span>



| <span data-ttu-id="ea1e7-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea1e7-120">Requirement</span></span> | <span data-ttu-id="ea1e7-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea1e7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea1e7-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea1e7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ea1e7-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea1e7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea1e7-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea1e7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ea1e7-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea1e7-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea1e7-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea1e7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea1e7-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea1e7-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea1e7-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea1e7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea1e7-129">**\_GETUNICODEFORMAT TCM**</span><span class="sxs-lookup"><span data-stu-id="ea1e7-129">**TCM\_GETUNICODEFORMAT**</span></span>](tcm-getunicodeformat.md)
</dt> </dl>

 

 





