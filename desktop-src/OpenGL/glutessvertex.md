---
title: gluTessVertex, fonction (Glu. h)
description: La fonction gluTessVertex spécifie un sommet sur un polygone.
ms.assetid: 9c555b32-5257-4eeb-9323-ccad59591097
keywords:
- gluTessVertex fonction OpenGL
topic_type:
- apiref
api_name:
- gluTessVertex
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 546bbad2be1205f62c7889fbb18f23d5b0e38b8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509294"
---
# <a name="glutessvertex-function"></a><span data-ttu-id="3f593-104">gluTessVertex fonction)</span><span class="sxs-lookup"><span data-stu-id="3f593-104">gluTessVertex function</span></span>

<span data-ttu-id="3f593-105">La fonction **gluTessVertex** spécifie un sommet sur un polygone.</span><span class="sxs-lookup"><span data-stu-id="3f593-105">The **gluTessVertex** function specifies a vertex on a polygon.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f593-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f593-106">Syntax</span></span>


```C++
void WINAPI gluTessVertex(
   GLUtesselator *tess,
   GLdouble      coords[3],
   void          *data
);
```



## <a name="parameters"></a><span data-ttu-id="3f593-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f593-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f593-108">*tess*</span><span class="sxs-lookup"><span data-stu-id="3f593-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="3f593-109">Objet de pavage (créé avec [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="3f593-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="3f593-110">*coordonnées*</span><span class="sxs-lookup"><span data-stu-id="3f593-110">*coords*</span></span> 
</dt> <dd>

<span data-ttu-id="3f593-111">Emplacement du vertex.</span><span class="sxs-lookup"><span data-stu-id="3f593-111">The location of the vertex.</span></span>

</dd> <dt>

<span data-ttu-id="3f593-112">*data*</span><span class="sxs-lookup"><span data-stu-id="3f593-112">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="3f593-113">Pointeur retourné au programme avec le rappel de vertex (comme spécifié par [*gluTessCallback*](glutess.md)).</span><span class="sxs-lookup"><span data-stu-id="3f593-113">An pointer passed back to the program with the vertex callback (as specified by [*gluTessCallback*](glutess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f593-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3f593-114">Return value</span></span>

<span data-ttu-id="3f593-115">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3f593-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f593-116">Notes</span><span class="sxs-lookup"><span data-stu-id="3f593-116">Remarks</span></span>

<span data-ttu-id="3f593-117">La fonction **gluTessVertex** décrit un vertex sur un polygone que l’utilisateur définit.</span><span class="sxs-lookup"><span data-stu-id="3f593-117">The **gluTessVertex** function describes a vertex on a polygon that the user is defining.</span></span> <span data-ttu-id="3f593-118">Les appels **gluTessVertex** successifs décrivent un contour fermé.</span><span class="sxs-lookup"><span data-stu-id="3f593-118">Successive **gluTessVertex** calls describe a closed contour.</span></span> <span data-ttu-id="3f593-119">Par exemple, pour décrire un quadrangulaires, appelez **gluTessVertex** quatre fois.</span><span class="sxs-lookup"><span data-stu-id="3f593-119">For example, to describe a quadrilateral, call **gluTessVertex** four times.</span></span> <span data-ttu-id="3f593-120">Vous pouvez uniquement appeler **gluTessVertex** entre [**gluTessBeginContour**](glutessbegincontour.md) et [**gluTessEndContour**](glutessendcontour.md).</span><span class="sxs-lookup"><span data-stu-id="3f593-120">You can only call **gluTessVertex** between [**gluTessBeginContour**](glutessbegincontour.md) and [**gluTessEndContour**](glutessendcontour.md).</span></span>

<span data-ttu-id="3f593-121">Le paramètre de *données* pointe normalement vers une structure contenant l’emplacement du vertex, ainsi que d’autres attributs par vertex tels que la couleur et la normale.</span><span class="sxs-lookup"><span data-stu-id="3f593-121">The *data* parameter normally points to a structure containing the vertex location, as well as other per-vertex attributes such as color and normal.</span></span> <span data-ttu-id="3f593-122">Ce pointeur est retourné au programme par le biais du \_ rappel de vertex Glu après pavage (voir [*gluTessCallback*](glutess.md)).</span><span class="sxs-lookup"><span data-stu-id="3f593-122">This pointer is passed back to the program through the GLU\_VERTEX callback after tessellation (see [*gluTessCallback*](glutess.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="3f593-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f593-123">Requirements</span></span>



| <span data-ttu-id="3f593-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f593-124">Requirement</span></span> | <span data-ttu-id="3f593-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f593-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3f593-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f593-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3f593-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f593-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3f593-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f593-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3f593-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f593-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3f593-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="3f593-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f593-131"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f593-131"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="3f593-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3f593-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="3f593-133"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f593-133"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3f593-134">DLL</span><span class="sxs-lookup"><span data-stu-id="3f593-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f593-135"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f593-135"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f593-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f593-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f593-137">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="3f593-137">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="3f593-138">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="3f593-138">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="3f593-139">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="3f593-139">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="3f593-140">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="3f593-140">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="3f593-141">**gluTessEndContour**</span><span class="sxs-lookup"><span data-stu-id="3f593-141">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="3f593-142">**gluTessNormal**</span><span class="sxs-lookup"><span data-stu-id="3f593-142">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="3f593-143">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="3f593-143">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> </dl>

 

 





