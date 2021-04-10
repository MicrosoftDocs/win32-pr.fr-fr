---
title: Message EM_NOSETFOCUS (commctrl. h)
description: Empêche un contrôle d’édition sur une seule ligne de recevoir le focus clavier. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro modifier NoSetFocus.
ms.assetid: aeb5ed6b-7d4f-4c0d-a172-6cee7cab959c
keywords:
- EM_NOSETFOCUS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_NOSETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82830cda3402d2089d3421debaa7c4dbf13de5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105103"
---
# <a name="em_nosetfocus-message"></a><span data-ttu-id="c423a-105">\_Message NOSETFOCUS em</span><span class="sxs-lookup"><span data-stu-id="c423a-105">EM\_NOSETFOCUS message</span></span>

<span data-ttu-id="c423a-106">\[Destiné à un usage interne ; non recommandé pour une utilisation dans les applications.</span><span class="sxs-lookup"><span data-stu-id="c423a-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="c423a-107">Ce message n’est peut-être pas pris en charge dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c423a-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="c423a-108">Empêche un contrôle d’édition sur une seule ligne de recevoir le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="c423a-108">Prevents a single-line edit control from receiving keyboard focus.</span></span> <span data-ttu-id="c423a-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**modifier \_ NoSetFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus) .</span><span class="sxs-lookup"><span data-stu-id="c423a-109">You can send this message explicitly or by using the [**Edit\_NoSetFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c423a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c423a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c423a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c423a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c423a-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="c423a-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c423a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c423a-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c423a-114">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="c423a-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c423a-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c423a-115">Return value</span></span>

<span data-ttu-id="c423a-116">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c423a-116">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="c423a-117">Considérations relatives à la sécurité</span><span class="sxs-lookup"><span data-stu-id="c423a-117">Security Considerations</span></span>

<span data-ttu-id="c423a-118">L’utilisation de ce message peut compromettre la sécurité de votre programme.</span><span class="sxs-lookup"><span data-stu-id="c423a-118">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="c423a-119">Notes</span><span class="sxs-lookup"><span data-stu-id="c423a-119">Remarks</span></span>

<span data-ttu-id="c423a-120">Ce message est ignoré si le contrôle d’édition n’est pas un contrôle d’édition sur une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="c423a-120">This message is ignored if the edit control is not a single-line edit control.</span></span>

<span data-ttu-id="c423a-121">Une fois ce message envoyé, l’effet est permanent.</span><span class="sxs-lookup"><span data-stu-id="c423a-121">After this message is sent, the effect is permanent.</span></span>

## <a name="requirements"></a><span data-ttu-id="c423a-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c423a-122">Requirements</span></span>



| <span data-ttu-id="c423a-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c423a-123">Requirement</span></span> | <span data-ttu-id="c423a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c423a-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c423a-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c423a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c423a-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c423a-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c423a-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c423a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c423a-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c423a-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c423a-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="c423a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c423a-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c423a-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c423a-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c423a-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="c423a-132">**Référence**</span><span class="sxs-lookup"><span data-stu-id="c423a-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c423a-133">**Modifier \_ NoSetFocus**</span><span class="sxs-lookup"><span data-stu-id="c423a-133">**Edit\_NoSetFocus**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus)
</dt> <dt>

[<span data-ttu-id="c423a-134">**\_TAKEFOCUS em**</span><span class="sxs-lookup"><span data-stu-id="c423a-134">**EM\_TAKEFOCUS**</span></span>](em-takefocus.md)
</dt> </dl>

 

 





