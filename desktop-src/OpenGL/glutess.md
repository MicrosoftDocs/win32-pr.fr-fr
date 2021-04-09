---
title: gluTessCallback, fonction (Glu. h)
description: La fonction gluTessCallback définit un rappel pour un objet pavage.
ms.assetid: a9709919-d34c-42c4-82b8-6a503f2b39b0
keywords:
- gluTessCallback fonction OpenGL
topic_type:
- apiref
api_name:
- gluTessCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17cdba8b9dd9a3e762a93923a3c353fbc9578377
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942736"
---
# <a name="glutesscallback-function"></a><span data-ttu-id="d067e-104">gluTessCallback fonction)</span><span class="sxs-lookup"><span data-stu-id="d067e-104">gluTessCallback function</span></span>

<span data-ttu-id="d067e-105">La fonction **gluTessCallback** définit un rappel pour un objet pavage.</span><span class="sxs-lookup"><span data-stu-id="d067e-105">The **gluTessCallback** function defines a callback for a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d067e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d067e-106">Syntax</span></span>


```C++
void WINAPI gluTessCallback(
   GLUtesselator *tess,
   GLenum        which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a><span data-ttu-id="d067e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d067e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d067e-108">*tess*</span><span class="sxs-lookup"><span data-stu-id="d067e-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="d067e-109">Objet de pavage (créé avec [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="d067e-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="d067e-110">*et*</span><span class="sxs-lookup"><span data-stu-id="d067e-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="d067e-111">Rappel en cours de définition.</span><span class="sxs-lookup"><span data-stu-id="d067e-111">The callback being defined.</span></span> <span data-ttu-id="d067e-112">Les valeurs suivantes sont valides : GLU \_ Tess \_ Begin, Glu \_ Tess \_ Begin \_ Data, GLU \_ Tess \_ Edge \_ indicateur, Glu Tess \_ \_ Edge \_ Flag \_ Data, Glu \_ Tess \_ vertex, GLU \_ Tess \_ Vertex Data, Glu Tess end, Glu Tess \_ \_ \_ \_ \_ End \_ Data, Glu \_ Tess \_ combine, Glu \_ Tess \_ combine Data, Glu Tess \_ \_ \_ Error et Glu \_ Tess \_ Error \_ Data.</span><span class="sxs-lookup"><span data-stu-id="d067e-112">The following values are valid: GLU\_TESS\_BEGIN, GLU\_TESS\_BEGIN\_DATA, GLU\_TESS\_EDGE\_FLAG, GLU\_TESS\_EDGE\_FLAG\_DATA, GLU\_TESS\_VERTEX, GLU\_TESS\_VERTEX\_DATA, GLU\_TESS\_END, GLU\_TESS\_END\_DATA, GLU\_TESS\_COMBINE, GLU\_TESS\_COMBINE\_DATA, GLU\_TESS\_ERROR, and GLU\_TESS\_ERROR\_DATA.</span></span>

<span data-ttu-id="d067e-113">Pour plus d’informations sur ces rappels, consultez la section Notes suivante.</span><span class="sxs-lookup"><span data-stu-id="d067e-113">For more information on these callbacks, see the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="d067e-114">*FN*</span><span class="sxs-lookup"><span data-stu-id="d067e-114">*fn*</span></span> 
</dt> <dd>

<span data-ttu-id="d067e-115">Fonction à appeler.</span><span class="sxs-lookup"><span data-stu-id="d067e-115">The function to be called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d067e-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d067e-116">Return value</span></span>

<span data-ttu-id="d067e-117">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d067e-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d067e-118">Notes</span><span class="sxs-lookup"><span data-stu-id="d067e-118">Remarks</span></span>

<span data-ttu-id="d067e-119">Utilisez **gluTessCallback** pour spécifier un rappel à utiliser par un objet de pavage.</span><span class="sxs-lookup"><span data-stu-id="d067e-119">Use **gluTessCallback** to specify a callback to be used by a tessellation object.</span></span> <span data-ttu-id="d067e-120">Si le rappel spécifié est déjà défini, il est remplacé.</span><span class="sxs-lookup"><span data-stu-id="d067e-120">If the specified callback is already defined, then it is replaced.</span></span> <span data-ttu-id="d067e-121">Si *FN* a la **valeur null**, le rappel existant devient non défini.</span><span class="sxs-lookup"><span data-stu-id="d067e-121">If *fn* is **NULL**, then the existing callback becomes undefined.</span></span>

<span data-ttu-id="d067e-122">L’objet pavage utilise ces rappels pour décrire comment un polygone que vous spécifiez est divisé en triangles.</span><span class="sxs-lookup"><span data-stu-id="d067e-122">The tessellation object uses these callbacks to describe how a polygon that you specify is broken into triangles.</span></span>

<span data-ttu-id="d067e-123">Il existe deux versions de chaque rappel, une avec les données Polygon que vous pouvez définir et une autre sans.</span><span class="sxs-lookup"><span data-stu-id="d067e-123">There are two versions of each callback, one with polygon data that you can define and one without.</span></span> <span data-ttu-id="d067e-124">Si les deux versions d’un rappel particulier sont spécifiées, le rappel avec les données Polygon que vous spécifiez sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="d067e-124">If both versions of a particular callback are specified, the callback with the polygon data you specify will be used.</span></span> <span data-ttu-id="d067e-125">Le paramètre de *\_ données Polygon* de [**gluTessBeginPolygon**](glutessbeginpolygon.md) est une copie du pointeur qui a été spécifié lors de l’appel de **gluTessBeginPolygon** .</span><span class="sxs-lookup"><span data-stu-id="d067e-125">The *polygon\_data* parameter of [**gluTessBeginPolygon**](glutessbeginpolygon.md) is a copy of the pointer that was specified when **gluTessBeginPolygon** was called.</span></span>

<span data-ttu-id="d067e-126">Les rappels valides sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="d067e-126">The following are valid callbacks:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d067e-127">Rappel</span><span class="sxs-lookup"><span data-stu-id="d067e-127">Callback</span></span></th>
<th><span data-ttu-id="d067e-128">Description</span><span class="sxs-lookup"><span data-stu-id="d067e-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d067e-129">GLU_TESS_BEGIN</span><span class="sxs-lookup"><span data-stu-id="d067e-129">GLU_TESS_BEGIN</span></span></td>
<td><span data-ttu-id="d067e-130">Le rappel GLU_TESS_BEGIN est appelé comme <a href="glbegin.md"><strong>glBegin</strong></a> pour indiquer le début d’une primitive (triangle).</span><span class="sxs-lookup"><span data-stu-id="d067e-130">The GLU_TESS_BEGIN callback is invoked like <a href="glbegin.md"><strong>glBegin</strong></a> to indicate the start of a (triangle) primitive.</span></span> <span data-ttu-id="d067e-131">La fonction accepte un seul argument de type <strong>GLenum</strong>.</span><span class="sxs-lookup"><span data-stu-id="d067e-131">The function takes a single argument of type <strong>GLenum</strong>.</span></span> <span data-ttu-id="d067e-132">Si vous affectez à la propriété GLU_TESS_BOUNDARY_ONLY la valeur GL_FALSE, l’argument est défini sur GL_TRIANGLE_FAN, GL_TRIANGLE_STRIP ou GL_TRIANGLES.</span><span class="sxs-lookup"><span data-stu-id="d067e-132">If you set the GLU_TESS_BOUNDARY_ONLY property to GL_FALSE, the argument is set to either GL_TRIANGLE_FAN, GL_TRIANGLE_STRIP, or GL_TRIANGLES.</span></span> <span data-ttu-id="d067e-133">Si vous affectez à la propriété GLU_TESS_BOUNDARY_ONLY la valeur GL_TRUE, l’argument est défini sur GL_LINE_LOOP.</span><span class="sxs-lookup"><span data-stu-id="d067e-133">If you set the GLU_TESS_BOUNDARY_ONLY property to GL_TRUE, the argument is set to GL_LINE_LOOP.</span></span> <span data-ttu-id="d067e-134">Le prototype de fonction pour ce rappel est le suivant : <strong>void</strong> <strong>Begin</strong> ( <em>type</em><strong>GLenum</strong> );</span><span class="sxs-lookup"><span data-stu-id="d067e-134">The function prototype for this callback is as follows: <strong>void</strong> <strong>begin</strong> (<strong>GLenum</strong> <em>type</em>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d067e-135">GLU_TESS_BEGIN_DATA</span><span class="sxs-lookup"><span data-stu-id="d067e-135">GLU_TESS_BEGIN_DATA</span></span></td>
<td><span data-ttu-id="d067e-136">GLU_TESS_BEGIN_DATA est le même que le rappel GLU_TESS_BEGIN, sauf qu’il accepte un argument de pointeur supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="d067e-136">GLU_TESS_BEGIN_DATA is the same as the GLU_TESS_BEGIN callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="d067e-137">Ce pointeur est identique au pointeur opaque fourni lorsque vous appelez <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d067e-137">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="d067e-138">Le prototype de fonction pour ce rappel est : <strong>void</strong> <strong>beginData</strong> (<strong>GLenum</strong> <em>type</em>, <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="d067e-138">The function prototype for this callback is: <strong>void</strong> <strong>beginData</strong> (<strong>GLenum</strong> <em>type</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d067e-139">GLU_TESS_EDGE_FLAG</span><span class="sxs-lookup"><span data-stu-id="d067e-139">GLU_TESS_EDGE_FLAG</span></span></td>
<td><span data-ttu-id="d067e-140">Le rappel GLU_TESS_EDGE_FLAG est semblable à <a href="gledgeflag-functions.md"><strong>glEdgeFlag</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d067e-140">The GLU_TESS_EDGE_FLAG callback is similar to <a href="gledgeflag-functions.md"><strong>glEdgeFlag</strong></a>.</span></span> <span data-ttu-id="d067e-141">La fonction accepte un seul indicateur booléen qui indique les bords situés sur la limite du polygone.</span><span class="sxs-lookup"><span data-stu-id="d067e-141">The function takes a single Boolean flag that indicates which edges lie on the polygon boundary.</span></span> <span data-ttu-id="d067e-142">Si l’indicateur est GL_TRUE, chaque vertex qui suit commence un bord qui se trouve sur la limite du polygone ; autrement dit, une arête qui sépare une région intérieure d’une région extérieure.</span><span class="sxs-lookup"><span data-stu-id="d067e-142">If the flag is GL_TRUE, then each vertex that follows begins an edge that lies on the polygon boundary; that is, an edge which separates an interior region from an exterior one.</span></span> <span data-ttu-id="d067e-143">Si l’indicateur est GL_FALSE, chaque sommet qui suit commence un bord qui se trouve dans l’intérieur du polygone.</span><span class="sxs-lookup"><span data-stu-id="d067e-143">If the flag is GL_FALSE, then each vertex that follows begins an edge that lies in the polygon interior.</span></span> <span data-ttu-id="d067e-144">Le rappel GLU_TESS_EDGE_FLAG (s’il est défini) est appelé avant le premier rappel de vertex.</span><span class="sxs-lookup"><span data-stu-id="d067e-144">The GLU_TESS_EDGE_FLAG callback (if defined) is invoked before the first vertex callback is made.</span></span> <span data-ttu-id="d067e-145">Étant donné que les ventilateurs et les facettes de triangle ne prennent pas en charge les indicateurs de périphérie, le rappel de début n’est pas appelé avec GL_TRIANGLE_FAN ou GL_TRIANGLE_STRIP si un rappel de l’indicateur Edge est fourni.</span><span class="sxs-lookup"><span data-stu-id="d067e-145">Because triangle fans and triangle strips do not support edge flags, the begin callback is not called with GL_TRIANGLE_FAN or GL_TRIANGLE_STRIP if an edge flag callback is provided.</span></span> <span data-ttu-id="d067e-146">Au lieu de cela, les ventilateurs et les bandes sont convertis en triangles indépendants.</span><span class="sxs-lookup"><span data-stu-id="d067e-146">Instead, the fans and strips are converted to independent triangles.</span></span> <span data-ttu-id="d067e-147">Le prototype de fonction pour ce rappel est le suivant :</span><span class="sxs-lookup"><span data-stu-id="d067e-147">The function prototype for this callback is:</span></span><br/> <span data-ttu-id="d067e-148"><strong>void</strong> <strong>edgeFlag</strong> (<strong></strong> <em>indicateur</em>GLboolean);</span><span class="sxs-lookup"><span data-stu-id="d067e-148"><strong>void</strong> <strong>edgeFlag</strong> (<strong>GLboolean</strong> <em>flag</em>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d067e-149">GLU_TESS_EDGE_FLAG_DATA</span><span class="sxs-lookup"><span data-stu-id="d067e-149">GLU_TESS_EDGE_FLAG_DATA</span></span></td>
<td><span data-ttu-id="d067e-150">Le rappel GLU_TESS_EDGE_FLAG_DATA est le même que le rappel GLU_TESS_EDGE_FLAG, sauf qu’il accepte un argument de pointeur supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="d067e-150">The GLU_TESS_EDGE_FLAG_DATA callback is the same as the GLU_TESS_EDGE_FLAG callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="d067e-151">Ce pointeur est identique au pointeur opaque fourni lorsque vous appelez <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d067e-151">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="d067e-152">Le prototype de fonction pour ce rappel est : <strong>void</strong> <strong>edgeFlagData</strong> (<strong>GLboolean</strong> <em>Flag</em>, <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="d067e-152">The function prototype for this callback is: <strong>void</strong> <strong>edgeFlagData</strong> (<strong>GLboolean</strong> <em>flag</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d067e-153">GLU_TESS_VERTEX</span><span class="sxs-lookup"><span data-stu-id="d067e-153">GLU_TESS_VERTEX</span></span></td>
<td><span data-ttu-id="d067e-154">Le rappel GLU_TESS_VERTEX est appelé entre les rappels Begin et end.</span><span class="sxs-lookup"><span data-stu-id="d067e-154">The GLU_TESS_VERTEX callback is invoked between the begin and end callbacks.</span></span> <span data-ttu-id="d067e-155">Elle est similaire à glVertex et définit les sommets des triangles créés par le processus de pavage.</span><span class="sxs-lookup"><span data-stu-id="d067e-155">It is similar to glVertex , and it defines the vertexes of the triangles created by the tessellation process.</span></span> <span data-ttu-id="d067e-156">La fonction prend un pointeur comme seul argument.</span><span class="sxs-lookup"><span data-stu-id="d067e-156">The function takes a pointer as its only argument.</span></span> <span data-ttu-id="d067e-157">Ce pointeur est identique au pointeur opaque que vous avez fourni lorsque vous avez défini le vertex (voir <a href="glutessvertex.md"><strong>gluTessVertex</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="d067e-157">This pointer is identical to the opaque pointer that you provided when you defined the vertex (see <a href="glutessvertex.md"><strong>gluTessVertex</strong></a>).</span></span> <span data-ttu-id="d067e-158">Le prototype de fonction pour ce rappel est : <strong>void</strong> <strong>vertex</strong> (<strong>void</strong> \* <em>vertex_data</em>);</span><span class="sxs-lookup"><span data-stu-id="d067e-158">The function prototype for this callback is: <strong>void</strong> <strong>vertex</strong> (<strong>void</strong> \* <em>vertex_data</em>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d067e-159">GLU_TESS_VERTEX_DATA</span><span class="sxs-lookup"><span data-stu-id="d067e-159">GLU_TESS_VERTEX_DATA</span></span></td>
<td><span data-ttu-id="d067e-160">Le GLU_TESS_VERTEX_DATA est le même que le rappel GLU_TESS_VERTEX, sauf qu’il accepte un argument de pointeur supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="d067e-160">The GLU_TESS_VERTEX_DATA is the same as the GLU_TESS_VERTEX callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="d067e-161">Ce pointeur est identique au pointeur opaque fourni lorsque vous appelez <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d067e-161">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="d067e-162">Le prototype de fonction pour ce rappel est : <strong>void</strong>  <strong>vertexData</strong> (void \* <em>vertex_data</em>, <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="d067e-162">The function prototype for this callback is: <strong>void</strong>  <strong>vertexData</strong> (void \* <em>vertex_data</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d067e-163">GLU_TESS_END</span><span class="sxs-lookup"><span data-stu-id="d067e-163">GLU_TESS_END</span></span></td>
<td><span data-ttu-id="d067e-164">Le rappel GLU_TESS_END a le même objectif que <a href="glend.md"><strong>glEnd</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d067e-164">The GLU_TESS_END callback serves the same purpose as <a href="glend.md"><strong>glEnd</strong></a>.</span></span> <span data-ttu-id="d067e-165">Elle indique la fin d’une primitive et n’accepte aucun argument.</span><span class="sxs-lookup"><span data-stu-id="d067e-165">It indicates the end of a primitive, and it takes no arguments.</span></span> <span data-ttu-id="d067e-166">Le prototype de fonction pour ce rappel est : <strong>void</strong> <strong>end</strong> (<strong>void</strong>);</span><span class="sxs-lookup"><span data-stu-id="d067e-166">The function prototype for this callback is: <strong>void</strong> <strong>end</strong> (<strong>void</strong>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d067e-167">GLU_TESS_END_DATA</span><span class="sxs-lookup"><span data-stu-id="d067e-167">GLU_TESS_END_DATA</span></span></td>
<td><span data-ttu-id="d067e-168">Le rappel GLU_TESS_END_DATA est le même que le rappel GLU_TESS_END, sauf qu’il accepte un argument de pointeur supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="d067e-168">The GLU_TESS_END_DATA callback is the same as the GLU_TESS_END callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="d067e-169">Ce pointeur est identique au pointeur opaque fourni lorsque vous appelez <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d067e-169">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="d067e-170">Le prototype de fonction pour ce rappel est : <strong>void</strong> <strong>endData</strong> (<strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="d067e-170">The function prototype for this callback is: <strong>void</strong> <strong>endData</strong> (<strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d067e-171">GLU_TESS_COMBINE</span><span class="sxs-lookup"><span data-stu-id="d067e-171">GLU_TESS_COMBINE</span></span></td>
<td><span data-ttu-id="d067e-172">Appelez le rappel GLU_TESS_COMBINE pour créer un nouveau vertex lorsque le pavage détecte une intersection ou pour fusionner des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="d067e-172">Call the GLU_TESS_COMBINE callback to create a new vertex when the tessellation detects an intersection, or to merge features.</span></span> <span data-ttu-id="d067e-173">La fonction accepte quatre arguments : un tableau de trois éléments, chacun de type Gldouble.</span><span class="sxs-lookup"><span data-stu-id="d067e-173">The function takes four arguments: An array of three elements, each of type Gldouble.</span></span><br/> <span data-ttu-id="d067e-174">Tableau de quatre pointeurs.</span><span class="sxs-lookup"><span data-stu-id="d067e-174">An array of four pointers.</span></span><br/> <span data-ttu-id="d067e-175">Tableau de quatre éléments, chacun de type GLfloat.</span><span class="sxs-lookup"><span data-stu-id="d067e-175">An array of four elements, each of type GLfloat.</span></span><br/> <span data-ttu-id="d067e-176">Pointeur vers un pointeur.</span><span class="sxs-lookup"><span data-stu-id="d067e-176">A pointer to a pointer.</span></span><br/> <span data-ttu-id="d067e-177">Le prototype de fonction pour ce rappel est le suivant :</span><span class="sxs-lookup"><span data-stu-id="d067e-177">The function prototype for this callback is:</span></span> <br/> <span data-ttu-id="d067e-178"><strong>void</strong> <strong>combine</strong>(<strong>GLdouble</strong> <em>CoOrds</em>[3], <strong>void</strong> \* <em>vertex_data</em>[4], <strong>GLfloat</strong> <em>Weight</em>[4], <strong>void</strong>out  \*\* <em>Data</em>);</span><span class="sxs-lookup"><span data-stu-id="d067e-178"><strong>void</strong> <strong>combine</strong>(<strong>GLdouble</strong> <em>coords</em>[3], <strong>void</strong> \* <em>vertex_data</em>[4], <strong>GLfloat</strong> <em>weight</em>[4], <strong>void</strong> \*\*<em>outData</em>);</span></span><br/> <span data-ttu-id="d067e-179">Le vertex est défini comme une combinaison linéaire de jusqu’à quatre sommets existants, stockés dans vertex_data.</span><span class="sxs-lookup"><span data-stu-id="d067e-179">The vertex is defined as a linear combination of up to four existing vertexes, stored in vertex_data.</span></span> <span data-ttu-id="d067e-180">Les coefficients de la combinaison linéaire sont fournis par poids ; ces pondérations sont toujours additionnées à 1,0.</span><span class="sxs-lookup"><span data-stu-id="d067e-180">The coefficients of the linear combination are given by weight; these weights always sum to 1.0.</span></span> <span data-ttu-id="d067e-181">Tous les pointeurs de vertex sont valides même si certains des poids sont nuls.</span><span class="sxs-lookup"><span data-stu-id="d067e-181">All vertex pointers are valid even when some of the weights are zero.</span></span> <span data-ttu-id="d067e-182">Le paramètre coords indique l’emplacement du nouveau vertex.</span><span class="sxs-lookup"><span data-stu-id="d067e-182">The coords parameter gives the location of the new vertex.</span></span><br/> <span data-ttu-id="d067e-183">Allouez un autre vertex, interpolez les paramètres à l’aide de la vertex_data et du poids, puis retournez le nouveau pointeur de vertex dans les données de données.</span><span class="sxs-lookup"><span data-stu-id="d067e-183">Allocate another vertex, interpolate parameters using vertex_data and weight, and return the new vertex pointer in outData.</span></span> <span data-ttu-id="d067e-184">Ce handle est fourni lors du rendu des rappels.</span><span class="sxs-lookup"><span data-stu-id="d067e-184">This handle is supplied during rendering callbacks.</span></span> <span data-ttu-id="d067e-185">Libérez de la mémoire après avoir appelé <a href="glutessendpolygon.md"><strong>gluTessEndPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d067e-185">Free the memory sometime after calling <a href="glutessendpolygon.md"><strong>gluTessEndPolygon</strong></a>.</span></span><br/> <span data-ttu-id="d067e-186">Par exemple, si le polygone se trouve dans un plan arbitraire dans l’espace tridimensionnel et que vous associez une couleur à chaque vertex, le rappel GLU_TESS_COMBINE peut se présenter comme suit :</span><span class="sxs-lookup"><span data-stu-id="d067e-186">For example, if the polygon lies in an arbitrary plane in three-dimensional space, and you associate a color with each vertex, the GLU_TESS_COMBINE callback might look like the following:</span></span><br/>
<pre data-space="preserve"><code>void myCombine( GLdouble coords[3], VERTEX *d[4], 
                GLfloat w[4], VERTEX **dataOut ) 
{ 
    VERTEX *newVertex = new_vertex(); 
    newVertex->x = coords[0]; 
    newVertex->y = coords[1]; 
    newVertex->z = coords[2]; 
    newVertex->r = w[0]*d[0]->r + w[1]*d[1]->r + w[2]*d[2]->r + 
                   w[3]*d[3]->r; 
    newVertex->g = w[0]*d[0]->g + w[1]*d[1]->g + w[2]*d[2]->g + 
                   w[3]*d[3]->g; 
    newVertex->b = w[0]*d[0]->b + w[1]*d[1]->b + w[2]*d[2]->b + 
                   w[3]*d[3]->b; 
    newVertex->a = w[0]*d[0]->a + w[1]*d[1]->a + w[2]*d[2]->a + 
                   w[3]*d[3]->a; 
    *dataOut = newVertex; 
}</code></pre>
<span data-ttu-id="d067e-187">Lorsque le pavage détecte une intersection, le rappel GLU_TESS_COMBINE ou GLU_TESS_COMBINE_DATA (voir ci-dessous) doit être défini et doit écrire un pointeur non<strong>null</strong> dans dataOut.</span><span class="sxs-lookup"><span data-stu-id="d067e-187">When the tessellation detects an intersection, the GLU_TESS_COMBINE or GLU_TESS_COMBINE_DATA callback (see below) must be defined, and must write a non-<strong>NULL</strong> pointer into dataOut.</span></span> <span data-ttu-id="d067e-188">Dans le cas contraire, l’erreur GLU_TESS_NEED_COMBINE_CALLBACK se produit et aucune sortie n’est générée.</span><span class="sxs-lookup"><span data-stu-id="d067e-188">Otherwise the GLU_TESS_NEED_COMBINE_CALLBACK error occurs, and no output is generated.</span></span> <span data-ttu-id="d067e-189">(Il s’agit de la seule erreur qui peut se produire pendant le pavage et le rendu.)</span><span class="sxs-lookup"><span data-stu-id="d067e-189">(This is the only error that can occur during tessellation and rendering.)</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d067e-190">GLU_TESS_COMBINE_DATA</span><span class="sxs-lookup"><span data-stu-id="d067e-190">GLU_TESS_COMBINE_DATA</span></span></td>
<td><span data-ttu-id="d067e-191">Le rappel GLU_TESS_COMBINE_DATA est le même que le rappel GLU_TESS_COMBINE, sauf qu’il accepte un argument de pointeur supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="d067e-191">The GLU_TESS_COMBINE_DATA callback is the same as the GLU_TESS_COMBINE callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="d067e-192">Ce pointeur est identique au pointeur opaque fourni lorsque vous appelez <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d067e-192">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="d067e-193">Le prototype de fonction pour ce rappel est : <strong>void</strong> <strong>combineData</strong> (<strong>GLdouble</strong> <em>CoOrds</em>[3] <strong>, void</strong> \*<em>vertex_data</em>[4], <strong>GLfloat</strong> <em>Weight</em>[4], <strong>void</strong>  \*\* <em>UNdata</em>, <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="d067e-193">The function prototype for this callback is: <strong>void</strong> <strong>combineData</strong> (<strong>GLdouble</strong> <em>coords</em>[3], <strong>void</strong> \*<em>vertex_data</em>[4], <strong>GLfloat</strong> <em>weight</em>[4], <strong>void</strong> \*\*<em>outData</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d067e-194">GLU_TESS_ERROR</span><span class="sxs-lookup"><span data-stu-id="d067e-194">GLU_TESS_ERROR</span></span></td>
<td><span data-ttu-id="d067e-195">Le rappel GLU_TESS_ERROR est appelé lorsqu’une erreur est rencontrée.</span><span class="sxs-lookup"><span data-stu-id="d067e-195">The GLU_TESS_ERROR callback is called when an error is encountered.</span></span> <span data-ttu-id="d067e-196">L’argument est de type <strong>GLenum</strong>; elle indique l’erreur spécifique qui s’est produite et est définie sur l’une des valeurs suivantes : GLU_TESS_MISSING_BEGIN_POLYGON</span><span class="sxs-lookup"><span data-stu-id="d067e-196">The one argument is of type <strong>GLenum</strong>; it indicates the specific error that occurred and is set to one of the following: GLU_TESS_MISSING_BEGIN_POLYGON</span></span><br/> <span data-ttu-id="d067e-197">GLU_TESS_MISSING_END_POLYGON</span><span class="sxs-lookup"><span data-stu-id="d067e-197">GLU_TESS_MISSING_END_POLYGON</span></span><br/> <span data-ttu-id="d067e-198">GLU_TESS_MISSING_BEGIN_CONTOUR</span><span class="sxs-lookup"><span data-stu-id="d067e-198">GLU_TESS_MISSING_BEGIN_CONTOUR</span></span><br/> <span data-ttu-id="d067e-199">GLU_TESS_MISSING_END_CONTOUR</span><span class="sxs-lookup"><span data-stu-id="d067e-199">GLU_TESS_MISSING_END_CONTOUR</span></span><br/> <span data-ttu-id="d067e-200">GLU_TESS_COORD_TOO_LARGE</span><span class="sxs-lookup"><span data-stu-id="d067e-200">GLU_TESS_COORD_TOO_LARGE</span></span><br/> <span data-ttu-id="d067e-201">GLU_TESS_NEED_COMBINE_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="d067e-201">GLU_TESS_NEED_COMBINE_CALLBACK</span></span><br/> <span data-ttu-id="d067e-202">Appelez gluErrorString pour récupérer les chaînes de caractères décrivant ces erreurs.</span><span class="sxs-lookup"><span data-stu-id="d067e-202">Call gluErrorString to retrieve character strings describing these errors.</span></span> <span data-ttu-id="d067e-203">Le prototype de fonction pour ce rappel est le suivant :</span><span class="sxs-lookup"><span data-stu-id="d067e-203">The function prototype for this callback is as follows:</span></span><br/> <span data-ttu-id="d067e-204"><strong>void</strong> <strong>Error</strong> (<strong>GLenum</strong> <em>errno</em>);</span><span class="sxs-lookup"><span data-stu-id="d067e-204"><strong>void</strong> <strong>error</strong> (<strong>GLenum</strong> <em>errno</em>);</span></span><br/> <span data-ttu-id="d067e-205">La bibliothèque GLU récupère les quatre premières erreurs en insérant l’appel ou les appels manquants.</span><span class="sxs-lookup"><span data-stu-id="d067e-205">The GLU library recovers from the first four errors by inserting the missing call or calls.</span></span> <span data-ttu-id="d067e-206">GLU_TESS_COORD_TOO_LARGE indique que certaines coordonnées de vertex dépassent la constante prédéfinie GLU_TESS_MAX_COORD en valeur absolue et que la valeur a été ancrée.</span><span class="sxs-lookup"><span data-stu-id="d067e-206">GLU_TESS_COORD_TOO_LARGE indicates that some vertex coordinate exceeded the predefined constant GLU_TESS_MAX_COORD in absolute value, and that the value has been clamped.</span></span> <span data-ttu-id="d067e-207">(Les valeurs de coordonnée doivent être suffisamment petites pour que deux puissent être multipliées sans dépassement de capacité.) GLU_TESS_NEED_COMBINE_CALLBACK indique que la pavage a détecté une intersection entre deux bords dans les données d’entrée, et que le rappel GLU_TESS_COMBINE ou GLU_TESS_COMBINE_DATA n’a pas été fourni.</span><span class="sxs-lookup"><span data-stu-id="d067e-207">(Coordinate values must be small enough that two can be multiplied together without overflow.) GLU_TESS_NEED_COMBINE_CALLBACK indicates that the tessellation detected an intersection between two edges in the input data, and the GLU_TESS_COMBINE or GLU_TESS_COMBINE_DATA callback was not provided.</span></span> <span data-ttu-id="d067e-208">Aucune sortie ne sera générée.</span><span class="sxs-lookup"><span data-stu-id="d067e-208">No output will be generated.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d067e-209">GLU_TESS_ERROR_DATA</span><span class="sxs-lookup"><span data-stu-id="d067e-209">GLU_TESS_ERROR_DATA</span></span></td>
<td><span data-ttu-id="d067e-210">Le rappel GLU_TESS_ERROR_DATA est le même que le rappel GLU_TESS_ERROR, sauf qu’il accepte un argument de pointeur supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="d067e-210">The GLU_TESS_ERROR_DATA callback is the same as the GLU_TESS_ERROR callback, except that it takes an additional pointer argument.</span></span> <span data-ttu-id="d067e-211">Ce pointeur est identique au pointeur opaque fourni lorsque vous appelez <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d067e-211">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="d067e-212">Le prototype de fonction pour ce rappel est : <strong>void</strong> <strong>ErrorData</strong> (<strong>GLenum</strong> <em>errno</em>, <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="d067e-212">The function prototype for this callback is: <strong>void</strong> <strong>errorData</strong> (<strong>GLenum</strong> <em>errno</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="d067e-213">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d067e-213">Requirements</span></span>



| <span data-ttu-id="d067e-214">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d067e-214">Requirement</span></span> | <span data-ttu-id="d067e-215">Valeur</span><span class="sxs-lookup"><span data-stu-id="d067e-215">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d067e-216">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d067e-216">Minimum supported client</span></span><br/> | <span data-ttu-id="d067e-217">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d067e-217">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d067e-218">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d067e-218">Minimum supported server</span></span><br/> | <span data-ttu-id="d067e-219">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d067e-219">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d067e-220">En-tête</span><span class="sxs-lookup"><span data-stu-id="d067e-220">Header</span></span><br/>                   | <dl> <span data-ttu-id="d067e-221"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="d067e-221"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="d067e-222">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d067e-222">Library</span></span><br/>                  | <dl> <span data-ttu-id="d067e-223"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d067e-223"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d067e-224">DLL</span><span class="sxs-lookup"><span data-stu-id="d067e-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d067e-225"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d067e-225"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d067e-226">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d067e-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d067e-227">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="d067e-227">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d067e-228">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="d067e-228">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="d067e-229">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="d067e-229">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d067e-230">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="d067e-230">**glVertex**</span></span>](glvertex-functions.md)
</dt> <dt>

[<span data-ttu-id="d067e-231">**gluDeleteTess**</span><span class="sxs-lookup"><span data-stu-id="d067e-231">**gluDeleteTess**</span></span>](gludeletetess.md)
</dt> <dt>

[<span data-ttu-id="d067e-232">**gluErrorString**</span><span class="sxs-lookup"><span data-stu-id="d067e-232">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> <dt>

[<span data-ttu-id="d067e-233">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="d067e-233">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="d067e-234">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="d067e-234">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="d067e-235">**gluTessEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="d067e-235">**gluTessEndPolygon**</span></span>](glutessendpolygon.md)
</dt> <dt>

[<span data-ttu-id="d067e-236">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="d067e-236">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





