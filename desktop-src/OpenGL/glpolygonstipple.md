---
title: fonction glPolygonStipple (GL. h)
description: La fonction glPolygonStipple définit le modèle Polygon stippling.
ms.assetid: e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6
keywords:
- glPolygonStipple fonction OpenGL
topic_type:
- apiref
api_name:
- glPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a2eb0b2e4319f7e3e37191fb197cd7ff86a2a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465654"
---
# <a name="glpolygonstipple-function"></a><span data-ttu-id="62654-104">glPolygonStipple fonction)</span><span class="sxs-lookup"><span data-stu-id="62654-104">glPolygonStipple function</span></span>

<span data-ttu-id="62654-105">La fonction **glPolygonStipple** définit le modèle Polygon stippling.</span><span class="sxs-lookup"><span data-stu-id="62654-105">The **glPolygonStipple** function sets the polygon stippling pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="62654-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62654-106">Syntax</span></span>


```C++
void WINAPI glPolygonStipple(
   const GLubyte *mask
);
```



## <a name="parameters"></a><span data-ttu-id="62654-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62654-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62654-108">*mask*</span><span class="sxs-lookup"><span data-stu-id="62654-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="62654-109">Pointeur vers un modèle stipple 32x32 qui sera décompressé de la mémoire de la même façon que [**glDrawPixels**](gldrawpixels.md) décompresse les pixels.</span><span class="sxs-lookup"><span data-stu-id="62654-109">A pointer to a 32x32 stipple pattern that will be unpacked from memory in the same way that [**glDrawPixels**](gldrawpixels.md) unpacks pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62654-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="62654-110">Return value</span></span>

<span data-ttu-id="62654-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="62654-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="62654-112">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="62654-112">Error codes</span></span>

<span data-ttu-id="62654-113">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="62654-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="62654-114">Nom</span><span class="sxs-lookup"><span data-stu-id="62654-114">Name</span></span>                                                                                                  | <span data-ttu-id="62654-115">Signification</span><span class="sxs-lookup"><span data-stu-id="62654-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="62654-116"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="62654-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="62654-117">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="62654-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="62654-118">Notes</span><span class="sxs-lookup"><span data-stu-id="62654-118">Remarks</span></span>

<span data-ttu-id="62654-119">La fonction **glPolygonStipple** définit le modèle Polygon stippling.</span><span class="sxs-lookup"><span data-stu-id="62654-119">The **glPolygonStipple** function sets the polygon stippling pattern.</span></span> <span data-ttu-id="62654-120">Polygon stippling, comme Line stippling (voir [**glLineStipple**](gllinestipple.md)), masque certains fragments produits par pixellisation, en créant un modèle.</span><span class="sxs-lookup"><span data-stu-id="62654-120">Polygon stippling, like line stippling (see [**glLineStipple**](gllinestipple.md)), masks out certain fragments produced by rasterization, creating a pattern.</span></span> <span data-ttu-id="62654-121">Stippling est indépendant de l’anticrénelage de polygones.</span><span class="sxs-lookup"><span data-stu-id="62654-121">Stippling is independent of polygon antialiasing.</span></span>

