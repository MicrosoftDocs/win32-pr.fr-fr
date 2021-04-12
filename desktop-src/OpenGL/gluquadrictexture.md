---
title: gluQuadricTexture, fonction (Glu. h)
description: La fonction gluQuadricTexture spécifie si les Quadrics doivent être texturés.
ms.assetid: 11681497-f099-4856-a0ac-6a44abd3e1a1
keywords:
- gluQuadricTexture fonction OpenGL
topic_type:
- apiref
api_name:
- gluQuadricTexture
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc395564b6c6f30f38a8c5129c489d0bfca6b80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104929"
---
# <a name="gluquadrictexture-function"></a><span data-ttu-id="075c8-104">gluQuadricTexture fonction)</span><span class="sxs-lookup"><span data-stu-id="075c8-104">gluQuadricTexture function</span></span>

<span data-ttu-id="075c8-105">La fonction **gluQuadricTexture** spécifie si les Quadrics doivent être texturés.</span><span class="sxs-lookup"><span data-stu-id="075c8-105">The **gluQuadricTexture** function specifies whether quadrics are to be textured.</span></span>

## <a name="syntax"></a><span data-ttu-id="075c8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="075c8-106">Syntax</span></span>


```C++
void WINAPI gluQuadricTexture(
   GLUquadric *quadObject,
   GLboolean  textureCoords
);
```



## <a name="parameters"></a><span data-ttu-id="075c8-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="075c8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="075c8-108">*quadObject*</span><span class="sxs-lookup"><span data-stu-id="075c8-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="075c8-109">Objet quadric (créé avec [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="075c8-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="075c8-110">*textureCoords*</span><span class="sxs-lookup"><span data-stu-id="075c8-110">*textureCoords*</span></span> 
</dt> <dd>

<span data-ttu-id="075c8-111">Indicateur qui spécifie si les coordonnées de texture doivent être générées.</span><span class="sxs-lookup"><span data-stu-id="075c8-111">A flag indicating whether texture coordinates are to be generated.</span></span> <span data-ttu-id="075c8-112">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="075c8-112">The following values are valid.</span></span>



| <span data-ttu-id="075c8-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="075c8-113">Value</span></span>                                                                                                                                          | <span data-ttu-id="075c8-114">Signification</span><span class="sxs-lookup"><span data-stu-id="075c8-114">Meaning</span></span>                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="GL_TRUE"></span><span id="gl_true"></span><dl> <span data-ttu-id="075c8-115"><dt>**GL \_ true**</dt></span><span class="sxs-lookup"><span data-stu-id="075c8-115"><dt>**GL\_TRUE**</dt></span></span> </dl>    | <span data-ttu-id="075c8-116">Générer des coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="075c8-116">Generate texture coordinates.</span></span><br/>                                   |
| <span id="GL_FALSE"></span><span id="gl_false"></span><dl> <span data-ttu-id="075c8-117"><dt>**GL- \_ faux**</dt></span><span class="sxs-lookup"><span data-stu-id="075c8-117"><dt>**GL\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="075c8-118">Ne générez pas de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="075c8-118">Do not generate texture coordinates.</span></span> <span data-ttu-id="075c8-119">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="075c8-119">This is the default value.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="075c8-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="075c8-120">Return value</span></span>

<span data-ttu-id="075c8-121">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="075c8-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="075c8-122">Notes</span><span class="sxs-lookup"><span data-stu-id="075c8-122">Remarks</span></span>

<span data-ttu-id="075c8-123">La fonction **gluQuadricTexture** spécifie si les coordonnées de texture doivent être générées pour Quadrics rendu avec **quadObject**.</span><span class="sxs-lookup"><span data-stu-id="075c8-123">The **gluQuadricTexture** function specifies whether texture coordinates are to be generated for quadrics rendered with **quadObject**.</span></span>

<span data-ttu-id="075c8-124">La manière dont les coordonnées de texture sont générées dépend du rendu quadric spécifique.</span><span class="sxs-lookup"><span data-stu-id="075c8-124">The manner in which texture coordinates are generated depends upon the specific quadric rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="075c8-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="075c8-125">Requirements</span></span>



| <span data-ttu-id="075c8-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="075c8-126">Requirement</span></span> | <span data-ttu-id="075c8-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="075c8-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="075c8-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="075c8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="075c8-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="075c8-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="075c8-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="075c8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="075c8-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="075c8-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="075c8-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="075c8-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="075c8-133"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="075c8-133"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="075c8-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="075c8-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="075c8-135"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="075c8-135"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="075c8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="075c8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="075c8-137"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="075c8-137"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="075c8-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="075c8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="075c8-139">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="075c8-139">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="075c8-140">**gluQuadricDrawStyle**</span><span class="sxs-lookup"><span data-stu-id="075c8-140">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="075c8-141">**gluQuadricNormals**</span><span class="sxs-lookup"><span data-stu-id="075c8-141">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> </dl>

 

 





