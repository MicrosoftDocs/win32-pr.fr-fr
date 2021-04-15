---
title: Message EM_TAKEFOCUS (commctrl. h)
description: Force un contrôle d’édition sur une seule ligne à recevoir le focus clavier. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro modifier TakeFocus.
ms.assetid: 27470857-4219-4426-bc69-e1271afc6ffb
keywords:
- EM_TAKEFOCUS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_TAKEFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e4abdf926cdd337760b5cf151c3f8ee08cb418b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465382"
---
# <a name="em_takefocus-message"></a><span data-ttu-id="2836b-105">\_Message TAKEFOCUS em</span><span class="sxs-lookup"><span data-stu-id="2836b-105">EM\_TAKEFOCUS message</span></span>

<span data-ttu-id="2836b-106">\[Destiné à un usage interne ; non recommandé pour une utilisation dans les applications.</span><span class="sxs-lookup"><span data-stu-id="2836b-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="2836b-107">Ce message n’est peut-être pas pris en charge dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2836b-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="2836b-108">Force un contrôle d’édition sur une seule ligne à recevoir le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="2836b-108">Forces a single-line edit control to receive keyboard focus.</span></span> <span data-ttu-id="2836b-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**modifier \_ TakeFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus) .</span><span class="sxs-lookup"><span data-stu-id="2836b-109">You can send this message explicitly or by using the [**Edit\_TakeFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2836b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2836b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2836b-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2836b-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2836b-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="2836b-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2836b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2836b-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2836b-114">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="2836b-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2836b-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2836b-115">Return value</span></span>

<span data-ttu-id="2836b-116">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2836b-116">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="2836b-117">Considérations relatives à la sécurité</span><span class="sxs-lookup"><span data-stu-id="2836b-117">Security Considerations</span></span>

<span data-ttu-id="2836b-118">L’utilisation de ce message peut compromettre la sécurité de votre programme.</span><span class="sxs-lookup"><span data-stu-id="2836b-118">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="2836b-119">Notes</span><span class="sxs-lookup"><span data-stu-id="2836b-119">Remarks</span></span>

<span data-ttu-id="2836b-120">Ce message est ignoré si le contrôle d’édition n’est pas un contrôle d’édition sur une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="2836b-120">This message is ignored if the edit control is not a single-line edit control.</span></span>

<span data-ttu-id="2836b-121">Si le contrôle d’édition a précédemment reçu un message [**em \_ NOSETFOCUS**](em-nosetfocus.md) , le contrôle d’édition semble avoir le focus sans réellement l’avoir ; sinon, le contrôle d’édition reçoit le focus.</span><span class="sxs-lookup"><span data-stu-id="2836b-121">If the edit control previously received an [**EM\_NOSETFOCUS**](em-nosetfocus.md) message, the edit control will appear to have the focus without actually having it; otherwise, the edit control will receive focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="2836b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2836b-122">Requirements</span></span>



| <span data-ttu-id="2836b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2836b-123">Requirement</span></span> | <span data-ttu-id="2836b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="2836b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2836b-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2836b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2836b-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2836b-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2836b-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2836b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2836b-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2836b-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2836b-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="2836b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2836b-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2836b-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2836b-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2836b-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="2836b-132">**Référence**</span><span class="sxs-lookup"><span data-stu-id="2836b-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2836b-133">**Modifier \_ TakeFocus**</span><span class="sxs-lookup"><span data-stu-id="2836b-133">**Edit\_TakeFocus**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus)
</dt> <dt>

[<span data-ttu-id="2836b-134">**\_NOSETFOCUS em**</span><span class="sxs-lookup"><span data-stu-id="2836b-134">**EM\_NOSETFOCUS**</span></span>](em-nosetfocus.md)
</dt> </dl>

 

 





