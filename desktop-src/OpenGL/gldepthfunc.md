---
title: fonction glDepthFunc (GL. h)
description: La fonction glDepthFunc spécifie la valeur utilisée pour les comparaisons de mémoire tampon de profondeur.
ms.assetid: 6ab8774a-8887-4c1e-b567-4492c0a60cf2
keywords:
- glDepthFunc fonction OpenGL
topic_type:
- apiref
api_name:
- glDepthFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dec5130edb0b8ef30af1397be501fa9cd5d5744
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464726"
---
# <a name="gldepthfunc-function"></a><span data-ttu-id="afdc5-104">glDepthFunc fonction)</span><span class="sxs-lookup"><span data-stu-id="afdc5-104">glDepthFunc function</span></span>

<span data-ttu-id="afdc5-105">La fonction **glDepthFunc** spécifie la valeur utilisée pour les comparaisons de mémoire tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="afdc5-105">The **glDepthFunc** function specifies the value used for depth-buffer comparisons.</span></span>

## <a name="syntax"></a><span data-ttu-id="afdc5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="afdc5-106">Syntax</span></span>


```C++
void WINAPI glDepthFunc(
   GLenum func
);
```



## <a name="parameters"></a><span data-ttu-id="afdc5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="afdc5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afdc5-108">*func*</span><span class="sxs-lookup"><span data-stu-id="afdc5-108">*func*</span></span> 
</dt> <dd>

<span data-ttu-id="afdc5-109">Spécifie la fonction de comparaison de profondeur.</span><span class="sxs-lookup"><span data-stu-id="afdc5-109">Specifies the depth-comparison function.</span></span> <span data-ttu-id="afdc5-110">Les constantes symboliques suivantes sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="afdc5-110">The following symbolic constants are accepted.</span></span>



| <span data-ttu-id="afdc5-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="afdc5-111">Value</span></span>                                                                                                                                                   | <span data-ttu-id="afdc5-112">Signification</span><span class="sxs-lookup"><span data-stu-id="afdc5-112">Meaning</span></span>                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <span data-ttu-id="afdc5-113"><dt>**GL \_ jamais**</dt></span><span class="sxs-lookup"><span data-stu-id="afdc5-113"><dt>**GL\_NEVER**</dt></span></span> </dl>          | <span data-ttu-id="afdc5-114">Ne passe jamais.</span><span class="sxs-lookup"><span data-stu-id="afdc5-114">Never passes.</span></span><br/>                                                                                  |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <span data-ttu-id="afdc5-115"><dt>**GL \_ moins**</dt></span><span class="sxs-lookup"><span data-stu-id="afdc5-115"><dt>**GL\_LESS**</dt></span></span> </dl>             | <span data-ttu-id="afdc5-116">Passe si la valeur *z* entrante est inférieure à la valeur *z* stockée.</span><span class="sxs-lookup"><span data-stu-id="afdc5-116">Passes if the incoming *z* value is less than the stored *z* value.</span></span> <span data-ttu-id="afdc5-117">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="afdc5-117">This is the default value.</span></span><br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <span data-ttu-id="afdc5-118"><dt>**\_LEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="afdc5-118"><dt>**GL\_LEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="afdc5-119">Passe si la valeur z entrante est inférieure ou égale à la valeur z stockée.</span><span class="sxs-lookup"><span data-stu-id="afdc5-119">Passes if the incoming z value is less than or equal to the stored z value.</span></span><br/>                    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <span data-ttu-id="afdc5-120"><dt>**GL \_ égal**</dt></span><span class="sxs-lookup"><span data-stu-id="afdc5-120"><dt>**GL\_EQUAL**</dt></span></span> </dl>          | <span data-ttu-id="afdc5-121">Passe si la valeur z entrante est égale à la valeur z stockée.</span><span class="sxs-lookup"><span data-stu-id="afdc5-121">Passes if the incoming z value is equal to the stored z value.</span></span><br/>                                 |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <span data-ttu-id="afdc5-122"><dt>**GL \_ supérieur**</dt></span><span class="sxs-lookup"><span data-stu-id="afdc5-122"><dt>**GL\_GREATER**</dt></span></span> </dl>    | <span data-ttu-id="afdc5-123">Passe si la valeur z entrante est supérieure à la valeur z stockée.</span><span class="sxs-lookup"><span data-stu-id="afdc5-123">Passes if the incoming z value is greater than the stored z value.</span></span><br/>                             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <span data-ttu-id="afdc5-124"><dt>**\_NOTEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="afdc5-124"><dt>**GL\_NOTEQUAL**</dt></span></span> </dl> | <span data-ttu-id="afdc5-125">Passe si la valeur z entrante n’est pas égale à la valeur z stockée.</span><span class="sxs-lookup"><span data-stu-id="afdc5-125">Passes if the incoming z value is not equal to the stored z value.</span></span><br/>                             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <span data-ttu-id="afdc5-126"><dt>**\_GEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="afdc5-126"><dt>**GL\_GEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="afdc5-127">Passe si la valeur z entrante est supérieure ou égale à la valeur z stockée.</span><span class="sxs-lookup"><span data-stu-id="afdc5-127">Passes if the incoming z value is greater than or equal to the stored z value.</span></span><br/>                 |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <span data-ttu-id="afdc5-128"><dt>**\_toujours GL**</dt></span><span class="sxs-lookup"><span data-stu-id="afdc5-128"><dt>**GL\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="afdc5-129">Passe toujours.</span><span class="sxs-lookup"><span data-stu-id="afdc5-129">Always passes.</span></span><br/>                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afdc5-130">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="afdc5-130">Return value</span></span>

