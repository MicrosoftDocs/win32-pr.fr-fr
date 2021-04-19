---
title: fonction glEvalCoord1fv (GL. h)
description: La fonction glEvalCoord1fv évalue les mappages unidimensionnels activés.
ms.assetid: d5c1cc99-ecf6-4d78-99bb-953b4c362ff4
keywords:
- glEvalCoord1fv fonction OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord1fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9acb1f7060367b02fa836fb149151b8278b7274
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510984"
---
# <a name="glevalcoord1fv-function"></a><span data-ttu-id="67a58-104">glEvalCoord1fv fonction)</span><span class="sxs-lookup"><span data-stu-id="67a58-104">glEvalCoord1fv function</span></span>

<span data-ttu-id="67a58-105">La fonction **glEvalCoord1fv** évalue les mappages unidimensionnels activés.</span><span class="sxs-lookup"><span data-stu-id="67a58-105">The **glEvalCoord1fv** function evaluates enabled one-dimensional maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="67a58-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67a58-106">Syntax</span></span>


```C++
void WINAPI glEvalCoord1fv(
   const GLfloat *u
);
```



## <a name="parameters"></a><span data-ttu-id="67a58-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67a58-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67a58-108">*u*</span><span class="sxs-lookup"><span data-stu-id="67a58-108">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="67a58-109">Pointeur vers un tableau contenant la coordonnée de domaine *u*.</span><span class="sxs-lookup"><span data-stu-id="67a58-109">A pointer to an array containing the domain coordinate *u*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67a58-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="67a58-110">Return value</span></span>

<span data-ttu-id="67a58-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="67a58-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="67a58-112">Notes</span><span class="sxs-lookup"><span data-stu-id="67a58-112">Remarks</span></span>

