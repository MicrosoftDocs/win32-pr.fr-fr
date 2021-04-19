---
title: fonction glColor3i (GL. h)
description: Définit la couleur actuelle. | fonction glColor3i (GL. h)
ms.assetid: 9c68221b-1633-435b-9ae4-abc1c52601aa
keywords:
- glColor3i fonction OpenGL
topic_type:
- apiref
api_name:
- glColor3i
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6bb94421d44f7aed14c793c0f95d7b6467d7e38
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106531776"
---
# <a name="glcolor3i-function"></a><span data-ttu-id="1bc95-105">glColor3i fonction)</span><span class="sxs-lookup"><span data-stu-id="1bc95-105">glColor3i function</span></span>

<span data-ttu-id="1bc95-106">Définit la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="1bc95-106">Sets the current color.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bc95-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1bc95-107">Syntax</span></span>


```C++
void WINAPI glColor3i(
   GLint red,
   GLint green,
   GLint blue
);
```



## <a name="parameters"></a><span data-ttu-id="1bc95-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1bc95-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bc95-109">*rouge*</span><span class="sxs-lookup"><span data-stu-id="1bc95-109">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="1bc95-110">Nouvelle valeur rouge pour la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="1bc95-110">The new red value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="1bc95-111">*écologie*</span><span class="sxs-lookup"><span data-stu-id="1bc95-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="1bc95-112">Nouvelle valeur verte pour la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="1bc95-112">The new green value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="1bc95-113">*bleu*</span><span class="sxs-lookup"><span data-stu-id="1bc95-113">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="1bc95-114">Nouvelle valeur bleue pour la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="1bc95-114">The new blue value for the current color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bc95-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1bc95-115">Return value</span></span>

<span data-ttu-id="1bc95-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1bc95-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bc95-117">Notes</span><span class="sxs-lookup"><span data-stu-id="1bc95-117">Remarks</span></span>

<span data-ttu-id="1bc95-118">Le GL stocke à la fois un index de couleurs à valeur unique actuel et une couleur RVBA à quatre valeurs actuelle.</span><span class="sxs-lookup"><span data-stu-id="1bc95-118">The GL stores both a current single-valued color index and a current four-valued RGBA color.</span></span> <span data-ttu-id="1bc95-119">**glcolor** définit une nouvelle couleur RVBA à quatre valeurs.</span><span class="sxs-lookup"><span data-stu-id="1bc95-119">**glcolor** sets a new four-valued RGBA color.</span></span> <span data-ttu-id="1bc95-120">**glcolor** a deux variantes majeures : **glcolor3** et **glcolor4**.</span><span class="sxs-lookup"><span data-stu-id="1bc95-120">**glcolor** has two major variants: **glcolor3** and **glcolor4**.</span></span> <span data-ttu-id="1bc95-121">les variantes **glcolor3** spécifient les nouvelles valeurs de rouge, de vert et de bleu explicitement et définissent la valeur alpha actuelle sur 1,0 (intensité complète) de manière implicite.</span><span class="sxs-lookup"><span data-stu-id="1bc95-121">**glcolor3** variants specify new red, green, and blue values explicitly and set the current alpha value to 1.0 (full intensity) implicitly.</span></span> <span data-ttu-id="1bc95-122">les variantes **glcolor4** spécifient les quatre composants de couleur de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="1bc95-122">**glcolor4** variants specify all four color components explicitly.</span></span>

<span data-ttu-id="1bc95-123">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i** et **glcolor4i** prennent trois ou quatre entiers signés Byte, short ou long comme arguments.</span><span class="sxs-lookup"><span data-stu-id="1bc95-123">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i**, and **glcolor4i** take three or four signed byte, short, or long integers as arguments.</span></span> <span data-ttu-id="1bc95-124">Quand v est ajouté au nom, les commandes de couleur peuvent prendre un pointeur vers un tableau de telles valeurs.</span><span class="sxs-lookup"><span data-stu-id="1bc95-124">When v is appended to the name, the color commands can take a pointer to an array of such values.</span></span>

<span data-ttu-id="1bc95-125">Les valeurs de couleur actuelles sont stockées dans un format à virgule flottante, avec la mantisse et les tailles d’exposant non spécifiées.</span><span class="sxs-lookup"><span data-stu-id="1bc95-125">Current color values are stored in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="1bc95-126">Les composants de couleur d’entier non signé, lorsqu’ils sont spécifiés, sont mappés de manière linéaire aux valeurs à virgule flottante, de sorte que la plus grande valeur représentable correspond à 1,0 (intensité complète) et 0 correspond à 0,0 (intensité nulle).</span><span class="sxs-lookup"><span data-stu-id="1bc95-126">Unsigned integer color components, when specified, are linearly mapped to floating-point values such that the largest representable value maps to 1.0 (full intensity), and 0 maps to 0.0 (zero intensity).</span></span> <span data-ttu-id="1bc95-127">Les composants de couleur d’entier signé, lorsqu’ils sont spécifiés, sont mappés de manière linéaire aux valeurs à virgule flottante, de sorte que la valeur représentable la plus positive correspond à 1,0, et la valeur représentable la plus négative correspond à-1,0.</span><span class="sxs-lookup"><span data-stu-id="1bc95-127">Signed integer color components, when specified, are linearly mapped to floating-point values such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="1bc95-128">(Notez que ce mappage ne convertit pas 0 de manière précise en 0,0.) Les valeurs à virgule flottante sont mappées directement.</span><span class="sxs-lookup"><span data-stu-id="1bc95-128">(Note that this mapping does not convert 0 precisely to 0.0.) Floating-point values are mapped directly.</span></span>

<span data-ttu-id="1bc95-129">Ni les valeurs d’entier à virgule flottante ni les valeurs entières signées ne sont ancrées à la plage \[ 0, 1 \] avant la mise à jour de la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="1bc95-129">Neither floating-point nor signed integer values are clamped to the range \[0,1\] before the current color is updated.</span></span> <span data-ttu-id="1bc95-130">Toutefois, les composants de couleur sont bloqués dans cette plage avant d’être interpolés ou écrits dans une mémoire tampon de couleur.</span><span class="sxs-lookup"><span data-stu-id="1bc95-130">However, color components are clamped to this range before they are interpolated or written into a color buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bc95-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1bc95-131">Requirements</span></span>



| <span data-ttu-id="1bc95-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1bc95-132">Requirement</span></span> | <span data-ttu-id="1bc95-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="1bc95-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bc95-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1bc95-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1bc95-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1bc95-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1bc95-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1bc95-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1bc95-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1bc95-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1bc95-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="1bc95-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bc95-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bc95-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1bc95-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1bc95-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="1bc95-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1bc95-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1bc95-142">DLL</span><span class="sxs-lookup"><span data-stu-id="1bc95-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bc95-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1bc95-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bc95-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bc95-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bc95-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="1bc95-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1bc95-146">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="1bc95-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="1bc95-147">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="1bc95-147">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="1bc95-148">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="1bc95-148">**glIndex**</span></span>](glindexd.md)
</dt> </dl>

 

 