<span data-ttu-id="afdc5-131">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="afdc5-131">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="afdc5-132">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="afdc5-132">Error codes</span></span>

<span data-ttu-id="afdc5-133">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="afdc5-133">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="afdc5-134">Nom</span><span class="sxs-lookup"><span data-stu-id="afdc5-134">Name</span></span>                                                                                                  | <span data-ttu-id="afdc5-135">Signification</span><span class="sxs-lookup"><span data-stu-id="afdc5-135">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="afdc5-136"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="afdc5-136"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="afdc5-137">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="afdc5-137">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="afdc5-138">Notes</span><span class="sxs-lookup"><span data-stu-id="afdc5-138">Remarks</span></span>

<span data-ttu-id="afdc5-139">La fonction **glDepthFunc** spécifie la fonction utilisée pour comparer chaque valeur *z* de pixel entrante avec la valeur *z* présente dans la mémoire tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="afdc5-139">The **glDepthFunc** function specifies the function used to compare each incoming pixel *z* value with the *z* value present in the depth buffer.</span></span> <span data-ttu-id="afdc5-140">La comparaison est effectuée uniquement si le test de profondeur est activé.</span><span class="sxs-lookup"><span data-stu-id="afdc5-140">The comparison is performed only if depth testing is enabled.</span></span> <span data-ttu-id="afdc5-141">(Voir [**glEnable**](glenable.md) avec l’argument GL \_ TEST de profondeur \_ .)</span><span class="sxs-lookup"><span data-stu-id="afdc5-141">(See [**glEnable**](glenable.md) with the argument GL\_DEPTH\_TEST.)</span></span>

<span data-ttu-id="afdc5-142">Au départ, le test de profondeur est désactivé.</span><span class="sxs-lookup"><span data-stu-id="afdc5-142">Initially, depth testing is disabled.</span></span>

<span data-ttu-id="afdc5-143">Les fonctions suivantes récupèrent les informations relatives à **glDepthFunc**:</span><span class="sxs-lookup"><span data-stu-id="afdc5-143">The following functions retrieve information related to **glDepthFunc**:</span></span>

<span data-ttu-id="afdc5-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ profondeur \_ Func</span><span class="sxs-lookup"><span data-stu-id="afdc5-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DEPTH\_FUNC</span></span>

<span data-ttu-id="afdc5-145">[**glIsEnabled**](glisenabled.md) avec argument de profondeur du GL d’arguments \_ \_</span><span class="sxs-lookup"><span data-stu-id="afdc5-145">[**glIsEnabled**](glisenabled.md) with argument GL\_DEPTH\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="afdc5-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="afdc5-146">Requirements</span></span>



| <span data-ttu-id="afdc5-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="afdc5-147">Requirement</span></span> | <span data-ttu-id="afdc5-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="afdc5-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="afdc5-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="afdc5-149">Minimum supported client</span></span><br/> | <span data-ttu-id="afdc5-150">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="afdc5-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="afdc5-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="afdc5-151">Minimum supported server</span></span><br/> | <span data-ttu-id="afdc5-152">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="afdc5-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="afdc5-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="afdc5-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="afdc5-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="afdc5-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="afdc5-155">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="afdc5-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="afdc5-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="afdc5-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="afdc5-157">DLL</span><span class="sxs-lookup"><span data-stu-id="afdc5-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afdc5-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afdc5-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afdc5-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="afdc5-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afdc5-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="afdc5-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="afdc5-161">**glDepthRange**</span><span class="sxs-lookup"><span data-stu-id="afdc5-161">**glDepthRange**</span></span>](gldepthrange.md)
</dt> <dt>

[<span data-ttu-id="afdc5-162">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="afdc5-162">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="afdc5-163">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="afdc5-163">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="afdc5-164">**glGet**</span><span class="sxs-lookup"><span data-stu-id="afdc5-164">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="afdc5-165">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="afdc5-165">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





