---
title: Message TCM_SETUNICODEFORMAT (commctrl. h)
description: 'TCM_SETUNICODEFORMAT message : définit l’indicateur de format de caractère Unicode pour le contrôle.'
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
ms.openlocfilehash: c2b84f944be9bd20897d25e4b111f55ced558a43
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085847"
---
# <a name="tcm_setunicodeformat-message"></a><span data-ttu-id="5e3f8-104">\_Message SETUNICODEFORMAT TCM</span><span class="sxs-lookup"><span data-stu-id="5e3f8-104">TCM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="5e3f8-105">Définit l’indicateur de format de caractère Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="5e3f8-105">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="5e3f8-106">Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle.</span><span class="sxs-lookup"><span data-stu-id="5e3f8-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="5e3f8-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**TabCtrl \_ SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="5e3f8-107">You can send this message explicitly or use the [**TabCtrl\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5e3f8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e3f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e3f8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5e3f8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e3f8-110">Détermine le jeu de caractères utilisé par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="5e3f8-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="5e3f8-111">Si cette valeur est différente de zéro, le contrôle utilise des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="5e3f8-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="5e3f8-112">Si cette valeur est égale à zéro, le contrôle utilise des caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="5e3f8-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="5e3f8-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e3f8-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5e3f8-114">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="5e3f8-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e3f8-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5e3f8-115">Return value</span></span>

<span data-ttu-id="5e3f8-116">Retourne l’indicateur de format Unicode précédent pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="5e3f8-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e3f8-117">Notes </span><span class="sxs-lookup"><span data-stu-id="5e3f8-117">Remarks</span></span>

<span data-ttu-id="5e3f8-118">Pour plus d’informations sur ce message, consultez les notes relatives à [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="5e3f8-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e3f8-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e3f8-119">Requirements</span></span>



| <span data-ttu-id="5e3f8-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e3f8-120">Requirement</span></span> | <span data-ttu-id="5e3f8-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e3f8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e3f8-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e3f8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5e3f8-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e3f8-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5e3f8-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e3f8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5e3f8-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e3f8-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5e3f8-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="5e3f8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e3f8-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e3f8-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e3f8-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e3f8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e3f8-129">**\_GETUNICODEFORMAT TCM**</span><span class="sxs-lookup"><span data-stu-id="5e3f8-129">**TCM\_GETUNICODEFORMAT**</span></span>](tcm-getunicodeformat.md)
</dt> </dl>

 

 





