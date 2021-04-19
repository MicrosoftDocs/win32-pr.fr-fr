---
title: fonction glVertex2i (GL. h)
description: Spécifie un sommet. | fonction glVertex2i (GL. h)
ms.assetid: 13dc175b-9382-4266-962d-6dcf23ff5949
keywords:
- glVertex2i fonction OpenGL
topic_type:
- apiref
api_name:
- glVertex2i
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f810083c61fbd04d1c61349d57e7abd72ab95a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106542137"
---
# <a name="glvertex2i-function"></a><span data-ttu-id="a82d8-105">glVertex2i fonction)</span><span class="sxs-lookup"><span data-stu-id="a82d8-105">glVertex2i function</span></span>

<span data-ttu-id="a82d8-106">Spécifie un sommet.</span><span class="sxs-lookup"><span data-stu-id="a82d8-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="a82d8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a82d8-107">Syntax</span></span>


```C++
void WINAPI glVertex2i(
   GLint x,
   GLint y
);
```



## <a name="parameters"></a><span data-ttu-id="a82d8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a82d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a82d8-109">*x*</span><span class="sxs-lookup"><span data-stu-id="a82d8-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="a82d8-110">Spécifie la coordonnée x d’un vertex.</span><span class="sxs-lookup"><span data-stu-id="a82d8-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="a82d8-111">*y*</span><span class="sxs-lookup"><span data-stu-id="a82d8-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="a82d8-112">Spécifie la coordonnée y d’un vertex.</span><span class="sxs-lookup"><span data-stu-id="a82d8-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a82d8-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a82d8-113">Return value</span></span>

<span data-ttu-id="a82d8-114">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a82d8-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a82d8-115">Notes</span><span class="sxs-lookup"><span data-stu-id="a82d8-115">Remarks</span></span>

<span data-ttu-id="a82d8-116">Les commandes de fonction glVertex sont utilisées dans les paires [**glBegin**](glbegin.md) / [**glEnd**](glend.md) pour spécifier les sommets de points, de lignes et de polygones.</span><span class="sxs-lookup"><span data-stu-id="a82d8-116">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="a82d8-117">Les coordonnées de couleur actuelle, normale et de texture sont associées au vertex lorsque glVertex est appelé.</span><span class="sxs-lookup"><span data-stu-id="a82d8-117">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="a82d8-118">Si seuls *x* et *y* sont spécifiés, *z* a pour valeur par défaut 0,0 et *w* a la valeur par défaut 1,0.</span><span class="sxs-lookup"><span data-stu-id="a82d8-118">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="a82d8-119">Lorsque *x*, *y* et *z* sont spécifiés, *w* a pour valeur par défaut 1,0.</span><span class="sxs-lookup"><span data-stu-id="a82d8-119">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="a82d8-120">L’appel de glVertex en dehors d’une paire de / **glEnd** glBegin entraîne un comportement indéfini.</span><span class="sxs-lookup"><span data-stu-id="a82d8-120">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="a82d8-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a82d8-121">Requirements</span></span>



| <span data-ttu-id="a82d8-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a82d8-122">Requirement</span></span> | <span data-ttu-id="a82d8-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a82d8-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a82d8-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a82d8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a82d8-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a82d8-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a82d8-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a82d8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a82d8-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a82d8-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a82d8-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="a82d8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a82d8-129"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a82d8-129"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a82d8-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a82d8-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="a82d8-131"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a82d8-131"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a82d8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a82d8-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a82d8-133"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a82d8-133"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a82d8-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a82d8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a82d8-135">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a82d8-135">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a82d8-136">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="a82d8-136">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="a82d8-137">**glColor**</span><span class="sxs-lookup"><span data-stu-id="a82d8-137">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="a82d8-138">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="a82d8-138">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="a82d8-139">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="a82d8-139">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a82d8-140">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="a82d8-140">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="a82d8-141">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="a82d8-141">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="a82d8-142">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="a82d8-142">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="a82d8-143">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="a82d8-143">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="a82d8-144">**glRect**</span><span class="sxs-lookup"><span data-stu-id="a82d8-144">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="a82d8-145">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="a82d8-145">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





