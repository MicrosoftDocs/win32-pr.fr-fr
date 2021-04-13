---
title: fonction glRectdv (GL. h)
description: La fonction glRectdv dessine un rectangle.
ms.assetid: 53000734-bfc3-42c3-aa80-0a54e3dd36ec
keywords:
- glRectdv fonction OpenGL
topic_type:
- apiref
api_name:
- glRectdv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2956a1f658101a384ae69b05ed50418492d264
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383908"
---
# <a name="glrectdv-function"></a><span data-ttu-id="04940-104">glRectdv fonction)</span><span class="sxs-lookup"><span data-stu-id="04940-104">glRectdv function</span></span>

<span data-ttu-id="04940-105">La fonction **glRectdv** dessine un rectangle.</span><span class="sxs-lookup"><span data-stu-id="04940-105">The **glRectdv** function draws a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="04940-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04940-106">Syntax</span></span>


```C++
void WINAPI glRectdv(
   const GLdouble *v1,
   const GLdouble *v2
);
```



## <a name="parameters"></a><span data-ttu-id="04940-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04940-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04940-108">*v1*</span><span class="sxs-lookup"><span data-stu-id="04940-108">*v1*</span></span> 
</dt> <dd>

<span data-ttu-id="04940-109">Pointeur vers un sommet d’un rectangle.</span><span class="sxs-lookup"><span data-stu-id="04940-109">A pointer to one vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="04940-110">*v2*</span><span class="sxs-lookup"><span data-stu-id="04940-110">*v2*</span></span> 
</dt> <dd>

<span data-ttu-id="04940-111">pointeur vers le vertex opposé du rectangle.</span><span class="sxs-lookup"><span data-stu-id="04940-111">a pointer to the opposite vertex of the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04940-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="04940-112">Return value</span></span>

<span data-ttu-id="04940-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="04940-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="04940-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="04940-114">Error codes</span></span>

<span data-ttu-id="04940-115">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="04940-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="04940-116">Nom</span><span class="sxs-lookup"><span data-stu-id="04940-116">Name</span></span>                                                                                                  | <span data-ttu-id="04940-117">Signification</span><span class="sxs-lookup"><span data-stu-id="04940-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="04940-118"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="04940-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="04940-119">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="04940-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="04940-120">Notes</span><span class="sxs-lookup"><span data-stu-id="04940-120">Remarks</span></span>

<span data-ttu-id="04940-121">La fonction **glRectd** prend en charge une spécification efficace des rectangles sous la forme de deux points d’angle.</span><span class="sxs-lookup"><span data-stu-id="04940-121">The **glRectd** function supports efficient specification of rectangles as two corner points.</span></span> <span data-ttu-id="04940-122">Chaque commande de rectangle accepte quatre arguments, organisés en deux paires consécutives de coordonnées (*x*, *y*), ou en tant que deux pointeurs vers des tableaux, chacun contenant une paire (*x*, *y*).</span><span class="sxs-lookup"><span data-stu-id="04940-122">Each rectangle command takes four arguments, organized either as two consecutive pairs of (*x*, *y*) coordinates, or as two pointers to arrays, each containing an (*x*, *y*) pair.</span></span> <span data-ttu-id="04940-123">Le rectangle résultant est défini dans le plan *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="04940-123">The resulting rectangle is defined in the *z* = 0 plane.</span></span>

<span data-ttu-id="04940-124">La fonction **glRectd**(*x1,* *Y1,* *x2,* *Y2*) est exactement équivalente à la séquence suivante :</span><span class="sxs-lookup"><span data-stu-id="04940-124">The **glRectd**(*x1,* *y1,* *x2,* *y2*) function is exactly equivalent to the following sequence:</span></span>

<span data-ttu-id="04940-125">**glBegin**( \_ polygone GL);</span><span class="sxs-lookup"><span data-stu-id="04940-125">**glBegin**(GL\_POLYGON);</span></span>

<span data-ttu-id="04940-126">**glVertex2**( *x1,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="04940-126">**glVertex2**( *x1,* *y1* );</span></span>

<span data-ttu-id="04940-127">**glVertex2**( *x2,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="04940-127">**glVertex2**( *x2,* *y1* );</span></span>

<span data-ttu-id="04940-128">**glVertex2**( *x2,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="04940-128">**glVertex2**( *x2,* *y2* );</span></span>

<span data-ttu-id="04940-129">**glVertex2**( *x1,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="04940-129">**glVertex2**( *x1,* *y2* );</span></span>

<span data-ttu-id="04940-130">**glEnd**();</span><span class="sxs-lookup"><span data-stu-id="04940-130">**glEnd**( );</span></span>

<span data-ttu-id="04940-131">Notez que si le deuxième vertex est au-dessus et à droite du premier vertex, le rectangle est construit avec un enroulement dans le sens inverse des aiguilles d’une passe.</span><span class="sxs-lookup"><span data-stu-id="04940-131">Notice that if the second vertex is above and to the right of the first vertex, the rectangle is constructed with a counterclockwise winding.</span></span>

## <a name="requirements"></a><span data-ttu-id="04940-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04940-132">Requirements</span></span>



| <span data-ttu-id="04940-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04940-133">Requirement</span></span> | <span data-ttu-id="04940-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="04940-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04940-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04940-135">Minimum supported client</span></span><br/> | <span data-ttu-id="04940-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04940-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="04940-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04940-137">Minimum supported server</span></span><br/> | <span data-ttu-id="04940-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04940-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="04940-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="04940-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="04940-140"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="04940-140"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="04940-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="04940-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="04940-142"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04940-142"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="04940-143">DLL</span><span class="sxs-lookup"><span data-stu-id="04940-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04940-144"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04940-144"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04940-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04940-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04940-146">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="04940-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="04940-147">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="04940-147">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="04940-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="04940-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





