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
ms.openlocfilehash: 1bd5706e0bccf0b61c0737ef54d6e227e5593bc9
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590856"
---
# <a name="cdm_setdefext-message"></a><span data-ttu-id="4b9c2-104">\_Message CDM SETDEFEXT</span><span class="sxs-lookup"><span data-stu-id="4b9c2-104">CDM\_SETDEFEXT message</span></span>

<span data-ttu-id="4b9c2-105">\[À compter de Windows Vista, les boîtes de dialogue **ouvrir** et **Enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="4b9c2-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="4b9c2-106">Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]</span><span class="sxs-lookup"><span data-stu-id="4b9c2-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="4b9c2-107">Définit l’extension de nom de fichier par défaut pour une boîte de dialogue **ouvrir** ou **Enregistrer sous** de style Explorateur.</span><span class="sxs-lookup"><span data-stu-id="4b9c2-107">Sets the default file name extension for an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="4b9c2-108">La boîte de dialogue doit avoir été créée avec l’indicateur **OFN \_ Explorer** ; sinon, le message échoue.</span><span class="sxs-lookup"><span data-stu-id="4b9c2-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETDEFEXT           (CDM_FIRST + 0x0006)
```



## <a name="parameters"></a><span data-ttu-id="4b9c2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b9c2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b9c2-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4b9c2-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b9c2-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="4b9c2-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4b9c2-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4b9c2-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b9c2-113">Pointeur vers la nouvelle extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="4b9c2-113">A pointer to the new file name extension.</span></span> <span data-ttu-id="4b9c2-114">Ne doit pas inclure le point (.).</span><span class="sxs-lookup"><span data-stu-id="4b9c2-114">Must not include the dot (.).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b9c2-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4b9c2-115">Return value</span></span>

<span data-ttu-id="4b9c2-116">Ce message n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="4b9c2-116">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b9c2-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="4b9c2-117">Remarks</span></span>

<span data-ttu-id="4b9c2-118">La macro correspondante est la suivante :</span><span class="sxs-lookup"><span data-stu-id="4b9c2-118">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_SetDefExt(hwnd, lparam)
```

## <a name="requirements"></a><span data-ttu-id="4b9c2-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4b9c2-119">Requirements</span></span>



| <span data-ttu-id="4b9c2-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b9c2-120">Requirement</span></span> | <span data-ttu-id="4b9c2-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b9c2-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b9c2-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b9c2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4b9c2-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b9c2-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4b9c2-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b9c2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4b9c2-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b9c2-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4b9c2-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="4b9c2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b9c2-127"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b9c2-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b9c2-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b9c2-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="4b9c2-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="4b9c2-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4b9c2-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="4b9c2-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="4b9c2-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="4b9c2-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="4b9c2-132">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="4b9c2-132">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="4b9c2-133">**Conceptuel**</span><span class="sxs-lookup"><span data-stu-id="4b9c2-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4b9c2-134">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="4b9c2-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

