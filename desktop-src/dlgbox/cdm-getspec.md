---
title: Message d’CDM_GETSPEC (COMMDLG. h)
description: Récupère le nom de fichier (sans le chemin d’accès) du fichier actuellement sélectionné dans une boîte de dialogue Ouvrir ou enregistrer sous de style Explorateur.
ms.assetid: 22a67c92-bd24-4cba-bef8-291d241e6ec8
keywords:
- Boîtes de dialogue de CDM_GETSPEC message
topic_type:
- apiref
api_name:
- CDM_GETSPEC
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2732bf2a8c581439a40538445853531b57cfc77a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102780"
---
# <a name="cdm_getspec-message"></a><span data-ttu-id="87dea-104">\_Message CDM GETSPEC</span><span class="sxs-lookup"><span data-stu-id="87dea-104">CDM\_GETSPEC message</span></span>

<span data-ttu-id="87dea-105">\[À compter de Windows Vista, les boîtes de dialogue **ouvrir** et **Enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="87dea-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="87dea-106">Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]</span><span class="sxs-lookup"><span data-stu-id="87dea-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="87dea-107">Récupère le nom de fichier (sans le chemin d’accès) du fichier actuellement sélectionné dans une boîte de dialogue **ouvrir** ou **Enregistrer sous** de style Explorateur.</span><span class="sxs-lookup"><span data-stu-id="87dea-107">Retrieves the file name (not including the path) of the currently selected file in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="87dea-108">La boîte de dialogue doit avoir été créée avec l’indicateur **OFN \_ Explorer** ; sinon, le message échoue.</span><span class="sxs-lookup"><span data-stu-id="87dea-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETSPEC             (CDM_FIRST + 0x0000)
```



## <a name="parameters"></a><span data-ttu-id="87dea-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87dea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87dea-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="87dea-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87dea-111">Taille, en caractères, de la mémoire tampon *lParam* .</span><span class="sxs-lookup"><span data-stu-id="87dea-111">The size, in characters, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="87dea-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="87dea-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87dea-113">Pointeur vers la mémoire tampon qui reçoit le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="87dea-113">A pointer to the buffer that receives the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87dea-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="87dea-114">Return value</span></span>

<span data-ttu-id="87dea-115">Si le message est correctement exécuté, la valeur de retour est la taille, en caractères, de la chaîne de nom de fichier, y compris le caractère NULL de fin.</span><span class="sxs-lookup"><span data-stu-id="87dea-115">If the message succeeds, the return value is the size, in characters, of the file name string, including the terminating NULL character.</span></span> <span data-ttu-id="87dea-116">Il s’agit du nombre d’octets ou de caractères copiés dans la mémoire tampon, ou de la taille de mémoire tampon requise si la mémoire tampon est trop petite.</span><span class="sxs-lookup"><span data-stu-id="87dea-116">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="87dea-117">Si une erreur se produit, la valeur de retour est inférieure à zéro.</span><span class="sxs-lookup"><span data-stu-id="87dea-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="87dea-118">Notes</span><span class="sxs-lookup"><span data-stu-id="87dea-118">Remarks</span></span>

<span data-ttu-id="87dea-119">La macro correspondante est la suivante :</span><span class="sxs-lookup"><span data-stu-id="87dea-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetSpec(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="87dea-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87dea-120">Requirements</span></span>



| <span data-ttu-id="87dea-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87dea-121">Requirement</span></span> | <span data-ttu-id="87dea-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="87dea-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87dea-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87dea-123">Minimum supported client</span></span><br/> | <span data-ttu-id="87dea-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87dea-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="87dea-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87dea-125">Minimum supported server</span></span><br/> | <span data-ttu-id="87dea-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87dea-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="87dea-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="87dea-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="87dea-128"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87dea-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87dea-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87dea-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="87dea-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="87dea-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="87dea-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="87dea-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="87dea-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="87dea-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="87dea-133">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="87dea-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="87dea-134">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="87dea-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="87dea-135">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="87dea-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

