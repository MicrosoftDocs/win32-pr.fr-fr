---
title: fonction glRectf (GL. h)
description: La fonction glRectf dessine un rectangle.
ms.assetid: 3fb55382-6041-4d9a-83cb-09a5170cc95a
keywords:
- glRectf fonction OpenGL
topic_type:
- apiref
api_name:
- glRectf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0c7036ae7395dce66d88f52c30631be801c4af3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464331"
---
# <a name="glrectf-function"></a><span data-ttu-id="b91a1-104">glRectf fonction)</span><span class="sxs-lookup"><span data-stu-id="b91a1-104">glRectf function</span></span>

<span data-ttu-id="b91a1-105">La fonction [**glRectf**](glrectd.md) dessine un rectangle.</span><span class="sxs-lookup"><span data-stu-id="b91a1-105">The [**glRectf**](glrectd.md) function draws a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="b91a1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b91a1-106">Syntax</span></span>


```C++
void WINAPI glRectf(
   GLfloat x1,
   GLfloat y1,
   GLfloat x2,
   GLfloat y2
);
```



## <a name="parameters"></a><span data-ttu-id="b91a1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b91a1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b91a1-108">*x1*</span><span class="sxs-lookup"><span data-stu-id="b91a1-108">*x1*</span></span> 
</dt> <dd>

<span data-ttu-id="b91a1-109">Coordonnée *x* du vertex d’un rectangle.</span><span class="sxs-lookup"><span data-stu-id="b91a1-109">The *x* coordinate of the vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="b91a1-110">*y1*</span><span class="sxs-lookup"><span data-stu-id="b91a1-110">*y1*</span></span> 
</dt> <dd>

<span data-ttu-id="b91a1-111">Coordonnée *y* du vertex d’un rectangle.</span><span class="sxs-lookup"><span data-stu-id="b91a1-111">The *y* coordinate of the vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="b91a1-112">*x2*</span><span class="sxs-lookup"><span data-stu-id="b91a1-112">*x2*</span></span> 
</dt> <dd>

<span data-ttu-id="b91a1-113">Coordonnée *x* du vertex opposé du rectangle.</span><span class="sxs-lookup"><span data-stu-id="b91a1-113">The *x* coordinate of the opposite vertex of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="b91a1-114">*Y2*</span><span class="sxs-lookup"><span data-stu-id="b91a1-114">*y2*</span></span> 
</dt> <dd>

<span data-ttu-id="b91a1-115">Coordonnée *y* du vertex opposé du rectangle.</span><span class="sxs-lookup"><span data-stu-id="b91a1-115">The *y* coordinate of the opposite vertex of the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b91a1-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b91a1-116">Return value</span></span>

<span data-ttu-id="b91a1-117">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b91a1-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b91a1-118">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="b91a1-118">Error codes</span></span>

<span data-ttu-id="b91a1-119">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="b91a1-119">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b91a1-120">Nom</span><span class="sxs-lookup"><span data-stu-id="b91a1-120">Name</span></span>                                                                                                  | <span data-ttu-id="b91a1-121">Signification</span><span class="sxs-lookup"><span data-stu-id="b91a1-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b91a1-122"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b91a1-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b91a1-123">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b91a1-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b91a1-124">Notes</span><span class="sxs-lookup"><span data-stu-id="b91a1-124">Remarks</span></span>

<span data-ttu-id="b91a1-125">La fonction **glRectf** prend en charge une spécification efficace des rectangles sous la forme de deux points d’angle.</span><span class="sxs-lookup"><span data-stu-id="b91a1-125">The **glRectf** function supports efficient specification of rectangles as two corner points.</span></span> <span data-ttu-id="b91a1-126">Chaque commande de rectangle accepte quatre arguments, organisés en deux paires consécutives de coordonnées (*x*, *y*), ou en tant que deux pointeurs vers des tableaux, chacun contenant une paire (*x*, *y*).</span><span class="sxs-lookup"><span data-stu-id="b91a1-126">Each rectangle command takes four arguments, organized either as two consecutive pairs of (*x*, *y*) coordinates, or as two pointers to arrays, each containing an (*x*, *y*) pair.</span></span> <span data-ttu-id="b91a1-127">Le rectangle résultant est défini dans le plan *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="b91a1-127">The resulting rectangle is defined in the *z* = 0 plane.</span></span>

<span data-ttu-id="b91a1-128">La fonction **glRectf**(*x1,* *Y1,* *x2,* *Y2*) est exactement équivalente à la séquence suivante :</span><span class="sxs-lookup"><span data-stu-id="b91a1-128">The **glRectf**(*x1,* *y1,* *x2,* *y2*) function is exactly equivalent to the following sequence:</span></span>

<span data-ttu-id="b91a1-129">**glBegin**( \_ polygone GL);</span><span class="sxs-lookup"><span data-stu-id="b91a1-129">**glBegin**(GL\_POLYGON);</span></span>

<span data-ttu-id="b91a1-130">**glVertex2**( *x1,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="b91a1-130">**glVertex2**( *x1,* *y1* );</span></span>

<span data-ttu-id="b91a1-131">**glVertex2**( *x2,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="b91a1-131">**glVertex2**( *x2,* *y1* );</span></span>

<span data-ttu-id="b91a1-132">**glVertex2**( *x2,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="b91a1-132">**glVertex2**( *x2,* *y2* );</span></span>

<span data-ttu-id="b91a1-133">**glVertex2**( *x1,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="b91a1-133">**glVertex2**( *x1,* *y2* );</span></span>

<span data-ttu-id="b91a1-134">**glEnd**();</span><span class="sxs-lookup"><span data-stu-id="b91a1-134">**glEnd**( );</span></span>

<span data-ttu-id="b91a1-135">Notez que si le deuxième vertex est au-dessus et à droite du premier vertex, le rectangle est construit avec un enroulement dans le sens inverse des aiguilles d’une passe.</span><span class="sxs-lookup"><span data-stu-id="b91a1-135">Notice that if the second vertex is above and to the right of the first vertex, the rectangle is constructed with a counterclockwise winding.</span></span>

## <a name="requirements"></a><span data-ttu-id="b91a1-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b91a1-136">Requirements</span></span>



| <span data-ttu-id="b91a1-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b91a1-137">Requirement</span></span> | <span data-ttu-id="b91a1-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="b91a1-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b91a1-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b91a1-139">Minimum supported client</span></span><br/> | <span data-ttu-id="b91a1-140">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b91a1-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b91a1-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b91a1-141">Minimum supported server</span></span><br/> | <span data-ttu-id="b91a1-142">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b91a1-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b91a1-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="b91a1-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="b91a1-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b91a1-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b91a1-145">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b91a1-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="b91a1-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b91a1-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b91a1-147">DLL</span><span class="sxs-lookup"><span data-stu-id="b91a1-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b91a1-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b91a1-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b91a1-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b91a1-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b91a1-150">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b91a1-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b91a1-151">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b91a1-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b91a1-152">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="b91a1-152">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





