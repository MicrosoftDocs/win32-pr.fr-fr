---
description: Reconstruit un pointeur vers une liste d’identificateurs d’éléments (PIDL) à partir d’une représentation hiérarchique du dossier de Shell dans une représentation différente.
title: 'IShellFolderViewType :: TranslateViewPidl, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.TranslateViewPidl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b7fa6c4-3d02-44ed-b63d-80a799e4017a
ms.openlocfilehash: 75876e5088c610c1f9f02ba9374db5cea4a6023c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527310"
---
# <a name="ishellfolderviewtypetranslateviewpidl-method"></a><span data-ttu-id="1920e-103">IShellFolderViewType :: TranslateViewPidl, méthode</span><span class="sxs-lookup"><span data-stu-id="1920e-103">IShellFolderViewType::TranslateViewPidl method</span></span>

<span data-ttu-id="1920e-104">Reconstruit un pointeur vers une liste d’identificateurs d’éléments (PIDL) à partir d’une représentation hiérarchique du dossier de Shell dans une représentation différente.</span><span class="sxs-lookup"><span data-stu-id="1920e-104">Reconstructs a pointer to an item identifier list (PIDL) from one hierarchical representation of the Shell folder into a different representation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1920e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1920e-105">Syntax</span></span>


```C++
HRESULT TranslateViewPidl(
  [in] PCUIDLIST_RELATIVE pidl,
  [in] PCUIDLIST_RELATIVE pidlView,
  [in] PCUIDLIST_RELATIVE *ppidlOut
);
```



## <a name="parameters"></a><span data-ttu-id="1920e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1920e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1920e-107">*PIDL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1920e-107">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1920e-108">Type : **PCUIDLIST \_ relatif**</span><span class="sxs-lookup"><span data-stu-id="1920e-108">Type: **PCUIDLIST\_RELATIVE**</span></span>

<span data-ttu-id="1920e-109">Tableau d’ID d’élément par rapport au dossier racine.</span><span class="sxs-lookup"><span data-stu-id="1920e-109">The array of item IDs relative to the root folder.</span></span>

</dd> <dt>

<span data-ttu-id="1920e-110">*pidlView* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1920e-110">*pidlView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1920e-111">Type : **PCUIDLIST \_ relatif**</span><span class="sxs-lookup"><span data-stu-id="1920e-111">Type: **PCUIDLIST\_RELATIVE**</span></span>

<span data-ttu-id="1920e-112">PIDL spéciale de la vue.</span><span class="sxs-lookup"><span data-stu-id="1920e-112">Special PIDL of the view.</span></span>

</dd> <dt>

<span data-ttu-id="1920e-113">*ppidlOut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1920e-113">*ppidlOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1920e-114">Type : \**PCUIDLIST \_ relatif \** _</span><span class="sxs-lookup"><span data-stu-id="1920e-114">Type: \**PCUIDLIST\_RELATIVE\** _</span></span>

<span data-ttu-id="1920e-115">Adresse d’une variable PIDL pour recevoir la traduction.</span><span class="sxs-lookup"><span data-stu-id="1920e-115">The address of a PIDL variable to receive the translation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1920e-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1920e-116">Return value</span></span>

<span data-ttu-id="1920e-117">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="1920e-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="1920e-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1920e-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1920e-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1920e-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1920e-120">Notes</span><span class="sxs-lookup"><span data-stu-id="1920e-120">Remarks</span></span>

<span data-ttu-id="1920e-121">Lorsque vous avez terminé, vous devez libérer le PIDL retourné avec [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree).</span><span class="sxs-lookup"><span data-stu-id="1920e-121">When finished, you should free the returned PIDL with [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="1920e-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1920e-122">Requirements</span></span>



| <span data-ttu-id="1920e-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1920e-123">Requirement</span></span> | <span data-ttu-id="1920e-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="1920e-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1920e-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1920e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1920e-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1920e-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1920e-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1920e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1920e-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1920e-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1920e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="1920e-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1920e-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1920e-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




