---
title: fonction glPolygonMode (GL. h)
description: La fonction glPolygonMode sélectionne un mode de pixellisation de polygone.
ms.assetid: d8781bae-e78c-40fb-9f33-c742c70ebda1
keywords:
- glPolygonMode fonction OpenGL
topic_type:
- apiref
api_name:
- glPolygonMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23d133243c1655432842a939b8da0f3a981fdffd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512211"
---
# <a name="glpolygonmode-function"></a><span data-ttu-id="56bc1-104">glPolygonMode fonction)</span><span class="sxs-lookup"><span data-stu-id="56bc1-104">glPolygonMode function</span></span>

<span data-ttu-id="56bc1-105">La fonction **glPolygonMode** sélectionne un mode de pixellisation de polygone.</span><span class="sxs-lookup"><span data-stu-id="56bc1-105">The **glPolygonMode** function selects a polygon rasterization mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="56bc1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56bc1-106">Syntax</span></span>


```C++
void WINAPI glPolygonMode(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="56bc1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56bc1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56bc1-108">*se*</span><span class="sxs-lookup"><span data-stu-id="56bc1-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="56bc1-109">Polygones auxquels ce *mode* s’applique.</span><span class="sxs-lookup"><span data-stu-id="56bc1-109">The polygons that *mode* applies to.</span></span> <span data-ttu-id="56bc1-110">Doit être \_ de premier plan pour les polygones frontaux, le GL \_ de retour pour les polygones d’arrière-plan, ou le \_ recto \_ et l’arrière GL \_ pour les polygones frontaux et dorsaux.</span><span class="sxs-lookup"><span data-stu-id="56bc1-110">Must be GL\_FRONT for front-facing polygons, GL\_BACK for back-facing polygons, or GL\_FRONT\_AND\_BACK for front- and back-facing polygons.</span></span>

</dd> <dt>

<span data-ttu-id="56bc1-111">*mode*</span><span class="sxs-lookup"><span data-stu-id="56bc1-111">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="56bc1-112">Façon dont les polygones seront pixellisés.</span><span class="sxs-lookup"><span data-stu-id="56bc1-112">The way polygons will be rasterized.</span></span> <span data-ttu-id="56bc1-113">Les modes suivants sont définis et peuvent être spécifiés en *mode*.</span><span class="sxs-lookup"><span data-stu-id="56bc1-113">The following modes are defined and can be specified in *mode*.</span></span> <span data-ttu-id="56bc1-114">La valeur par défaut est \_ remplissage GL pour les polygones avant et arrière.</span><span class="sxs-lookup"><span data-stu-id="56bc1-114">The default is GL\_FILL for both front- and back-facing polygons.</span></span>



| <span data-ttu-id="56bc1-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="56bc1-115">Value</span></span>                                                                                                                                          | <span data-ttu-id="56bc1-116">Signification</span><span class="sxs-lookup"><span data-stu-id="56bc1-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINT"></span><span id="gl_point"></span><dl> <span data-ttu-id="56bc1-117"><dt>**\_point GL**</dt></span><span class="sxs-lookup"><span data-stu-id="56bc1-117"><dt>**GL\_POINT**</dt></span></span> </dl> | <span data-ttu-id="56bc1-118">Les sommets de polygone marqués comme point de départ d’un bord de limite sont dessinés en tant que points.</span><span class="sxs-lookup"><span data-stu-id="56bc1-118">Polygon vertices that are marked as the start of a boundary edge are drawn as points.</span></span> <span data-ttu-id="56bc1-119">Les attributs de point tels \_ que \_ la taille du point GL et \_ le point de contrôle de l’état du GL \_ déterminent la pixellisation des points.</span><span class="sxs-lookup"><span data-stu-id="56bc1-119">Point attributes such as GL\_POINT\_SIZE and GL\_POINT\_SMOOTH control the rasterization of the points.</span></span> <span data-ttu-id="56bc1-120">Les attributs de pixellisation de polygone autres que le \_ mode polygone GL n' \_ ont aucun effet.</span><span class="sxs-lookup"><span data-stu-id="56bc1-120">Polygon rasterization attributes other than GL\_POLYGON\_MODE have no effect.</span></span><br/>                                                                                                                                                    |
| <span id="GL_LINE"></span><span id="gl_line"></span><dl> <span data-ttu-id="56bc1-121"><dt>**\_ligne GL**</dt></span><span class="sxs-lookup"><span data-stu-id="56bc1-121"><dt>**GL\_LINE**</dt></span></span> </dl>    | <span data-ttu-id="56bc1-122">Les bords limites du polygone sont dessinés sous forme de segments de ligne.</span><span class="sxs-lookup"><span data-stu-id="56bc1-122">Boundary edges of the polygon are drawn as line segments.</span></span> <span data-ttu-id="56bc1-123">Ils sont traités comme des segments de ligne connectés pour la ligne stippling ; le compteur et le modèle de ligne stipple ne sont pas réinitialisés entre les segments (voir [**glLineStipple**](gllinestipple.md)).</span><span class="sxs-lookup"><span data-stu-id="56bc1-123">They are treated as connected line segments for line stippling; the line stipple counter and pattern are not reset between segments (see [**glLineStipple**](gllinestipple.md)).</span></span> <span data-ttu-id="56bc1-124">Les attributs de ligne tels \_ que \_ la largeur de ligne GL et \_ \_ le contrôle de ligne GL lissent la pixellisation des lignes.</span><span class="sxs-lookup"><span data-stu-id="56bc1-124">Line attributes such as GL\_LINE\_WIDTH and GL\_LINE\_SMOOTH control the rasterization of the lines.</span></span> <span data-ttu-id="56bc1-125">Les attributs de pixellisation de polygone autres que le \_ mode polygone GL n' \_ ont aucun effet.</span><span class="sxs-lookup"><span data-stu-id="56bc1-125">Polygon rasterization attributes other than GL\_POLYGON\_MODE have no effect.</span></span><br/> |
| <span id="GL_FILL"></span><span id="gl_fill"></span><dl> <span data-ttu-id="56bc1-126"><dt>**remplissage du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="56bc1-126"><dt>**GL\_FILL**</dt></span></span> </dl>    | <span data-ttu-id="56bc1-127">L’intérieur du polygone est rempli.</span><span class="sxs-lookup"><span data-stu-id="56bc1-127">The interior of the polygon is filled.</span></span> <span data-ttu-id="56bc1-128">Les attributs Polygon tels que GL \_ Polygon \_ STIPPLE et GL \_ Polygon \_ lisse contrôlent la pixellisation du polygone.</span><span class="sxs-lookup"><span data-stu-id="56bc1-128">Polygon attributes such as GL\_POLYGON\_STIPPLE and GL\_POLYGON\_SMOOTH control the rasterization of the polygon.</span></span><br/>                                                                                                                                                                                                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56bc1-129">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="56bc1-129">Return value</span></span>

<span data-ttu-id="56bc1-130">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="56bc1-130">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="56bc1-131">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="56bc1-131">Error codes</span></span>

<span data-ttu-id="56bc1-132">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="56bc1-132">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="56bc1-133">Nom</span><span class="sxs-lookup"><span data-stu-id="56bc1-133">Name</span></span>                                                                                                  | <span data-ttu-id="56bc1-134">Signification</span><span class="sxs-lookup"><span data-stu-id="56bc1-134">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="56bc1-135"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="56bc1-135"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="56bc1-136">La *face* ou le *mode* n’était pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="56bc1-136">Either *face* or *mode* was not an accepted value.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="56bc1-137"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="56bc1-137"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="56bc1-138">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="56bc1-138">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="56bc1-139">Notes</span><span class="sxs-lookup"><span data-stu-id="56bc1-139">Remarks</span></span>

<span data-ttu-id="56bc1-140">La fonction **glPolygonMode** contrôle l’interprétation des polygones pour la pixellisation.</span><span class="sxs-lookup"><span data-stu-id="56bc1-140">The **glPolygonMode** function controls the interpretation of polygons for rasterization.</span></span> <span data-ttu-id="56bc1-141">Le paramètre *face* décrit quel *mode* Polygon s’applique à : les polygones frontaux (GL \_ frontal), les polygones d’arrière-plan (GL \_ Back) ou les deux ( \_ recto \_ et verso GL \_ ).</span><span class="sxs-lookup"><span data-stu-id="56bc1-141">The *face* parameter describes which polygons *mode* applies to: front-facing polygons (GL\_FRONT), back-facing polygons (GL\_BACK), or both (GL\_FRONT\_AND\_BACK).</span></span> <span data-ttu-id="56bc1-142">Le mode polygone affecte uniquement la pixellisation finale des polygones.</span><span class="sxs-lookup"><span data-stu-id="56bc1-142">The polygon mode affects only the final rasterization of polygons.</span></span> <span data-ttu-id="56bc1-143">En particulier, les vertex d’un polygone sont allumés et le polygone est coupé et éventuellement Culling avant l’application de ces modes.</span><span class="sxs-lookup"><span data-stu-id="56bc1-143">In particular, a polygon's vertices are lit and the polygon is clipped and possibly culled before these modes are applied.</span></span>

<span data-ttu-id="56bc1-144">Pour dessiner une surface avec des polygones retournés vers l’avant et des polygones prédéfinis, appelez</span><span class="sxs-lookup"><span data-stu-id="56bc1-144">To draw a surface with filled back-facing polygons and outlined front-facing polygons, call</span></span>

<span data-ttu-id="56bc1-145">**glPolygonMode**(GL \_ frontal, \_ ligne GL);</span><span class="sxs-lookup"><span data-stu-id="56bc1-145">**glPolygonMode**(GL\_FRONT, GL\_LINE);</span></span>

<span data-ttu-id="56bc1-146">Les sommets sont marqués comme limites ou non liés par un indicateur de bord.</span><span class="sxs-lookup"><span data-stu-id="56bc1-146">Vertices are marked as boundary or nonboundary with an edge flag.</span></span> <span data-ttu-id="56bc1-147">Les indicateurs de périphérie sont générés en interne par OpenGL lorsqu’ils décomposent des polygones, et ils peuvent être définis explicitement à l’aide de [**glEdgeFlag**](gledgeflag-functions.md).</span><span class="sxs-lookup"><span data-stu-id="56bc1-147">Edge flags are generated internally by OpenGL when it decomposes polygons, and they can be set explicitly using [**glEdgeFlag**](gledgeflag-functions.md).</span></span>

<span data-ttu-id="56bc1-148">La fonction suivante récupère des informations relatives à **glPolygonMode**:</span><span class="sxs-lookup"><span data-stu-id="56bc1-148">The following function retrieves information related to **glPolygonMode**:</span></span>

<span data-ttu-id="56bc1-149">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ polygone \_ mode</span><span class="sxs-lookup"><span data-stu-id="56bc1-149">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POLYGON\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="56bc1-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56bc1-150">Requirements</span></span>



| <span data-ttu-id="56bc1-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56bc1-151">Requirement</span></span> | <span data-ttu-id="56bc1-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="56bc1-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56bc1-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56bc1-153">Minimum supported client</span></span><br/> | <span data-ttu-id="56bc1-154">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56bc1-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="56bc1-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56bc1-155">Minimum supported server</span></span><br/> | <span data-ttu-id="56bc1-156">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56bc1-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="56bc1-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="56bc1-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="56bc1-158"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="56bc1-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="56bc1-159">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="56bc1-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="56bc1-160"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56bc1-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="56bc1-161">DLL</span><span class="sxs-lookup"><span data-stu-id="56bc1-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56bc1-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56bc1-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56bc1-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56bc1-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56bc1-164">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="56bc1-164">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="56bc1-165">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="56bc1-165">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="56bc1-166">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="56bc1-166">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="56bc1-167">**glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="56bc1-167">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="56bc1-168">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="56bc1-168">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="56bc1-169">**glPointSize**</span><span class="sxs-lookup"><span data-stu-id="56bc1-169">**glPointSize**</span></span>](glpointsize.md)
</dt> <dt>

[<span data-ttu-id="56bc1-170">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="56bc1-170">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> </dl>

 

 





