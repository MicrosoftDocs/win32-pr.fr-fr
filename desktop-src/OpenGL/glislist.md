---
title: fonction glIsList (GL. h)
description: La fonction gllsList teste l’existence de la liste d’affichage.
ms.assetid: 86ef3684-8047-4ee4-befd-ec26bcd036c3
keywords:
- glIsList fonction OpenGL
topic_type:
- apiref
api_name:
- glIsList
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fdc67d0a7dad18f8850c283f0d5eb224ff9ebbd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317390"
---
# <a name="glislist-function"></a><span data-ttu-id="e414f-104">glIsList fonction)</span><span class="sxs-lookup"><span data-stu-id="e414f-104">glIsList function</span></span>

<span data-ttu-id="e414f-105">La fonction **gllsList** teste l’existence de la liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="e414f-105">The **gllsList** function tests for display list existence.</span></span>

## <a name="syntax"></a><span data-ttu-id="e414f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e414f-106">Syntax</span></span>


```C++
GLboolean WINAPI glIsList(
   GLuint list
);
```



## <a name="parameters"></a><span data-ttu-id="e414f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e414f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e414f-108">*list*</span><span class="sxs-lookup"><span data-stu-id="e414f-108">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="e414f-109">Nom de la liste d’affichage potentielle.</span><span class="sxs-lookup"><span data-stu-id="e414f-109">A potential display list name.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="e414f-110">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="e414f-110">Error codes</span></span>

<span data-ttu-id="e414f-111">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="e414f-111">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e414f-112">Nom</span><span class="sxs-lookup"><span data-stu-id="e414f-112">Name</span></span>                                                                                                  | <span data-ttu-id="e414f-113">Signification</span><span class="sxs-lookup"><span data-stu-id="e414f-113">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e414f-114"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e414f-114"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e414f-115">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="e414f-115">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e414f-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e414f-116">Remarks</span></span>

<span data-ttu-id="e414f-117">La fonction **gllsList** retourne GL \_ true si *List* est le nom d’une liste d’affichage et retourne la \_ valeur GL false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e414f-117">The **gllsList** function returns GL\_TRUE if *list* is the name of a display list and returns GL\_FALSE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e414f-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e414f-118">Requirements</span></span>



| <span data-ttu-id="e414f-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e414f-119">Requirement</span></span> | <span data-ttu-id="e414f-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e414f-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e414f-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e414f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e414f-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e414f-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e414f-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e414f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e414f-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e414f-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e414f-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="e414f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e414f-126"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e414f-126"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e414f-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e414f-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="e414f-128"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e414f-128"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e414f-129">DLL</span><span class="sxs-lookup"><span data-stu-id="e414f-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e414f-130"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e414f-130"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e414f-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e414f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e414f-132">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e414f-132">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e414f-133">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="e414f-133">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="e414f-134">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="e414f-134">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="e414f-135">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="e414f-135">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="e414f-136">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e414f-136">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e414f-137">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="e414f-137">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="e414f-138">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="e414f-138">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 





