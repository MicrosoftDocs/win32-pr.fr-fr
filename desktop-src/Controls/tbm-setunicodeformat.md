---
title: Message TBM_SETUNICODEFORMAT (commctrl. h)
description: 'TBM_SETUNICODEFORMAT message : définit l’indicateur de format de caractère Unicode pour le contrôle. Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle.'
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
ms.openlocfilehash: f076efe2a575eff131c9bc2a1fe3df9ecab0fe68
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104037"
---
# <a name="tbm_setunicodeformat-message"></a><span data-ttu-id="57263-105">\_Message TBM SETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="57263-105">TBM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="57263-106">Définit l’indicateur de format de caractère Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="57263-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="57263-107">Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle.</span><span class="sxs-lookup"><span data-stu-id="57263-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="57263-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57263-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57263-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="57263-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57263-110">Détermine le jeu de caractères utilisé par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="57263-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="57263-111">Si cette valeur est différente de zéro, le contrôle utilise des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="57263-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="57263-112">Si cette valeur est égale à zéro, le contrôle utilise des caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="57263-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="57263-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57263-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="57263-114">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="57263-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57263-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="57263-115">Return value</span></span>

<span data-ttu-id="57263-116">Retourne l’indicateur de format Unicode précédent pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="57263-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="57263-117">Notes </span><span class="sxs-lookup"><span data-stu-id="57263-117">Remarks</span></span>

<span data-ttu-id="57263-118">Pour plus d’informations sur ce message, consultez les notes relatives à [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="57263-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="57263-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57263-119">Requirements</span></span>



| <span data-ttu-id="57263-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57263-120">Requirement</span></span> | <span data-ttu-id="57263-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="57263-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="57263-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57263-122">Minimum supported client</span></span><br/> | <span data-ttu-id="57263-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57263-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="57263-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57263-124">Minimum supported server</span></span><br/> | <span data-ttu-id="57263-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57263-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="57263-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="57263-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="57263-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="57263-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57263-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57263-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57263-129">**TBM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="57263-129">**TBM\_GETUNICODEFORMAT**</span></span>](tbm-getunicodeformat.md)
</dt> </dl>

 

 





