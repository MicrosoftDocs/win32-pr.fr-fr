---
title: Message TDM_SET_ELEMENT_TEXT (commctrl. h)
description: Met à jour un élément de texte dans une boîte de dialogue de tâche.
ms.assetid: e3f15805-5d48-4549-9959-69ec01345e57
keywords:
- TDM_SET_ELEMENT_TEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TDM_SET_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2229dc269f14c9a3b0765675dcc97dc9776b72c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033197"
---
# <a name="tdm_set_element_text-message"></a><span data-ttu-id="e9620-104">\_Message texte de l’élément d’ensemble TDM \_ \_</span><span class="sxs-lookup"><span data-stu-id="e9620-104">TDM\_SET\_ELEMENT\_TEXT message</span></span>

<span data-ttu-id="e9620-105">Met à jour un élément de texte dans une boîte de dialogue de tâche.</span><span class="sxs-lookup"><span data-stu-id="e9620-105">Updates a text element in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="e9620-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9620-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9620-107">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e9620-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9620-108">Indique l’élément à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="e9620-108">Indicates the element to update.</span></span> <span data-ttu-id="e9620-109">(Pour obtenir une illustration, consultez [à propos des boîtes de dialogue de tâches](task-dialogs-overview.md).) Ce paramètre doit avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e9620-109">(For an illustration, see [About Task Dialogs](task-dialogs-overview.md).) This parameter must be one of the following values.</span></span>



| <span data-ttu-id="e9620-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9620-110">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="e9620-111">Signification</span><span class="sxs-lookup"><span data-stu-id="e9620-111">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <span data-ttu-id="e9620-112"><dt>**\_contenu TDE**</dt></span><span class="sxs-lookup"><span data-stu-id="e9620-112"><dt>**TDE\_CONTENT**</dt></span></span> </dl>                                         | <span data-ttu-id="e9620-113">Contenu.</span><span class="sxs-lookup"><span data-stu-id="e9620-113">Content.</span></span><br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <span data-ttu-id="e9620-114"><dt>**\_informations développées \_ TDE**</dt></span><span class="sxs-lookup"><span data-stu-id="e9620-114"><dt>**TDE\_EXPANDED\_INFORMATION**</dt></span></span> </dl> | <span data-ttu-id="e9620-115">Informations développées.</span><span class="sxs-lookup"><span data-stu-id="e9620-115">Expanded information.</span></span><br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <span data-ttu-id="e9620-116"><dt>**\_pied de page TDE**</dt></span><span class="sxs-lookup"><span data-stu-id="e9620-116"><dt>**TDE\_FOOTER**</dt></span></span> </dl>                                            | <span data-ttu-id="e9620-117">Texte de pied de page.</span><span class="sxs-lookup"><span data-stu-id="e9620-117">Footer text.</span></span><br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <span data-ttu-id="e9620-118"><dt>**\_instruction principale \_ TDE**</dt></span><span class="sxs-lookup"><span data-stu-id="e9620-118"><dt>**TDE\_MAIN\_INSTRUCTION**</dt></span></span> </dl>             | <span data-ttu-id="e9620-119">Instruction principale.</span><span class="sxs-lookup"><span data-stu-id="e9620-119">Main instruction.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="e9620-120">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e9620-120">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9620-121">Nouveau texte à utiliser.</span><span class="sxs-lookup"><span data-stu-id="e9620-121">The new text to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9620-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e9620-122">Return value</span></span>

<span data-ttu-id="e9620-123">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="e9620-123">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9620-124">Notes</span><span class="sxs-lookup"><span data-stu-id="e9620-124">Remarks</span></span>

<span data-ttu-id="e9620-125">La taille ou la disposition de la boîte de dialogue de tâches peut changer pour s’adapter au nouveau texte.</span><span class="sxs-lookup"><span data-stu-id="e9620-125">The size or layout of the task dialog may change to accommodate the new text.</span></span>

## <a name="examples"></a><span data-ttu-id="e9620-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="e9620-126">Examples</span></span>

<span data-ttu-id="e9620-127">L’exemple de code suivant montre comment définir le texte de pied de page dans la boîte de dialogue de tâches représentée par *HWND*.</span><span class="sxs-lookup"><span data-stu-id="e9620-127">The following example code shows how to set the footer text in the task dialog represented by *hwnd*.</span></span>


```C++
SendMessage(hwnd, TDM_SET_ELEMENT_TEXT, (WPARAM)TDE_FOOTER, (LPARAM)L"New footer text.");
```



## <a name="requirements"></a><span data-ttu-id="e9620-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9620-128">Requirements</span></span>



| <span data-ttu-id="e9620-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9620-129">Requirement</span></span> | <span data-ttu-id="e9620-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9620-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9620-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9620-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e9620-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9620-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e9620-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9620-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e9620-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9620-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e9620-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9620-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9620-136"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9620-136"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9620-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9620-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9620-138">**texte de l' \_ élément de mise à jour TDM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e9620-138">**TDM\_UPDATE\_ELEMENT\_TEXT**</span></span>](tdm-update-element-text.md)
</dt> </dl>

 

 





