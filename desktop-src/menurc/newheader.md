---
title: NEWHEADER, structure
description: Contient le nombre de composants icône ou curseur dans un groupe de ressources. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: 1549579a-b558-42a9-9b3b-5b382334221c
keywords:
- Menus de la structure NEWHEADER et autres ressources
topic_type:
- apiref
api_name:
- NEWHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d215bc00ef414d4e626d3da657dcecfd7a8a6c8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941804"
---
# <a name="newheader-structure"></a><span data-ttu-id="67d13-105">NEWHEADER, structure</span><span class="sxs-lookup"><span data-stu-id="67d13-105">NEWHEADER structure</span></span>

<span data-ttu-id="67d13-106">Contient le nombre de composants icône ou curseur dans un groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="67d13-106">Contains the number of icon or cursor components in a resource group.</span></span> <span data-ttu-id="67d13-107">La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.</span><span class="sxs-lookup"><span data-stu-id="67d13-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="67d13-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67d13-108">Syntax</span></span>


```C++
typedef struct {
  WORD Reserved;
  WORD ResType;
  WORD ResCount;
} NEWHEADER, *NEWHEADER;
```



## <a name="members"></a><span data-ttu-id="67d13-109">Membres</span><span class="sxs-lookup"><span data-stu-id="67d13-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="67d13-110">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="67d13-110">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="67d13-111">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="67d13-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="67d13-112">Réservé doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="67d13-112">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="67d13-113">**ResType**</span><span class="sxs-lookup"><span data-stu-id="67d13-113">**ResType**</span></span>
</dt> <dd>

<span data-ttu-id="67d13-114">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="67d13-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="67d13-115">Type de ressource.</span><span class="sxs-lookup"><span data-stu-id="67d13-115">The resource type.</span></span> <span data-ttu-id="67d13-116">Ce membre doit avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="67d13-116">This member must have one of the following values.</span></span>



| <span data-ttu-id="67d13-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="67d13-117">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="67d13-118">Signification</span><span class="sxs-lookup"><span data-stu-id="67d13-118">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="RES_CURSOR"></span><span id="res_cursor"></span><dl> <span data-ttu-id="67d13-119"><dt>**Ressource \_ CURSEUR**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="67d13-119"><dt>**RES\_CURSOR**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="67d13-120">Type de ressource de curseur.</span><span class="sxs-lookup"><span data-stu-id="67d13-120">Cursor resource type.</span></span><br/> |
| <span id="RES_ICON"></span><span id="res_icon"></span><dl> <span data-ttu-id="67d13-121"><dt>**Ressource \_ ICÔNE**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="67d13-121"><dt>**RES\_ICON**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="67d13-122">Type de ressource d’icône.</span><span class="sxs-lookup"><span data-stu-id="67d13-122">Icon resource type.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="67d13-123">**ResCount**</span><span class="sxs-lookup"><span data-stu-id="67d13-123">**ResCount**</span></span>
</dt> <dd>

<span data-ttu-id="67d13-124">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="67d13-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="67d13-125">Nombre de composants icône ou curseur dans le groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="67d13-125">The number of icon or cursor components in the resource group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67d13-126">Notes</span><span class="sxs-lookup"><span data-stu-id="67d13-126">Remarks</span></span>

<span data-ttu-id="67d13-127">Une ou plusieurs structures [**RESDIR**](resdir.md) suivent immédiatement la structure **NEWHEADER** dans le fichier. res.</span><span class="sxs-lookup"><span data-stu-id="67d13-127">One or more [**RESDIR**](resdir.md) structures immediately follow the **NEWHEADER** structure in the .res file.</span></span> <span data-ttu-id="67d13-128">Le membre **ResCount** spécifie le nombre de structures **RESDIR** .</span><span class="sxs-lookup"><span data-stu-id="67d13-128">The **ResCount** member specifies the number of **RESDIR** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="67d13-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67d13-129">Requirements</span></span>



| <span data-ttu-id="67d13-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67d13-130">Requirement</span></span> | <span data-ttu-id="67d13-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="67d13-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="67d13-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67d13-132">Minimum supported client</span></span><br/> | <span data-ttu-id="67d13-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67d13-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="67d13-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67d13-134">Minimum supported server</span></span><br/> | <span data-ttu-id="67d13-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67d13-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="67d13-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67d13-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="67d13-137">**Référence**</span><span class="sxs-lookup"><span data-stu-id="67d13-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="67d13-138">**RESDIR**</span><span class="sxs-lookup"><span data-stu-id="67d13-138">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="67d13-139">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="67d13-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="67d13-140">Ressources</span><span class="sxs-lookup"><span data-stu-id="67d13-140">Resources</span></span>](resources.md)
</dt> </dl>

 

 





