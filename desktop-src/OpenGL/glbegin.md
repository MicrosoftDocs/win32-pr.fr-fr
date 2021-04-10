---
title: fonction glBegin (GL. h)
description: Les fonctions glBegin et Glend délimitent les vertex d’une primitive ou d’un groupe de primitives similaires. | fonction glBegin (GL. h)
ms.assetid: 8e8e98f8-89e8-40f5-89c1-492c9e3bbd74
keywords:
- glBegin fonction OpenGL
topic_type:
- apiref
api_name:
- glBegin
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8227d30adf97bf27fecc19603a5e5e32e4f44822
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953672"
---
# <a name="glbegin-function"></a><span data-ttu-id="1a99e-105">glBegin fonction)</span><span class="sxs-lookup"><span data-stu-id="1a99e-105">glBegin function</span></span>

<span data-ttu-id="1a99e-106">Les fonctions **glBegin** et [**Glend**](glend.md) délimitent les vertex d’une primitive ou d’un groupe de primitives similaires.</span><span class="sxs-lookup"><span data-stu-id="1a99e-106">The **glBegin** and [**glend**](glend.md) functions delimit the vertices of a primitive or a group of like primitives.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a99e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a99e-107">Syntax</span></span>


```C++
void WINAPI glBegin(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="1a99e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a99e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a99e-109">*mode*</span><span class="sxs-lookup"><span data-stu-id="1a99e-109">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="1a99e-110">Primitives ou primitives qui seront créées à partir des vertex présentés entre les **glBegin** et les [**Glend**](glend.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="1a99e-110">The primitive or primitives that will be created from vertices presented between **glBegin** and the subsequent [**glend**](glend.md).</span></span> <span data-ttu-id="1a99e-111">Les constantes symboliques acceptées et leurs significations sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1a99e-111">The following are accepted symbolic constants and their meanings:</span></span>



| <span data-ttu-id="1a99e-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a99e-112">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="1a99e-113">Signification</span><span class="sxs-lookup"><span data-stu-id="1a99e-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINTS"></span><span id="gl_points"></span><dl> <span data-ttu-id="1a99e-114"><dt>**POINTS du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1a99e-114"><dt>**GL\_POINTS**</dt></span></span> </dl>                          | <span data-ttu-id="1a99e-115">Traite chaque vertex comme un point unique.</span><span class="sxs-lookup"><span data-stu-id="1a99e-115">Treats each vertex as a single point.</span></span> <span data-ttu-id="1a99e-116">Le vertex *n* définit le point *n*.</span><span class="sxs-lookup"><span data-stu-id="1a99e-116">Vertex *n* defines point *n*.</span></span> <span data-ttu-id="1a99e-117">*N* points sont dessinés.</span><span class="sxs-lookup"><span data-stu-id="1a99e-117">*N* points are drawn.</span></span><br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_LINES"></span><span id="gl_lines"></span><dl> <span data-ttu-id="1a99e-118"><dt>**\_lignes GL**</dt></span><span class="sxs-lookup"><span data-stu-id="1a99e-118"><dt>**GL\_LINES**</dt></span></span> </dl>                             | <span data-ttu-id="1a99e-119">Traite chaque paire de vertex comme un segment de ligne indépendant.</span><span class="sxs-lookup"><span data-stu-id="1a99e-119">Treats each pair of vertices as an independent line segment.</span></span> <span data-ttu-id="1a99e-120">Vertex *2n-1* et *2n* définir la ligne *n*.</span><span class="sxs-lookup"><span data-stu-id="1a99e-120">Vertices *2n - 1* and *2n* define line *n*.</span></span> <span data-ttu-id="1a99e-121">Les lignes *N/2* sont dessinées.</span><span class="sxs-lookup"><span data-stu-id="1a99e-121">*N/2* lines are drawn.</span></span><br/>                                                                                                                                                                                                                                                                |
| <span id="GL_LINE_STRIP"></span><span id="gl_line_strip"></span><dl> <span data-ttu-id="1a99e-122"><dt>**\_bande de lignes GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1a99e-122"><dt>**GL\_LINE\_STRIP**</dt></span></span> </dl>             | <span data-ttu-id="1a99e-123">Dessine un groupe connecté de segments de ligne du premier vertex au dernier.</span><span class="sxs-lookup"><span data-stu-id="1a99e-123">Draws a connected group of line segments from the first vertex to the last.</span></span> <span data-ttu-id="1a99e-124">Les vertex *n* et *n + 1* définissent la ligne *n*.</span><span class="sxs-lookup"><span data-stu-id="1a99e-124">Vertices *n* and *n+1* define line *n*.</span></span> <span data-ttu-id="1a99e-125">*N-1* lignes sont dessinées.</span><span class="sxs-lookup"><span data-stu-id="1a99e-125">*N - 1* lines are drawn.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="GL_LINE_LOOP"></span><span id="gl_line_loop"></span><dl> <span data-ttu-id="1a99e-126"><dt>**\_boucle de lignes GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1a99e-126"><dt>**GL\_LINE\_LOOP**</dt></span></span> </dl>                | <span data-ttu-id="1a99e-127">Dessine un groupe connecté de segments de ligne à partir du premier vertex jusqu’au dernier, puis de nouveau vers le premier.</span><span class="sxs-lookup"><span data-stu-id="1a99e-127">Draws a connected group of line segments from the first vertex to the last, then back to the first.</span></span> <span data-ttu-id="1a99e-128">Les vertex *n* et *n + 1* définissent la ligne *n*.</span><span class="sxs-lookup"><span data-stu-id="1a99e-128">Vertices *n* and *n + 1* define line *n*.</span></span> <span data-ttu-id="1a99e-129">La dernière ligne, toutefois, est définie par les vertex *N* et *1*.</span><span class="sxs-lookup"><span data-stu-id="1a99e-129">The last line, however, is defined by vertices *N* and *1*.</span></span> <span data-ttu-id="1a99e-130">*N* lignes sont dessinées.</span><span class="sxs-lookup"><span data-stu-id="1a99e-130">*N* lines are drawn.</span></span><br/>                                                                                                                                                                 |
| <span id="GL_TRIANGLES"></span><span id="gl_triangles"></span><dl> <span data-ttu-id="1a99e-131"><dt>**\_TRIangles GL**</dt></span><span class="sxs-lookup"><span data-stu-id="1a99e-131"><dt>**GL\_TRIANGLES**</dt></span></span> </dl>                 | <span data-ttu-id="1a99e-132">Traite chaque triplet de vertex comme un triangle indépendant.</span><span class="sxs-lookup"><span data-stu-id="1a99e-132">Treats each triplet of vertices as an independent triangle.</span></span> <span data-ttu-id="1a99e-133">Vertex *3n-2*, *3n-1* et *3N* définissent le triangle *n*.</span><span class="sxs-lookup"><span data-stu-id="1a99e-133">Vertices *3n - 2*, *3n - 1*, and *3n* define triangle *n*.</span></span> <span data-ttu-id="1a99e-134">Les triangles *N/3* sont dessinés.</span><span class="sxs-lookup"><span data-stu-id="1a99e-134">*N/3* triangles are drawn.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="GL_TRIANGLE_STRIP"></span><span id="gl_triangle_strip"></span><dl> <span data-ttu-id="1a99e-135"><dt>**\_bande triangulaire GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1a99e-135"><dt>**GL\_TRIANGLE\_STRIP**</dt></span></span> </dl> | <span data-ttu-id="1a99e-136">Dessine un groupe de triangles connecté.</span><span class="sxs-lookup"><span data-stu-id="1a99e-136">Draws a connected group of triangles.</span></span> <span data-ttu-id="1a99e-137">Un triangle est défini pour chaque vertex présenté après les deux premiers sommets.</span><span class="sxs-lookup"><span data-stu-id="1a99e-137">One triangle is defined for each vertex presented after the first two vertices.</span></span> <span data-ttu-id="1a99e-138">Pour *n*, les vertex *n*, *n + 1* et *n + 2* définissent le triangle *n*.</span><span class="sxs-lookup"><span data-stu-id="1a99e-138">For odd *n*, vertices *n*, *n + 1*, and *n + 2* define triangle *n*.</span></span> <span data-ttu-id="1a99e-139">Pour *n*, les sommets *n + 1*, *n* et *n + 2* définissent le triangle *n*.</span><span class="sxs-lookup"><span data-stu-id="1a99e-139">For even *n*, vertices *n + 1*, *n*, and *n + 2* define triangle *n*.</span></span> <span data-ttu-id="1a99e-140">Les triangles *N-2* sont dessinés.</span><span class="sxs-lookup"><span data-stu-id="1a99e-140">*N - 2* triangles are drawn.</span></span><br/>                                                                                                  |
| <span id="GL_TRIANGLE_FAN"></span><span id="gl_triangle_fan"></span><dl> <span data-ttu-id="1a99e-141"><dt>**\_ventilateur à triangles GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1a99e-141"><dt>**GL\_TRIANGLE\_FAN**</dt></span></span> </dl>       | <span data-ttu-id="1a99e-142">Dessine un groupe de triangles connecté.</span><span class="sxs-lookup"><span data-stu-id="1a99e-142">Draws a connected group of triangles.</span></span> <span data-ttu-id="1a99e-143">un triangle est défini pour chaque vertex présenté après les deux premiers sommets.</span><span class="sxs-lookup"><span data-stu-id="1a99e-143">one triangle is defined for each vertex presented after the first two vertices.</span></span> <span data-ttu-id="1a99e-144">Vertex *1*, *n + 1*, *n + 2* définissent le triangle *n*.</span><span class="sxs-lookup"><span data-stu-id="1a99e-144">Vertices *1*, *n + 1*, *n + 2* define triangle *n*.</span></span> <span data-ttu-id="1a99e-145">Les triangles *N-2* sont dessinés.</span><span class="sxs-lookup"><span data-stu-id="1a99e-145">*N - 2* triangles are drawn.</span></span><br/>                                                                                                                                                                                         |
| <span id="GL_QUADS"></span><span id="gl_quads"></span><dl> <span data-ttu-id="1a99e-146"><dt>**à \_ quatre processeurs GL**</dt></span><span class="sxs-lookup"><span data-stu-id="1a99e-146"><dt>**GL\_QUADS**</dt></span></span> </dl>                             | <span data-ttu-id="1a99e-147">Traite chaque groupe de quatre vertex comme un quadrangulaires indépendant.</span><span class="sxs-lookup"><span data-stu-id="1a99e-147">Treats each group of four vertices as an independent quadrilateral.</span></span> <span data-ttu-id="1a99e-148">Vertex *4n-3*, *4N-2*, *4N-1* et *4N* définir quadrangulaires *n*.</span><span class="sxs-lookup"><span data-stu-id="1a99e-148">Vertices *4n - 3*, *4n - 2*, *4n - 1*, and *4n* define quadrilateral *n*.</span></span> <span data-ttu-id="1a99e-149">Les quadrilatères *N/4* sont dessinés.</span><span class="sxs-lookup"><span data-stu-id="1a99e-149">*N/4* quadrilaterals are drawn.</span></span><br/>                                                                                                                                                                                                                  |
| <span id="GL_QUAD_STRIP"></span><span id="gl_quad_strip"></span><dl> <span data-ttu-id="1a99e-150"><dt>**à \_ quatre \_ bandes GL**</dt></span><span class="sxs-lookup"><span data-stu-id="1a99e-150"><dt>**GL\_QUAD\_STRIP**</dt></span></span> </dl>             | <span data-ttu-id="1a99e-151">Dessine un groupe connecté de quadrilatères.</span><span class="sxs-lookup"><span data-stu-id="1a99e-151">Draws a connected group of quadrilaterals.</span></span> <span data-ttu-id="1a99e-152">Un quadrangulaires est défini pour chaque paire de vertex présentée après la première paire.</span><span class="sxs-lookup"><span data-stu-id="1a99e-152">One quadrilateral is defined for each pair of vertices presented after the first pair.</span></span> <span data-ttu-id="1a99e-153">Les vertex *2n-1* *, 2n,* *2n + 2* et *2n + 1* définissent quadrangulaires *n*.</span><span class="sxs-lookup"><span data-stu-id="1a99e-153">Vertices *2n - 1*, *2n*, *2n + 2*, and *2n + 1* define quadrilateral *n*.</span></span> <span data-ttu-id="1a99e-154">*N/2-1* quadrilatères sont dessinés.</span><span class="sxs-lookup"><span data-stu-id="1a99e-154">*N/2 - 1* quadrilaterals are drawn.</span></span> <span data-ttu-id="1a99e-155">Notez que l’ordre dans lequel les vertex sont utilisés pour construire un quadrangulaires à partir de données de bandes est différent de celui utilisé avec les données indépendantes.</span><span class="sxs-lookup"><span data-stu-id="1a99e-155">Note that the order in which vertices are used to construct a quadrilateral from strip data is different from that used with independent data.</span></span><br/> |
| <span id="GL_POLYGON"></span><span id="gl_polygon"></span><dl> <span data-ttu-id="1a99e-156"><dt>**Polygone du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1a99e-156"><dt>**GL\_POLYGON**</dt></span></span> </dl>                       | <span data-ttu-id="1a99e-157">Dessine un polygone unique et convexe.</span><span class="sxs-lookup"><span data-stu-id="1a99e-157">Draws a single, convex polygon.</span></span> <span data-ttu-id="1a99e-158">Les vertex *1* à *N* définissent ce polygone.</span><span class="sxs-lookup"><span data-stu-id="1a99e-158">Vertices *1* through *N* define this polygon.</span></span><br/>                                                                                                                                                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a99e-159">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1a99e-159">Return value</span></span>

<span data-ttu-id="1a99e-160">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1a99e-160">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1a99e-161">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="1a99e-161">Error codes</span></span>

<span data-ttu-id="1a99e-162">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="1a99e-162">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1a99e-163">Nom</span><span class="sxs-lookup"><span data-stu-id="1a99e-163">Name</span></span>                                                                                                  | <span data-ttu-id="1a99e-164">Signification</span><span class="sxs-lookup"><span data-stu-id="1a99e-164">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1a99e-165"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1a99e-165"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="1a99e-166">le *mode* a été défini sur une valeur non acceptée.</span><span class="sxs-lookup"><span data-stu-id="1a99e-166">*mode* was set to an unaccepted value.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="1a99e-167"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1a99e-167"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="1a99e-168">Une fonction autre que [glVertex](glvertex-functions.md), [glColor](glcolor-functions.md), [glIndex](glindex-functions.md), [glNormal](glnormal-functions.md), [glTexCoord](gltexcoord-functions.md), [glEvalCoord](glevalcoord-functions.md), [GlEvalPoint](glevalpoint.md), [glMaterial](glmaterial-functions.md), [glEdgeFlag](gledgeflag-functions.md), [**glCallList**](glcalllist.md)ou [**glCallLists**](glcalllists.md) a été appelée entre **glBegin** et le [**Glend**](glend.md)correspondant.</span><span class="sxs-lookup"><span data-stu-id="1a99e-168">A function other than [glVertex](glvertex-functions.md), [glColor](glcolor-functions.md), [glIndex](glindex-functions.md), [glNormal](glnormal-functions.md), [glTexCoord](gltexcoord-functions.md), [glEvalCoord](glevalcoord-functions.md), [glEvalPoint](glevalpoint.md), [glMaterial](glmaterial-functions.md), [glEdgeFlag](gledgeflag-functions.md), [**glCallList**](glcalllist.md), or [**glCallLists**](glcalllists.md) was called between **glBegin** and the corresponding [**glend**](glend.md).</span></span> <span data-ttu-id="1a99e-169">La fonction **Glend** a été appelée avant l’appel de la méthode **glBegin** correspondante, ou **glBegin** a été appelée dans une  / séquence **Glend** glBegin.</span><span class="sxs-lookup"><span data-stu-id="1a99e-169">The function **glend** was called before the corresponding **glBegin** was called, or **glBegin** was called within a **glBegin**/**glend** sequence.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="1a99e-170">Notes</span><span class="sxs-lookup"><span data-stu-id="1a99e-170">Remarks</span></span>

<span data-ttu-id="1a99e-171">Les fonctions **glBegin** et [**Glend**](glend.md) délimitent les vertex qui définissent une primitive ou un groupe de primitives similaires.</span><span class="sxs-lookup"><span data-stu-id="1a99e-171">The **glBegin** and [**glend**](glend.md) functions delimit the vertices that define a primitive or a group of like primitives.</span></span> <span data-ttu-id="1a99e-172">La fonction **glBegin** accepte un argument unique qui spécifie laquelle des dix primitives compose les sommets.</span><span class="sxs-lookup"><span data-stu-id="1a99e-172">The **glBegin** function accepts a single argument that specifies which of ten primitives the vertices compose.</span></span> <span data-ttu-id="1a99e-173">En acceptant *n* comme nombre entier à partir de 1, et *n* comme nombre total de vertex spécifiés, les interprétations sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1a99e-173">Taking *n* as an integer count starting at one, and *N* as the total number of vertices specified, the interpretations are as follows:</span></span>

-   <span data-ttu-id="1a99e-174">Vous ne pouvez utiliser qu’un sous-ensemble de fonctions OpenGL entre **glBegin** et [**Glend**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="1a99e-174">You can use only a subset of OpenGL functions between **glBegin** and [**glend**](glend.md).</span></span> <span data-ttu-id="1a99e-175">Les fonctions que vous pouvez utiliser sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1a99e-175">The functions you can use are:</span></span>

    [<span data-ttu-id="1a99e-176">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="1a99e-176">**glVertex**</span></span>](glvertex-functions.md)

     

    [<span data-ttu-id="1a99e-177">**glColor**</span><span class="sxs-lookup"><span data-stu-id="1a99e-177">**glColor**</span></span>](glcolor-functions.md)

     

    [<span data-ttu-id="1a99e-178">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="1a99e-178">**glIndex**</span></span>](glindex-functions.md)

     

    [<span data-ttu-id="1a99e-179">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="1a99e-179">**glNormal**</span></span>](glnormal-functions.md)

     

    [<span data-ttu-id="1a99e-180">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="1a99e-180">**glTexCoord**</span></span>](gltexcoord-functions.md)

     

    [<span data-ttu-id="1a99e-181">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="1a99e-181">**glEvalCoord**</span></span>](glevalcoord-functions.md)

     

    [<span data-ttu-id="1a99e-182">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="1a99e-182">**glEvalPoint**</span></span>](glevalpoint.md)

     

    [<span data-ttu-id="1a99e-183">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="1a99e-183">**glMaterial**</span></span>](glmaterial-functions.md)

     

    [<span data-ttu-id="1a99e-184">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="1a99e-184">**glEdgeFlag**</span></span>](gledgeflag-functions.md)

    <span data-ttu-id="1a99e-185">Vous pouvez également utiliser [**glCallList**](glcalllist.md) ou [**glCallLists**](glcalllists.md) pour exécuter des listes d’affichage qui incluent uniquement les fonctions précédentes.</span><span class="sxs-lookup"><span data-stu-id="1a99e-185">You can also use [**glCallList**](glcalllist.md) or [**glCallLists**](glcalllists.md) to execute display lists that include only the preceding functions.</span></span> <span data-ttu-id="1a99e-186">Si une autre fonction OpenGL est appelée entre **glBegin** et [**Glend**](glend.md), l’indicateur d’erreur est défini et la fonction est ignorée.</span><span class="sxs-lookup"><span data-stu-id="1a99e-186">If any other OpenGL function is called between **glBegin** and [**glend**](glend.md), the error flag is set and the function is ignored.</span></span>

-   <span data-ttu-id="1a99e-187">Quelle que soit la valeur choisie pour *mode* dans **glBegin**, il n’y a aucune limite au nombre de vertex que vous pouvez définir entre **glBegin** et [**Glend**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="1a99e-187">Regardless of the value chosen for *mode* in **glBegin**, there is no limit to the number of vertices you can define between **glBegin** and [**glend**](glend.md).</span></span> <span data-ttu-id="1a99e-188">Les lignes, triangles, quadrilatères et polygones qui ne sont pas complets spécifiés ne sont pas dessinés.</span><span class="sxs-lookup"><span data-stu-id="1a99e-188">Lines, triangles, quadrilaterals, and polygons that are incompletely specified are not drawn.</span></span> <span data-ttu-id="1a99e-189">Les résultats de spécifications sont incomplets lorsqu’un nombre trop faible de vertex est fourni pour spécifier une seule primitive ou lorsqu’un multiple de vertex incorrect est spécifié.</span><span class="sxs-lookup"><span data-stu-id="1a99e-189">Incomplete specification results when either too few vertices are provided to specify even a single primitive or when an incorrect multiple of vertices is specified.</span></span> <span data-ttu-id="1a99e-190">La primitive incomplète est ignorée ; les primitives complètes sont dessinées.</span><span class="sxs-lookup"><span data-stu-id="1a99e-190">The incomplete primitive is ignored; the complete primitives are drawn.</span></span>
-   <span data-ttu-id="1a99e-191">La spécification minimale des vertex pour chaque primitive est la suivante :</span><span class="sxs-lookup"><span data-stu-id="1a99e-191">The minimum specification of vertices for each primitive is:</span></span> 

    | <span data-ttu-id="1a99e-192">Nombre minimal de vertex</span><span class="sxs-lookup"><span data-stu-id="1a99e-192">Minimum number of vertices</span></span> | <span data-ttu-id="1a99e-193">Type de primitive</span><span class="sxs-lookup"><span data-stu-id="1a99e-193">Type of primitive</span></span> |
    |----------------------------|-------------------|
    | <span data-ttu-id="1a99e-194">1</span><span class="sxs-lookup"><span data-stu-id="1a99e-194">1</span></span>                          | <span data-ttu-id="1a99e-195">point</span><span class="sxs-lookup"><span data-stu-id="1a99e-195">point</span></span>             |
    | <span data-ttu-id="1a99e-196">2</span><span class="sxs-lookup"><span data-stu-id="1a99e-196">2</span></span>                          | <span data-ttu-id="1a99e-197">line</span><span class="sxs-lookup"><span data-stu-id="1a99e-197">line</span></span>              |
    | <span data-ttu-id="1a99e-198">3</span><span class="sxs-lookup"><span data-stu-id="1a99e-198">3</span></span>                          | <span data-ttu-id="1a99e-199">triangle</span><span class="sxs-lookup"><span data-stu-id="1a99e-199">triangle</span></span>          |
    | <span data-ttu-id="1a99e-200">4</span><span class="sxs-lookup"><span data-stu-id="1a99e-200">4</span></span>                          | <span data-ttu-id="1a99e-201">quadrangulaires</span><span class="sxs-lookup"><span data-stu-id="1a99e-201">quadrilateral</span></span>     |
    | <span data-ttu-id="1a99e-202">3</span><span class="sxs-lookup"><span data-stu-id="1a99e-202">3</span></span>                          | <span data-ttu-id="1a99e-203">polygon</span><span class="sxs-lookup"><span data-stu-id="1a99e-203">polygon</span></span>           |

    

     

-   <span data-ttu-id="1a99e-204">Les modes qui requièrent un certain nombre de vertex sont les lignes de GL \_ (2), les \_ triangles GL (3), \_ les quads GL (4) et le GL \_ Quad \_ Strip (2).</span><span class="sxs-lookup"><span data-stu-id="1a99e-204">Modes that require a certain multiple of vertices are GL\_LINES (2), GL\_TRIANGLES (3), GL\_QUADS (4), and GL\_QUAD\_STRIP (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a99e-205">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a99e-205">Requirements</span></span>



| <span data-ttu-id="1a99e-206">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a99e-206">Requirement</span></span> | <span data-ttu-id="1a99e-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a99e-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a99e-208">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a99e-208">Minimum supported client</span></span><br/> | <span data-ttu-id="1a99e-209">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a99e-209">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1a99e-210">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a99e-210">Minimum supported server</span></span><br/> | <span data-ttu-id="1a99e-211">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a99e-211">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1a99e-212">En-tête</span><span class="sxs-lookup"><span data-stu-id="1a99e-212">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a99e-213"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a99e-213"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1a99e-214">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1a99e-214">Library</span></span><br/>                  | <dl> <span data-ttu-id="1a99e-215"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a99e-215"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1a99e-216">DLL</span><span class="sxs-lookup"><span data-stu-id="1a99e-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a99e-217"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a99e-217"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a99e-218">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a99e-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a99e-219">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="1a99e-219">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="1a99e-220">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="1a99e-220">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="1a99e-221">**glColor**</span><span class="sxs-lookup"><span data-stu-id="1a99e-221">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="1a99e-222">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="1a99e-222">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="1a99e-223">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="1a99e-223">**glEnd**</span></span>](/windows/desktop/OpenGL/glend)
</dt> <dt>

[<span data-ttu-id="1a99e-224">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="1a99e-224">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="1a99e-225">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="1a99e-225">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="1a99e-226">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="1a99e-226">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="1a99e-227">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="1a99e-227">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="1a99e-228">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="1a99e-228">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="1a99e-229">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="1a99e-229">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="1a99e-230">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="1a99e-230">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

