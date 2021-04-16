---
title: fonction glEvalCoord2fv (GL. h)
description: La fonction glEvalCoord2fv évalue les mappages à deux dimensions activés.
ms.assetid: fff786b4-a9e1-4f3e-a62e-36e89bc9c35d
keywords:
- glEvalCoord2fv fonction OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord2fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e277b0b71361588f8a9835ec3b8891b49f9482a
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104566363"
---
# <a name="glevalcoord2fv-function"></a><span data-ttu-id="ab6b0-104">glEvalCoord2fv fonction)</span><span class="sxs-lookup"><span data-stu-id="ab6b0-104">glEvalCoord2fv function</span></span>

<span data-ttu-id="ab6b0-105">La fonction **glEvalCoord2fv** évalue les mappages à deux dimensions activés.</span><span class="sxs-lookup"><span data-stu-id="ab6b0-105">The **glEvalCoord2fv** function evaluates enabled two-dimensional maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab6b0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab6b0-106">Syntax</span></span>


```C++
void WINAPI glEvalCoord2fv(
   const GLfloat *u
);
```



## <a name="parameters"></a><span data-ttu-id="ab6b0-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab6b0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab6b0-108">*u*</span><span class="sxs-lookup"><span data-stu-id="ab6b0-108">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="ab6b0-109">Pointeur vers un tableau contenant la coordonnée de domaine *u*.</span><span class="sxs-lookup"><span data-stu-id="ab6b0-109">A pointer to an array containing the domain coordinate *u*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab6b0-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ab6b0-110">Return value</span></span>

<span data-ttu-id="ab6b0-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ab6b0-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab6b0-112">Notes</span><span class="sxs-lookup"><span data-stu-id="ab6b0-112">Remarks</span></span>

