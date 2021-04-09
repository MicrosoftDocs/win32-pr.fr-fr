---
title: Message d’CDM_GETFOLDERPATH (COMMDLG. h)
description: Récupère le chemin d’accès du dossier ou du répertoire actuellement ouvert pour une boîte de dialogue Ouvrir ou enregistrer sous de style Explorateur.
ms.assetid: 7c3d4598-b45d-46c1-ad0d-cb0ecd20b3eb
keywords:
- Boîtes de dialogue de CDM_GETFOLDERPATH message
topic_type:
- apiref
api_name:
- CDM_GETFOLDERPATH
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff15e72d93e921968601f9c8472901d20769478
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942212"
---
# <a name="cdm_getfolderpath-message"></a><span data-ttu-id="5d261-104">\_Message CDM GETFOLDERPATH</span><span class="sxs-lookup"><span data-stu-id="5d261-104">CDM\_GETFOLDERPATH message</span></span>

<span data-ttu-id="5d261-105">\[À compter de Windows Vista, les boîtes de dialogue **ouvrir** et **Enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5d261-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="5d261-106">Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]</span><span class="sxs-lookup"><span data-stu-id="5d261-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="5d261-107">Récupère le chemin d’accès du dossier ou du répertoire actuellement ouvert pour une boîte de dialogue **ouvrir** ou **Enregistrer sous** de style Explorateur.</span><span class="sxs-lookup"><span data-stu-id="5d261-107">Retrieves the path of the currently open folder or directory for an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="5d261-108">La boîte de dialogue doit avoir été créée avec l’indicateur **OFN \_ Explorer** ; sinon, le message échoue.</span><span class="sxs-lookup"><span data-stu-id="5d261-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERPATH       (CDM_FIRST + 0x0002)
```



## <a name="parameters"></a><span data-ttu-id="5d261-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d261-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d261-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5d261-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d261-111">Taille, en caractères, de la mémoire tampon *lParam* .</span><span class="sxs-lookup"><span data-stu-id="5d261-111">The size, in characters, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5d261-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5d261-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d261-113">Pointeur vers la mémoire tampon qui reçoit le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="5d261-113">A pointer to the buffer that receives the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d261-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d261-114">Return value</span></span>

<span data-ttu-id="5d261-115">Si le message est correctement exécuté, la valeur de retour est la taille, en caractères, de la chaîne de chemin d’accès, y compris le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="5d261-115">If the message succeeds, the return value is the size, in characters, of the path string, including the terminating null character.</span></span> <span data-ttu-id="5d261-116">Il s’agit du nombre d’octets ou de caractères copiés dans la mémoire tampon, ou de la taille de mémoire tampon requise si la mémoire tampon est trop petite.</span><span class="sxs-lookup"><span data-stu-id="5d261-116">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="5d261-117">Si une erreur se produit, la valeur de retour est inférieure à zéro.</span><span class="sxs-lookup"><span data-stu-id="5d261-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d261-118">Notes</span><span class="sxs-lookup"><span data-stu-id="5d261-118">Remarks</span></span>

<span data-ttu-id="5d261-119">La macro correspondante est la suivante :</span><span class="sxs-lookup"><span data-stu-id="5d261-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFolderPath(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="5d261-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d261-120">Requirements</span></span>



| <span data-ttu-id="5d261-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d261-121">Requirement</span></span> | <span data-ttu-id="5d261-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d261-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d261-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d261-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5d261-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d261-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5d261-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d261-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5d261-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d261-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5d261-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d261-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d261-128"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d261-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d261-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d261-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="5d261-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="5d261-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5d261-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="5d261-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="5d261-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="5d261-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="5d261-133">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="5d261-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="5d261-134">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="5d261-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5d261-135">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="5d261-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

