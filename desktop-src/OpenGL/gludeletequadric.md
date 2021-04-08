---
title: gluDeleteQuadric, fonction (Glu. h)
description: La fonction gluDeleteQuadric détruit un objet quadric.
ms.assetid: 09efd887-0fe8-4a56-bc6f-2177a4930035
keywords:
- gluDeleteQuadric fonction OpenGL
topic_type:
- apiref
api_name:
- gluDeleteQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b5ee85e943cd958e394efb191932393d228d948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742229"
---
# <a name="gludeletequadric-function"></a><span data-ttu-id="f9248-104">gluDeleteQuadric fonction)</span><span class="sxs-lookup"><span data-stu-id="f9248-104">gluDeleteQuadric function</span></span>

<span data-ttu-id="f9248-105">La fonction **gluDeleteQuadric** détruit un objet quadric.</span><span class="sxs-lookup"><span data-stu-id="f9248-105">The **gluDeleteQuadric** function destroys a quadric object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9248-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9248-106">Syntax</span></span>


```C++
void WINAPI gluDeleteQuadric(
   GLUquadricObj *state
);
```



## <a name="parameters"></a><span data-ttu-id="f9248-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9248-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9248-108">*state*</span><span class="sxs-lookup"><span data-stu-id="f9248-108">*state*</span></span> 
</dt> <dd>

<span data-ttu-id="f9248-109">Objet quadric à détruire (créé avec [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="f9248-109">The quadric object to be destroyed (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9248-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f9248-110">Return value</span></span>

<span data-ttu-id="f9248-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f9248-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9248-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f9248-112">Remarks</span></span>

<span data-ttu-id="f9248-113">La fonction **gluDeleteQuadric** détruit l’objet quadric et libère toute mémoire qu’il utilisait.</span><span class="sxs-lookup"><span data-stu-id="f9248-113">The **gluDeleteQuadric** function destroys the quadric object and frees any memory that it used.</span></span> <span data-ttu-id="f9248-114">Une fois que vous avez appelé **gluDeleteQuadric**, vous ne pouvez plus utiliser l' *État* .</span><span class="sxs-lookup"><span data-stu-id="f9248-114">After you have called **gluDeleteQuadric**, you cannot use *state* again.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9248-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9248-115">Requirements</span></span>



| <span data-ttu-id="f9248-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9248-116">Requirement</span></span> | <span data-ttu-id="f9248-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9248-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f9248-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9248-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f9248-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9248-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f9248-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9248-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f9248-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9248-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f9248-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9248-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9248-123"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9248-123"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="f9248-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f9248-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="f9248-125"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9248-125"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f9248-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f9248-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9248-127"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9248-127"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9248-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9248-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9248-129">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="f9248-129">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> </dl>

 

 





