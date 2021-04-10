---
title: gluPickMatrix, fonction (Glu. h)
description: La fonction gluPickMatrix définit une région de prélèvement.
ms.assetid: 2f57345c-17a0-4716-8ab8-170aaed2b4f9
keywords:
- gluPickMatrix fonction OpenGL
topic_type:
- apiref
api_name:
- gluPickMatrix
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c54e62f82f52fedc7de7c7c4af1cd3ed1ccdf149
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941641"
---
# <a name="glupickmatrix-function"></a><span data-ttu-id="546da-104">gluPickMatrix fonction)</span><span class="sxs-lookup"><span data-stu-id="546da-104">gluPickMatrix function</span></span>

<span data-ttu-id="546da-105">La fonction **gluPickMatrix** définit une région de prélèvement.</span><span class="sxs-lookup"><span data-stu-id="546da-105">The **gluPickMatrix** function defines a picking region.</span></span>

## <a name="syntax"></a><span data-ttu-id="546da-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="546da-106">Syntax</span></span>


```C++
void WINAPI gluPickMatrix(
   GLdouble x,
   GLdouble y,
   GLdouble height,
   GLdouble width,
   GLint    viewport[4]
);
```



## <a name="parameters"></a><span data-ttu-id="546da-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="546da-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="546da-108">*x*</span><span class="sxs-lookup"><span data-stu-id="546da-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="546da-109">Coordonnée x de la fenêtre d’une région de prélèvement.</span><span class="sxs-lookup"><span data-stu-id="546da-109">The x window coordinate of a picking region.</span></span>

</dd> <dt>

<span data-ttu-id="546da-110">*y*</span><span class="sxs-lookup"><span data-stu-id="546da-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="546da-111">Coordonnée de la fenêtre y d’une région de prélèvement.</span><span class="sxs-lookup"><span data-stu-id="546da-111">The y window coordinate of a picking region.</span></span>

</dd> <dt>

<span data-ttu-id="546da-112">*height*</span><span class="sxs-lookup"><span data-stu-id="546da-112">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="546da-113">Hauteur de la région de prélèvement en coordonnées de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="546da-113">The height of the picking region in window coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="546da-114">*width*</span><span class="sxs-lookup"><span data-stu-id="546da-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="546da-115">Largeur de la région de prélèvement en coordonnées de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="546da-115">The width of the picking region in window coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="546da-116">*vue*</span><span class="sxs-lookup"><span data-stu-id="546da-116">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="546da-117">La fenêtre d’affichage actuelle (à partir d’un appel [**glGetIntegerv**](glgetintegerv.md) ).</span><span class="sxs-lookup"><span data-stu-id="546da-117">The current viewport (as from a [**glGetIntegerv**](glgetintegerv.md) call).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="546da-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="546da-118">Return value</span></span>

<span data-ttu-id="546da-119">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="546da-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="546da-120">Notes</span><span class="sxs-lookup"><span data-stu-id="546da-120">Remarks</span></span>

<span data-ttu-id="546da-121">La fonction **gluPickMatrix** crée une matrice de projection que vous pouvez utiliser pour restreindre le dessin à une petite zone de la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="546da-121">The **gluPickMatrix** function creates a projection matrix you can use to restrict drawing to a small region of the viewport.</span></span>

1.  <span data-ttu-id="546da-122">Utilisez **gluPickMatrix** pour restreindre le dessin à une petite zone autour du curseur.</span><span class="sxs-lookup"><span data-stu-id="546da-122">Use **gluPickMatrix** to restrict drawing to a small region around the cursor.</span></span>
2.  <span data-ttu-id="546da-123">Entrez le mode de sélection (avec [**glRenderMode**](glrendermode.md)), puis rerendez la scène.</span><span class="sxs-lookup"><span data-stu-id="546da-123">Enter selection mode (with [**glRenderMode**](glrendermode.md)), and then rerender the scene.</span></span>

    <span data-ttu-id="546da-124">Toutes les primitives qui auraient été dessinées près du curseur sont identifiées et stockées dans la mémoire tampon de sélection.</span><span class="sxs-lookup"><span data-stu-id="546da-124">All primitives that would have been drawn near the cursor are identified and stored in the selection buffer.</span></span>

