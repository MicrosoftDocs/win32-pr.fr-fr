---
description: La structure FORM_INFO_1 contient des informations sur un formulaire d’impression. Les informations incluent l’origine des formulaires imprimés, son nom, ses dimensions et les dimensions de sa zone imprimable.
ms.assetid: 1c42ea6c-82cf-463c-bc67-44a8d8c4a1e7
title: Structure FORM_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_1
- _FORM_INFO_1A
- _FORM_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 516f646d664a034f81a76eb2262b3ea8c950a87e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529272"
---
# <a name="form_info_1-structure"></a><span data-ttu-id="8911d-104">Structure FORM_INFO_1</span><span class="sxs-lookup"><span data-stu-id="8911d-104">FORM_INFO_1 structure</span></span>

<span data-ttu-id="8911d-105">La structure **FORM_INFO_1** contient des informations sur un formulaire d’impression.</span><span class="sxs-lookup"><span data-stu-id="8911d-105">The **FORM_INFO_1** structure contains information about a print form.</span></span> <span data-ttu-id="8911d-106">Les informations incluent l’origine du formulaire d’impression, son nom, ses dimensions et les dimensions de sa zone imprimable.</span><span class="sxs-lookup"><span data-stu-id="8911d-106">The information includes the print form's origin, its name, its dimensions, and the dimensions of its printable area.</span></span>

## <a name="syntax"></a><span data-ttu-id="8911d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8911d-107">Syntax</span></span>


```C++
typedef struct _FORM_INFO_1 {
  DWORD  Flags;
  LPTSTR pName;
  SIZEL  Size;
  RECTL  ImageableArea;
} FORM_INFO_1, *PFORM_INFO_1;
```



## <a name="members"></a><span data-ttu-id="8911d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="8911d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8911d-109">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="8911d-109">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="8911d-110">Propriétés du formulaire.</span><span class="sxs-lookup"><span data-stu-id="8911d-110">The form properties.</span></span> <span data-ttu-id="8911d-111">Les valeurs suivantes sont définies.</span><span class="sxs-lookup"><span data-stu-id="8911d-111">The following values are defined.</span></span>



| <span data-ttu-id="8911d-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="8911d-112">Value</span></span>         | <span data-ttu-id="8911d-113">Signification</span><span class="sxs-lookup"><span data-stu-id="8911d-113">Meaning</span></span>                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8911d-114">FORM_USER</span><span class="sxs-lookup"><span data-stu-id="8911d-114">FORM_USER</span></span>    | <span data-ttu-id="8911d-115">Si cet indicateur de bit est défini, le formulaire a été défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8911d-115">If this bit flag is set, the form has been defined by the user.</span></span> <span data-ttu-id="8911d-116">Les formulaires avec cet indicateur défini sont définis dans le registre.</span><span class="sxs-lookup"><span data-stu-id="8911d-116">Forms with this flag set are defined in the registry.</span></span>        |
| <span data-ttu-id="8911d-117">FORM_BUILTIN</span><span class="sxs-lookup"><span data-stu-id="8911d-117">FORM_BUILTIN</span></span> | <span data-ttu-id="8911d-118">Si cet indicateur de bit est défini, le formulaire fait partie du spouleur.</span><span class="sxs-lookup"><span data-stu-id="8911d-118">If this bit-flag is set, the form is part of the spooler.</span></span> <span data-ttu-id="8911d-119">Les définitions de formulaire pour lesquelles cet indicateur est défini n’apparaissent pas dans le registre.</span><span class="sxs-lookup"><span data-stu-id="8911d-119">Form definitions with this flag set do not appear in the registry.</span></span> |
| <span data-ttu-id="8911d-120">FORM_PRINTER</span><span class="sxs-lookup"><span data-stu-id="8911d-120">FORM_PRINTER</span></span> | <span data-ttu-id="8911d-121">Si cet indicateur de bit est défini, le formulaire est associé à une certaine imprimante et sa définition apparaît dans le registre.</span><span class="sxs-lookup"><span data-stu-id="8911d-121">If this bit flag is set, the form is associated with a certain printer, and its definition appears in the registry.</span></span>          |



 

</dd> <dt>

<span data-ttu-id="8911d-122">**pName**</span><span class="sxs-lookup"><span data-stu-id="8911d-122">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="8911d-123">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du formulaire.</span><span class="sxs-lookup"><span data-stu-id="8911d-123">Pointer to a null-terminated string that specifies the name of the form.</span></span> <span data-ttu-id="8911d-124">Le nom du formulaire ne peut pas dépasser 31 caractères.</span><span class="sxs-lookup"><span data-stu-id="8911d-124">The form name cannot exceed 31 characters.</span></span>

</dd> <dt>

<span data-ttu-id="8911d-125">**Taille**</span><span class="sxs-lookup"><span data-stu-id="8911d-125">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="8911d-126">Largeur et hauteur, en millièmes de millimètres, du formulaire.</span><span class="sxs-lookup"><span data-stu-id="8911d-126">The width and height, in thousandths of millimeters, of the form.</span></span>

</dd> <dt>

<span data-ttu-id="8911d-127">**ImageableArea**</span><span class="sxs-lookup"><span data-stu-id="8911d-127">**ImageableArea**</span></span>
</dt> <dd>

<span data-ttu-id="8911d-128">Largeur et hauteur, en millièmes de millimètres, du formulaire.</span><span class="sxs-lookup"><span data-stu-id="8911d-128">The width and height, in thousandths of millimeters, of the form.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8911d-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8911d-129">Requirements</span></span>



| <span data-ttu-id="8911d-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8911d-130">Requirement</span></span> | <span data-ttu-id="8911d-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="8911d-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8911d-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8911d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8911d-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8911d-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8911d-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8911d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8911d-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8911d-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8911d-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="8911d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="8911d-137"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8911d-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8911d-138">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="8911d-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8911d-139">**_FORM_INFO_1W** (Unicode) et **_FORM_INFO_1A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8911d-139">**_FORM_INFO_1W** (Unicode) and **_FORM_INFO_1A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="8911d-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8911d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8911d-141">Impression</span><span class="sxs-lookup"><span data-stu-id="8911d-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8911d-142">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="8911d-142">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="8911d-143">**AddForm**</span><span class="sxs-lookup"><span data-stu-id="8911d-143">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="8911d-144">**GetForm**</span><span class="sxs-lookup"><span data-stu-id="8911d-144">**GetForm**</span></span>](getform.md)
</dt> <dt>

[<span data-ttu-id="8911d-145">**SetForm**</span><span class="sxs-lookup"><span data-stu-id="8911d-145">**SetForm**</span></span>](setform.md)
</dt> </dl>

 

 




