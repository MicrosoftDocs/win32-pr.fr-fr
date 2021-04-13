---
title: Message EM_INSERTIMAGE (RichEdit. h)
description: Remplace la sélection par un objet BLOB qui affiche une image.
ms.assetid: 147B298B-C4A9-455B-9736-A0B09D72902B
keywords:
- EM_INSERTIMAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_INSERTIMAGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9ff1e0fd355cf5dd8d43d211c44fda6417c638
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464535"
---
# <a name="em_insertimage-message"></a><span data-ttu-id="0dc9f-104">\_Message INSERTIMAGE em</span><span class="sxs-lookup"><span data-stu-id="0dc9f-104">EM\_INSERTIMAGE message</span></span>

<span data-ttu-id="0dc9f-105">Remplace la sélection par un objet BLOB qui affiche une image.</span><span class="sxs-lookup"><span data-stu-id="0dc9f-105">Replaces the selection with a blob that displays an image.</span></span>


```C++
#define EM_INSERTIMAGE       (WM_USER + 314)
```



## <a name="parameters"></a><span data-ttu-id="0dc9f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0dc9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dc9f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0dc9f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0dc9f-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="0dc9f-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0dc9f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0dc9f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0dc9f-110">Pointeur vers une structure [**de \_ \_ paramètres d’image RichEdit**](/windows/win32/api/richedit/ns-richedit-richedit_image_parameters) qui contient l’objet blob d’image.</span><span class="sxs-lookup"><span data-stu-id="0dc9f-110">A pointer to a [**RICHEDIT\_IMAGE\_PARAMETERS**](/windows/win32/api/richedit/ns-richedit-richedit_image_parameters) structure that contains the image blob.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dc9f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0dc9f-111">Return value</span></span>

<span data-ttu-id="0dc9f-112">Retourne S \_ OK en cas de réussite, ou l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="0dc9f-112">Returns S\_OK if successful, or one of the following error codes.</span></span>



| <span data-ttu-id="0dc9f-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0dc9f-113">Return code</span></span>                                                                                    | <span data-ttu-id="0dc9f-114">Description</span><span class="sxs-lookup"><span data-stu-id="0dc9f-114">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="0dc9f-115"><dt>**E \_ ÉCHEC**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9f-115"><dt>**E\_FAIL** </dt></span></span> </dl>        | <span data-ttu-id="0dc9f-116">Impossible d’insérer l’image.</span><span class="sxs-lookup"><span data-stu-id="0dc9f-116">Cannot insert the image.</span></span> <br/>                          |
| <dl> <span data-ttu-id="0dc9f-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9f-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="0dc9f-118">Le paramètre *lParam* a la valeur null ou pointe vers une image non valide.</span><span class="sxs-lookup"><span data-stu-id="0dc9f-118">The *lParam* parameter is NULL or points to an invalid image.</span></span> |
| <dl> <span data-ttu-id="0dc9f-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9f-119"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl> | <span data-ttu-id="0dc9f-120">La mémoire disponible est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="0dc9f-120">Insufficient memory is available.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="0dc9f-121">Notes</span><span class="sxs-lookup"><span data-stu-id="0dc9f-121">Remarks</span></span>

<span data-ttu-id="0dc9f-122">Si la sélection est un point d’insertion, l’objet blob d’image est inséré au point d’insertion.</span><span class="sxs-lookup"><span data-stu-id="0dc9f-122">If the selection is an insertion point, the image blob is inserted at the insertion point.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dc9f-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0dc9f-123">Requirements</span></span>



| <span data-ttu-id="0dc9f-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0dc9f-124">Requirement</span></span> | <span data-ttu-id="0dc9f-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="0dc9f-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0dc9f-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0dc9f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0dc9f-127">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0dc9f-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0dc9f-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0dc9f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0dc9f-129">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0dc9f-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0dc9f-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="0dc9f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0dc9f-131"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0dc9f-131"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0dc9f-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0dc9f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dc9f-133">**\_INSERTTABLE em**</span><span class="sxs-lookup"><span data-stu-id="0dc9f-133">**EM\_INSERTTABLE**</span></span>](em-inserttable.md)
</dt> </dl>

 

 





