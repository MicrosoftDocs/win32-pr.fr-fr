---
title: Message d’CDM_GETFILEPATH (COMMDLG. h)
description: Récupère le chemin d’accès et le nom de fichier du fichier sélectionné dans une boîte de dialogue Ouvrir ou enregistrer sous de style Explorateur.
ms.assetid: fad8c5e2-9838-45a8-8c51-4326c989d939
keywords:
- Boîtes de dialogue de CDM_GETFILEPATH message
topic_type:
- apiref
api_name:
- CDM_GETFILEPATH
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b7cc278d1d5a2305b3d2a311ce9c82886f9b7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942604"
---
# <a name="cdm_getfilepath-message"></a><span data-ttu-id="4a6f2-104">\_Message CDM GETFILEPATH</span><span class="sxs-lookup"><span data-stu-id="4a6f2-104">CDM\_GETFILEPATH message</span></span>

<span data-ttu-id="4a6f2-105">\[À compter de Windows Vista, les boîtes de dialogue **ouvrir** et **Enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4a6f2-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="4a6f2-106">Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]</span><span class="sxs-lookup"><span data-stu-id="4a6f2-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="4a6f2-107">Récupère le chemin d’accès et le nom de fichier du fichier sélectionné dans une boîte de dialogue **ouvrir** ou **Enregistrer sous** de style Explorateur.</span><span class="sxs-lookup"><span data-stu-id="4a6f2-107">Retrieves the path and file name of the selected file in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="4a6f2-108">La boîte de dialogue doit avoir été créée avec l’indicateur **OFN \_ Explorer** ; sinon, le message échoue.</span><span class="sxs-lookup"><span data-stu-id="4a6f2-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFILEPATH         (CDM_FIRST + 0x0001)
```



## <a name="parameters"></a><span data-ttu-id="4a6f2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a6f2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a6f2-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4a6f2-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a6f2-111">Taille, en caractères, de la mémoire tampon *lParam* .</span><span class="sxs-lookup"><span data-stu-id="4a6f2-111">The size, in characters, of the *lParam* buffer.</span></span> <span data-ttu-id="4a6f2-112">Pour la version ANSI, il s’agit du nombre d’octets ; pour la version Unicode, il s’agit du nombre de caractères.</span><span class="sxs-lookup"><span data-stu-id="4a6f2-112">For the ANSI version, this is the number of bytes; for the Unicode version, this is the number of characters.</span></span>

</dd> <dt>

<span data-ttu-id="4a6f2-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4a6f2-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a6f2-114">Pointeur vers la mémoire tampon qui reçoit le nom et le chemin d’accès du fichier.</span><span class="sxs-lookup"><span data-stu-id="4a6f2-114">A pointer to the buffer that receives the file name and path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a6f2-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4a6f2-115">Return value</span></span>

<span data-ttu-id="4a6f2-116">Si le message est correctement exécuté, la valeur de retour est la taille, en caractères, du nom de fichier et de la chaîne de chemin d’accès, y compris le caractère NULL de fin.</span><span class="sxs-lookup"><span data-stu-id="4a6f2-116">If the message succeeds, the return value is the size, in characters, of the file name and path string, including the terminating NULL character.</span></span> <span data-ttu-id="4a6f2-117">Il s’agit du nombre d’octets ou de caractères copiés dans la mémoire tampon, ou de la taille de mémoire tampon requise si la mémoire tampon est trop petite.</span><span class="sxs-lookup"><span data-stu-id="4a6f2-117">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="4a6f2-118">Si une erreur se produit, la valeur de retour est inférieure à zéro.</span><span class="sxs-lookup"><span data-stu-id="4a6f2-118">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a6f2-119">Notes</span><span class="sxs-lookup"><span data-stu-id="4a6f2-119">Remarks</span></span>

<span data-ttu-id="4a6f2-120">La macro correspondante est la suivante :</span><span class="sxs-lookup"><span data-stu-id="4a6f2-120">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFilePath(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="4a6f2-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a6f2-121">Requirements</span></span>



| <span data-ttu-id="4a6f2-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a6f2-122">Requirement</span></span> | <span data-ttu-id="4a6f2-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a6f2-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a6f2-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a6f2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4a6f2-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a6f2-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4a6f2-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a6f2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4a6f2-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a6f2-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4a6f2-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="4a6f2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a6f2-129"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a6f2-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a6f2-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a6f2-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="4a6f2-131">**Référence**</span><span class="sxs-lookup"><span data-stu-id="4a6f2-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4a6f2-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="4a6f2-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="4a6f2-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="4a6f2-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="4a6f2-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="4a6f2-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="4a6f2-135">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="4a6f2-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4a6f2-136">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="4a6f2-136">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

