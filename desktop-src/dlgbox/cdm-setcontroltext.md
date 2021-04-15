---
title: Message d’CDM_SETCONTROLTEXT (COMMDLG. h)
description: Définit le texte pour le contrôle spécifié dans une boîte de dialogue Ouvrir ou enregistrer sous de style Explorateur.
ms.assetid: ff0e50b7-a14d-40d1-8576-f93a612f3aa3
keywords:
- Boîtes de dialogue de CDM_SETCONTROLTEXT message
topic_type:
- apiref
api_name:
- CDM_SETCONTROLTEXT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87490ba20b5785da4fb9660d97b1b9232d047671
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383803"
---
# <a name="cdm_setcontroltext-message"></a><span data-ttu-id="cf400-104">\_Message CDM SETCONTROLTEXT</span><span class="sxs-lookup"><span data-stu-id="cf400-104">CDM\_SETCONTROLTEXT message</span></span>

<span data-ttu-id="cf400-105">\[À compter de Windows Vista, les boîtes de dialogue **ouvrir** et **Enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cf400-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="cf400-106">Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]</span><span class="sxs-lookup"><span data-stu-id="cf400-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="cf400-107">Définit le texte pour le contrôle spécifié dans une boîte de dialogue **ouvrir** ou **Enregistrer sous** de style Explorateur.</span><span class="sxs-lookup"><span data-stu-id="cf400-107">Sets the text for the specified control in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="cf400-108">La boîte de dialogue doit avoir été créée avec l’indicateur **OFN \_ Explorer** ; sinon, le message échoue.</span><span class="sxs-lookup"><span data-stu-id="cf400-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETCONTROLTEXT      (CDM_FIRST + 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="cf400-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cf400-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf400-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cf400-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf400-111">Identificateur du contrôle dont le texte doit être défini.</span><span class="sxs-lookup"><span data-stu-id="cf400-111">The identifier of the control to whose text is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="cf400-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cf400-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf400-113">Nouveau texte pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="cf400-113">The new text for the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf400-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cf400-114">Return value</span></span>

<span data-ttu-id="cf400-115">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="cf400-115">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf400-116">Notes</span><span class="sxs-lookup"><span data-stu-id="cf400-116">Remarks</span></span>

<span data-ttu-id="cf400-117">La macro correspondante est la suivante :</span><span class="sxs-lookup"><span data-stu-id="cf400-117">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_SetControlText(hwnd, wparam, lparam)
```

## <a name="requirements"></a><span data-ttu-id="cf400-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf400-118">Requirements</span></span>



| <span data-ttu-id="cf400-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf400-119">Requirement</span></span> | <span data-ttu-id="cf400-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf400-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf400-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf400-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cf400-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf400-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cf400-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf400-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cf400-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf400-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cf400-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="cf400-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf400-126"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf400-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf400-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf400-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="cf400-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="cf400-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cf400-129">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="cf400-129">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="cf400-130">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="cf400-130">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="cf400-131">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="cf400-131">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="cf400-132">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="cf400-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cf400-133">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="cf400-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

