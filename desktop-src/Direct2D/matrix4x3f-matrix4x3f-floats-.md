---
title: Constructeur Matrix4x3F Matrix4x3F (FLOAT, float, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT) (D2d1 \_ Helper. h)
description: Instancie une nouvelle instance d’une classe Matrix4x3F qui est initialisée avec toutes les valeurs de la matrice à virgule flottante.
ms.assetid: 1B4359BD-9B92-4C9F-9FED-49246D45F0E3
keywords:
- Matrix4x3F, constructeur Direct2D
- Matrix4x3F, constructeur Direct2D, interface Matrix4x3F
- Matrix4x3F, interface Direct2D, constructeur Matrix4x3F
topic_type:
- apiref
api_name:
- Matrix4x3F.Matrix4x3F
api_location:
- D2d1.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7858a0d5a6204e3f966205c7cf6dab6e68180524
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844417"
---
# <a name="matrix4x3fmatrix4x3ffloat-float-float-float-float-float-float-float-float-float-float-float-constructor"></a><span data-ttu-id="a0591-106">Constructeur Matrix4x3F :: Matrix4x3F (FLOAT, float, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT)</span><span class="sxs-lookup"><span data-stu-id="a0591-106">Matrix4x3F::Matrix4x3F(FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT) constructor</span></span>

<span data-ttu-id="a0591-107">Instancie une nouvelle instance d’une classe [**Matrix4x3F**](matrix4x3f.md) qui est initialisée avec toutes les valeurs de la matrice à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="a0591-107">Instantiates a new instance of a [**Matrix4x3F**](matrix4x3f.md) class that is initialized with all of the floating point matrix values.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0591-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0591-108">Syntax</span></span>


```C++
inline Matrix4x3F(
   FLOAT m11,
   FLOAT m12,
   FLOAT m13,
   FLOAT m21,
   FLOAT m22,
   FLOAT m23,
   FLOAT m31,
   FLOAT m32,
   FLOAT m33,
   FLOAT m41,
   FLOAT m42,
   FLOAT m43
);
```



## <a name="parameters"></a><span data-ttu-id="a0591-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0591-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0591-110">*m11*</span><span class="sxs-lookup"><span data-stu-id="a0591-110">*m11*</span></span> 
</dt> <dd>

<span data-ttu-id="a0591-111">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="a0591-111">Type: **FLOAT**</span></span>

<span data-ttu-id="a0591-112">Valeur de la première ligne et de la première colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="a0591-112">The value in the first row and first column of the matrix.</span></span>

</dd> <dt>

<span data-ttu-id="a0591-113">*M12*</span><span class="sxs-lookup"><span data-stu-id="a0591-113">*m12*</span></span> 
</dt> <dd>

<span data-ttu-id="a0591-114">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="a0591-114">Type: **FLOAT**</span></span>

<span data-ttu-id="a0591-115">Valeur de la première ligne et de la deuxième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="a0591-115">The value in the first row and second column of the matrix.</span></span>

</dd> <dt>

<span data-ttu-id="a0591-116">*m13*</span><span class="sxs-lookup"><span data-stu-id="a0591-116">*m13*</span></span> 
</dt> <dd>

<span data-ttu-id="a0591-117">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="a0591-117">Type: **FLOAT**</span></span>

<span data-ttu-id="a0591-118">Valeur de la première ligne et de la troisième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="a0591-118">The value in the first row and third column of the matrix.</span></span>

</dd> <dt>

<span data-ttu-id="a0591-119">*m21*</span><span class="sxs-lookup"><span data-stu-id="a0591-119">*m21*</span></span> 
</dt> <dd>

<span data-ttu-id="a0591-120">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="a0591-120">Type: **FLOAT**</span></span>

<span data-ttu-id="a0591-121">Valeur de la deuxième ligne et de la première colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="a0591-121">The value in the second row and first column of the matrix.</span></span>

</dd> <dt>

<span data-ttu-id="a0591-122">*m22*</span><span class="sxs-lookup"><span data-stu-id="a0591-122">*m22*</span></span> 
</dt> <dd>

<span data-ttu-id="a0591-123">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="a0591-123">Type: **FLOAT**</span></span>

<span data-ttu-id="a0591-124">Valeur de la deuxième ligne et de la deuxième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="a0591-124">The value in the second row and second column of the matrix.</span></span>

</dd> <dt>

<span data-ttu-id="a0591-125">*m23*</span><span class="sxs-lookup"><span data-stu-id="a0591-125">*m23*</span></span> 
</dt> <dd>

<span data-ttu-id="a0591-126">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="a0591-126">Type: **FLOAT**</span></span>

