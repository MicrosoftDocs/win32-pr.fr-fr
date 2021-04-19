---
title: fonction glColor3d (GL. h)
description: Définit la couleur actuelle. | fonction glColor3d (GL. h)
ms.assetid: 55221cd6-a38c-4249-a6c1-31650fb93eb2
keywords:
- glColor3d fonction OpenGL
topic_type:
- apiref
api_name:
- glColor3d
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e04b5bcf9c8584f572cff05607290d5f509b2f9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106539841"
---
# <a name="glcolor3d-function"></a><span data-ttu-id="8031d-105">glColor3d fonction)</span><span class="sxs-lookup"><span data-stu-id="8031d-105">glColor3d function</span></span>

<span data-ttu-id="8031d-106">Définit la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="8031d-106">Sets the current color.</span></span>

## <a name="syntax"></a><span data-ttu-id="8031d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8031d-107">Syntax</span></span>


```C++
void WINAPI glColor3d(
   GLdouble red,
   GLdouble green,
   GLdouble blue
);
```



## <a name="parameters"></a><span data-ttu-id="8031d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8031d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8031d-109">*rouge*</span><span class="sxs-lookup"><span data-stu-id="8031d-109">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="8031d-110">Nouvelle valeur rouge pour la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="8031d-110">The new red value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="8031d-111">*écologie*</span><span class="sxs-lookup"><span data-stu-id="8031d-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="8031d-112">Nouvelle valeur verte pour la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="8031d-112">The new green value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="8031d-113">*bleu*</span><span class="sxs-lookup"><span data-stu-id="8031d-113">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="8031d-114">Nouvelle valeur bleue pour la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="8031d-114">The new blue value for the current color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8031d-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8031d-115">Return value</span></span>

<span data-ttu-id="8031d-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8031d-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8031d-117">Notes</span><span class="sxs-lookup"><span data-stu-id="8031d-117">Remarks</span></span>

<span data-ttu-id="8031d-118">Le GL stocke à la fois un index de couleurs à valeur unique actuel et une couleur RVBA à quatre valeurs actuelle.</span><span class="sxs-lookup"><span data-stu-id="8031d-118">The GL stores both a current single-valued color index and a current four-valued RGBA color.</span></span> <span data-ttu-id="8031d-119">**glcolor** définit une nouvelle couleur RVBA à quatre valeurs.</span><span class="sxs-lookup"><span data-stu-id="8031d-119">**glcolor** sets a new four-valued RGBA color.</span></span> <span data-ttu-id="8031d-120">**glcolor** a deux variantes majeures : **glcolor3** et **glcolor4**.</span><span class="sxs-lookup"><span data-stu-id="8031d-120">**glcolor** has two major variants: **glcolor3** and **glcolor4**.</span></span> <span data-ttu-id="8031d-121">les variantes **glcolor3** spécifient les nouvelles valeurs de rouge, de vert et de bleu explicitement et définissent la valeur alpha actuelle sur 1,0 (intensité complète) de manière implicite.</span><span class="sxs-lookup"><span data-stu-id="8031d-121">**glcolor3** variants specify new red, green, and blue values explicitly and set the current alpha value to 1.0 (full intensity) implicitly.</span></span> <span data-ttu-id="8031d-122">les variantes **glcolor4** spécifient les quatre composants de couleur de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="8031d-122">**glcolor4** variants specify all four color components explicitly.</span></span>

<span data-ttu-id="8031d-123">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i** et **glcolor4i** prennent trois ou quatre entiers signés Byte, short ou long comme arguments.</span><span class="sxs-lookup"><span data-stu-id="8031d-123">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i**, and **glcolor4i** take three or four signed byte, short, or long integers as arguments.</span></span> <span data-ttu-id="8031d-124">Quand v est ajouté au nom, les commandes de couleur peuvent prendre un pointeur vers un tableau de telles valeurs.</span><span class="sxs-lookup"><span data-stu-id="8031d-124">When v is appended to the name, the color commands can take a pointer to an array of such values.</span></span>

<span data-ttu-id="8031d-125">Les valeurs de couleur actuelles sont stockées dans un format à virgule flottante, avec la mantisse et les tailles d’exposant non spécifiées.</span><span class="sxs-lookup"><span data-stu-id="8031d-125">Current color values are stored in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="8031d-126">Les composants de couleur d’entier non signé, lorsqu’ils sont spécifiés, sont mappés de manière linéaire aux valeurs à virgule flottante, de sorte que la plus grande valeur représentable correspond à 1,0 (intensité complète) et 0 correspond à 0,0 (intensité nulle).</span><span class="sxs-lookup"><span data-stu-id="8031d-126">Unsigned integer color components, when specified, are linearly mapped to floating-point values such that the largest representable value maps to 1.0 (full intensity), and 0 maps to 0.0 (zero intensity).</span></span> <span data-ttu-id="8031d-127">Les composants de couleur d’entier signé, lorsqu’ils sont spécifiés, sont mappés de manière linéaire aux valeurs à virgule flottante, de sorte que la valeur représentable la plus positive correspond à 1,0, et la valeur représentable la plus négative correspond à-1,0.</span><span class="sxs-lookup"><span data-stu-id="8031d-127">Signed integer color components, when specified, are linearly mapped to floating-point values such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="8031d-128">(Notez que ce mappage ne convertit pas 0 de manière précise en 0,0.) Les valeurs à virgule flottante sont mappées directement.</span><span class="sxs-lookup"><span data-stu-id="8031d-128">(Note that this mapping does not convert 0 precisely to 0.0.) Floating-point values are mapped directly.</span></span>

<span data-ttu-id="8031d-129">Ni les valeurs d’entier à virgule flottante ni les valeurs entières signées ne sont ancrées à la plage \[ 0, 1 \] avant la mise à jour de la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="8031d-129">Neither floating-point nor signed integer values are clamped to the range \[0,1\] before the current color is updated.</span></span> <span data-ttu-id="8031d-130">Toutefois, les composants de couleur sont bloqués dans cette plage avant d’être interpolés ou écrits dans une mémoire tampon de couleur.</span><span class="sxs-lookup"><span data-stu-id="8031d-130">However, color components are clamped to this range before they are interpolated or written into a color buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="8031d-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8031d-131">Requirements</span></span>



| <span data-ttu-id="8031d-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8031d-132">Requirement</span></span> | <span data-ttu-id="8031d-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="8031d-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8031d-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8031d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="8031d-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8031d-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8031d-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8031d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="8031d-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8031d-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8031d-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="8031d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="8031d-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8031d-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8031d-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8031d-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="8031d-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8031d-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8031d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="8031d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8031d-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8031d-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8031d-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8031d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8031d-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="8031d-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="8031d-146">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="8031d-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="8031d-147">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="8031d-147">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="8031d-148">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="8031d-148">**glIndex**</span></span>](glindexd.md)
</dt> </dl>

 

 





