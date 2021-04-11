---
title: gluOrtho2D, fonction (Glu. h)
description: La fonction gluOrtho2D définit une matrice de projection orthographique 2D.
ms.assetid: ba83fb5c-e5c7-4486-a815-a1aff0469757
keywords:
- gluOrtho2D fonction OpenGL
topic_type:
- apiref
api_name:
- gluOrtho2D
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a36b321f312a074a5dd78340968f1c9b2b844c6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383835"
---
# <a name="gluortho2d-function"></a><span data-ttu-id="a9e7b-104">gluOrtho2D fonction)</span><span class="sxs-lookup"><span data-stu-id="a9e7b-104">gluOrtho2D function</span></span>

<span data-ttu-id="a9e7b-105">La fonction **gluOrtho2D** définit une matrice de projection orthographique 2D.</span><span class="sxs-lookup"><span data-stu-id="a9e7b-105">The **gluOrtho2D** function defines a 2-D orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9e7b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9e7b-106">Syntax</span></span>


```C++
void WINAPI gluOrtho2D(
   GLdouble left,
   GLdouble right,
   GLdouble top,
   GLdouble bottom
);
```



## <a name="parameters"></a><span data-ttu-id="a9e7b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9e7b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9e7b-108">*gauche*</span><span class="sxs-lookup"><span data-stu-id="a9e7b-108">*left*</span></span> 
</dt> <dd>

<span data-ttu-id="a9e7b-109">Coordonnée du plan de découpage vertical gauche.</span><span class="sxs-lookup"><span data-stu-id="a9e7b-109">The coordinate for the left vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="a9e7b-110">*Oui*</span><span class="sxs-lookup"><span data-stu-id="a9e7b-110">*right*</span></span> 
</dt> <dd>

<span data-ttu-id="a9e7b-111">Coordonnée du plan de découpage vertical droit.</span><span class="sxs-lookup"><span data-stu-id="a9e7b-111">The coordinate for the right vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="a9e7b-112">*top*</span><span class="sxs-lookup"><span data-stu-id="a9e7b-112">*top*</span></span> 
</dt> <dd>

<span data-ttu-id="a9e7b-113">Coordonnée du plan de découpage horizontal supérieur.</span><span class="sxs-lookup"><span data-stu-id="a9e7b-113">The coordinate for the top horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="a9e7b-114">*ballon*</span><span class="sxs-lookup"><span data-stu-id="a9e7b-114">*bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="a9e7b-115">Coordonnée du plan de découpage horizontal inférieur.</span><span class="sxs-lookup"><span data-stu-id="a9e7b-115">The coordinate for the bottom horizontal clipping plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9e7b-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a9e7b-116">Return value</span></span>

<span data-ttu-id="a9e7b-117">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a9e7b-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9e7b-118">Notes</span><span class="sxs-lookup"><span data-stu-id="a9e7b-118">Remarks</span></span>

<span data-ttu-id="a9e7b-119">La fonction **gluOrtho2D** définit une zone d’affichage orthographique à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="a9e7b-119">The **gluOrtho2D** function sets up a two-dimensional orthographic viewing region.</span></span> <span data-ttu-id="a9e7b-120">Cela équivaut à appeler [**glOrtho**](glortho.md) avec near = 1 et Far = 1.</span><span class="sxs-lookup"><span data-stu-id="a9e7b-120">This is equivalent to calling [**glOrtho**](glortho.md) with near =  1 and far = 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9e7b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9e7b-121">Requirements</span></span>



| <span data-ttu-id="a9e7b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9e7b-122">Requirement</span></span> | <span data-ttu-id="a9e7b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9e7b-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a9e7b-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9e7b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a9e7b-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9e7b-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a9e7b-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9e7b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a9e7b-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9e7b-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a9e7b-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="a9e7b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9e7b-129"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9e7b-129"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="a9e7b-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a9e7b-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="a9e7b-131"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9e7b-131"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a9e7b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a9e7b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9e7b-133"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9e7b-133"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9e7b-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9e7b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9e7b-135">**glOrtho**</span><span class="sxs-lookup"><span data-stu-id="a9e7b-135">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="a9e7b-136">**gluPerspective**</span><span class="sxs-lookup"><span data-stu-id="a9e7b-136">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