<span data-ttu-id="62654-122">Le paramètre *Mask* est un pointeur vers un modèle 32 x 32 stipple qui est stocké en mémoire comme les données de pixels fournies à **glDrawPixels** avec une *hauteur* et une *largeur* égales à 32, un *format* de pixel de l’index de couleur GL \_ et le \_ *type* de données de la \_ bitmap GL.</span><span class="sxs-lookup"><span data-stu-id="62654-122">The *mask* parameter is a pointer to a 32x32 stipple pattern that is stored in memory just like the pixel data supplied to **glDrawPixels** with *height* and *width* both equal to 32, a pixel *format* of GL\_COLOR\_INDEX, and data *type* of GL\_BITMAP.</span></span> <span data-ttu-id="62654-123">Autrement dit, le modèle stipple est représenté sous la forme d’un tableau 32x32 d’index de couleurs 1 bits, compacté en octets non signés.</span><span class="sxs-lookup"><span data-stu-id="62654-123">That is, the stipple pattern is represented as a 32x32 array of 1-bit color indexes packed in unsigned bytes.</span></span> <span data-ttu-id="62654-124">Les paramètres de la fonction [**glPixelStore**](glpixelstore-functions.md) , tels que \_ décompresser les \_ \_ octets d’échange et \_ décompresser les \_ LSB au format GL \_ , affectent tout d’abord l’assemblage des bits dans un modèle stipple.</span><span class="sxs-lookup"><span data-stu-id="62654-124">The [**glPixelStore**](glpixelstore-functions.md) function parameters, such as GL\_UNPACK\_SWAP\_BYTES and GL\_UNPACK\_LSB\_FIRST, affect the assembling of the bits into a stipple pattern.</span></span> <span data-ttu-id="62654-125">Toutefois, les opérations de transfert de pixels (Maj, décalage et mappage de pixels) ne sont pas appliquées à l’image stipple.</span><span class="sxs-lookup"><span data-stu-id="62654-125">Pixel transfer operations (shift, offset, and pixel map) are not applied to the stipple image, however.</span></span>

<span data-ttu-id="62654-126">Polygon stippling est activé et désactivé avec [**glEnable**](glenable.md) et **glDisable**, à l’aide de l’argument GL \_ Polygon \_ STIPPLE.</span><span class="sxs-lookup"><span data-stu-id="62654-126">Polygon stippling is enabled and disabled with [**glEnable**](glenable.md) and **glDisable**, using argument GL\_POLYGON\_STIPPLE.</span></span> <span data-ttu-id="62654-127">Si cette option est activée, un fragment de polygone pixellisé avec les coordonnées de fenêtre *x*<sub>w</sub> et *y*<sub>w</sub> est envoyé à l’étape suivante d’OpenGL si et seulement si le bit (*x*<sub>w</sub> mod 32) de la ligne (*y*<sub>w</sub> mod 32) TH est un.</span><span class="sxs-lookup"><span data-stu-id="62654-127">If enabled, a rasterized polygon fragment with window coordinates *x*<sub>w</sub> and *y*<sub>w</sub> is sent to the next stage of OpenGL if and only if the (*x*<sub>w</sub> mod 32)th bit in the (*y*<sub>w</sub> mod 32)th row of the stipple pattern is one.</span></span> <span data-ttu-id="62654-128">Lorsque Polygon stippling est désactivé, c’est comme si le modèle stipple était tous des éléments.</span><span class="sxs-lookup"><span data-stu-id="62654-128">When polygon stippling is disabled, it is as if the stipple pattern were all ones.</span></span>

<span data-ttu-id="62654-129">Les fonctions suivantes récupèrent les informations relatives à **glPolygonStipple**:</span><span class="sxs-lookup"><span data-stu-id="62654-129">The following functions retrieve information related to **glPolygonStipple**:</span></span>

[<span data-ttu-id="62654-130">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="62654-130">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)

<span data-ttu-id="62654-131">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Polygon \_ STIPPLE</span><span class="sxs-lookup"><span data-stu-id="62654-131">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_STIPPLE</span></span>

## <a name="requirements"></a><span data-ttu-id="62654-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62654-132">Requirements</span></span>



| <span data-ttu-id="62654-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62654-133">Requirement</span></span> | <span data-ttu-id="62654-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="62654-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62654-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62654-135">Minimum supported client</span></span><br/> | <span data-ttu-id="62654-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62654-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="62654-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62654-137">Minimum supported server</span></span><br/> | <span data-ttu-id="62654-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62654-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="62654-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="62654-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="62654-140"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="62654-140"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="62654-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="62654-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="62654-142"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62654-142"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="62654-143">DLL</span><span class="sxs-lookup"><span data-stu-id="62654-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62654-144"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62654-144"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62654-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62654-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62654-146">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="62654-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="62654-147">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="62654-147">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="62654-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="62654-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="62654-149">**glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="62654-149">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="62654-150">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="62654-150">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="62654-151">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="62654-151">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> </dl>

 

 





