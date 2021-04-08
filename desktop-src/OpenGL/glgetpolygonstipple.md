---
title: fonction glGetPolygonStipple (GL. h)
description: La fonction glGetPolygonStipple retourne le modèle Polygon stipple.
ms.assetid: 95c1ebfa-8465-4bc1-b3f5-eed696a83816
keywords:
- glGetPolygonStipple fonction OpenGL
topic_type:
- apiref
api_name:
- glGetPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643d0ea6b7583f26565ab7b9233f7df1dce9aead
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843233"
---
# <a name="glgetpolygonstipple-function"></a><span data-ttu-id="27354-104">glGetPolygonStipple fonction)</span><span class="sxs-lookup"><span data-stu-id="27354-104">glGetPolygonStipple function</span></span>

<span data-ttu-id="27354-105">La fonction **glGetPolygonStipple** retourne le modèle Polygon stipple.</span><span class="sxs-lookup"><span data-stu-id="27354-105">The **glGetPolygonStipple** function returns the polygon stipple pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="27354-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27354-106">Syntax</span></span>


```C++
void WINAPI glGetPolygonStipple(
   GLubyte *mask
);
```



## <a name="parameters"></a><span data-ttu-id="27354-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="27354-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27354-108">*mask*</span><span class="sxs-lookup"><span data-stu-id="27354-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="27354-109">Retourne le modèle stipple.</span><span class="sxs-lookup"><span data-stu-id="27354-109">Returns the stipple pattern.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27354-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="27354-110">Return value</span></span>

<span data-ttu-id="27354-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="27354-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="27354-112">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="27354-112">Error codes</span></span>

<span data-ttu-id="27354-113">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="27354-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="27354-114">Nom</span><span class="sxs-lookup"><span data-stu-id="27354-114">Name</span></span>                                                                                                  | <span data-ttu-id="27354-115">Signification</span><span class="sxs-lookup"><span data-stu-id="27354-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="27354-116"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="27354-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="27354-117">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="27354-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="27354-118">Notes</span><span class="sxs-lookup"><span data-stu-id="27354-118">Remarks</span></span>

<span data-ttu-id="27354-119">La fonction **glGetPolygonStipple** retourne un modèle de stipple de polygone 32 x 32 via le paramètre *Mask* .</span><span class="sxs-lookup"><span data-stu-id="27354-119">The **glGetPolygonStipple** function returns a 32x32 polygon stipple pattern through the *mask* parameter.</span></span> <span data-ttu-id="27354-120">Le modèle est compressé en mémoire comme si [**glReadPixels**](glreadpixels.md) avec la *hauteur* et la *largeur* de 32, le *type* de \_ bitmap GL et le *format* de \_ l’index de couleur GL \_ ont été appelés, et le modèle stipple était stocké dans une mémoire tampon d’index de couleurs 32 x 32 interne.</span><span class="sxs-lookup"><span data-stu-id="27354-120">The pattern is packed into memory as if [**glReadPixels**](glreadpixels.md) with both *height* and *width* of 32, *type* of GL\_BITMAP, and *format* of GL\_COLOR\_INDEX were called, and the stipple pattern were stored in an internal 32x32 color-index buffer.</span></span> <span data-ttu-id="27354-121">Contrairement à **glReadPixels**, toutefois, les opérations de transfert de pixels (décalage, décalage et carte de pixels) ne sont pas appliquées à l’image stipple retournée.</span><span class="sxs-lookup"><span data-stu-id="27354-121">Unlike **glReadPixels**, however, pixel-transfer operations (shift, offset, and pixel map) are not applied to the returned stipple image.</span></span>

<span data-ttu-id="27354-122">Si une erreur est générée, aucune modification n’est apportée au contenu du *masque*.</span><span class="sxs-lookup"><span data-stu-id="27354-122">If an error is generated, no change is made to the contents of *mask*.</span></span>

## <a name="requirements"></a><span data-ttu-id="27354-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27354-123">Requirements</span></span>



| <span data-ttu-id="27354-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="27354-124">Requirement</span></span> | <span data-ttu-id="27354-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="27354-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27354-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27354-126">Minimum supported client</span></span><br/> | <span data-ttu-id="27354-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27354-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="27354-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27354-128">Minimum supported server</span></span><br/> | <span data-ttu-id="27354-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27354-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="27354-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="27354-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="27354-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="27354-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="27354-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="27354-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="27354-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27354-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="27354-134">DLL</span><span class="sxs-lookup"><span data-stu-id="27354-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27354-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27354-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27354-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27354-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27354-137">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="27354-137">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="27354-138">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="27354-138">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="27354-139">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="27354-139">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="27354-140">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="27354-140">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="27354-141">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="27354-141">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="27354-142">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="27354-142">**glReadPixels**</span></span>](glreadpixels.md)
</dt> </dl>

 

 





