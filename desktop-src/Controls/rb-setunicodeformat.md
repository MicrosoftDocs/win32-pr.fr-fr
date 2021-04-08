---
title: Message RB_SETUNICODEFORMAT (commctrl. h)
description: Définit l’indicateur de format de caractère Unicode pour le contrôle. Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle.
ms.assetid: 769b74e0-c1f0-4068-80c4-075f1db2058a
keywords:
- RB_SETUNICODEFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfc9d0ce256af0de740c487fd6514848db79c2e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742517"
---
# <a name="rb_setunicodeformat-message"></a><span data-ttu-id="f0c3a-105">\_Message SETUNICODEFORMAT RB</span><span class="sxs-lookup"><span data-stu-id="f0c3a-105">RB\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="f0c3a-106">Définit l’indicateur de format de caractère Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="f0c3a-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="f0c3a-107">Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle.</span><span class="sxs-lookup"><span data-stu-id="f0c3a-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f0c3a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0c3a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0c3a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f0c3a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0c3a-110">Détermine le jeu de caractères utilisé par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="f0c3a-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="f0c3a-111">Si cette valeur est différente de zéro, le contrôle utilise des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="f0c3a-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="f0c3a-112">Si cette valeur est égale à zéro, le contrôle utilise des caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="f0c3a-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="f0c3a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0c3a-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f0c3a-114">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="f0c3a-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0c3a-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f0c3a-115">Return value</span></span>

<span data-ttu-id="f0c3a-116">Retourne l’indicateur de format Unicode précédent pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="f0c3a-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0c3a-117">Notes</span><span class="sxs-lookup"><span data-stu-id="f0c3a-117">Remarks</span></span>

<span data-ttu-id="f0c3a-118">Pour plus d’informations sur ce message, consultez les notes relatives à [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="f0c3a-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0c3a-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0c3a-119">Requirements</span></span>



| <span data-ttu-id="f0c3a-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0c3a-120">Requirement</span></span> | <span data-ttu-id="f0c3a-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0c3a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0c3a-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0c3a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f0c3a-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0c3a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f0c3a-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0c3a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f0c3a-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0c3a-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f0c3a-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0c3a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0c3a-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0c3a-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0c3a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0c3a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0c3a-129">**\_GETUNICODEFORMAT RB**</span><span class="sxs-lookup"><span data-stu-id="f0c3a-129">**RB\_GETUNICODEFORMAT**</span></span>](rb-getunicodeformat.md)
</dt> </dl>

 

 





