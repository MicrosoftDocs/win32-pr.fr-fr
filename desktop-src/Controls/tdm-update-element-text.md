---
title: Message TDM_UPDATE_ELEMENT_TEXT (commctrl. h)
description: Met à jour un élément de texte dans une boîte de dialogue de tâche.
ms.assetid: 2df446c8-db87-42b5-b5bd-40fadbf9d45b
keywords:
- TDM_UPDATE_ELEMENT_TEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TDM_UPDATE_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6dac6787c68d0cbe619bbf28fa1a6383606e99f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106246"
---
# <a name="tdm_update_element_text-message"></a><span data-ttu-id="f00ea-104">\_Message texte de l’élément de mise à jour TDM \_ \_</span><span class="sxs-lookup"><span data-stu-id="f00ea-104">TDM\_UPDATE\_ELEMENT\_TEXT message</span></span>

<span data-ttu-id="f00ea-105">Met à jour un élément de texte dans une boîte de dialogue de tâche.</span><span class="sxs-lookup"><span data-stu-id="f00ea-105">Updates a text element in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="f00ea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f00ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f00ea-107">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f00ea-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f00ea-108">Indique l’élément à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="f00ea-108">Indicates the element to update.</span></span> <span data-ttu-id="f00ea-109">(Pour obtenir une illustration des éléments, consultez [à propos des boîtes de dialogue de tâches](task-dialogs-overview.md).) Ce paramètre doit avoir l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="f00ea-109">(For an illustration of the elements, see [About Task Dialogs](task-dialogs-overview.md).) This parameter must be one of the following values:</span></span>



| <span data-ttu-id="f00ea-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="f00ea-110">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="f00ea-111">Signification</span><span class="sxs-lookup"><span data-stu-id="f00ea-111">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <span data-ttu-id="f00ea-112"><dt>**\_contenu TDE**</dt></span><span class="sxs-lookup"><span data-stu-id="f00ea-112"><dt>**TDE\_CONTENT**</dt></span></span> </dl>                                         | <span data-ttu-id="f00ea-113">Contenu.</span><span class="sxs-lookup"><span data-stu-id="f00ea-113">Content.</span></span><br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <span data-ttu-id="f00ea-114"><dt>**\_informations développées \_ TDE**</dt></span><span class="sxs-lookup"><span data-stu-id="f00ea-114"><dt>**TDE\_EXPANDED\_INFORMATION**</dt></span></span> </dl> | <span data-ttu-id="f00ea-115">Informations développées.</span><span class="sxs-lookup"><span data-stu-id="f00ea-115">Expanded information.</span></span><br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <span data-ttu-id="f00ea-116"><dt>**\_pied de page TDE**</dt></span><span class="sxs-lookup"><span data-stu-id="f00ea-116"><dt>**TDE\_FOOTER**</dt></span></span> </dl>                                            | <span data-ttu-id="f00ea-117">Texte de pied de page.</span><span class="sxs-lookup"><span data-stu-id="f00ea-117">Footer text.</span></span><br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <span data-ttu-id="f00ea-118"><dt>**\_instruction principale \_ TDE**</dt></span><span class="sxs-lookup"><span data-stu-id="f00ea-118"><dt>**TDE\_MAIN\_INSTRUCTION**</dt></span></span> </dl>             | <span data-ttu-id="f00ea-119">Instruction principale.</span><span class="sxs-lookup"><span data-stu-id="f00ea-119">Main instruction.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="f00ea-120">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f00ea-120">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f00ea-121">Pointeur vers une chaîne Unicode qui contient le nouveau texte.</span><span class="sxs-lookup"><span data-stu-id="f00ea-121">Pointer to a Unicode string that contains the new text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f00ea-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f00ea-122">Return value</span></span>

<span data-ttu-id="f00ea-123">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="f00ea-123">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="f00ea-124">Notes</span><span class="sxs-lookup"><span data-stu-id="f00ea-124">Remarks</span></span>

<span data-ttu-id="f00ea-125">Pour éviter le découpage, le nouveau texte ne doit pas être plus long que le texte existant.</span><span class="sxs-lookup"><span data-stu-id="f00ea-125">To avoid clipping, the new text must be no longer than the existing text.</span></span> <span data-ttu-id="f00ea-126">La définition du texte sur une chaîne plus petite n’entraîne pas le redimensionnement de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f00ea-126">Setting the text to a shorter string does not cause the dialog box to resize.</span></span>

<span data-ttu-id="f00ea-127">Si le membre **pszExpandedInformation** de la structure [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) utilisée pour créer la boîte de dialogue de tâche a la **valeur null** et que vous envoyez un message **\_ \_ \_ texte d’élément de mise à jour TDM** avec des \_ informations développées TDE \_ , rien ne se produit.</span><span class="sxs-lookup"><span data-stu-id="f00ea-127">If the **pszExpandedInformation** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog was **NULL**, and you send a **TDM\_UPDATE\_ELEMENT\_TEXT** message with TDE\_EXPANDED\_INFORMATION, nothing will happen.</span></span>

<span data-ttu-id="f00ea-128">Les éléments ci-dessus s’appliquent également aux pieds de page et pieds de \_ page TDE.</span><span class="sxs-lookup"><span data-stu-id="f00ea-128">The above also applies to the footer and TDE\_FOOTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="f00ea-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f00ea-129">Requirements</span></span>



| <span data-ttu-id="f00ea-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f00ea-130">Requirement</span></span> | <span data-ttu-id="f00ea-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="f00ea-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f00ea-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f00ea-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f00ea-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f00ea-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f00ea-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f00ea-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f00ea-135">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f00ea-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f00ea-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="f00ea-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f00ea-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f00ea-137"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f00ea-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f00ea-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f00ea-139">**texte de l' \_ élément de jeu TDM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f00ea-139">**TDM\_SET\_ELEMENT\_TEXT**</span></span>](tdm-set-element-text.md)
</dt> </dl>

 

 





