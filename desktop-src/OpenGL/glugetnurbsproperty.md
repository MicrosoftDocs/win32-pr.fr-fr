---
title: gluGetNurbsProperty, fonction (Glu. h)
description: La fonction gluGetNurbsProperty obtient une propriété NURBS B-spline (NURBS) non uniforme.
ms.assetid: 7dbc75a0-d04e-4794-b3dd-a602addf9dfa
keywords:
- gluGetNurbsProperty fonction OpenGL
topic_type:
- apiref
api_name:
- gluGetNurbsProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583da688e3495ebc2eb9d6f71972658c6426469c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103425"
---
# <a name="glugetnurbsproperty-function"></a><span data-ttu-id="a9b71-104">gluGetNurbsProperty fonction)</span><span class="sxs-lookup"><span data-stu-id="a9b71-104">gluGetNurbsProperty function</span></span>

<span data-ttu-id="a9b71-105">La fonction **gluGetNurbsProperty** obtient une propriété NURBS B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) non uniforme.</span><span class="sxs-lookup"><span data-stu-id="a9b71-105">The **gluGetNurbsProperty** function gets a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9b71-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9b71-106">Syntax</span></span>


```C++
void WINAPI gluGetNurbsProperty(
   GLUnurbs *nobj,
   GLenum   property,
   GLfloat  *value
);
```



## <a name="parameters"></a><span data-ttu-id="a9b71-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9b71-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9b71-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="a9b71-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="a9b71-109">Objet NURBS (créé avec [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="a9b71-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a9b71-110">*property*</span><span class="sxs-lookup"><span data-stu-id="a9b71-110">*property*</span></span> 
</dt> <dd>

<span data-ttu-id="a9b71-111">Propriété dont la valeur doit être récupérée.</span><span class="sxs-lookup"><span data-stu-id="a9b71-111">The property whose value is to be retrieved.</span></span> <span data-ttu-id="a9b71-112">Les valeurs suivantes sont valides : \_ tolérance d’échantillonnage Glu \_ , \_ mode d’affichage Glu \_ , \_ élimination de Glu, \_ matrice de chargement automatique Glu \_ \_ , \_ tolérance paramétrique Glu \_ , méthode d' \_ échantillonnage Glu \_ , \_ étape Glu U \_ et \_ étape Glu V \_ .</span><span class="sxs-lookup"><span data-stu-id="a9b71-112">The following values are valid: GLU\_SAMPLING\_TOLERANCE, GLU\_DISPLAY\_MODE, GLU\_CULLING, GLU\_AUTO\_LOAD\_MATRIX, GLU\_PARAMETRIC\_TOLERANCE, GLU\_SAMPLING\_METHOD, GLU\_U\_STEP, and GLU\_V\_STEP.</span></span>

</dd> <dt>

<span data-ttu-id="a9b71-113">*value*</span><span class="sxs-lookup"><span data-stu-id="a9b71-113">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="a9b71-114">Pointeur vers l’emplacement dans lequel la valeur de la propriété nommée est écrite.</span><span class="sxs-lookup"><span data-stu-id="a9b71-114">A pointer to the location into which the value of the named property is written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9b71-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a9b71-115">Return value</span></span>

<span data-ttu-id="a9b71-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a9b71-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9b71-117">Notes</span><span class="sxs-lookup"><span data-stu-id="a9b71-117">Remarks</span></span>

<span data-ttu-id="a9b71-118">Utilisez **gluGetNurbsProperty** pour récupérer les propriétés stockées dans un objet NURBS.</span><span class="sxs-lookup"><span data-stu-id="a9b71-118">Use **gluGetNurbsProperty** to retrieve properties stored in a NURBS object.</span></span> <span data-ttu-id="a9b71-119">Ces propriétés affectent le mode de rendu des courbes et des surfaces NURBS.</span><span class="sxs-lookup"><span data-stu-id="a9b71-119">These properties affect the way NURBS curves and surfaces are rendered.</span></span> <span data-ttu-id="a9b71-120">Pour plus d’informations sur les propriétés NURBS, consultez [**gluNurbsProperty**](glunurbsproperty.md).</span><span class="sxs-lookup"><span data-stu-id="a9b71-120">For information about NURBS properties, see [**gluNurbsProperty**](glunurbsproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9b71-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9b71-121">Requirements</span></span>



| <span data-ttu-id="a9b71-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9b71-122">Requirement</span></span> | <span data-ttu-id="a9b71-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9b71-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a9b71-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9b71-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a9b71-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9b71-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a9b71-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9b71-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a9b71-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9b71-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a9b71-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="a9b71-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9b71-129"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9b71-129"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="a9b71-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a9b71-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="a9b71-131"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9b71-131"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a9b71-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a9b71-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9b71-133"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9b71-133"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9b71-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9b71-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9b71-135">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="a9b71-135">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="a9b71-136">**gluNurbsProperty**</span><span class="sxs-lookup"><span data-stu-id="a9b71-136">**gluNurbsProperty**</span></span>](glunurbsproperty.md)
</dt> </dl>

 

 





