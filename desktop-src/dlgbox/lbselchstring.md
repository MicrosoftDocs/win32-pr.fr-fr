---
title: Message LBSELCHSTRING (COMMDLG. h)
description: Une boîte de dialogue Ouvrir ou enregistrer sous envoie le message LBSELCHSTRING Registered à votre procédure de hook lorsque la sélection change dans l’une des zones de liste ou des zones de liste modifiable de la boîte de dialogue.
ms.assetid: 3a8ebc63-b324-43ed-bb6f-34779f6043e7
keywords:
- Boîtes de dialogue de message LBSELCHSTRING
topic_type:
- apiref
api_name:
- LBSELCHSTRING
- LBSELCHSTRINGA
- LBSELCHSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62d61f88bd7cb6a84a94a3d8a246e6045f88a305
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550044"
---
# <a name="lbselchstring-message"></a><span data-ttu-id="1a404-104">Message LBSELCHSTRING</span><span class="sxs-lookup"><span data-stu-id="1a404-104">LBSELCHSTRING message</span></span>

<span data-ttu-id="1a404-105">\[À compter de Windows Vista, les boîtes de dialogue **ouvrir** et **Enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="1a404-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="1a404-106">Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]</span><span class="sxs-lookup"><span data-stu-id="1a404-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="1a404-107">Une boîte de dialogue **ouvrir** ou **Enregistrer sous** envoie le message **LBSELCHSTRING** Registered à votre procédure de hook lorsque la sélection change dans l’une des zones de liste ou des zones de liste modifiable de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="1a404-107">An **Open** or **Save As** dialog box sends the **LBSELCHSTRING** registered message to your hook procedure when the selection changes in any of the list boxes or combo boxes of the dialog box.</span></span>


```C++
#define LBSELCHSTRING TEXT("commdlg_LBSelChangedNotify")
```



## <a name="parameters"></a><span data-ttu-id="1a404-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a404-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a404-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1a404-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a404-110">Identificateur de la zone de liste ou zone de liste déroulante dans laquelle la sélection a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="1a404-110">The identifier of the list box or combo box in which the selection changed.</span></span>

</dd> <dt>

<span data-ttu-id="1a404-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a404-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a404-112">Le mot de poids faible spécifie le numéro d’élément de la chaîne sélectionnée dans la zone de liste ou la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="1a404-112">The low-order word specifies the item number of the selected string in the list box or combo box.</span></span> <span data-ttu-id="1a404-113">Le mot de poids fort spécifie le type de modification de la sélection.</span><span class="sxs-lookup"><span data-stu-id="1a404-113">The high-order word specifies the type of selection change.</span></span> <span data-ttu-id="1a404-114">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1a404-114">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="1a404-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a404-115">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="1a404-116">Signification</span><span class="sxs-lookup"><span data-stu-id="1a404-116">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="CD_LBSELCHANGE"></span><span id="cd_lbselchange"></span><dl> <span data-ttu-id="1a404-117"><dt>**CD-ROM \_ LBSELCHANGE**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1a404-117"><dt>**CD\_LBSELCHANGE**</dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="1a404-118">L’élément est le seul élément sélectionné dans une zone de liste à sélection unique.</span><span class="sxs-lookup"><span data-stu-id="1a404-118">The item is the only item selected in a single-selection list box.</span></span><br/>      |
| <span id="CD_LBSELADD"></span><span id="cd_lbseladd"></span><dl> <span data-ttu-id="1a404-119"><dt>**CD-ROM \_ LBSELADD**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1a404-119"><dt>**CD\_LBSELADD**</dt> <dt>2</dt></span></span> </dl>              | <span data-ttu-id="1a404-120">L’élément est l’un des éléments sélectionnés dans une zone de liste à sélection multiple.</span><span class="sxs-lookup"><span data-stu-id="1a404-120">The item is one of the items selected in a multiple-selection list box.</span></span><br/> |
| <span id="CD_LBSELSUB"></span><span id="cd_lbselsub"></span><dl> <span data-ttu-id="1a404-121"><dt>**CD-ROM \_ LBSELSUB**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1a404-121"><dt>**CD\_LBSELSUB**</dt> <dt>1</dt></span></span> </dl>              | <span data-ttu-id="1a404-122">L’élément n’est plus sélectionné dans une zone de liste à sélection multiple.</span><span class="sxs-lookup"><span data-stu-id="1a404-122">The item is no longer selected in a multiple-selection list box.</span></span><br/>        |
| <span id="CD_LBSELNOITEMS"></span><span id="cd_lbselnoitems"></span><dl> <span data-ttu-id="1a404-123"><dt>**CD-ROM \_ LBSELNOITEMS**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="1a404-123"><dt>**CD\_LBSELNOITEMS**</dt> <dt>-1</dt></span></span> </dl> | <span data-ttu-id="1a404-124">Il n’existe aucun élément dans une zone de liste à sélection multiple.</span><span class="sxs-lookup"><span data-stu-id="1a404-124">No items exist in a multiple-selection list box.</span></span><br/>                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a404-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1a404-125">Return value</span></span>

<span data-ttu-id="1a404-126">Ce message n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="1a404-126">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a404-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="1a404-127">Remarks</span></span>

<span data-ttu-id="1a404-128">La procédure de hook doit spécifier la constante **LBSELCHSTRING** dans un appel à la fonction [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) pour obtenir l’identificateur du message envoyé par la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="1a404-128">The hook procedure must specify the **LBSELCHSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a404-129">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1a404-129">Requirements</span></span>



| <span data-ttu-id="1a404-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a404-130">Requirement</span></span> | <span data-ttu-id="1a404-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a404-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a404-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a404-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1a404-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a404-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1a404-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a404-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1a404-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a404-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1a404-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="1a404-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a404-137"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a404-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1a404-138">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="1a404-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1a404-139">**LBSELCHSTRINGW** (Unicode) et **LBSELCHSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1a404-139">**LBSELCHSTRINGW** (Unicode) and **LBSELCHSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="1a404-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a404-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="1a404-141">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="1a404-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1a404-142">**\_selChange CDN**</span><span class="sxs-lookup"><span data-stu-id="1a404-142">**CDN\_SELCHANGE**</span></span>](cdn-selchange.md)
</dt> <dt>

[<span data-ttu-id="1a404-143">**\_TYPECHANGE CDN**</span><span class="sxs-lookup"><span data-stu-id="1a404-143">**CDN\_TYPECHANGE**</span></span>](cdn-typechange.md)
</dt> <dt>

[<span data-ttu-id="1a404-144">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="1a404-144">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="1a404-145">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="1a404-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1a404-146">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="1a404-146">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