<span data-ttu-id="546da-125">La matrice créée par **gluPickMatrix** est multipliée par la matrice actuelle comme si [**glMultMatrix**](glmultmatrix.md) était appelé avec la matrice générée.</span><span class="sxs-lookup"><span data-stu-id="546da-125">The matrix created by **gluPickMatrix** is multiplied by the current matrix just as if [**glMultMatrix**](glmultmatrix.md) were called with the generated matrix.</span></span>

1.  <span data-ttu-id="546da-126">Appelez [**glLoadIdentity**](glloadidentity.md) pour charger une matrice d’identité dans la pile de la matrice de perspective.</span><span class="sxs-lookup"><span data-stu-id="546da-126">Call [**glLoadIdentity**](glloadidentity.md) to load an identity matrix onto the perspective matrix stack.</span></span>
2.  <span data-ttu-id="546da-127">Appelez **gluPickMatrix**.</span><span class="sxs-lookup"><span data-stu-id="546da-127">Call **gluPickMatrix**.</span></span>
3.  <span data-ttu-id="546da-128">Appelez une fonction (telle que [**gluPerspective**](gluperspective.md)) pour multiplier la matrice de perspective par la matrice Pick.</span><span class="sxs-lookup"><span data-stu-id="546da-128">Call a function (such as [**gluPerspective**](gluperspective.md)) to multiply the perspective matrix by the pick matrix.</span></span>

<span data-ttu-id="546da-129">Quand vous utilisez **gluPickMatrix** pour choisir une courbe B-spline rationnelle non uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)), veillez à désactiver la propriété NURBS Glu la \_ matrice de \_ chargement automatique \_ .</span><span class="sxs-lookup"><span data-stu-id="546da-129">When using **gluPickMatrix** to pick Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)), be careful to turn off the NURBS property, GLU\_AUTO\_LOAD\_MATRIX.</span></span> <span data-ttu-id="546da-130">Si \_ \_ \_ la matrice de chargement automatique Glu n’est pas désactivée, toute surface NURBS rendue est sous-divisée différemment avec la matrice Pick de la manière dont elle a été subdivisée sans la matrice Pick.</span><span class="sxs-lookup"><span data-stu-id="546da-130">If GLU\_AUTO\_LOAD\_MATRIX is not turned off, any NURBS surface rendered is subdivided differently with the pick matrix from how it was subdivided without the pick matrix.</span></span>

## <a name="examples"></a><span data-ttu-id="546da-131">Exemples</span><span class="sxs-lookup"><span data-stu-id="546da-131">Examples</span></span>

<span data-ttu-id="546da-132">Lors du rendu d’une scène, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="546da-132">When rendering a scene as follows:</span></span>


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



<span data-ttu-id="546da-133">le code suivant sélectionne une partie de la fenêtre d’affichage :</span><span class="sxs-lookup"><span data-stu-id="546da-133">the following code selects a portion of the viewport:</span></span>


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPickMatrix(x, y, width, height, viewport);  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



## <a name="requirements"></a><span data-ttu-id="546da-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="546da-134">Requirements</span></span>



| <span data-ttu-id="546da-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="546da-135">Requirement</span></span> | <span data-ttu-id="546da-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="546da-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="546da-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="546da-137">Minimum supported client</span></span><br/> | <span data-ttu-id="546da-138">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="546da-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="546da-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="546da-139">Minimum supported server</span></span><br/> | <span data-ttu-id="546da-140">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="546da-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="546da-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="546da-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="546da-142"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="546da-142"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="546da-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="546da-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="546da-144"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="546da-144"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="546da-145">DLL</span><span class="sxs-lookup"><span data-stu-id="546da-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="546da-146"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="546da-146"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="546da-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="546da-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="546da-148">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="546da-148">**glGetIntegerv**</span></span>](glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="546da-149">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="546da-149">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="546da-150">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="546da-150">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="546da-151">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="546da-151">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="546da-152">**gluPerspective**</span><span class="sxs-lookup"><span data-stu-id="546da-152">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