<span data-ttu-id="ab6b0-113">La fonction **glEvalCoord2fv** évalue les mappages à deux dimensions activés à l’aide de deux valeurs de domaine, *u* et *v*.</span><span class="sxs-lookup"><span data-stu-id="ab6b0-113">The **glEvalCoord2fv** function evaluates enabled two-dimensional maps using two domain values, *u* and *v*.</span></span> <span data-ttu-id="ab6b0-114">Définissez Maps avec [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="ab6b0-114">Define maps with [**glMap1**](glmap1.md).</span></span> <span data-ttu-id="ab6b0-115">Activez ou désactivez-les avec [**glEnable**](glenable.md) et [**glDisable**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="ab6b0-115">Enable or disable them with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="ab6b0-116">Lorsque l’une des fonctions **glEvalCoord** est émise, tous les mappages actuellement activés de la dimension indiquée sont évalués.</span><span class="sxs-lookup"><span data-stu-id="ab6b0-116">When one of the **glEvalCoord** functions is issued, all currently enabled maps of the indicated dimension are evaluated.</span></span> <span data-ttu-id="ab6b0-117">Ensuite, pour chaque mappage activé, c’est comme si la fonction OpenGL correspondante avait été émise avec la valeur calculée.</span><span class="sxs-lookup"><span data-stu-id="ab6b0-117">Then, for each enabled map, it is as if the corresponding OpenGL function were issued with the computed value.</span></span> <span data-ttu-id="ab6b0-118">Autrement dit, si l’index \_ Map1 GL \_ ou l' \_ index map2 GL \_ est activé, une fonction [**glIndex**](glindex-functions.md) est simulée.</span><span class="sxs-lookup"><span data-stu-id="ab6b0-118">That is, if GL\_MAP1\_INDEX or GL\_MAP2\_INDEX is enabled, a [**glIndex**](glindex-functions.md) function is simulated.</span></span> <span data-ttu-id="ab6b0-119">Si GL \_ Map1 \_ Color \_ 4 ou GL \_ map2 \_ Color \_ 4 est activé, une fonction **glcolor** est simulée.</span><span class="sxs-lookup"><span data-stu-id="ab6b0-119">If GL\_MAP1\_COLOR\_4 or GL\_MAP2\_COLOR\_4 is enabled, a **glcolor** function is simulated.</span></span> <span data-ttu-id="ab6b0-120">Si GL \_ Map1 \_ normal ou GL \_ map2 \_ normal est activé, un vecteur normal est produit, et si l’un des \_ Map1 de \_ texture GL \_ Coord \_ 1, GL \_ Map1 texture Coord \_ \_ \_ 2, GL \_ Map1 texture Coord \_ \_ \_ 3, GL \_ Map1 \_ texture \_ Coord 4, GL map2 texture Coord \_ \_ \_ \_ \_ 1, GL \_ map2 \_ texture \_ Coord \_ 2, GL \_ map2 \_ texture \_ Coord \_ 3 et GL \_ map2 \_ texture \_ Coord \_ 4 est activé, une fonction [**glTexCoord**](gltexcoord-functions.md) appropriée est simulée.</span><span class="sxs-lookup"><span data-stu-id="ab6b0-120">If GL\_MAP1\_NORMAL or GL\_MAP2\_NORMAL is enabled, a normal vector is produced, and if any of GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, and GL\_MAP2\_TEXTURE\_COORD\_4 is enabled, then an appropriate [**glTexCoord**](gltexcoord-functions.md) function is simulated.</span></span>

<span data-ttu-id="ab6b0-121">OpenGL utilise des valeurs évaluées au lieu des valeurs actuelles pour les évaluations qui sont activées, et les valeurs actuelles dans le cas contraire, pour les coordonnées de couleur, d’index de couleur, normales et de texture.</span><span class="sxs-lookup"><span data-stu-id="ab6b0-121">OpenGL uses evaluated values instead of current values for those evaluations that are enabled, and current values otherwise, for color, color index, normal, and texture coordinates.</span></span> <span data-ttu-id="ab6b0-122">Toutefois, les valeurs évaluées ne mettent pas à jour les valeurs actuelles.</span><span class="sxs-lookup"><span data-stu-id="ab6b0-122">However, the evaluated values do not update the current values.</span></span> <span data-ttu-id="ab6b0-123">Ainsi, si les fonctions [**glVertex**](glvertex-functions.md) sont intercalées avec les fonctions **glEvalCoord** , les coordonnées de couleur, normale et de texture associées aux fonctions **glVertex** ne sont pas affectées par les valeurs générées par les fonctions **GlEvalCoord** , mais uniquement par les fonctions [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md)et [**glTexCoord**](gltexcoord-functions.md) les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="ab6b0-123">Thus, if [**glVertex**](glvertex-functions.md) functions are interspersed with **glEvalCoord** functions, the color, normal, and texture coordinates associated with the **glVertex** functions are not affected by the values generated by the **glEvalCoord** functions, but only by the most recent [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md), and [**glTexCoord**](gltexcoord-functions.md) functions.</span></span>

<span data-ttu-id="ab6b0-124">Si la génération automatique normale est activée, **glEvalCoord2fv** appelle [**glEnable**](glenable.md) avec l’argument GL \_ auto \_ normal pour générer des normales de surface analytiques, quel que soit le contenu ou l’activation de la \_ \_ carte normale GL map2.</span><span class="sxs-lookup"><span data-stu-id="ab6b0-124">If automatic normal generation is enabled, **glEvalCoord2fv** calls [**glEnable**](glenable.md) with argument GL\_AUTO\_NORMAL to generate surface normals analytically, regardless of the contents or enabling of the GL\_MAP2\_NORMAL map.</span></span> <span data-ttu-id="ab6b0-125">Let</span><span class="sxs-lookup"><span data-stu-id="ab6b0-125">Let</span></span>

![Équation représentant une valeur de produit croisé pour une carte m.](images/evlcrd01.png)

<span data-ttu-id="ab6b0-127">Le **n** normal généré est</span><span class="sxs-lookup"><span data-stu-id="ab6b0-127">The generated normal **n** is</span></span>

![Équation qui indique la n normale générée pour la carte.](images/evlcrd02.png)

<span data-ttu-id="ab6b0-129">Les fonctions suivantes récupèrent les informations relatives à la fonction **glEvalCoord2fv** :</span><span class="sxs-lookup"><span data-stu-id="ab6b0-129">The following functions retrieve information related to the **glEvalCoord2fv** function:</span></span>

<span data-ttu-id="ab6b0-130">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="ab6b0-130">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_3</span></span>

<span data-ttu-id="ab6b0-131">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="ab6b0-131">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_4</span></span>

<span data-ttu-id="ab6b0-132">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ index</span><span class="sxs-lookup"><span data-stu-id="ab6b0-132">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_INDEX</span></span>

<span data-ttu-id="ab6b0-133">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ couleur \_ 4</span><span class="sxs-lookup"><span data-stu-id="ab6b0-133">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_COLOR\_4</span></span>

<span data-ttu-id="ab6b0-134">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ normal</span><span class="sxs-lookup"><span data-stu-id="ab6b0-134">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_NORMAL</span></span>

<span data-ttu-id="ab6b0-135">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ texture \_ Coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="ab6b0-135">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="ab6b0-136">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ texture \_ Coord \_ 2</span><span class="sxs-lookup"><span data-stu-id="ab6b0-136">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="ab6b0-137">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ texture \_ repère \_ 3</span><span class="sxs-lookup"><span data-stu-id="ab6b0-137">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="ab6b0-138">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ texture \_ Coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="ab6b0-138">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="ab6b0-139">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="ab6b0-139">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_3</span></span>

<span data-ttu-id="ab6b0-140">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="ab6b0-140">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_4</span></span>

<span data-ttu-id="ab6b0-141">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ index</span><span class="sxs-lookup"><span data-stu-id="ab6b0-141">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_INDEX</span></span>

<span data-ttu-id="ab6b0-142">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ couleur \_ 4</span><span class="sxs-lookup"><span data-stu-id="ab6b0-142">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_COLOR\_4</span></span>

<span data-ttu-id="ab6b0-143">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ normal</span><span class="sxs-lookup"><span data-stu-id="ab6b0-143">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_NORMAL</span></span>

<span data-ttu-id="ab6b0-144">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ texture \_ Coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="ab6b0-144">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="ab6b0-145">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ texture \_ Coord \_ 2</span><span class="sxs-lookup"><span data-stu-id="ab6b0-145">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="ab6b0-146">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ texture \_ repère \_ 3</span><span class="sxs-lookup"><span data-stu-id="ab6b0-146">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="ab6b0-147">[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ texture \_ Coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="ab6b0-147">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="ab6b0-148">[**glIsEnabled**](glisenabled.md) avec l’argument GL \_ auto \_ normal</span><span class="sxs-lookup"><span data-stu-id="ab6b0-148">[**glIsEnabled**](glisenabled.md) with argument GL\_AUTO\_NORMAL</span></span>

## <a name="requirements"></a><span data-ttu-id="ab6b0-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab6b0-149">Requirements</span></span>



| <span data-ttu-id="ab6b0-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab6b0-150">Requirement</span></span> | <span data-ttu-id="ab6b0-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab6b0-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab6b0-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab6b0-152">Minimum supported client</span></span><br/> | <span data-ttu-id="ab6b0-153">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab6b0-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ab6b0-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab6b0-154">Minimum supported server</span></span><br/> | <span data-ttu-id="ab6b0-155">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab6b0-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ab6b0-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="ab6b0-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab6b0-157"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab6b0-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ab6b0-158">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ab6b0-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="ab6b0-159"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab6b0-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ab6b0-160">DLL</span><span class="sxs-lookup"><span data-stu-id="ab6b0-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab6b0-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab6b0-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab6b0-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab6b0-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab6b0-163">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ab6b0-163">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ab6b0-164">**glColor**</span><span class="sxs-lookup"><span data-stu-id="ab6b0-164">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="ab6b0-165">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="ab6b0-165">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="ab6b0-166">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="ab6b0-166">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="ab6b0-167">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="ab6b0-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="ab6b0-168">**glEvalMesh**</span><span class="sxs-lookup"><span data-stu-id="ab6b0-168">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="ab6b0-169">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="ab6b0-169">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="ab6b0-170">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="ab6b0-170">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="ab6b0-171">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="ab6b0-171">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="ab6b0-172">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="ab6b0-172">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="ab6b0-173">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="ab6b0-173">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="ab6b0-174">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="ab6b0-174">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="ab6b0-175">**glMapGrid**</span><span class="sxs-lookup"><span data-stu-id="ab6b0-175">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> <dt>

[<span data-ttu-id="ab6b0-176">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="ab6b0-176">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="ab6b0-177">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="ab6b0-177">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="ab6b0-178">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="ab6b0-178">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





