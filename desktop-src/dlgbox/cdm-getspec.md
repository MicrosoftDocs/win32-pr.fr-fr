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
ms.openlocfilehash: 938536ea7cc72ebb950420ad3d5c9bd35c64db72
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590926"
---
# <a name="cdm_getspec-message"></a><span data-ttu-id="ad0b1-104">\_Message CDM GETSPEC</span><span class="sxs-lookup"><span data-stu-id="ad0b1-104">CDM\_GETSPEC message</span></span>

<span data-ttu-id="ad0b1-105">\[À compter de Windows Vista, les boîtes de dialogue **ouvrir** et **Enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="ad0b1-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="ad0b1-106">Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]</span><span class="sxs-lookup"><span data-stu-id="ad0b1-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="ad0b1-107">Récupère le nom de fichier (sans le chemin d’accès) du fichier actuellement sélectionné dans une boîte de dialogue **ouvrir** ou **Enregistrer sous** de style Explorateur.</span><span class="sxs-lookup"><span data-stu-id="ad0b1-107">Retrieves the file name (not including the path) of the currently selected file in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="ad0b1-108">La boîte de dialogue doit avoir été créée avec l’indicateur **OFN \_ Explorer** ; sinon, le message échoue.</span><span class="sxs-lookup"><span data-stu-id="ad0b1-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETSPEC             (CDM_FIRST + 0x0000)
```



## <a name="parameters"></a><span data-ttu-id="ad0b1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad0b1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad0b1-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ad0b1-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad0b1-111">Taille, en caractères, de la mémoire tampon *lParam* .</span><span class="sxs-lookup"><span data-stu-id="ad0b1-111">The size, in characters, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ad0b1-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ad0b1-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad0b1-113">Pointeur vers la mémoire tampon qui reçoit le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="ad0b1-113">A pointer to the buffer that receives the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad0b1-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ad0b1-114">Return value</span></span>

<span data-ttu-id="ad0b1-115">Si le message est correctement exécuté, la valeur de retour est la taille, en caractères, de la chaîne de nom de fichier, y compris le caractère NULL de fin.</span><span class="sxs-lookup"><span data-stu-id="ad0b1-115">If the message succeeds, the return value is the size, in characters, of the file name string, including the terminating NULL character.</span></span> <span data-ttu-id="ad0b1-116">Il s’agit du nombre d’octets ou de caractères copiés dans la mémoire tampon, ou de la taille de mémoire tampon requise si la mémoire tampon est trop petite.</span><span class="sxs-lookup"><span data-stu-id="ad0b1-116">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="ad0b1-117">Si une erreur se produit, la valeur de retour est inférieure à zéro.</span><span class="sxs-lookup"><span data-stu-id="ad0b1-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad0b1-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="ad0b1-118">Remarks</span></span>

<span data-ttu-id="ad0b1-119">La macro correspondante est la suivante :</span><span class="sxs-lookup"><span data-stu-id="ad0b1-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetSpec(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="ad0b1-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ad0b1-120">Requirements</span></span>



| <span data-ttu-id="ad0b1-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad0b1-121">Requirement</span></span> | <span data-ttu-id="ad0b1-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad0b1-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad0b1-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad0b1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ad0b1-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad0b1-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ad0b1-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad0b1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ad0b1-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad0b1-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ad0b1-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad0b1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad0b1-128"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad0b1-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad0b1-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad0b1-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="ad0b1-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="ad0b1-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ad0b1-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="ad0b1-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="ad0b1-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="ad0b1-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="ad0b1-133">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="ad0b1-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="ad0b1-134">**Conceptuel**</span><span class="sxs-lookup"><span data-stu-id="ad0b1-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ad0b1-135">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="ad0b1-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

