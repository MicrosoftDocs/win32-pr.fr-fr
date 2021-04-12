---
title: gluGetTessProperty, fonction (Glu. h)
description: La fonction gluGetTessProperty obtient une propriété d’objet de pavage.
ms.assetid: 6aa565d8-2257-4259-a959-b7d806a7ed96
keywords:
- gluGetTessProperty fonction OpenGL
topic_type:
- apiref
api_name:
- gluGetTessProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 482f32b227dbcf0c2a62405e344aa719bb4b9e17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384459"
---
# <a name="glugettessproperty-function"></a><span data-ttu-id="d4b5e-104">gluGetTessProperty fonction)</span><span class="sxs-lookup"><span data-stu-id="d4b5e-104">gluGetTessProperty function</span></span>

<span data-ttu-id="d4b5e-105">La fonction **gluGetTessProperty** obtient une propriété d’objet de pavage.</span><span class="sxs-lookup"><span data-stu-id="d4b5e-105">The **gluGetTessProperty** function gets a tessellation object property.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4b5e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4b5e-106">Syntax</span></span>


```C++
void WINAPI gluGetTessProperty(
   GLUtesselator *tess,
   GLenum        which,
   GLdouble      *value
);
```



## <a name="parameters"></a><span data-ttu-id="d4b5e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4b5e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4b5e-108">*tess*</span><span class="sxs-lookup"><span data-stu-id="d4b5e-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="d4b5e-109">Objet de pavage (créé avec [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="d4b5e-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="d4b5e-110">*et*</span><span class="sxs-lookup"><span data-stu-id="d4b5e-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="d4b5e-111">Propriété dont la valeur doit être récupérée.</span><span class="sxs-lookup"><span data-stu-id="d4b5e-111">The property whose value is to be retrieved.</span></span> <span data-ttu-id="d4b5e-112">Les valeurs suivantes sont valides : \_ \_ règle d’enroulement Tess Glu \_ , limite de Glu \_ Tess \_ \_ uniquement et \_ tolérance Glu Tess \_ .</span><span class="sxs-lookup"><span data-stu-id="d4b5e-112">The following values are valid: GLU\_TESS\_WINDING\_RULE, GLU\_TESS\_BOUNDARY\_ONLY, and GLU\_TESS\_TOLERANCE.</span></span>

</dd> <dt>

<span data-ttu-id="d4b5e-113">*value*</span><span class="sxs-lookup"><span data-stu-id="d4b5e-113">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="d4b5e-114">Pointeur vers l’emplacement où la valeur de la propriété nommée est écrite.</span><span class="sxs-lookup"><span data-stu-id="d4b5e-114">A pointer to the location where the value of the named property is written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4b5e-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d4b5e-115">Return value</span></span>

<span data-ttu-id="d4b5e-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d4b5e-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4b5e-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d4b5e-117">Remarks</span></span>

<span data-ttu-id="d4b5e-118">Utilisez **gluGetTessProperty** pour récupérer les propriétés stockées dans un objet pavage.</span><span class="sxs-lookup"><span data-stu-id="d4b5e-118">Use **gluGetTessProperty** to retrieve properties stored in a tessellation object.</span></span> <span data-ttu-id="d4b5e-119">Ces propriétés affectent la manière dont les objets de pavage sont interprétés et rendus.</span><span class="sxs-lookup"><span data-stu-id="d4b5e-119">These properties affect the way tessellation objects are interpreted and rendered.</span></span> <span data-ttu-id="d4b5e-120">Pour plus d’informations sur ce que sont les propriétés et sur ce qu’elles font, consultez [**gluTessProperty**](glutessproperty.md).</span><span class="sxs-lookup"><span data-stu-id="d4b5e-120">For information about what the properties are and what they do, see [**gluTessProperty**](glutessproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4b5e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4b5e-121">Requirements</span></span>



| <span data-ttu-id="d4b5e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4b5e-122">Requirement</span></span> | <span data-ttu-id="d4b5e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4b5e-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d4b5e-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4b5e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d4b5e-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d4b5e-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d4b5e-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4b5e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d4b5e-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d4b5e-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d4b5e-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4b5e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4b5e-129"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4b5e-129"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="d4b5e-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d4b5e-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="d4b5e-131"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4b5e-131"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d4b5e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d4b5e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4b5e-133"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4b5e-133"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4b5e-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4b5e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4b5e-135">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="d4b5e-135">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="d4b5e-136">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="d4b5e-136">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> </dl>

 

 





