---
title: fonction glEvalCoord2f (GL. h)
description: La fonction glEvalCoord2f évalue les mappages à deux dimensions activés.
ms.assetid: feb2a324-9148-4e3f-8e6e-c545e36962c6
keywords:
- glEvalCoord2f fonction OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord2f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e586991b319e047957ae53362534c1bb0c90590
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104321341"
---
# <a name="glevalcoord2f-function"></a><span data-ttu-id="bade8-104">glEvalCoord2f fonction)</span><span class="sxs-lookup"><span data-stu-id="bade8-104">glEvalCoord2f function</span></span>

<span data-ttu-id="bade8-105">La fonction [**glEvalCoord2f**](glevalcoord2d.md) évalue les mappages à deux dimensions activés.</span><span class="sxs-lookup"><span data-stu-id="bade8-105">The [**glEvalCoord2f**](glevalcoord2d.md) function evaluates enabled two-dimensional maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="bade8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bade8-106">Syntax</span></span>


```C++
void WINAPI glEvalCoord2f(
   GLfloat u,
   GLfloat v
);
```



## <a name="parameters"></a><span data-ttu-id="bade8-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bade8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bade8-108">*u*</span><span class="sxs-lookup"><span data-stu-id="bade8-108">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="bade8-109">Valeur qui est la coordonnée de domaine *u* à la fonction de base définie dans une fonction [**glMap2**](glmap2.md) précédente.</span><span class="sxs-lookup"><span data-stu-id="bade8-109">A value that is the domain coordinate *u* to the basis function defined in a previous [**glMap2**](glmap2.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="bade8-110">*v*</span><span class="sxs-lookup"><span data-stu-id="bade8-110">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="bade8-111">Valeur qui est la coordonnée de domaine *v* à la fonction de base définie dans une fonction [**glMap2**](glmap2.md) précédente.</span><span class="sxs-lookup"><span data-stu-id="bade8-111">A value that is the domain coordinate *v* to the basis function defined in a previous [**glMap2**](glmap2.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bade8-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bade8-112">Return value</span></span>

<span data-ttu-id="bade8-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="bade8-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bade8-114">Notes</span><span class="sxs-lookup"><span data-stu-id="bade8-114">Remarks</span></span>

