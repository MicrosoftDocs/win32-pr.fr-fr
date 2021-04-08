---
title: Message PSM_SETFINISHTEXT (Prsht. h)
description: Définit le texte du bouton Terminer dans un Assistant, affiche et active le bouton et masque les boutons suivant et précédent. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet SetFinishText.
ms.assetid: fa89c6d7-9ab7-4e7c-ba08-d665420492a3
keywords:
- PSM_SETFINISHTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_SETFINISHTEXT
- PSM_SETFINISHTEXTA
- PSM_SETFINISHTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08195cddc96c8b92f403be6940f31099e21151f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740100"
---
# <a name="psm_setfinishtext-message"></a><span data-ttu-id="f7b8d-105">\_Message PSM SETFINISHTEXT</span><span class="sxs-lookup"><span data-stu-id="f7b8d-105">PSM\_SETFINISHTEXT message</span></span>

<span data-ttu-id="f7b8d-106">Définit le texte du bouton **Terminer** dans un Assistant, affiche et active le bouton et masque les boutons **suivant** et **précédent** .</span><span class="sxs-lookup"><span data-stu-id="f7b8d-106">Sets the text of the **Finish** button in a wizard, shows and enables the button, and hides the **Next** and **Back** buttons.</span></span> <span data-ttu-id="f7b8d-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ SetFinishText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) .</span><span class="sxs-lookup"><span data-stu-id="f7b8d-107">You can send this message explicitly or by using the [**PropSheet\_SetFinishText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f7b8d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7b8d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7b8d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f7b8d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7b8d-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f7b8d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f7b8d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7b8d-112">Pointeur vers le nouveau texte pour le bouton **Terminer** .</span><span class="sxs-lookup"><span data-stu-id="f7b8d-112">Pointer to the new text for the **Finish** button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7b8d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f7b8d-113">Return value</span></span>

<span data-ttu-id="f7b8d-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7b8d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f7b8d-115">Remarks</span></span>

<span data-ttu-id="f7b8d-116">Par défaut, le bouton **Terminer** n’a pas d’accélérateur clavier.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-116">By default, the **Finish** button does not have a keyboard accelerator.</span></span> <span data-ttu-id="f7b8d-117">Vous pouvez créer une touche d’accès rapide avec ce message en incluant une esperluette (&) dans la chaîne de texte que vous attribuez à *lParam*.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-117">You can create a keyboard accelerator with this message by including an ampersand (&) in the text string that you assign to *lParam*.</span></span> <span data-ttu-id="f7b8d-118">Par exemple, « &Finish » définit F comme touche accélérateur.</span><span class="sxs-lookup"><span data-stu-id="f7b8d-118">For example, "&Finish" defines F as the accelerator key.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7b8d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7b8d-119">Requirements</span></span>



| <span data-ttu-id="f7b8d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7b8d-120">Requirement</span></span> | <span data-ttu-id="f7b8d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7b8d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b8d-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7b8d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f7b8d-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7b8d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f7b8d-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7b8d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f7b8d-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7b8d-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f7b8d-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="f7b8d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7b8d-127"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7b8d-127"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="f7b8d-128">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="f7b8d-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f7b8d-129">**PSM \_ SETFINISHTEXTW** (Unicode) et **PSM \_ SETFINISHTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f7b8d-129">**PSM\_SETFINISHTEXTW** (Unicode) and **PSM\_SETFINISHTEXTA** (ANSI)</span></span><br/>    |



 

 





