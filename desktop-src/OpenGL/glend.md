---
title: fonction glEnd (GL. h)
description: Les fonctions glBegin et Glend délimitent les vertex d’une primitive ou d’un groupe de primitives similaires. | fonction glEnd (GL. h)
ms.assetid: 040f8573-683c-4a8a-ae51-66abb0541ac4
keywords:
- glEnd fonction OpenGL
topic_type:
- apiref
api_name:
- glEnd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9bb41395b3ed2e38a64094506e07e2a69ad1d52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522297"
---
# <a name="glend-function"></a><span data-ttu-id="4271b-105">glEnd fonction)</span><span class="sxs-lookup"><span data-stu-id="4271b-105">glEnd function</span></span>

<span data-ttu-id="4271b-106">Les fonctions [**glBegin**](glbegin.md) et **Glend** délimitent les vertex d’une primitive ou d’un groupe de primitives similaires.</span><span class="sxs-lookup"><span data-stu-id="4271b-106">The [**glBegin**](glbegin.md) and **glend** functions delimit the vertices of a primitive or a group of like primitives.</span></span>

## <a name="syntax"></a><span data-ttu-id="4271b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4271b-107">Syntax</span></span>


```C++
void WINAPI glEnd(void);
```



## <a name="parameters"></a><span data-ttu-id="4271b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4271b-108">Parameters</span></span>

<span data-ttu-id="4271b-109">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="4271b-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4271b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4271b-110">Return value</span></span>

<span data-ttu-id="4271b-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4271b-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4271b-112">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="4271b-112">Error codes</span></span>

<span data-ttu-id="4271b-113">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="4271b-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="4271b-114">Nom</span><span class="sxs-lookup"><span data-stu-id="4271b-114">Name</span></span>                                                                                                  | <span data-ttu-id="4271b-115">Signification</span><span class="sxs-lookup"><span data-stu-id="4271b-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4271b-116"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4271b-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="4271b-117">Une fonction autre que **glVertex**, **glColor**, **glIndex**, **glNormal**, **glTexCoord**, **glEvalCoord**, **GlEvalPoint**, **glMaterial**, **glEdgeFlag**, **glCallList** ou **glCallLists** a été appelée entre **glBegin** et le **glEnd** correspondant.</span><span class="sxs-lookup"><span data-stu-id="4271b-117">A function other than **glVertex**, **glColor**, **glIndex**, **glNormal**, **glTexCoord**, **glEvalCoord**, **glEvalPoint**, **glMaterial**, **glEdgeFlag**, **glCallList**, or **glCallLists** was called between **glBegin** and the corresponding **glEnd**.</span></span> <span data-ttu-id="4271b-118">La fonction **glEnd** a été appelée avant l’appel de la méthode **glBegin** correspondante, ou **glBegin** a été appelée dans une  / séquence **glEnd** glBegin.</span><span class="sxs-lookup"><span data-stu-id="4271b-118">The function **glEnd** was called before the corresponding **glBegin** was called, or **glBegin** was called within a **glBegin**/**glEnd** sequence.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="4271b-119">Notes</span><span class="sxs-lookup"><span data-stu-id="4271b-119">Remarks</span></span>

<span data-ttu-id="4271b-120">Les fonctions [**glBegin**](glbegin.md) et **Glend** délimitent les vertex qui définissent une primitive ou un groupe de primitives similaires.</span><span class="sxs-lookup"><span data-stu-id="4271b-120">The [**glBegin**](glbegin.md) and **glend** functions delimit the vertices that define a primitive or a group of like primitives.</span></span> <span data-ttu-id="4271b-121">La fonction **glBegin** accepte un argument unique qui spécifie laquelle des dix primitives compose les sommets.</span><span class="sxs-lookup"><span data-stu-id="4271b-121">The **glBegin** function accepts a single argument that specifies which of ten primitives the vertices compose.</span></span> <span data-ttu-id="4271b-122">En acceptant *n* comme nombre entier à partir de 1, et *n* comme nombre total de vertex spécifiés, les interprétations sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="4271b-122">Taking *n* as an integer count starting at one, and *N* as the total number of vertices specified, the interpretations are as follows:</span></span>

