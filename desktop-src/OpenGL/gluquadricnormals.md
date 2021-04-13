---
title: gluQuadricNormals, fonction (Glu. h)
description: La fonction gluQuadricNormals spécifie le type de normal à utiliser pour Quadrics.
ms.assetid: 945759ec-ed4a-480f-8243-49fc785867c1
keywords:
- gluQuadricNormals fonction OpenGL
topic_type:
- apiref
api_name:
- gluQuadricNormals
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f11f9d8cd1884d7a5d1bc4cd03797517ba484126
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466175"
---
# <a name="gluquadricnormals-function"></a><span data-ttu-id="6a8bd-104">gluQuadricNormals fonction)</span><span class="sxs-lookup"><span data-stu-id="6a8bd-104">gluQuadricNormals function</span></span>

<span data-ttu-id="6a8bd-105">La fonction **gluQuadricNormals** spécifie le type de normal à utiliser pour Quadrics.</span><span class="sxs-lookup"><span data-stu-id="6a8bd-105">The **gluQuadricNormals** function specifies what kind of normals are to be used for quadrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a8bd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a8bd-106">Syntax</span></span>


```C++
void WINAPI gluQuadricNormals(
   GLUquadric *quadObject,
   GLenum     normals
);
```



## <a name="parameters"></a><span data-ttu-id="6a8bd-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a8bd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a8bd-108">*quadObject*</span><span class="sxs-lookup"><span data-stu-id="6a8bd-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="6a8bd-109">Objet quadric (créé avec [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="6a8bd-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="6a8bd-110">*normales*</span><span class="sxs-lookup"><span data-stu-id="6a8bd-110">*normals*</span></span> 
</dt> <dd>

<span data-ttu-id="6a8bd-111">Type de normalisation souhaité.</span><span class="sxs-lookup"><span data-stu-id="6a8bd-111">The desired type of normals.</span></span> <span data-ttu-id="6a8bd-112">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="6a8bd-112">The following values are valid.</span></span>



| <span data-ttu-id="6a8bd-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a8bd-113">Value</span></span>                                                                                                                                                | <span data-ttu-id="6a8bd-114">Signification</span><span class="sxs-lookup"><span data-stu-id="6a8bd-114">Meaning</span></span>                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="GLU_NONE"></span><span id="glu_none"></span><dl> <span data-ttu-id="6a8bd-115"><dt>**GLU \_ aucun**</dt></span><span class="sxs-lookup"><span data-stu-id="6a8bd-115"><dt>**GLU\_NONE**</dt></span></span> </dl>       | <span data-ttu-id="6a8bd-116">Aucune normale n’est générée.</span><span class="sxs-lookup"><span data-stu-id="6a8bd-116">No normals are generated.</span></span><br/>                                                         |
| <span id="GLU_FLAT"></span><span id="glu_flat"></span><dl> <span data-ttu-id="6a8bd-117"><dt>**GLU \_ plat**</dt></span><span class="sxs-lookup"><span data-stu-id="6a8bd-117"><dt>**GLU\_FLAT**</dt></span></span> </dl>       | <span data-ttu-id="6a8bd-118">Une normale est générée pour chaque facette d’un quadric.</span><span class="sxs-lookup"><span data-stu-id="6a8bd-118">One normal is generated for every facet of a quadric.</span></span><br/>                             |
| <span id="GLU_SMOOTH"></span><span id="glu_smooth"></span><dl> <span data-ttu-id="6a8bd-119"><dt>**GLU \_ lisse**</dt></span><span class="sxs-lookup"><span data-stu-id="6a8bd-119"><dt>**GLU\_SMOOTH**</dt></span></span> </dl> | <span data-ttu-id="6a8bd-120">Une normale est générée pour chaque vertex d’un quadric.</span><span class="sxs-lookup"><span data-stu-id="6a8bd-120">One normal is generated for every vertex of a quadric.</span></span> <span data-ttu-id="6a8bd-121">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="6a8bd-121">This is the default value.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a8bd-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6a8bd-122">Return value</span></span>

<span data-ttu-id="6a8bd-123">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6a8bd-123">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a8bd-124">Notes</span><span class="sxs-lookup"><span data-stu-id="6a8bd-124">Remarks</span></span>

<span data-ttu-id="6a8bd-125">La fonction **gluQuadricNormals** spécifie le type de normal à utiliser pour le rendu de Quadrics avec **quadObject**.</span><span class="sxs-lookup"><span data-stu-id="6a8bd-125">The **gluQuadricNormals** function specifies what kind of normals are to be used for quadrics rendered with **quadObject**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a8bd-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a8bd-126">Requirements</span></span>



| <span data-ttu-id="6a8bd-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a8bd-127">Requirement</span></span> | <span data-ttu-id="6a8bd-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a8bd-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6a8bd-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a8bd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6a8bd-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a8bd-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6a8bd-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a8bd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6a8bd-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a8bd-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6a8bd-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="6a8bd-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a8bd-134"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a8bd-134"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="6a8bd-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6a8bd-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="6a8bd-136"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a8bd-136"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6a8bd-137">DLL</span><span class="sxs-lookup"><span data-stu-id="6a8bd-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a8bd-138"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a8bd-138"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a8bd-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a8bd-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a8bd-140">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="6a8bd-140">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="6a8bd-141">**gluQuadricDrawStyle**</span><span class="sxs-lookup"><span data-stu-id="6a8bd-141">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="6a8bd-142">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="6a8bd-142">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="6a8bd-143">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="6a8bd-143">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





