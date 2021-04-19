---
title: Message d’CDM_HIDECONTROL (COMMDLG. h)
description: Masque le contrôle spécifié dans une boîte de dialogue Ouvrir ou enregistrer sous de style Explorateur.
ms.assetid: 5bf7f861-d38c-491a-89f0-5b3dfce8abfc
keywords:
- Boîtes de dialogue de CDM_HIDECONTROL message
topic_type:
- apiref
api_name:
- CDM_HIDECONTROL
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c0f2f41017373d9064da8f1024066f131063d9d
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590876"
---
# <a name="cdm_hidecontrol-message"></a><span data-ttu-id="24c41-104">\_Message CDM HIDECONTROL</span><span class="sxs-lookup"><span data-stu-id="24c41-104">CDM\_HIDECONTROL message</span></span>

<span data-ttu-id="24c41-105">\[À compter de Windows Vista, les boîtes de dialogue **ouvrir** et **Enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="24c41-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="24c41-106">Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]</span><span class="sxs-lookup"><span data-stu-id="24c41-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="24c41-107">Masque le contrôle spécifié dans une boîte de dialogue **ouvrir** ou **Enregistrer sous** de style Explorateur.</span><span class="sxs-lookup"><span data-stu-id="24c41-107">Hides the specified control in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="24c41-108">La boîte de dialogue doit avoir été créée avec l’indicateur **OFN \_ Explorer** ; sinon, le message échoue.</span><span class="sxs-lookup"><span data-stu-id="24c41-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_HIDECONTROL         (CDM_FIRST + 0x0005)
```



## <a name="parameters"></a><span data-ttu-id="24c41-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="24c41-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24c41-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24c41-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24c41-111">Identificateur du contrôle à masquer.</span><span class="sxs-lookup"><span data-stu-id="24c41-111">The identifier of the control to be hidden.</span></span>

</dd> <dt>

<span data-ttu-id="24c41-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24c41-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24c41-113">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="24c41-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24c41-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="24c41-114">Return value</span></span>

<span data-ttu-id="24c41-115">Ce message n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="24c41-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="24c41-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="24c41-116">Remarks</span></span>

<span data-ttu-id="24c41-117">La macro correspondante est la suivante :</span><span class="sxs-lookup"><span data-stu-id="24c41-117">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_HideControl(hwnd, wparam);
```

## <a name="requirements"></a><span data-ttu-id="24c41-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="24c41-118">Requirements</span></span>



| <span data-ttu-id="24c41-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24c41-119">Requirement</span></span> | <span data-ttu-id="24c41-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="24c41-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24c41-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24c41-121">Minimum supported client</span></span><br/> | <span data-ttu-id="24c41-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24c41-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="24c41-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24c41-123">Minimum supported server</span></span><br/> | <span data-ttu-id="24c41-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24c41-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="24c41-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="24c41-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="24c41-126"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24c41-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24c41-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24c41-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="24c41-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="24c41-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="24c41-129">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="24c41-129">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="24c41-130">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="24c41-130">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="24c41-131">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="24c41-131">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="24c41-132">**Conceptuel**</span><span class="sxs-lookup"><span data-stu-id="24c41-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="24c41-133">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="24c41-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