-   <span data-ttu-id="4271b-123">Vous ne pouvez utiliser qu’un sous-ensemble de fonctions OpenGL entre **glBegin** et **glEnd**.</span><span class="sxs-lookup"><span data-stu-id="4271b-123">You can use only a subset of OpenGL functions between **glBegin** and **glEnd**.</span></span> <span data-ttu-id="4271b-124">Les fonctions que vous pouvez utiliser sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="4271b-124">The functions you can use are:</span></span>

    -   [<span data-ttu-id="4271b-125">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="4271b-125">**glVertex**</span></span>](glvertex-functions.md)
    -   [<span data-ttu-id="4271b-126">**glColor**</span><span class="sxs-lookup"><span data-stu-id="4271b-126">**glColor**</span></span>](glcolor-functions.md)
    -   [<span data-ttu-id="4271b-127">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="4271b-127">**glIndex**</span></span>](glindex-functions.md)
    -   [<span data-ttu-id="4271b-128">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="4271b-128">**glNormal**</span></span>](glnormal-functions.md)
    -   [<span data-ttu-id="4271b-129">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="4271b-129">**glTexCoord**</span></span>](gltexcoord-functions.md)
    -   [<span data-ttu-id="4271b-130">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="4271b-130">**glEvalCoord**</span></span>](glevalcoord-functions.md)
    -   [<span data-ttu-id="4271b-131">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="4271b-131">**glEvalPoint**</span></span>](glevalpoint.md)
    -   [<span data-ttu-id="4271b-132">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="4271b-132">**glMaterial**</span></span>](glmaterial-functions.md)
    -   [<span data-ttu-id="4271b-133">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="4271b-133">**glEdgeFlag**</span></span>](gledgeflag-functions.md)

    <span data-ttu-id="4271b-134">Vous pouvez également utiliser [**glCallList**](glcalllist.md) ou [**glCallLists**](glcalllists.md) pour exécuter des listes d’affichage qui incluent uniquement les fonctions précédentes.</span><span class="sxs-lookup"><span data-stu-id="4271b-134">You can also use [**glCallList**](glcalllist.md) or [**glCallLists**](glcalllists.md) to execute display lists that include only the preceding functions.</span></span> <span data-ttu-id="4271b-135">Si une autre fonction OpenGL est appelée entre **glBegin** et **glEnd**, l’indicateur d’erreur est défini et la fonction est ignorée.</span><span class="sxs-lookup"><span data-stu-id="4271b-135">If any other OpenGL function is called between **glBegin** and **glEnd**, the error flag is set and the function is ignored.</span></span>

