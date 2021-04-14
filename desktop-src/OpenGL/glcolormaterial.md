---
title: fonction glColorMaterial (GL. h)
description: La fonction glColorMaterial fait en sorte qu’une couleur matérielle effectue le suivi de la couleur actuelle.
ms.assetid: 6dbef2c2-f902-4f25-8a87-9e3d710dd807
keywords:
- glColorMaterial fonction OpenGL
topic_type:
- apiref
api_name:
- glColorMaterial
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32823eaa82e6a260790dd6fa23747f2b4228649
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384823"
---
# <a name="glcolormaterial-function"></a><span data-ttu-id="e7f7c-104">glColorMaterial fonction)</span><span class="sxs-lookup"><span data-stu-id="e7f7c-104">glColorMaterial function</span></span>

<span data-ttu-id="e7f7c-105">La fonction **glColorMaterial** fait en sorte qu’une couleur matérielle effectue le suivi de la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="e7f7c-105">The **glColorMaterial** function causes a material color to track the current color.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7f7c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7f7c-106">Syntax</span></span>


```C++
void WINAPI glColorMaterial(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="e7f7c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7f7c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7f7c-108">*se*</span><span class="sxs-lookup"><span data-stu-id="e7f7c-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="e7f7c-109">Spécifie si les paramètres front, back ou les deux paramètres de matériau avant et arrière doivent suivre la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="e7f7c-109">Specifies whether front, back, or both front and back material parameters should track the current color.</span></span> <span data-ttu-id="e7f7c-110">Les valeurs acceptées sont le front GL, l’arrière-plan \_ GL et le \_ \_ recto \_ et l’arrière GL \_ .</span><span class="sxs-lookup"><span data-stu-id="e7f7c-110">Accepted values are GL\_FRONT, GL\_BACK, and GL\_FRONT\_AND\_BACK.</span></span> <span data-ttu-id="e7f7c-111">La valeur par défaut est \_ recto-verso (GL) \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e7f7c-111">The default value is GL\_FRONT\_AND\_BACK.</span></span>

</dd> <dt>

<span data-ttu-id="e7f7c-112">*mode*</span><span class="sxs-lookup"><span data-stu-id="e7f7c-112">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="e7f7c-113">Spécifie quels paramètres de matériau effectuent le suivi de la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="e7f7c-113">Specifies which of several material parameters track the current color.</span></span> <span data-ttu-id="e7f7c-114">Les valeurs acceptées sont les \_ émissions GL, le GL \_ ambiant, la \_ diffusion GL, la spéculation générale du GL et l' \_ \_ ambiant et la diffusion du GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e7f7c-114">Accepted values are GL\_EMISSION, GL\_AMBIENT, GL\_DIFFUSE, GL\_SPECULAR, and GL\_AMBIENT\_AND\_DIFFUSE.</span></span> <span data-ttu-id="e7f7c-115">La valeur par défaut est \_ ambiant \_ et \_ diffuse du GL.</span><span class="sxs-lookup"><span data-stu-id="e7f7c-115">The default value is GL\_AMBIENT\_AND\_DIFFUSE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7f7c-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e7f7c-116">Return value</span></span>

<span data-ttu-id="e7f7c-117">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e7f7c-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e7f7c-118">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="e7f7c-118">Error codes</span></span>

<span data-ttu-id="e7f7c-119">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="e7f7c-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e7f7c-120">Nom</span><span class="sxs-lookup"><span data-stu-id="e7f7c-120">Name</span></span>                                                                                                  | <span data-ttu-id="e7f7c-121">Signification</span><span class="sxs-lookup"><span data-stu-id="e7f7c-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e7f7c-122"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e7f7c-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="e7f7c-123">la *face* ou le *mode* n’était pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="e7f7c-123">*face* or *mode* was not an accepted value.</span></span><br/>                                                                                |
| <dl> <span data-ttu-id="e7f7c-124"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e7f7c-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e7f7c-125">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="e7f7c-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e7f7c-126">Notes</span><span class="sxs-lookup"><span data-stu-id="e7f7c-126">Remarks</span></span>

<span data-ttu-id="e7f7c-127">La fonction **glColorMaterial** spécifie les paramètres de matière qui effectuent le suivi de la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="e7f7c-127">The **glColorMaterial** function specifies which material parameters track the current color.</span></span> <span data-ttu-id="e7f7c-128">Lorsque vous activez le \_ \_ matériel de couleur GL, pour chacun des matériaux ou matériaux spécifiés par *visage*, le ou les paramètres du matériau spécifiés par le *mode* suivent à tout moment la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="e7f7c-128">When you enable GL\_COLOR\_MATERIAL, for each of the material or materials specified by *face*, the material parameter or parameters specified by *mode* track the current color at all times.</span></span> <span data-ttu-id="e7f7c-129">Activez et désactivez \_ \_ le matériel de couleur GL avec les fonctions [**glEnable**](glenable.md) et [**glDisable**](gldisable.md), que vous appelez avec la documentation de \_ couleur GL \_ comme argument.</span><span class="sxs-lookup"><span data-stu-id="e7f7c-129">Enable and disable GL\_COLOR\_MATERIAL with the functions [**glEnable**](glenable.md) and [**glDisable**](gldisable.md), which you call with GL\_COLOR\_MATERIAL as their argument.</span></span> <span data-ttu-id="e7f7c-130">Par défaut, le \_ matériel de couleur de GL \_ est désactivé.</span><span class="sxs-lookup"><span data-stu-id="e7f7c-130">By default, GL\_COLOR\_MATERIAL is disabled.</span></span>

<span data-ttu-id="e7f7c-131">Avec **glColorMaterial**, vous pouvez modifier un sous-ensemble de paramètres de matériau pour chaque vertex en utilisant uniquement la fonction [**glColor**](glcolor-functions.md) , sans appeler [**glMaterial**](glmaterial-functions.md).</span><span class="sxs-lookup"><span data-stu-id="e7f7c-131">With **glColorMaterial**, you can change a subset of material parameters for each vertex using only the [**glColor**](glcolor-functions.md) function, without calling [**glMaterial**](glmaterial-functions.md).</span></span> <span data-ttu-id="e7f7c-132">Si vous ne spécifiez qu’un seul sous-ensemble de paramètres pour chaque vertex, il est préférable de le faire avec **glColorMaterial** qu’avec **glMaterial**.</span><span class="sxs-lookup"><span data-stu-id="e7f7c-132">If you are going to specify only such a subset of parameters for each vertex, it is better to do so with **glColorMaterial** than with **glMaterial**.</span></span>

<span data-ttu-id="e7f7c-133">Les fonctions suivantes récupèrent les informations relatives à **glColorMaterial**:</span><span class="sxs-lookup"><span data-stu-id="e7f7c-133">The following functions retrieve information related to **glColorMaterial**:</span></span>

<span data-ttu-id="e7f7c-134">[**paramètre glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Color \_ Material \_</span><span class="sxs-lookup"><span data-stu-id="e7f7c-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_COLOR\_MATERIAL\_PARAMETER</span></span>

<span data-ttu-id="e7f7c-135">**glGet** avec argument \_ mat couleur de la comptabilité \_ \_</span><span class="sxs-lookup"><span data-stu-id="e7f7c-135">**glGet** with argument GL\_COLOR\_MATERIAL\_FACE</span></span>

<span data-ttu-id="e7f7c-136">[**glIsEnabled**](glisenabled.md) avec argument de couleur de GL d’argument \_ \_</span><span class="sxs-lookup"><span data-stu-id="e7f7c-136">[**glIsEnabled**](glisenabled.md) with argument GL\_COLOR\_MATERIAL</span></span>

## <a name="requirements"></a><span data-ttu-id="e7f7c-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7f7c-137">Requirements</span></span>



| <span data-ttu-id="e7f7c-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7f7c-138">Requirement</span></span> | <span data-ttu-id="e7f7c-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7f7c-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7f7c-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7f7c-140">Minimum supported client</span></span><br/> | <span data-ttu-id="e7f7c-141">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7f7c-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e7f7c-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7f7c-142">Minimum supported server</span></span><br/> | <span data-ttu-id="e7f7c-143">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7f7c-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e7f7c-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7f7c-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7f7c-145"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7f7c-145"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e7f7c-146">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e7f7c-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="e7f7c-147"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7f7c-147"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e7f7c-148">DLL</span><span class="sxs-lookup"><span data-stu-id="e7f7c-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7f7c-149"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7f7c-149"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7f7c-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7f7c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7f7c-151">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e7f7c-151">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e7f7c-152">**glColor**</span><span class="sxs-lookup"><span data-stu-id="e7f7c-152">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="e7f7c-153">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="e7f7c-153">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="e7f7c-154">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="e7f7c-154">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="e7f7c-155">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e7f7c-155">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e7f7c-156">**glGet**</span><span class="sxs-lookup"><span data-stu-id="e7f7c-156">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="e7f7c-157">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="e7f7c-157">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="e7f7c-158">**glLight**</span><span class="sxs-lookup"><span data-stu-id="e7f7c-158">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="e7f7c-159">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="e7f7c-159">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="e7f7c-160">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="e7f7c-160">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





