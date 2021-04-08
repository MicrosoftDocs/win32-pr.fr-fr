---
title: Message d’CDM_SETDEFEXT (COMMDLG. h)
description: Définit l’extension de nom de fichier par défaut pour une boîte de dialogue Ouvrir ou enregistrer sous de style Explorateur.
ms.assetid: bd4999f1-0a7e-4b7f-a0ba-a7c2a7f196c6
keywords:
- Boîtes de dialogue de CDM_SETDEFEXT message
topic_type:
- apiref
api_name:
- CDM_SETDEFEXT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd722a5ae172e06879ae9aaafadc5180ee77867e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033113"
---
# <a name="cdm_setdefext-message"></a><span data-ttu-id="2e3cb-104">\_Message CDM SETDEFEXT</span><span class="sxs-lookup"><span data-stu-id="2e3cb-104">CDM\_SETDEFEXT message</span></span>

<span data-ttu-id="2e3cb-105">\[À compter de Windows Vista, les boîtes de dialogue **ouvrir** et **Enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2e3cb-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="2e3cb-106">Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]</span><span class="sxs-lookup"><span data-stu-id="2e3cb-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="2e3cb-107">Définit l’extension de nom de fichier par défaut pour une boîte de dialogue **ouvrir** ou **Enregistrer sous** de style Explorateur.</span><span class="sxs-lookup"><span data-stu-id="2e3cb-107">Sets the default file name extension for an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="2e3cb-108">La boîte de dialogue doit avoir été créée avec l’indicateur **OFN \_ Explorer** ; sinon, le message échoue.</span><span class="sxs-lookup"><span data-stu-id="2e3cb-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETDEFEXT           (CDM_FIRST + 0x0006)
```



## <a name="parameters"></a><span data-ttu-id="2e3cb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e3cb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e3cb-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e3cb-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e3cb-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="2e3cb-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2e3cb-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e3cb-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e3cb-113">Pointeur vers la nouvelle extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="2e3cb-113">A pointer to the new file name extension.</span></span> <span data-ttu-id="2e3cb-114">Ne doit pas inclure le point (.).</span><span class="sxs-lookup"><span data-stu-id="2e3cb-114">Must not include the dot (.).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e3cb-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2e3cb-115">Return value</span></span>

<span data-ttu-id="2e3cb-116">Ce message n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="2e3cb-116">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e3cb-117">Notes</span><span class="sxs-lookup"><span data-stu-id="2e3cb-117">Remarks</span></span>

<span data-ttu-id="2e3cb-118">La macro correspondante est la suivante :</span><span class="sxs-lookup"><span data-stu-id="2e3cb-118">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_SetDefExt(hwnd, lparam)
```

## <a name="requirements"></a><span data-ttu-id="2e3cb-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e3cb-119">Requirements</span></span>



| <span data-ttu-id="2e3cb-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e3cb-120">Requirement</span></span> | <span data-ttu-id="2e3cb-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e3cb-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e3cb-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e3cb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2e3cb-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2e3cb-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2e3cb-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e3cb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2e3cb-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2e3cb-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2e3cb-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="2e3cb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e3cb-127"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2e3cb-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e3cb-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e3cb-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="2e3cb-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="2e3cb-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2e3cb-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="2e3cb-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="2e3cb-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="2e3cb-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="2e3cb-132">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="2e3cb-132">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="2e3cb-133">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="2e3cb-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2e3cb-134">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="2e3cb-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