-   <span data-ttu-id="4271b-136">Quelle que soit la valeur choisie pour *mode* dans **glBegin**, il n’y a aucune limite au nombre de vertex que vous pouvez définir entre **glBegin** et **glEnd**.</span><span class="sxs-lookup"><span data-stu-id="4271b-136">Regardless of the value chosen for *mode* in **glBegin**, there is no limit to the number of vertices you can define between **glBegin** and **glEnd**.</span></span> <span data-ttu-id="4271b-137">Les lignes, triangles, quadrilatères et polygones qui ne sont pas complets spécifiés ne sont pas dessinés.</span><span class="sxs-lookup"><span data-stu-id="4271b-137">Lines, triangles, quadrilaterals, and polygons that are incompletely specified are not drawn.</span></span> <span data-ttu-id="4271b-138">Les résultats de spécifications sont incomplets lorsqu’un nombre trop faible de vertex est fourni pour spécifier une seule primitive ou lorsqu’un multiple de vertex incorrect est spécifié.</span><span class="sxs-lookup"><span data-stu-id="4271b-138">Incomplete specification results when either too few vertices are provided to specify even a single primitive or when an incorrect multiple of vertices is specified.</span></span> <span data-ttu-id="4271b-139">La primitive incomplète est ignorée ; les primitives complètes sont dessinées.</span><span class="sxs-lookup"><span data-stu-id="4271b-139">The incomplete primitive is ignored; the complete primitives are drawn.</span></span>
-   <span data-ttu-id="4271b-140">La spécification minimale des vertex pour chaque primitive est la suivante :</span><span class="sxs-lookup"><span data-stu-id="4271b-140">The minimum specification of vertices for each primitive is:</span></span> 

    | <span data-ttu-id="4271b-141">Nombre minimal de vertex</span><span class="sxs-lookup"><span data-stu-id="4271b-141">Minimum number of vertices</span></span> | <span data-ttu-id="4271b-142">Type de primitive</span><span class="sxs-lookup"><span data-stu-id="4271b-142">Type of primitive</span></span> |
    |----------------------------|-------------------|
    | <span data-ttu-id="4271b-143">1</span><span class="sxs-lookup"><span data-stu-id="4271b-143">1</span></span>                          | <span data-ttu-id="4271b-144">point</span><span class="sxs-lookup"><span data-stu-id="4271b-144">point</span></span>             |
    | <span data-ttu-id="4271b-145">2</span><span class="sxs-lookup"><span data-stu-id="4271b-145">2</span></span>                          | <span data-ttu-id="4271b-146">line</span><span class="sxs-lookup"><span data-stu-id="4271b-146">line</span></span>              |
    | <span data-ttu-id="4271b-147">3</span><span class="sxs-lookup"><span data-stu-id="4271b-147">3</span></span>                          | <span data-ttu-id="4271b-148">triangle</span><span class="sxs-lookup"><span data-stu-id="4271b-148">triangle</span></span>          |
    | <span data-ttu-id="4271b-149">4</span><span class="sxs-lookup"><span data-stu-id="4271b-149">4</span></span>                          | <span data-ttu-id="4271b-150">quadrangulaires</span><span class="sxs-lookup"><span data-stu-id="4271b-150">quadrilateral</span></span>     |
    | <span data-ttu-id="4271b-151">3</span><span class="sxs-lookup"><span data-stu-id="4271b-151">3</span></span>                          | <span data-ttu-id="4271b-152">polygon</span><span class="sxs-lookup"><span data-stu-id="4271b-152">polygon</span></span>           |

    

     

-   <span data-ttu-id="4271b-153">Les modes qui requièrent un certain nombre de vertex sont les lignes de GL \_ (2), les \_ triangles GL (3), \_ les quads GL (4) et le GL \_ Quad \_ Strip (2).</span><span class="sxs-lookup"><span data-stu-id="4271b-153">Modes that require a certain multiple of vertices are GL\_LINES (2), GL\_TRIANGLES (3), GL\_QUADS (4), and GL\_QUAD\_STRIP (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="4271b-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4271b-154">Requirements</span></span>



| <span data-ttu-id="4271b-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4271b-155">Requirement</span></span> | <span data-ttu-id="4271b-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="4271b-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4271b-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4271b-157">Minimum supported client</span></span><br/> | <span data-ttu-id="4271b-158">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4271b-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4271b-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4271b-159">Minimum supported server</span></span><br/> | <span data-ttu-id="4271b-160">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4271b-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4271b-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="4271b-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="4271b-162"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4271b-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4271b-163">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4271b-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="4271b-164"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4271b-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4271b-165">DLL</span><span class="sxs-lookup"><span data-stu-id="4271b-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4271b-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4271b-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4271b-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4271b-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4271b-168">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="4271b-168">**glBegin**</span></span>](/windows/desktop/OpenGL/glbegin)
</dt> <dt>

[<span data-ttu-id="4271b-169">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="4271b-169">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="4271b-170">**glColor**</span><span class="sxs-lookup"><span data-stu-id="4271b-170">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="4271b-171">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="4271b-171">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="4271b-172">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="4271b-172">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="4271b-173">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="4271b-173">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="4271b-174">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="4271b-174">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="4271b-175">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="4271b-175">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="4271b-176">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="4271b-176">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="4271b-177">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="4271b-177">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="4271b-178">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="4271b-178">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

