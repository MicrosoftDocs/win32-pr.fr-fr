---
title: Message d’CDM_GETFOLDERIDLIST (COMMDLG. h)
description: Récupère l’adresse de la liste d’identificateurs d’éléments correspondant au dossier qu’une boîte de dialogue Ouvrir ou enregistrer sous d’un navigateur est actuellement ouverte.
ms.assetid: 9d2d2c35-ff1d-43de-ab0b-c96e0f1e9e24
keywords:
- Boîtes de dialogue de CDM_GETFOLDERIDLIST message
topic_type:
- apiref
api_name:
- CDM_GETFOLDERIDLIST
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb3ffff4f80dc21ed685e589ed4780b43592c2d2
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549704"
---
# <a name="cdm_getfolderidlist-message"></a><span data-ttu-id="99b73-104">\_Message CDM GETFOLDERIDLIST</span><span class="sxs-lookup"><span data-stu-id="99b73-104">CDM\_GETFOLDERIDLIST message</span></span>

<span data-ttu-id="99b73-105">\[À compter de Windows Vista, les boîtes de dialogue **ouvrir** et **Enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="99b73-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="99b73-106">Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]</span><span class="sxs-lookup"><span data-stu-id="99b73-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="99b73-107">Récupère l’adresse de la liste d’identificateurs d’éléments correspondant au dossier qu’une boîte de dialogue **ouvrir** ou **Enregistrer sous** d’un navigateur est actuellement ouverte.</span><span class="sxs-lookup"><span data-stu-id="99b73-107">Retrieves the address of the item identifier list corresponding to the folder that an Explorer-style **Open** or **Save As** dialog box currently has open.</span></span> <span data-ttu-id="99b73-108">La boîte de dialogue doit avoir été créée avec l’indicateur **OFN \_ Explorer** ; sinon, le message échoue.</span><span class="sxs-lookup"><span data-stu-id="99b73-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERIDLIST     (CDM_FIRST + 0x0003)
```



## <a name="parameters"></a><span data-ttu-id="99b73-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99b73-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99b73-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="99b73-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99b73-111">Taille, en octets, de la mémoire tampon *lParam* .</span><span class="sxs-lookup"><span data-stu-id="99b73-111">The size, in bytes, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="99b73-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="99b73-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99b73-113">Pointeur vers la mémoire tampon qui reçoit la liste d’identificateurs d’élément.</span><span class="sxs-lookup"><span data-stu-id="99b73-113">A pointer to the buffer that receives the list of item identifiers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99b73-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="99b73-114">Return value</span></span>

<span data-ttu-id="99b73-115">Si le message est correctement exécuté, la valeur de retour est la taille, en octets, de la liste d’identificateurs d’éléments.</span><span class="sxs-lookup"><span data-stu-id="99b73-115">If the message succeeds, the return value is the size, in bytes, of the list of item identifiers.</span></span> <span data-ttu-id="99b73-116">Il s’agit du nombre d’octets copiés dans la mémoire tampon, ou de la taille de mémoire tampon requise si la mémoire tampon est trop petite.</span><span class="sxs-lookup"><span data-stu-id="99b73-116">This is either the number of bytes copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="99b73-117">Si une erreur se produit, la valeur de retour est inférieure à zéro.</span><span class="sxs-lookup"><span data-stu-id="99b73-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="99b73-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="99b73-118">Remarks</span></span>

<span data-ttu-id="99b73-119">La macro correspondante est la suivante :</span><span class="sxs-lookup"><span data-stu-id="99b73-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFolderIDList(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="99b73-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="99b73-120">Requirements</span></span>



| <span data-ttu-id="99b73-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99b73-121">Requirement</span></span> | <span data-ttu-id="99b73-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="99b73-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99b73-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99b73-123">Minimum supported client</span></span><br/> | <span data-ttu-id="99b73-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="99b73-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="99b73-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99b73-125">Minimum supported server</span></span><br/> | <span data-ttu-id="99b73-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="99b73-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="99b73-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="99b73-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="99b73-128"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99b73-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99b73-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99b73-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="99b73-130">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="99b73-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="99b73-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="99b73-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="99b73-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="99b73-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="99b73-133">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="99b73-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="99b73-134">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="99b73-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="99b73-135">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="99b73-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

