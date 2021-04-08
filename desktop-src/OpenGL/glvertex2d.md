---
title: fonction glVertex2d (GL. h)
description: Spécifie un sommet. | fonction glVertex2d (GL. h)
ms.assetid: 96398c2a-35d9-4e40-8471-28a1630c81fd
keywords:
- glVertex2d fonction OpenGL
topic_type:
- apiref
api_name:
- glVertex2d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c44a70716fdf19ef40564e359530bbdf5bcdc85
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761696"
---
# <a name="glvertex2d-function"></a><span data-ttu-id="96b65-105">glVertex2d fonction)</span><span class="sxs-lookup"><span data-stu-id="96b65-105">glVertex2d function</span></span>

<span data-ttu-id="96b65-106">Spécifie un sommet.</span><span class="sxs-lookup"><span data-stu-id="96b65-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="96b65-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96b65-107">Syntax</span></span>


```C++
void WINAPI glVertex2d(
   GLdouble x,
   GLdouble y
);
```



## <a name="parameters"></a><span data-ttu-id="96b65-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96b65-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96b65-109">*x*</span><span class="sxs-lookup"><span data-stu-id="96b65-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="96b65-110">Spécifie la coordonnée x d’un vertex.</span><span class="sxs-lookup"><span data-stu-id="96b65-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="96b65-111">*y*</span><span class="sxs-lookup"><span data-stu-id="96b65-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="96b65-112">Spécifie la coordonnée y d’un vertex.</span><span class="sxs-lookup"><span data-stu-id="96b65-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96b65-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="96b65-113">Return value</span></span>

<span data-ttu-id="96b65-114">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="96b65-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="96b65-115">Notes</span><span class="sxs-lookup"><span data-stu-id="96b65-115">Remarks</span></span>

<span data-ttu-id="96b65-116">Les commandes de fonction glVertex sont utilisées dans les paires [**glBegin**](glbegin.md) / [**glEnd**](glend.md) pour spécifier les sommets de points, de lignes et de polygones.</span><span class="sxs-lookup"><span data-stu-id="96b65-116">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="96b65-117">Les coordonnées de couleur actuelle, normale et de texture sont associées au vertex lorsque glVertex est appelé.</span><span class="sxs-lookup"><span data-stu-id="96b65-117">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="96b65-118">Si seuls *x* et *y* sont spécifiés, *z* a pour valeur par défaut 0,0 et *w* a la valeur par défaut 1,0.</span><span class="sxs-lookup"><span data-stu-id="96b65-118">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="96b65-119">Lorsque *x*, *y* et *z* sont spécifiés, *w* a pour valeur par défaut 1,0.</span><span class="sxs-lookup"><span data-stu-id="96b65-119">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="96b65-120">L’appel de glVertex en dehors d’une paire de / **glEnd** glBegin entraîne un comportement indéfini.</span><span class="sxs-lookup"><span data-stu-id="96b65-120">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="96b65-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96b65-121">Requirements</span></span>



| <span data-ttu-id="96b65-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="96b65-122">Requirement</span></span> | <span data-ttu-id="96b65-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="96b65-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96b65-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96b65-124">Minimum supported client</span></span><br/> | <span data-ttu-id="96b65-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="96b65-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="96b65-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96b65-126">Minimum supported server</span></span><br/> | <span data-ttu-id="96b65-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="96b65-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="96b65-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="96b65-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="96b65-129"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="96b65-129"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="96b65-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="96b65-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="96b65-131"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96b65-131"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="96b65-132">DLL</span><span class="sxs-lookup"><span data-stu-id="96b65-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96b65-133"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96b65-133"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96b65-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96b65-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96b65-135">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="96b65-135">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="96b65-136">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="96b65-136">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="96b65-137">**glColor**</span><span class="sxs-lookup"><span data-stu-id="96b65-137">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="96b65-138">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="96b65-138">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="96b65-139">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="96b65-139">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="96b65-140">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="96b65-140">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="96b65-141">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="96b65-141">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="96b65-142">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="96b65-142">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="96b65-143">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="96b65-143">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="96b65-144">**glRect**</span><span class="sxs-lookup"><span data-stu-id="96b65-144">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="96b65-145">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="96b65-145">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