<span data-ttu-id="bade8-115">La fonction [**glEvalCoord2f**](glevalcoord2d.md) évalue les mappages à deux dimensions activés à l’aide de deux valeurs de domaine, *u* et *v*.</span><span class="sxs-lookup"><span data-stu-id="bade8-115">The [**glEvalCoord2f**](glevalcoord2d.md) function evaluates enabled two-dimensional maps using two domain values, *u* and *v*.</span></span> <span data-ttu-id="bade8-116">Définissez Maps avec [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="bade8-116">Define maps with [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="bade8-117">Activez ou désactivez-les avec [**glEnable**](glenable.md) et [**glDisable**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="bade8-117">Enable or disable them with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="bade8-118">Lorsque l’une des fonctions **glEvalCoord** est émise, tous les mappages actuellement activés de la dimension indiquée sont évalués.</span><span class="sxs-lookup"><span data-stu-id="bade8-118">When one of the **glEvalCoord** functions is issued, all currently enabled maps of the indicated dimension are evaluated.</span></span> <span data-ttu-id="bade8-119">Ensuite, pour chaque mappage activé, c’est comme si la fonction OpenGL correspondante avait été émise avec la valeur calculée.</span><span class="sxs-lookup"><span data-stu-id="bade8-119">Then, for each enabled map, it is as if the corresponding OpenGL function were issued with the computed value.</span></span> <span data-ttu-id="bade8-120">Autrement dit, si l’index \_ Map1 GL \_ ou l' \_ index map2 GL \_ est activé, une fonction [**glIndex**](glindex-functions.md) est simulée.</span><span class="sxs-lookup"><span data-stu-id="bade8-120">That is, if GL\_MAP1\_INDEX or GL\_MAP2\_INDEX is enabled, a [**glIndex**](glindex-functions.md) function is simulated.</span></span> <span data-ttu-id="bade8-121">Si GL \_ Map1 \_ Color \_ 4 ou GL \_ map2 \_ Color \_ 4 est activé, une fonction **glcolor** est simulée.</span><span class="sxs-lookup"><span data-stu-id="bade8-121">If GL\_MAP1\_COLOR\_4 or GL\_MAP2\_COLOR\_4 is enabled, a **glcolor** function is simulated.</span></span> <span data-ttu-id="bade8-122">Si GL \_ Map1 \_ normal ou GL \_ map2 \_ normal est activé, un vecteur normal est produit, et si l’un des \_ Map1 de \_ texture GL \_ Coord \_ 1, GL \_ Map1 texture Coord \_ \_ \_ 2, GL \_ Map1 texture Coord \_ \_ \_ 3, GL \_ Map1 \_ texture \_ Coord 4, GL map2 texture Coord \_ \_ \_ \_ \_ 1, GL \_ map2 \_ texture \_ Coord \_ 2, GL \_ map2 \_ texture \_ Coord \_ 3 et GL \_ map2 \_ texture \_ Coord \_ 4 est activé, une fonction [**glTexCoord**](gltexcoord-functions.md) appropriée est simulée.</span><span class="sxs-lookup"><span data-stu-id="bade8-122">If GL\_MAP1\_NORMAL or GL\_MAP2\_NORMAL is enabled, a normal vector is produced, and if any of GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, and GL\_MAP2\_TEXTURE\_COORD\_4 is enabled, then an appropriate [**glTexCoord**](gltexcoord-functions.md) function is simulated.</span></span>

<span data-ttu-id="bade8-123">OpenGL utilise des valeurs évaluées au lieu des valeurs actuelles pour les évaluations qui sont activées, et les valeurs actuelles dans le cas contraire, pour les coordonnées de couleur, d’index de couleur, normales et de texture.</span><span class="sxs-lookup"><span data-stu-id="bade8-123">OpenGL uses evaluated values instead of current values for those evaluations that are enabled, and current values otherwise, for color, color index, normal, and texture coordinates.</span></span> <span data-ttu-id="bade8-124">Toutefois, les valeurs évaluées ne mettent pas à jour les valeurs actuelles.</span><span class="sxs-lookup"><span data-stu-id="bade8-124">However, the evaluated values do not update the current values.</span></span> <span data-ttu-id="bade8-125">Ainsi, si les fonctions [**glVertex**](glvertex-functions.md) sont intercalées avec les fonctions **glEvalCoord** , les coordonnées de couleur, normale et de texture associées aux fonctions **glVertex** ne sont pas affectées par les valeurs générées par les fonctions **GlEvalCoord** , mais uniquement par les fonctions [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md)et [**glTexCoord**](gltexcoord-functions.md) les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="bade8-125">Thus, if [**glVertex**](glvertex-functions.md) functions are interspersed with **glEvalCoord** functions, the color, normal, and texture coordinates associated with the **glVertex** functions are not affected by the values generated by the **glEvalCoord** functions, but only by the most recent [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md), and [**glTexCoord**](gltexcoord-functions.md) functions.</span></span>

<span data-ttu-id="bade8-126">Si la génération automatique normale est activée, [**glEvalCoord2f**](glevalcoord2d.md) appelle [**glEnable**](glenable.md) avec l’argument GL \_ auto \_ normal pour générer des normales de surface analytiques, quel que soit le contenu ou l’activation de la \_ \_ carte normale GL map2.</span><span class="sxs-lookup"><span data-stu-id="bade8-126">If automatic normal generation is enabled, [**glEvalCoord2f**](glevalcoord2d.md) calls [**glEnable**](glenable.md) with argument GL\_AUTO\_NORMAL to generate surface normals analytically, regardless of the contents or enabling of the GL\_MAP2\_NORMAL map.</span></span> <span data-ttu-id="bade8-127">Let</span><span class="sxs-lookup"><span data-stu-id="bade8-127">Let</span></span>

![Équation représentant une valeur de produit croisé pour une carte m.](images/evlcrd01.png)

<span data-ttu-id="bade8-129">Le **n** normal généré est</span><span class="sxs-lookup"><span data-stu-id="bade8-129">The generated normal **n** is</span></span>

![Équation qui indique la n normale générée pour la carte.](images/evlcrd02.png)

<span data-ttu-id="bade8-131">Les fonctions suivantes récupèrent les informations relatives à la fonction [**glEvalCoord2f**](glevalcoord2d.md) :</span><span class="sxs-lookup"><span data-stu-id="bade8-131">The following functions retrieve information related to the [**glEvalCoord2f**](glevalcoord2d.md) function:</span></span>

<span data-ttu-id="bade8-132">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="bade8-132">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_3</span></span>

<span data-ttu-id="bade8-133">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="bade8-133">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_4</span></span>

<span data-ttu-id="bade8-134">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ index</span><span class="sxs-lookup"><span data-stu-id="bade8-134">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_INDEX</span></span>

<span data-ttu-id="bade8-135">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ couleur \_ 4</span><span class="sxs-lookup"><span data-stu-id="bade8-135">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_COLOR\_4</span></span>

<span data-ttu-id="bade8-136">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ normal</span><span class="sxs-lookup"><span data-stu-id="bade8-136">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_NORMAL</span></span>

<span data-ttu-id="bade8-137">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ texture \_ Coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="bade8-137">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="bade8-138">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ texture \_ Coord \_ 2</span><span class="sxs-lookup"><span data-stu-id="bade8-138">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="bade8-139">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ texture \_ repère \_ 3</span><span class="sxs-lookup"><span data-stu-id="bade8-139">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="bade8-140">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ texture \_ Coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="bade8-140">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="bade8-141">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="bade8-141">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_3</span></span>

<span data-ttu-id="bade8-142">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="bade8-142">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_4</span></span>

<span data-ttu-id="bade8-143">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ index</span><span class="sxs-lookup"><span data-stu-id="bade8-143">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_INDEX</span></span>

<span data-ttu-id="bade8-144">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ couleur \_ 4</span><span class="sxs-lookup"><span data-stu-id="bade8-144">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_COLOR\_4</span></span>

<span data-ttu-id="bade8-145">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ normal</span><span class="sxs-lookup"><span data-stu-id="bade8-145">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_NORMAL</span></span>

<span data-ttu-id="bade8-146">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ texture \_ Coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="bade8-146">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="bade8-147">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ texture \_ Coord \_ 2</span><span class="sxs-lookup"><span data-stu-id="bade8-147">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="bade8-148">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ texture \_ repère \_ 3</span><span class="sxs-lookup"><span data-stu-id="bade8-148">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="bade8-149">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ texture \_ Coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="bade8-149">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="bade8-150">[**glIsEnabled**](glisenabled.md) avec l’argument GL \_ auto \_ normal</span><span class="sxs-lookup"><span data-stu-id="bade8-150">[**glIsEnabled**](glisenabled.md) with argument GL\_AUTO\_NORMAL</span></span>

## <a name="requirements"></a><span data-ttu-id="bade8-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bade8-151">Requirements</span></span>



| <span data-ttu-id="bade8-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bade8-152">Requirement</span></span> | <span data-ttu-id="bade8-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="bade8-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bade8-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bade8-154">Minimum supported client</span></span><br/> | <span data-ttu-id="bade8-155">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bade8-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bade8-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bade8-156">Minimum supported server</span></span><br/> | <span data-ttu-id="bade8-157">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bade8-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bade8-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="bade8-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="bade8-159"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="bade8-159"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="bade8-160">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bade8-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="bade8-161"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bade8-161"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bade8-162">DLL</span><span class="sxs-lookup"><span data-stu-id="bade8-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bade8-163"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bade8-163"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bade8-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bade8-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bade8-165">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="bade8-165">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="bade8-166">**glColor**</span><span class="sxs-lookup"><span data-stu-id="bade8-166">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="bade8-167">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="bade8-167">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="bade8-168">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="bade8-168">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="bade8-169">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="bade8-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="bade8-170">**glEvalMesh**</span><span class="sxs-lookup"><span data-stu-id="bade8-170">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="bade8-171">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="bade8-171">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="bade8-172">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="bade8-172">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="bade8-173">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="bade8-173">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="bade8-174">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="bade8-174">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="bade8-175">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="bade8-175">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="bade8-176">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="bade8-176">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="bade8-177">**glMapGrid**</span><span class="sxs-lookup"><span data-stu-id="bade8-177">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> <dt>

[<span data-ttu-id="bade8-178">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="bade8-178">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="bade8-179">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="bade8-179">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="bade8-180">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="bade8-180">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





