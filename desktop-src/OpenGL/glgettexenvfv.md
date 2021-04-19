---
title: fonction glGetTexEnvfv (GL. h)
description: Les fonctions glGetTexEnvfv et glGetTexEnviv retournent les paramètres d’environnement de texture. | fonction glGetTexEnvfv (GL. h)
ms.assetid: aa037494-e227-48f1-8d5e-9f82073dc2ea
keywords:
- glGetTexEnvfv fonction OpenGL
topic_type:
- apiref
api_name:
- glGetTexEnvfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36d542461b05a824c78bbad82d843735289f2fb4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522302"
---
# <a name="glgettexenvfv-function"></a><span data-ttu-id="5a8db-105">glGetTexEnvfv fonction)</span><span class="sxs-lookup"><span data-stu-id="5a8db-105">glGetTexEnvfv function</span></span>

<span data-ttu-id="5a8db-106">Les fonctions **glGetTexEnvfv** et [**glGetTexEnviv**](glgettexenviv.md) retournent les paramètres d’environnement de texture.</span><span class="sxs-lookup"><span data-stu-id="5a8db-106">The **glGetTexEnvfv** and [**glGetTexEnviv**](glgettexenviv.md) functions return texture environment parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a8db-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a8db-107">Syntax</span></span>


```C++
void WINAPI glGetTexEnvfv(
   GLenum  target,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="5a8db-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a8db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a8db-109">*cible*</span><span class="sxs-lookup"><span data-stu-id="5a8db-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="5a8db-110">Environnement de texture.</span><span class="sxs-lookup"><span data-stu-id="5a8db-110">A texture environment.</span></span> <span data-ttu-id="5a8db-111">Doit être une \_ texture GL \_ env.</span><span class="sxs-lookup"><span data-stu-id="5a8db-111">Must be GL\_TEXTURE\_ENV.</span></span>

</dd> <dt>

<span data-ttu-id="5a8db-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="5a8db-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="5a8db-113">Nom symbolique d’un paramètre d’environnement de texture.</span><span class="sxs-lookup"><span data-stu-id="5a8db-113">The symbolic name of a texture environment parameter.</span></span> <span data-ttu-id="5a8db-114">Les valeurs suivantes sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="5a8db-114">The following values are accepted.</span></span>



| <span data-ttu-id="5a8db-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a8db-115">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="5a8db-116">Signification</span><span class="sxs-lookup"><span data-stu-id="5a8db-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span><dl> <span data-ttu-id="5a8db-117"><dt>**\_ \_ mode env de la texture GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5a8db-117"><dt>**GL\_TEXTURE\_ENV\_MODE**</dt></span></span> </dl>    | <span data-ttu-id="5a8db-118">Le paramètre *params* retourne le mode d’environnement de texture à valeur unique, une constante symbolique.</span><span class="sxs-lookup"><span data-stu-id="5a8db-118">The *params* parameter returns the single-valued texture environment mode, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                           |
| <span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span><dl> <span data-ttu-id="5a8db-119"><dt>**couleur de la texture du GL \_ \_ env \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5a8db-119"><dt>**GL\_TEXTURE\_ENV\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="5a8db-120">Le paramètre *params* retourne quatre valeurs entières ou à virgule flottante qui sont la couleur de l’environnement de texture.</span><span class="sxs-lookup"><span data-stu-id="5a8db-120">The *params* parameter returns four integer or floating-point values that are the texture environment color.</span></span> <span data-ttu-id="5a8db-121">Les valeurs entières, quand elles sont demandées, sont mappées de façon linéaire à partir de la représentation interne à virgule flottante, de sorte que 1,0 correspond à l’entier pouvant être représenté le plus positif, et-1,0 correspond à l’entier représentable le plus négatif.</span><span class="sxs-lookup"><span data-stu-id="5a8db-121">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer, and -1.0 maps to the most negative representable integer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5a8db-122">*params*</span><span class="sxs-lookup"><span data-stu-id="5a8db-122">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="5a8db-123">Retourne les données demandées.</span><span class="sxs-lookup"><span data-stu-id="5a8db-123">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a8db-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5a8db-124">Return value</span></span>

<span data-ttu-id="5a8db-125">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5a8db-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5a8db-126">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="5a8db-126">Error codes</span></span>

<span data-ttu-id="5a8db-127">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="5a8db-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5a8db-128">Nom</span><span class="sxs-lookup"><span data-stu-id="5a8db-128">Name</span></span>                                                                                                  | <span data-ttu-id="5a8db-129">Signification</span><span class="sxs-lookup"><span data-stu-id="5a8db-129">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5a8db-130"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5a8db-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="5a8db-131">*target* ou *pname* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="5a8db-131">*target* or *pname* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="5a8db-132"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5a8db-132"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="5a8db-133">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="5a8db-133">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5a8db-134">Notes</span><span class="sxs-lookup"><span data-stu-id="5a8db-134">Remarks</span></span>

<span data-ttu-id="5a8db-135">La fonction **glGetTexEnv** retourne dans *params* les valeurs sélectionnées d’un environnement de texture qui a été spécifié avec [**glTexEnv**](gltexenv-functions.md).</span><span class="sxs-lookup"><span data-stu-id="5a8db-135">The **glGetTexEnv** function returns in *params* selected values of a texture environment that was specified with [**glTexEnv**](gltexenv-functions.md).</span></span> <span data-ttu-id="5a8db-136">Le paramètre *target* spécifie un environnement de texture.</span><span class="sxs-lookup"><span data-stu-id="5a8db-136">The *target* parameter specifies a texture environment.</span></span> <span data-ttu-id="5a8db-137">Actuellement, un seul environnement de texture est défini et pris en charge : la \_ texture GL \_ env.</span><span class="sxs-lookup"><span data-stu-id="5a8db-137">Currently, only one texture environment is defined and supported: GL\_TEXTURE\_ENV.</span></span>

<span data-ttu-id="5a8db-138">Le paramètre *pname* désigne un paramètre d’environnement de texture spécifique.</span><span class="sxs-lookup"><span data-stu-id="5a8db-138">The *pname* parameter names a specific texture environment parameter.</span></span>

<span data-ttu-id="5a8db-139">Si une erreur est générée, aucune modification n’est apportée au contenu des *paramètres*.</span><span class="sxs-lookup"><span data-stu-id="5a8db-139">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a8db-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a8db-140">Requirements</span></span>



| <span data-ttu-id="5a8db-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a8db-141">Requirement</span></span> | <span data-ttu-id="5a8db-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a8db-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a8db-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a8db-143">Minimum supported client</span></span><br/> | <span data-ttu-id="5a8db-144">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a8db-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5a8db-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a8db-145">Minimum supported server</span></span><br/> | <span data-ttu-id="5a8db-146">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a8db-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5a8db-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a8db-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a8db-148"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a8db-148"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5a8db-149">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5a8db-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="5a8db-150"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a8db-150"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5a8db-151">DLL</span><span class="sxs-lookup"><span data-stu-id="5a8db-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a8db-152"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a8db-152"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a8db-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a8db-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a8db-154">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="5a8db-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5a8db-155">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="5a8db-155">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="5a8db-156">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="5a8db-156">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> </dl>

 

 





