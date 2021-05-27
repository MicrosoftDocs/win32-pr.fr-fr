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
ms.openlocfilehash: 7d531999757d46e127b73584adf1b563e64ea25b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548664"
---
# <a name="cdm_getfilepath-message"></a><span data-ttu-id="3153b-104">\_Message CDM GETFILEPATH</span><span class="sxs-lookup"><span data-stu-id="3153b-104">CDM\_GETFILEPATH message</span></span>

<span data-ttu-id="3153b-105">\[À compter de Windows Vista, les boîtes de dialogue **ouvrir** et **Enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="3153b-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="3153b-106">Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]</span><span class="sxs-lookup"><span data-stu-id="3153b-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="3153b-107">Récupère le chemin d’accès et le nom de fichier du fichier sélectionné dans une boîte de dialogue **ouvrir** ou **Enregistrer sous** de style Explorateur.</span><span class="sxs-lookup"><span data-stu-id="3153b-107">Retrieves the path and file name of the selected file in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="3153b-108">La boîte de dialogue doit avoir été créée avec l’indicateur **OFN \_ Explorer** ; sinon, le message échoue.</span><span class="sxs-lookup"><span data-stu-id="3153b-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFILEPATH         (CDM_FIRST + 0x0001)
```



## <a name="parameters"></a><span data-ttu-id="3153b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3153b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3153b-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3153b-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3153b-111">Taille, en caractères, de la mémoire tampon *lParam* .</span><span class="sxs-lookup"><span data-stu-id="3153b-111">The size, in characters, of the *lParam* buffer.</span></span> <span data-ttu-id="3153b-112">Pour la version ANSI, il s’agit du nombre d’octets ; pour la version Unicode, il s’agit du nombre de caractères.</span><span class="sxs-lookup"><span data-stu-id="3153b-112">For the ANSI version, this is the number of bytes; for the Unicode version, this is the number of characters.</span></span>

</dd> <dt>

<span data-ttu-id="3153b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3153b-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3153b-114">Pointeur vers la mémoire tampon qui reçoit le nom et le chemin d’accès du fichier.</span><span class="sxs-lookup"><span data-stu-id="3153b-114">A pointer to the buffer that receives the file name and path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3153b-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3153b-115">Return value</span></span>

<span data-ttu-id="3153b-116">Si le message est correctement exécuté, la valeur de retour est la taille, en caractères, du nom de fichier et de la chaîne de chemin d’accès, y compris le caractère NULL de fin.</span><span class="sxs-lookup"><span data-stu-id="3153b-116">If the message succeeds, the return value is the size, in characters, of the file name and path string, including the terminating NULL character.</span></span> <span data-ttu-id="3153b-117">Il s’agit du nombre d’octets ou de caractères copiés dans la mémoire tampon, ou de la taille de mémoire tampon requise si la mémoire tampon est trop petite.</span><span class="sxs-lookup"><span data-stu-id="3153b-117">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="3153b-118">Si une erreur se produit, la valeur de retour est inférieure à zéro.</span><span class="sxs-lookup"><span data-stu-id="3153b-118">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3153b-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="3153b-119">Remarks</span></span>

<span data-ttu-id="3153b-120">La macro correspondante est la suivante :</span><span class="sxs-lookup"><span data-stu-id="3153b-120">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFilePath(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="3153b-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3153b-121">Requirements</span></span>



| <span data-ttu-id="3153b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3153b-122">Requirement</span></span> | <span data-ttu-id="3153b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="3153b-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3153b-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3153b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3153b-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3153b-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3153b-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3153b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3153b-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3153b-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3153b-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="3153b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3153b-129"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3153b-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3153b-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3153b-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="3153b-131">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="3153b-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3153b-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="3153b-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="3153b-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="3153b-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="3153b-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="3153b-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="3153b-135">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="3153b-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3153b-136">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="3153b-136">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

