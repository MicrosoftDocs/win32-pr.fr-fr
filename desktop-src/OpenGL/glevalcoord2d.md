---
title: fonction glEvalCoord2d (GL. h)
description: La fonction glEvalCoord2d évalue les mappages à deux dimensions activés.
ms.assetid: 95963abc-841a-4154-92d5-5ae3e6de0f97
keywords:
- glEvalCoord2d fonction OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord2d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 036e2ee10d1ceac6df6a68a35c1da881d1d478b5
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104565466"
---
# <a name="glevalcoord2d-function"></a><span data-ttu-id="3f926-104">glEvalCoord2d fonction)</span><span class="sxs-lookup"><span data-stu-id="3f926-104">glEvalCoord2d function</span></span>

<span data-ttu-id="3f926-105">La fonction **glEvalCoord2d** évalue les mappages à deux dimensions activés.</span><span class="sxs-lookup"><span data-stu-id="3f926-105">The **glEvalCoord2d** function evaluates enabled two-dimensional maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f926-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f926-106">Syntax</span></span>


```C++
void WINAPI glEvalCoord2d(
   GLdouble u,
   GLdouble v
);
```



## <a name="parameters"></a><span data-ttu-id="3f926-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f926-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f926-108">*u*</span><span class="sxs-lookup"><span data-stu-id="3f926-108">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="3f926-109">Valeur qui est la coordonnée de domaine *u* à la fonction de base définie dans une fonction [**glMap2**](glmap2.md) précédente.</span><span class="sxs-lookup"><span data-stu-id="3f926-109">A value that is the domain coordinate *u* to the basis function defined in a previous [**glMap2**](glmap2.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="3f926-110">*v*</span><span class="sxs-lookup"><span data-stu-id="3f926-110">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="3f926-111">Valeur qui est la coordonnée de domaine *v* à la fonction de base définie dans une fonction [**glMap2**](glmap2.md) précédente.</span><span class="sxs-lookup"><span data-stu-id="3f926-111">A value that is the domain coordinate *v* to the basis function defined in a previous [**glMap2**](glmap2.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f926-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3f926-112">Return value</span></span>

<span data-ttu-id="3f926-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3f926-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f926-114">Notes</span><span class="sxs-lookup"><span data-stu-id="3f926-114">Remarks</span></span>