<span data-ttu-id="a0591-127">Valeur de la deuxième ligne et de la troisième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="a0591-127">The value in the second row and third column of the matrix.</span></span>

</dd> <dt>

<span data-ttu-id="a0591-128">*m31*</span><span class="sxs-lookup"><span data-stu-id="a0591-128">*m31*</span></span> 
</dt> <dd>

<span data-ttu-id="a0591-129">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="a0591-129">Type: **FLOAT**</span></span>

<span data-ttu-id="a0591-130">Valeur de la troisième ligne et de la première colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="a0591-130">The value in the third row and first column of the matrix.</span></span>

</dd> <dt>

<span data-ttu-id="a0591-131">*m32*</span><span class="sxs-lookup"><span data-stu-id="a0591-131">*m32*</span></span> 
</dt> <dd>

<span data-ttu-id="a0591-132">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="a0591-132">Type: **FLOAT**</span></span>

<span data-ttu-id="a0591-133">Valeur de la troisième ligne et de la deuxième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="a0591-133">The value in the third row and second column of the matrix.</span></span>

</dd> <dt>

<span data-ttu-id="a0591-134">*m33*</span><span class="sxs-lookup"><span data-stu-id="a0591-134">*m33*</span></span> 
</dt> <dd>

<span data-ttu-id="a0591-135">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="a0591-135">Type: **FLOAT**</span></span>

<span data-ttu-id="a0591-136">Valeur de la troisième ligne et de la troisième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="a0591-136">The value in the third row and third column of the matrix.</span></span>

</dd> <dt>

<span data-ttu-id="a0591-137">*m41*</span><span class="sxs-lookup"><span data-stu-id="a0591-137">*m41*</span></span> 
</dt> <dd>

<span data-ttu-id="a0591-138">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="a0591-138">Type: **FLOAT**</span></span>

<span data-ttu-id="a0591-139">Valeur de la quatrième ligne et de la première colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="a0591-139">The value in the fourth row and first column of the matrix.</span></span>

</dd> <dt>

<span data-ttu-id="a0591-140">*m42*</span><span class="sxs-lookup"><span data-stu-id="a0591-140">*m42*</span></span> 
</dt> <dd>

<span data-ttu-id="a0591-141">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="a0591-141">Type: **FLOAT**</span></span>

<span data-ttu-id="a0591-142">Valeur de la quatrième ligne et de la deuxième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="a0591-142">The value in the fourth row and second column of the matrix.</span></span>

</dd> <dt>

<span data-ttu-id="a0591-143">*m43*</span><span class="sxs-lookup"><span data-stu-id="a0591-143">*m43*</span></span> 
</dt> <dd>

<span data-ttu-id="a0591-144">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="a0591-144">Type: **FLOAT**</span></span>

<span data-ttu-id="a0591-145">Valeur de la quatrième ligne et de la troisième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="a0591-145">The value in the fourth row and third column of the matrix.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0591-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0591-146">Requirements</span></span>



| <span data-ttu-id="a0591-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0591-147">Requirement</span></span> | <span data-ttu-id="a0591-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0591-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0591-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0591-149">Minimum supported client</span></span><br/> | <span data-ttu-id="a0591-150">Windows 7, Windows Vista avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Vista \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0591-150">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a0591-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0591-151">Minimum supported server</span></span><br/> | <span data-ttu-id="a0591-152">Windows Server 2008 R2, Windows Server 2008 avec SP2 et mise à jour de plateforme pour les applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0591-152">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a0591-153">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0591-153">Minimum supported phone</span></span><br/>  | <span data-ttu-id="a0591-154">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="a0591-154">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                           |
| <span data-ttu-id="a0591-155">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a0591-155">Namespace</span></span><br/>                | <span data-ttu-id="a0591-156">D2D1</span><span class="sxs-lookup"><span data-stu-id="a0591-156">D2D1</span></span><br/>                                                                                                                   |
| <span data-ttu-id="a0591-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="a0591-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0591-158"><dt>D2d1 \_ Helper. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0591-158"><dt>D2d1\_helper.h</dt></span></span> </dl>                                         |
| <span data-ttu-id="a0591-159">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a0591-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="a0591-160"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0591-160"><dt>D2d1.lib</dt></span></span> </dl>                                               |
| <span data-ttu-id="a0591-161">DLL</span><span class="sxs-lookup"><span data-stu-id="a0591-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0591-162"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0591-162"><dt>D2d1.dll</dt></span></span> </dl>                                               |



## <a name="see-also"></a><span data-ttu-id="a0591-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0591-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0591-164">**Matrix4x3F**</span><span class="sxs-lookup"><span data-stu-id="a0591-164">**Matrix4x3F**</span></span>](matrix4x3f.md)
</dt> </dl>

 

 