<span data-ttu-id="67a58-113">La fonction [**glEvalCoord1fv**](glevalcoord1dv.md) évalue les mappages unidimensionnels activés au niveau de l’argument *u*.</span><span class="sxs-lookup"><span data-stu-id="67a58-113">The [**glEvalCoord1fv**](glevalcoord1dv.md) function evaluates enabled one-dimensional maps at argument *u*.</span></span> <span data-ttu-id="67a58-114">Définissez Maps avec [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="67a58-114">Define maps with [**glMap1**](glmap1.md).</span></span> <span data-ttu-id="67a58-115">Activez ou désactivez-les avec [**glEnable**](glenable.md) et [**glDisable**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="67a58-115">Enable or disable them with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="67a58-116">Lorsque l’une des fonctions **glEvalCoord** est émise, tous les mappages actuellement activés de la dimension indiquée sont évalués.</span><span class="sxs-lookup"><span data-stu-id="67a58-116">When one of the **glEvalCoord** functions is issued, all currently enabled maps of the indicated dimension are evaluated.</span></span> <span data-ttu-id="67a58-117">Ensuite, pour chaque mappage activé, c’est comme si la fonction OpenGL correspondante avait été émise avec la valeur calculée.</span><span class="sxs-lookup"><span data-stu-id="67a58-117">Then, for each enabled map, it is as if the corresponding OpenGL function were issued with the computed value.</span></span> <span data-ttu-id="67a58-118">Autrement dit, si l’index \_ Map1 GL \_ ou l' \_ index map2 GL \_ est activé, une fonction [**glIndex**](glindex-functions.md) est simulée.</span><span class="sxs-lookup"><span data-stu-id="67a58-118">That is, if GL\_MAP1\_INDEX or GL\_MAP2\_INDEX is enabled, a [**glIndex**](glindex-functions.md) function is simulated.</span></span> <span data-ttu-id="67a58-119">Si GL \_ Map1 \_ Color \_ 4 ou GL \_ map2 \_ Color \_ 4 est activé, une fonction **glcolor** est simulée.</span><span class="sxs-lookup"><span data-stu-id="67a58-119">If GL\_MAP1\_COLOR\_4 or GL\_MAP2\_COLOR\_4 is enabled, a **glcolor** function is simulated.</span></span> <span data-ttu-id="67a58-120">Si GL \_ Map1 \_ normal ou GL \_ map2 \_ normal est activé, un vecteur normal est produit, et si l’un des \_ Map1 de \_ texture GL \_ Coord \_ 1, GL \_ Map1 texture Coord \_ \_ \_ 2, GL \_ Map1 texture Coord \_ \_ \_ 3, GL \_ Map1 \_ texture \_ Coord 4, GL map2 texture Coord \_ \_ \_ \_ \_ 1, GL \_ map2 \_ texture \_ Coord \_ 2, GL \_ map2 \_ texture \_ Coord \_ 3 et GL \_ map2 \_ texture \_ Coord \_ 4 est activé, une fonction [**glTexCoord**](gltexcoord-functions.md) appropriée est simulée.</span><span class="sxs-lookup"><span data-stu-id="67a58-120">If GL\_MAP1\_NORMAL or GL\_MAP2\_NORMAL is enabled, a normal vector is produced, and if any of GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, and GL\_MAP2\_TEXTURE\_COORD\_4 is enabled, then an appropriate [**glTexCoord**](gltexcoord-functions.md) function is simulated.</span></span>

<span data-ttu-id="67a58-121">OpenGL utilise des valeurs évaluées au lieu des valeurs actuelles pour les évaluations qui sont activées, et les valeurs actuelles dans le cas contraire, pour les coordonnées de couleur, d’index de couleur, normales et de texture.</span><span class="sxs-lookup"><span data-stu-id="67a58-121">OpenGL uses evaluated values instead of current values for those evaluations that are enabled, and current values otherwise, for color, color index, normal, and texture coordinates.</span></span> <span data-ttu-id="67a58-122">Toutefois, les valeurs évaluées ne mettent pas à jour les valeurs actuelles.</span><span class="sxs-lookup"><span data-stu-id="67a58-122">However, the evaluated values do not update the current values.</span></span> <span data-ttu-id="67a58-123">Ainsi, si les fonctions [**glVertex**](glvertex-functions.md) sont intercalées avec les fonctions **glEvalCoord** , les coordonnées de couleur, normale et de texture associées aux fonctions **glVertex** ne sont pas affectées par les valeurs générées par les fonctions **GlEvalCoord** , mais uniquement par les fonctions [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md)et [**glTexCoord**](gltexcoord-functions.md) les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="67a58-123">Thus, if [**glVertex**](glvertex-functions.md) functions are interspersed with **glEvalCoord** functions, the color, normal, and texture coordinates associated with the **glVertex** functions are not affected by the values generated by the **glEvalCoord** functions, but only by the most recent [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md), and [**glTexCoord**](gltexcoord-functions.md) functions.</span></span>

<span data-ttu-id="67a58-124">Les fonctions suivantes récupèrent les informations relatives à la fonction **glEvalCoord1fv** :</span><span class="sxs-lookup"><span data-stu-id="67a58-124">The following functions retrieve information related to the **glEvalCoord1fv** function:</span></span>

<span data-ttu-id="67a58-125">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="67a58-125">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_3</span></span>

<span data-ttu-id="67a58-126">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="67a58-126">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_4</span></span>

<span data-ttu-id="67a58-127">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ index</span><span class="sxs-lookup"><span data-stu-id="67a58-127">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_INDEX</span></span>

<span data-ttu-id="67a58-128">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ couleur \_ 4</span><span class="sxs-lookup"><span data-stu-id="67a58-128">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_COLOR\_4</span></span>

<span data-ttu-id="67a58-129">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ normal</span><span class="sxs-lookup"><span data-stu-id="67a58-129">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_NORMAL</span></span>

<span data-ttu-id="67a58-130">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ texture \_ Coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="67a58-130">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="67a58-131">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ texture \_ Coord \_ 2</span><span class="sxs-lookup"><span data-stu-id="67a58-131">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="67a58-132">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ texture \_ repère \_ 3</span><span class="sxs-lookup"><span data-stu-id="67a58-132">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="67a58-133">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ texture \_ Coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="67a58-133">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="67a58-134">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="67a58-134">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_3</span></span>

<span data-ttu-id="67a58-135">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="67a58-135">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_4</span></span>

<span data-ttu-id="67a58-136">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ index</span><span class="sxs-lookup"><span data-stu-id="67a58-136">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_INDEX</span></span>

<span data-ttu-id="67a58-137">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ couleur \_ 4</span><span class="sxs-lookup"><span data-stu-id="67a58-137">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_COLOR\_4</span></span>

<span data-ttu-id="67a58-138">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ normal</span><span class="sxs-lookup"><span data-stu-id="67a58-138">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_NORMAL</span></span>

<span data-ttu-id="67a58-139">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ texture \_ Coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="67a58-139">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="67a58-140">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ texture \_ Coord \_ 2</span><span class="sxs-lookup"><span data-stu-id="67a58-140">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="67a58-141">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ texture \_ repère \_ 3</span><span class="sxs-lookup"><span data-stu-id="67a58-141">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="67a58-142">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ texture \_ Coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="67a58-142">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="67a58-143">[**glIsEnabled**](glisenabled.md) avec l’argument GL \_ auto \_ normal</span><span class="sxs-lookup"><span data-stu-id="67a58-143">[**glIsEnabled**](glisenabled.md) with argument GL\_AUTO\_NORMAL</span></span>

## <a name="requirements"></a><span data-ttu-id="67a58-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67a58-144">Requirements</span></span>



| <span data-ttu-id="67a58-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67a58-145">Requirement</span></span> | <span data-ttu-id="67a58-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="67a58-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67a58-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67a58-147">Minimum supported client</span></span><br/> | <span data-ttu-id="67a58-148">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67a58-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="67a58-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67a58-149">Minimum supported server</span></span><br/> | <span data-ttu-id="67a58-150">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67a58-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="67a58-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="67a58-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="67a58-152"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="67a58-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="67a58-153">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="67a58-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="67a58-154"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67a58-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="67a58-155">DLL</span><span class="sxs-lookup"><span data-stu-id="67a58-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67a58-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67a58-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67a58-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67a58-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67a58-158">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="67a58-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="67a58-159">**glColor**</span><span class="sxs-lookup"><span data-stu-id="67a58-159">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="67a58-160">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="67a58-160">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="67a58-161">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="67a58-161">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="67a58-162">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="67a58-162">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="67a58-163">**glEvalMesh**</span><span class="sxs-lookup"><span data-stu-id="67a58-163">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="67a58-164">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="67a58-164">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="67a58-165">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="67a58-165">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="67a58-166">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="67a58-166">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="67a58-167">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="67a58-167">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="67a58-168">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="67a58-168">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="67a58-169">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="67a58-169">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="67a58-170">**glMapGrid**</span><span class="sxs-lookup"><span data-stu-id="67a58-170">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> <dt>

[<span data-ttu-id="67a58-171">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="67a58-171">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="67a58-172">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="67a58-172">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="67a58-173">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="67a58-173">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





