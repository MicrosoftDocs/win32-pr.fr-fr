---
title: fonction glGetTexEnviv (GL. h)
description: Les fonctions glGetTexEnvfv et glGetTexEnviv retournent les paramètres d’environnement de texture. | fonction glGetTexEnviv (GL. h)
ms.assetid: c1429cb9-4392-41ef-a978-a51db66445f2
keywords:
- glGetTexEnviv fonction OpenGL
topic_type:
- apiref
api_name:
- glGetTexEnviv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ff222b7de0bfcd5fa50e9fa5f260e329c60c69d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106524812"
---
# <a name="glgettexenviv-function"></a><span data-ttu-id="9448f-105">glGetTexEnviv fonction)</span><span class="sxs-lookup"><span data-stu-id="9448f-105">glGetTexEnviv function</span></span>

<span data-ttu-id="9448f-106">Les fonctions [**glGetTexEnvfv**](glgettexenvfv.md) et **glGetTexEnviv** retournent les paramètres d’environnement de texture.</span><span class="sxs-lookup"><span data-stu-id="9448f-106">The [**glGetTexEnvfv**](glgettexenvfv.md) and **glGetTexEnviv** functions return texture environment parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="9448f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9448f-107">Syntax</span></span>


```C++
void WINAPI glGetTexEnviv(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="9448f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9448f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9448f-109">*cible*</span><span class="sxs-lookup"><span data-stu-id="9448f-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="9448f-110">Environnement de texture.</span><span class="sxs-lookup"><span data-stu-id="9448f-110">A texture environment.</span></span> <span data-ttu-id="9448f-111">Doit être une \_ texture GL \_ env.</span><span class="sxs-lookup"><span data-stu-id="9448f-111">Must be GL\_TEXTURE\_ENV.</span></span>

</dd> <dt>

<span data-ttu-id="9448f-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="9448f-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="9448f-113">Nom symbolique d’un paramètre d’environnement de texture.</span><span class="sxs-lookup"><span data-stu-id="9448f-113">The symbolic name of a texture environment parameter.</span></span> <span data-ttu-id="9448f-114">Les valeurs suivantes sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="9448f-114">The following values are accepted.</span></span>



| <span data-ttu-id="9448f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="9448f-115">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="9448f-116">Signification</span><span class="sxs-lookup"><span data-stu-id="9448f-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span><dl> <span data-ttu-id="9448f-117"><dt>**\_ \_ mode env de la texture GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9448f-117"><dt>**GL\_TEXTURE\_ENV\_MODE**</dt></span></span> </dl>    | <span data-ttu-id="9448f-118">Le paramètre *params* retourne le mode d’environnement de texture à valeur unique, une constante symbolique.</span><span class="sxs-lookup"><span data-stu-id="9448f-118">The *params* parameter returns the single-valued texture environment mode, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                           |
| <span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span><dl> <span data-ttu-id="9448f-119"><dt>**couleur de la texture du GL \_ \_ env \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9448f-119"><dt>**GL\_TEXTURE\_ENV\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="9448f-120">Le paramètre *params* retourne quatre valeurs entières ou à virgule flottante qui sont la couleur de l’environnement de texture.</span><span class="sxs-lookup"><span data-stu-id="9448f-120">The *params* parameter returns four integer or floating-point values that are the texture environment color.</span></span> <span data-ttu-id="9448f-121">Les valeurs entières, quand elles sont demandées, sont mappées de façon linéaire à partir de la représentation interne à virgule flottante, de sorte que 1,0 correspond à l’entier pouvant être représenté le plus positif, et-1,0 correspond à l’entier représentable le plus négatif.</span><span class="sxs-lookup"><span data-stu-id="9448f-121">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer, and -1.0 maps to the most negative representable integer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9448f-122">*params*</span><span class="sxs-lookup"><span data-stu-id="9448f-122">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="9448f-123">Retourne les données demandées.</span><span class="sxs-lookup"><span data-stu-id="9448f-123">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9448f-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9448f-124">Return value</span></span>

<span data-ttu-id="9448f-125">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9448f-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9448f-126">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="9448f-126">Error codes</span></span>

<span data-ttu-id="9448f-127">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="9448f-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9448f-128">Nom</span><span class="sxs-lookup"><span data-stu-id="9448f-128">Name</span></span>                                                                                                  | <span data-ttu-id="9448f-129">Signification</span><span class="sxs-lookup"><span data-stu-id="9448f-129">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9448f-130"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9448f-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="9448f-131">*target* ou *pname* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="9448f-131">*target* or *pname* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="9448f-132"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9448f-132"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9448f-133">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="9448f-133">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9448f-134">Notes</span><span class="sxs-lookup"><span data-stu-id="9448f-134">Remarks</span></span>

<span data-ttu-id="9448f-135">La fonction **glGetTexEnv** retourne dans *params* les valeurs sélectionnées d’un environnement de texture qui a été spécifié avec [**glTexEnv**](gltexenv-functions.md).</span><span class="sxs-lookup"><span data-stu-id="9448f-135">The **glGetTexEnv** function returns in *params* selected values of a texture environment that was specified with [**glTexEnv**](gltexenv-functions.md).</span></span> <span data-ttu-id="9448f-136">Le paramètre *target* spécifie un environnement de texture.</span><span class="sxs-lookup"><span data-stu-id="9448f-136">The *target* parameter specifies a texture environment.</span></span> <span data-ttu-id="9448f-137">Actuellement, un seul environnement de texture est défini et pris en charge : la \_ texture GL \_ env.</span><span class="sxs-lookup"><span data-stu-id="9448f-137">Currently, only one texture environment is defined and supported: GL\_TEXTURE\_ENV.</span></span>

<span data-ttu-id="9448f-138">Le paramètre *pname* désigne un paramètre d’environnement de texture spécifique.</span><span class="sxs-lookup"><span data-stu-id="9448f-138">The *pname* parameter names a specific texture environment parameter.</span></span>

<span data-ttu-id="9448f-139">Si une erreur est générée, aucune modification n’est apportée au contenu des *paramètres*.</span><span class="sxs-lookup"><span data-stu-id="9448f-139">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="9448f-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9448f-140">Requirements</span></span>



| <span data-ttu-id="9448f-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9448f-141">Requirement</span></span> | <span data-ttu-id="9448f-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="9448f-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9448f-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9448f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="9448f-144">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9448f-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9448f-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9448f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="9448f-146">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9448f-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9448f-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="9448f-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="9448f-148"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9448f-148"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9448f-149">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9448f-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="9448f-150"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9448f-150"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9448f-151">DLL</span><span class="sxs-lookup"><span data-stu-id="9448f-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9448f-152"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9448f-152"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9448f-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9448f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9448f-154">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9448f-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9448f-155">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="9448f-155">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9448f-156">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="9448f-156">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> </dl>

 

 





