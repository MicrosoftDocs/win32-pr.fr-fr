---
title: fonction glColor4i (GL. h)
description: Définit la couleur actuelle. | fonction glColor4i (GL. h)
ms.assetid: d71b2b7d-64e8-4387-91ab-d0f96c0a584f
keywords:
- glColor4i fonction OpenGL
topic_type:
- apiref
api_name:
- glColor4i
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29ae63d605565c85d46ba6926d18404762549179
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869938"
---
# <a name="glcolor4i-function"></a><span data-ttu-id="54817-105">glColor4i fonction)</span><span class="sxs-lookup"><span data-stu-id="54817-105">glColor4i function</span></span>

<span data-ttu-id="54817-106">Définit la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="54817-106">Sets the current color.</span></span>

## <a name="syntax"></a><span data-ttu-id="54817-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54817-107">Syntax</span></span>


```C++
void WINAPI glColor4i(
   GLint red,
   GLint green,
   GLint blue,
   GLint alpha
);
```



## <a name="parameters"></a><span data-ttu-id="54817-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54817-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54817-109">*rouge*</span><span class="sxs-lookup"><span data-stu-id="54817-109">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="54817-110">Nouvelle valeur rouge pour la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="54817-110">The new red value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="54817-111">*écologie*</span><span class="sxs-lookup"><span data-stu-id="54817-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="54817-112">Nouvelle valeur verte pour la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="54817-112">The new green value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="54817-113">*bleu*</span><span class="sxs-lookup"><span data-stu-id="54817-113">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="54817-114">Nouvelle valeur bleue pour la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="54817-114">The new blue value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="54817-115">*alpha*</span><span class="sxs-lookup"><span data-stu-id="54817-115">*alpha*</span></span> 
</dt> <dd>

<span data-ttu-id="54817-116">Nouvelle valeur alpha pour la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="54817-116">The new alpha value for the current color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54817-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="54817-117">Return value</span></span>

<span data-ttu-id="54817-118">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="54817-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="54817-119">Notes</span><span class="sxs-lookup"><span data-stu-id="54817-119">Remarks</span></span>

<span data-ttu-id="54817-120">Le GL stocke à la fois un index de couleurs à valeur unique actuel et une couleur RVBA à quatre valeurs actuelle.</span><span class="sxs-lookup"><span data-stu-id="54817-120">The GL stores both a current single-valued color index and a current four-valued RGBA color.</span></span> <span data-ttu-id="54817-121">**glcolor** définit une nouvelle couleur RVBA à quatre valeurs.</span><span class="sxs-lookup"><span data-stu-id="54817-121">**glcolor** sets a new four-valued RGBA color.</span></span> <span data-ttu-id="54817-122">**glcolor** a deux variantes majeures : **glcolor3** et **glcolor4**.</span><span class="sxs-lookup"><span data-stu-id="54817-122">**glcolor** has two major variants: **glcolor3** and **glcolor4**.</span></span> <span data-ttu-id="54817-123">les variantes **glcolor3** spécifient les nouvelles valeurs de rouge, de vert et de bleu explicitement et définissent la valeur alpha actuelle sur 1,0 (intensité complète) de manière implicite.</span><span class="sxs-lookup"><span data-stu-id="54817-123">**glcolor3** variants specify new red, green, and blue values explicitly and set the current alpha value to 1.0 (full intensity) implicitly.</span></span> <span data-ttu-id="54817-124">les variantes **glcolor4** spécifient les quatre composants de couleur de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="54817-124">**glcolor4** variants specify all four color components explicitly.</span></span>

<span data-ttu-id="54817-125">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i** et **glcolor4i** prennent trois ou quatre entiers signés Byte, short ou long comme arguments.</span><span class="sxs-lookup"><span data-stu-id="54817-125">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i**, and **glcolor4i** take three or four signed byte, short, or long integers as arguments.</span></span> <span data-ttu-id="54817-126">Quand v est ajouté au nom, les commandes de couleur peuvent prendre un pointeur vers un tableau de telles valeurs.</span><span class="sxs-lookup"><span data-stu-id="54817-126">When v is appended to the name, the color commands can take a pointer to an array of such values.</span></span>

<span data-ttu-id="54817-127">Les valeurs de couleur actuelles sont stockées dans un format à virgule flottante, avec la mantisse et les tailles d’exposant non spécifiées.</span><span class="sxs-lookup"><span data-stu-id="54817-127">Current color values are stored in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="54817-128">Les composants de couleur d’entier non signé, lorsqu’ils sont spécifiés, sont mappés de manière linéaire aux valeurs à virgule flottante, de sorte que la plus grande valeur représentable correspond à 1,0 (intensité complète) et 0 correspond à 0,0 (intensité nulle).</span><span class="sxs-lookup"><span data-stu-id="54817-128">Unsigned integer color components, when specified, are linearly mapped to floating-point values such that the largest representable value maps to 1.0 (full intensity), and 0 maps to 0.0 (zero intensity).</span></span> <span data-ttu-id="54817-129">Les composants de couleur d’entier signé, lorsqu’ils sont spécifiés, sont mappés de manière linéaire aux valeurs à virgule flottante, de sorte que la valeur représentable la plus positive correspond à 1,0, et la valeur représentable la plus négative correspond à-1,0.</span><span class="sxs-lookup"><span data-stu-id="54817-129">Signed integer color components, when specified, are linearly mapped to floating-point values such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="54817-130">(Notez que ce mappage ne convertit pas 0 de manière précise en 0,0.) Les valeurs à virgule flottante sont mappées directement.</span><span class="sxs-lookup"><span data-stu-id="54817-130">(Note that this mapping does not convert 0 precisely to 0.0.) Floating-point values are mapped directly.</span></span>

<span data-ttu-id="54817-131">Ni les valeurs d’entier à virgule flottante ni les valeurs entières signées ne sont ancrées à la plage \[ 0, 1 \] avant la mise à jour de la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="54817-131">Neither floating-point nor signed integer values are clamped to the range \[0,1\] before the current color is updated.</span></span> <span data-ttu-id="54817-132">Toutefois, les composants de couleur sont bloqués dans cette plage avant d’être interpolés ou écrits dans une mémoire tampon de couleur.</span><span class="sxs-lookup"><span data-stu-id="54817-132">However, color components are clamped to this range before they are interpolated or written into a color buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="54817-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54817-133">Requirements</span></span>



| <span data-ttu-id="54817-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54817-134">Requirement</span></span> | <span data-ttu-id="54817-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="54817-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54817-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54817-136">Minimum supported client</span></span><br/> | <span data-ttu-id="54817-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54817-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="54817-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54817-138">Minimum supported server</span></span><br/> | <span data-ttu-id="54817-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54817-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="54817-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="54817-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="54817-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="54817-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="54817-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="54817-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="54817-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54817-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="54817-144">DLL</span><span class="sxs-lookup"><span data-stu-id="54817-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54817-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54817-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54817-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54817-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54817-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="54817-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="54817-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="54817-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="54817-149">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="54817-149">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="54817-150">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="54817-150">**glIndex**</span></span>](glindexd.md)
</dt> </dl>

 

 