<span data-ttu-id="3f926-115">La fonction **glEvalCoord2d** évalue les mappages à deux dimensions activés à l’aide de deux valeurs de domaine, *u* et *v*.</span><span class="sxs-lookup"><span data-stu-id="3f926-115">The **glEvalCoord2d** function evaluates enabled two-dimensional maps using two domain values, *u* and *v*.</span></span> <span data-ttu-id="3f926-116">Définissez Maps avec [**glMap1**](glmap1.md) et [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="3f926-116">Define maps with [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="3f926-117">Activez ou désactivez-les avec [**glEnable**](glenable.md) et [**glDisable**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="3f926-117">Enable or disable them with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="3f926-118">Lorsque l’une des fonctions **glEvalCoord** est émise, tous les mappages actuellement activés de la dimension indiquée sont évalués.</span><span class="sxs-lookup"><span data-stu-id="3f926-118">When one of the **glEvalCoord** functions is issued, all currently enabled maps of the indicated dimension are evaluated.</span></span> <span data-ttu-id="3f926-119">Ensuite, pour chaque mappage activé, c’est comme si la fonction OpenGL correspondante avait été émise avec la valeur calculée.</span><span class="sxs-lookup"><span data-stu-id="3f926-119">Then, for each enabled map, it is as if the corresponding OpenGL function were issued with the computed value.</span></span> <span data-ttu-id="3f926-120">Autrement dit, si l’index \_ Map1 GL \_ ou l' \_ index map2 GL \_ est activé, une fonction [**glIndex**](glindex-functions.md) est simulée.</span><span class="sxs-lookup"><span data-stu-id="3f926-120">That is, if GL\_MAP1\_INDEX or GL\_MAP2\_INDEX is enabled, a [**glIndex**](glindex-functions.md) function is simulated.</span></span> <span data-ttu-id="3f926-121">Si GL \_ Map1 \_ Color \_ 4 ou GL \_ map2 \_ Color \_ 4 est activé, une fonction **glcolor** est simulée.</span><span class="sxs-lookup"><span data-stu-id="3f926-121">If GL\_MAP1\_COLOR\_4 or GL\_MAP2\_COLOR\_4 is enabled, a **glcolor** function is simulated.</span></span> <span data-ttu-id="3f926-122">Si GL \_ Map1 \_ normal ou GL \_ map2 \_ normal est activé, un vecteur normal est produit, et si l’un des \_ Map1 de \_ texture GL \_ Coord \_ 1, GL \_ Map1 texture Coord \_ \_ \_ 2, GL \_ Map1 texture Coord \_ \_ \_ 3, GL \_ Map1 \_ texture \_ Coord 4, GL map2 texture Coord \_ \_ \_ \_ \_ 1, GL \_ map2 \_ texture \_ Coord \_ 2, GL \_ map2 \_ texture \_ Coord \_ 3 et GL \_ map2 \_ texture \_ Coord \_ 4 est activé, une fonction [**glTexCoord**](gltexcoord-functions.md) appropriée est simulée.</span><span class="sxs-lookup"><span data-stu-id="3f926-122">If GL\_MAP1\_NORMAL or GL\_MAP2\_NORMAL is enabled, a normal vector is produced, and if any of GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, and GL\_MAP2\_TEXTURE\_COORD\_4 is enabled, then an appropriate [**glTexCoord**](gltexcoord-functions.md) function is simulated.</span></span>

<span data-ttu-id="3f926-123">OpenGL utilise des valeurs évaluées au lieu des valeurs actuelles pour les évaluations qui sont activées, et les valeurs actuelles dans le cas contraire, pour les coordonnées de couleur, d’index de couleur, normales et de texture.</span><span class="sxs-lookup"><span data-stu-id="3f926-123">OpenGL uses evaluated values instead of current values for those evaluations that are enabled, and current values otherwise, for color, color index, normal, and texture coordinates.</span></span> <span data-ttu-id="3f926-124">Toutefois, les valeurs évaluées ne mettent pas à jour les valeurs actuelles.</span><span class="sxs-lookup"><span data-stu-id="3f926-124">However, the evaluated values do not update the current values.</span></span> <span data-ttu-id="3f926-125">Ainsi, si les fonctions [**glVertex**](glvertex-functions.md) sont intercalées avec les fonctions **glEvalCoord** , les coordonnées de couleur, normale et de texture associées aux fonctions **glVertex** ne sont pas affectées par les valeurs générées par les fonctions **GlEvalCoord** , mais uniquement par les fonctions [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md)et [**glTexCoord**](gltexcoord-functions.md) les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="3f926-125">Thus, if [**glVertex**](glvertex-functions.md) functions are interspersed with **glEvalCoord** functions, the color, normal, and texture coordinates associated with the **glVertex** functions are not affected by the values generated by the **glEvalCoord** functions, but only by the most recent [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md), and [**glTexCoord**](gltexcoord-functions.md) functions.</span></span>

<span data-ttu-id="3f926-126">Si la génération automatique normale est activée, **glEvalCoord2d** appelle [**glEnable**](glenable.md) avec l’argument GL \_ auto \_ normal pour générer des normales de surface analytiques, quel que soit le contenu ou l’activation de la \_ \_ carte normale GL map2.</span><span class="sxs-lookup"><span data-stu-id="3f926-126">If automatic normal generation is enabled, **glEvalCoord2d** calls [**glEnable**](glenable.md) with argument GL\_AUTO\_NORMAL to generate surface normals analytically, regardless of the contents or enabling of the GL\_MAP2\_NORMAL map.</span></span> <span data-ttu-id="3f926-127">Let</span><span class="sxs-lookup"><span data-stu-id="3f926-127">Let</span></span>

![Équation représentant une valeur de produit croisé pour une carte m.](images/evlcrd01.png)

<span data-ttu-id="3f926-129">Le **n** normal généré est</span><span class="sxs-lookup"><span data-stu-id="3f926-129">The generated normal **n** is</span></span>

![Équation qui indique la n normale générée pour la carte.](images/evlcrd02.png)

<span data-ttu-id="3f926-131">Les fonctions suivantes récupèrent les informations relatives à la fonction **glEvalCoord2d** :</span><span class="sxs-lookup"><span data-stu-id="3f926-131">The following functions retrieve information related to the **glEvalCoord2d** function:</span></span>

<span data-ttu-id="3f926-132">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="3f926-132">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_3</span></span>

<span data-ttu-id="3f926-133">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="3f926-133">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_4</span></span>

<span data-ttu-id="3f926-134">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ index</span><span class="sxs-lookup"><span data-stu-id="3f926-134">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_INDEX</span></span>

<span data-ttu-id="3f926-135">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ couleur \_ 4</span><span class="sxs-lookup"><span data-stu-id="3f926-135">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_COLOR\_4</span></span>

<span data-ttu-id="3f926-136">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ normal</span><span class="sxs-lookup"><span data-stu-id="3f926-136">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_NORMAL</span></span>

<span data-ttu-id="3f926-137">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ texture \_ Coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="3f926-137">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="3f926-138">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ texture \_ Coord \_ 2</span><span class="sxs-lookup"><span data-stu-id="3f926-138">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="3f926-139">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ texture \_ repère \_ 3</span><span class="sxs-lookup"><span data-stu-id="3f926-139">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="3f926-140">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ texture \_ Coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="3f926-140">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="3f926-141">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="3f926-141">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_3</span></span>

<span data-ttu-id="3f926-142">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="3f926-142">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_4</span></span>

<span data-ttu-id="3f926-143">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ index</span><span class="sxs-lookup"><span data-stu-id="3f926-143">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_INDEX</span></span>

<span data-ttu-id="3f926-144">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ couleur \_ 4</span><span class="sxs-lookup"><span data-stu-id="3f926-144">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_COLOR\_4</span></span>

<span data-ttu-id="3f926-145">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ normal</span><span class="sxs-lookup"><span data-stu-id="3f926-145">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_NORMAL</span></span>

<span data-ttu-id="3f926-146">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ texture \_ Coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="3f926-146">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="3f926-147">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ texture \_ Coord \_ 2</span><span class="sxs-lookup"><span data-stu-id="3f926-147">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="3f926-148">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ texture \_ repère \_ 3</span><span class="sxs-lookup"><span data-stu-id="3f926-148">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="3f926-149">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ texture \_ Coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="3f926-149">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="3f926-150">[**glIsEnabled**](glisenabled.md) avec l’argument GL \_ auto \_ normal</span><span class="sxs-lookup"><span data-stu-id="3f926-150">[**glIsEnabled**](glisenabled.md) with argument GL\_AUTO\_NORMAL</span></span>

## <a name="requirements"></a><span data-ttu-id="3f926-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f926-151">Requirements</span></span>



| <span data-ttu-id="3f926-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f926-152">Requirement</span></span> | <span data-ttu-id="3f926-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f926-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f926-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f926-154">Minimum supported client</span></span><br/> | <span data-ttu-id="3f926-155">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f926-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3f926-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f926-156">Minimum supported server</span></span><br/> | <span data-ttu-id="3f926-157">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f926-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3f926-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="3f926-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f926-159"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f926-159"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3f926-160">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3f926-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="3f926-161"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f926-161"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3f926-162">DLL</span><span class="sxs-lookup"><span data-stu-id="3f926-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f926-163"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f926-163"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f926-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f926-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f926-165">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3f926-165">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3f926-166">**glColor**</span><span class="sxs-lookup"><span data-stu-id="3f926-166">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="3f926-167">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="3f926-167">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="3f926-168">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="3f926-168">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="3f926-169">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="3f926-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3f926-170">**glEvalMesh**</span><span class="sxs-lookup"><span data-stu-id="3f926-170">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="3f926-171">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="3f926-171">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="3f926-172">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="3f926-172">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="3f926-173">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="3f926-173">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="3f926-174">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="3f926-174">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="3f926-175">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="3f926-175">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="3f926-176">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="3f926-176">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="3f926-177">**glMapGrid**</span><span class="sxs-lookup"><span data-stu-id="3f926-177">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> <dt>

[<span data-ttu-id="3f926-178">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="3f926-178">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="3f926-179">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="3f926-179">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="3f926-180">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="3f926-180">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





