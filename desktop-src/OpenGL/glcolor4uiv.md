---
title: fonction glColor4uiv (GL. h)
description: Définit la couleur actuelle à partir d’un tableau de valeurs de couleur déjà existant. | fonction glColor4uiv (GL. h)
ms.assetid: de21116b-50f6-4a80-8fa1-e8cf6e4978e9
keywords:
- glColor4uiv fonction OpenGL
topic_type:
- apiref
api_name:
- glColor4uiv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2acc9a413436b4d6b6fad4ca175aa74821ad2dbe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953544"
---
# <a name="glcolor4uiv-function"></a><span data-ttu-id="032d2-105">glColor4uiv fonction)</span><span class="sxs-lookup"><span data-stu-id="032d2-105">glColor4uiv function</span></span>

<span data-ttu-id="032d2-106">Définit la couleur actuelle à partir d’un tableau de valeurs de couleur déjà existant.</span><span class="sxs-lookup"><span data-stu-id="032d2-106">Sets the current color from an already existing array of color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="032d2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="032d2-107">Syntax</span></span>


```C++
void WINAPI glColor4uiv(
   const GLuint *v
);
```



## <a name="parameters"></a><span data-ttu-id="032d2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="032d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="032d2-109">*v*</span><span class="sxs-lookup"><span data-stu-id="032d2-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="032d2-110">Pointeur vers un tableau qui contient les valeurs rouge, vert, bleu et alpha.</span><span class="sxs-lookup"><span data-stu-id="032d2-110">A pointer to an array that contains red, green, blue, and alpha values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="032d2-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="032d2-111">Return value</span></span>

<span data-ttu-id="032d2-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="032d2-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="032d2-113">Notes</span><span class="sxs-lookup"><span data-stu-id="032d2-113">Remarks</span></span>

<span data-ttu-id="032d2-114">Le GL stocke à la fois un index de couleurs à valeur unique actuel et une couleur RVBA à quatre valeurs actuelle.</span><span class="sxs-lookup"><span data-stu-id="032d2-114">The GL stores both a current single-valued color index and a current four-valued RGBA color.</span></span> <span data-ttu-id="032d2-115">**glcolor** définit une nouvelle couleur RVBA à quatre valeurs.</span><span class="sxs-lookup"><span data-stu-id="032d2-115">**glcolor** sets a new four-valued RGBA color.</span></span> <span data-ttu-id="032d2-116">**glcolor** a deux variantes majeures : **glcolor3** et **glcolor4**.</span><span class="sxs-lookup"><span data-stu-id="032d2-116">**glcolor** has two major variants: **glcolor3** and **glcolor4**.</span></span> <span data-ttu-id="032d2-117">les variantes **glcolor3** spécifient les nouvelles valeurs de rouge, de vert et de bleu explicitement et définissent la valeur alpha actuelle sur 1,0 (intensité complète) de manière implicite.</span><span class="sxs-lookup"><span data-stu-id="032d2-117">**glcolor3** variants specify new red, green, and blue values explicitly and set the current alpha value to 1.0 (full intensity) implicitly.</span></span> <span data-ttu-id="032d2-118">les variantes **glcolor4** spécifient les quatre composants de couleur de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="032d2-118">**glcolor4** variants specify all four color components explicitly.</span></span>

<span data-ttu-id="032d2-119">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i** et **glcolor4i** prennent trois ou quatre entiers signés Byte, short ou long comme arguments.</span><span class="sxs-lookup"><span data-stu-id="032d2-119">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i**, and **glcolor4i** take three or four signed byte, short, or long integers as arguments.</span></span> <span data-ttu-id="032d2-120">Quand v est ajouté au nom, les commandes de couleur peuvent prendre un pointeur vers un tableau de telles valeurs.</span><span class="sxs-lookup"><span data-stu-id="032d2-120">When v is appended to the name, the color commands can take a pointer to an array of such values.</span></span>

<span data-ttu-id="032d2-121">Les valeurs de couleur actuelles sont stockées dans un format à virgule flottante, avec la mantisse et les tailles d’exposant non spécifiées.</span><span class="sxs-lookup"><span data-stu-id="032d2-121">Current color values are stored in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="032d2-122">Les composants de couleur d’entier non signé, lorsqu’ils sont spécifiés, sont mappés de manière linéaire aux valeurs à virgule flottante, de sorte que la plus grande valeur représentable correspond à 1,0 (intensité complète) et 0 correspond à 0,0 (intensité nulle).</span><span class="sxs-lookup"><span data-stu-id="032d2-122">Unsigned integer color components, when specified, are linearly mapped to floating-point values such that the largest representable value maps to 1.0 (full intensity), and 0 maps to 0.0 (zero intensity).</span></span> <span data-ttu-id="032d2-123">Les composants de couleur d’entier signé, lorsqu’ils sont spécifiés, sont mappés de manière linéaire aux valeurs à virgule flottante, de sorte que la valeur représentable la plus positive correspond à 1,0, et la valeur représentable la plus négative correspond à-1,0.</span><span class="sxs-lookup"><span data-stu-id="032d2-123">Signed integer color components, when specified, are linearly mapped to floating-point values such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="032d2-124">(Notez que ce mappage ne convertit pas 0 de manière précise en 0,0.) Les valeurs à virgule flottante sont mappées directement.</span><span class="sxs-lookup"><span data-stu-id="032d2-124">(Note that this mapping does not convert 0 precisely to 0.0.) Floating-point values are mapped directly.</span></span>

<span data-ttu-id="032d2-125">Ni les valeurs d’entier à virgule flottante ni les valeurs entières signées ne sont ancrées à la plage \[ 0, 1 \] avant la mise à jour de la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="032d2-125">Neither floating-point nor signed integer values are clamped to the range \[0,1\] before the current color is updated.</span></span> <span data-ttu-id="032d2-126">Toutefois, les composants de couleur sont bloqués dans cette plage avant d’être interpolés ou écrits dans une mémoire tampon de couleur.</span><span class="sxs-lookup"><span data-stu-id="032d2-126">However, color components are clamped to this range before they are interpolated or written into a color buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="032d2-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="032d2-127">Requirements</span></span>



| <span data-ttu-id="032d2-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="032d2-128">Requirement</span></span> | <span data-ttu-id="032d2-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="032d2-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="032d2-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="032d2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="032d2-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="032d2-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="032d2-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="032d2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="032d2-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="032d2-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="032d2-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="032d2-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="032d2-135"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="032d2-135"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="032d2-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="032d2-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="032d2-137"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="032d2-137"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="032d2-138">DLL</span><span class="sxs-lookup"><span data-stu-id="032d2-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="032d2-139"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="032d2-139"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="032d2-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="032d2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="032d2-141">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="032d2-141">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="032d2-142">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="032d2-142">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="032d2-143">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="032d2-143">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="032d2-144">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="032d2-144">**glIndex**</span></span>](glindexd.md)
</dt> </dl>

 

 





