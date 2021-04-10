---
title: fonction glGetString (GL. h)
description: La fonction glGetString retourne une chaîne décrivant la connexion OpenGL actuelle.
ms.assetid: 768e6ec2-3f00-44e6-b3cb-de0f06d6a73d
keywords:
- glGetString fonction OpenGL
topic_type:
- apiref
api_name:
- glGetString
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e263e35802af752fa262c898d036fccaa37aff87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942739"
---
# <a name="glgetstring-function"></a><span data-ttu-id="9323f-104">glGetString fonction)</span><span class="sxs-lookup"><span data-stu-id="9323f-104">glGetString function</span></span>

<span data-ttu-id="9323f-105">La fonction **glGetString** retourne une chaîne décrivant la connexion OpenGL actuelle.</span><span class="sxs-lookup"><span data-stu-id="9323f-105">The **glGetString** function returns a string describing the current OpenGL connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9323f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9323f-106">Syntax</span></span>


```C++
const GLubyte* WINAPI glGetString(
   GLenum name
);
```



## <a name="parameters"></a><span data-ttu-id="9323f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9323f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9323f-108">*name*</span><span class="sxs-lookup"><span data-stu-id="9323f-108">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="9323f-109">L’une des constantes symboliques suivantes.</span><span class="sxs-lookup"><span data-stu-id="9323f-109">One of the following symbolic constants.</span></span>



| <span data-ttu-id="9323f-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="9323f-110">Value</span></span>                                                                                                                                                         | <span data-ttu-id="9323f-111">Signification</span><span class="sxs-lookup"><span data-stu-id="9323f-111">Meaning</span></span>                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_VENDOR"></span><span id="gl_vendor"></span><dl> <span data-ttu-id="9323f-112"><dt>**fournisseur du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9323f-112"><dt>**GL\_VENDOR**</dt></span></span> </dl>             | <span data-ttu-id="9323f-113">Retourne la société responsable de cette implémentation OpenGL.</span><span class="sxs-lookup"><span data-stu-id="9323f-113">Returns the company responsible for this OpenGL implementation.</span></span> <span data-ttu-id="9323f-114">Ce nom ne passe pas de Release à Release.</span><span class="sxs-lookup"><span data-stu-id="9323f-114">This name does not change from release to release.</span></span><br/>                                                  |
| <span id="GL_RENDERER"></span><span id="gl_renderer"></span><dl> <span data-ttu-id="9323f-115"><dt>**\_convertisseur GL**</dt></span><span class="sxs-lookup"><span data-stu-id="9323f-115"><dt>**GL\_RENDERER**</dt></span></span> </dl>       | <span data-ttu-id="9323f-116">Retourne le nom du convertisseur.</span><span class="sxs-lookup"><span data-stu-id="9323f-116">Returns the name of the renderer.</span></span> <span data-ttu-id="9323f-117">Ce nom est généralement spécifique à une configuration particulière d’une plateforme matérielle.</span><span class="sxs-lookup"><span data-stu-id="9323f-117">This name is typically specific to a particular configuration of a hardware platform.</span></span> <span data-ttu-id="9323f-118">Il ne passe pas de Release à Release.</span><span class="sxs-lookup"><span data-stu-id="9323f-118">It does not change from release to release.</span></span><br/> |
| <span id="GL_VERSION"></span><span id="gl_version"></span><dl> <span data-ttu-id="9323f-119"><dt>**VERSION du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9323f-119"><dt>**GL\_VERSION**</dt></span></span> </dl>          | <span data-ttu-id="9323f-120">Retourne un numéro de version ou de version.</span><span class="sxs-lookup"><span data-stu-id="9323f-120">Returns a version or release number.</span></span><br/>                                                                                                                                |
| <span id="GL_EXTENSIONS"></span><span id="gl_extensions"></span><dl> <span data-ttu-id="9323f-121"><dt>**EXTENSIONS du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9323f-121"><dt>**GL\_EXTENSIONS**</dt></span></span> </dl> | <span data-ttu-id="9323f-122">Retourne une liste séparée par des espaces des extensions prises en charge par OpenGL.</span><span class="sxs-lookup"><span data-stu-id="9323f-122">Returns a space-separated list of supported extensions to OpenGL.</span></span><br/>                                                                                                   |



 

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="9323f-123">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="9323f-123">Error codes</span></span>

<span data-ttu-id="9323f-124">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="9323f-124">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9323f-125">Nom</span><span class="sxs-lookup"><span data-stu-id="9323f-125">Name</span></span>                                                                                                  | <span data-ttu-id="9323f-126">Signification</span><span class="sxs-lookup"><span data-stu-id="9323f-126">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9323f-127"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9323f-127"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="9323f-128">le *nom* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="9323f-128">*name* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="9323f-129"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9323f-129"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9323f-130">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="9323f-130">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9323f-131">Notes</span><span class="sxs-lookup"><span data-stu-id="9323f-131">Remarks</span></span>

<span data-ttu-id="9323f-132">La fonction **glGetString** retourne un pointeur vers une chaîne statique décrivant certains aspects de la connexion OpenGL actuelle.</span><span class="sxs-lookup"><span data-stu-id="9323f-132">The **glGetString** function returns a pointer to a static string describing some aspect of the current OpenGL connection.</span></span>

<span data-ttu-id="9323f-133">Comme OpenGL n’inclut pas de requêtes pour les caractéristiques de performances d’une implémentation, il est prévu que certaines applications soient écrites pour reconnaître les plateformes connues et modifient leur utilisation de OpenGL en fonction des caractéristiques de performances connues de ces plateformes.</span><span class="sxs-lookup"><span data-stu-id="9323f-133">Because OpenGL does not include queries for the performance characteristics of an implementation, it is expected that some applications will be written to recognize known platforms and will modify their OpenGL usage based on known performance characteristics of these platforms.</span></span> <span data-ttu-id="9323f-134">Les chaînes fournisseur du GL \_ et \_ convertisseur GL regroupent de façon unique une plateforme, et ne changent pas d’une version à l’autres.</span><span class="sxs-lookup"><span data-stu-id="9323f-134">The strings GL\_VENDOR and GL\_RENDERER together uniquely specify a platform, and will not change from release to release.</span></span> <span data-ttu-id="9323f-135">Ils doivent être utilisés en tant que tels par les algorithmes de reconnaissance de plateforme.</span><span class="sxs-lookup"><span data-stu-id="9323f-135">They should be used as such by platform recognition algorithms.</span></span>

<span data-ttu-id="9323f-136">Le format et le contenu de la chaîne retournée par **glGetString** dépendent de l’implémentation, à l’exception de :</span><span class="sxs-lookup"><span data-stu-id="9323f-136">The format and contents of the string that **glGetString** returns depend on the implementation, except that:</span></span>

-   <span data-ttu-id="9323f-137">Les noms d’extension n’incluent pas de caractères d’espace et seront séparés par des espaces dans la \_ chaîne d’extensions GL.</span><span class="sxs-lookup"><span data-stu-id="9323f-137">Extension names will not include space characters and will be separated by space characters in the GL\_EXTENSIONS string.</span></span>
-   <span data-ttu-id="9323f-138">La chaîne de version du GL \_ commence par un numéro de version.</span><span class="sxs-lookup"><span data-stu-id="9323f-138">The GL\_VERSION string begins with a version number.</span></span> <span data-ttu-id="9323f-139">Le numéro de version utilise l’une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="9323f-139">The version number uses one of these forms:</span></span>

    <span data-ttu-id="9323f-140">*\_ nombre majeur*. *\_ nombre mineur*</span><span class="sxs-lookup"><span data-stu-id="9323f-140">*major\_number*.*minor\_number*</span></span>

    <span data-ttu-id="9323f-141">*\_ nombre majeur*. *\_ nombre mineur*. *\_ numéro de version*</span><span class="sxs-lookup"><span data-stu-id="9323f-141">*major\_number*.*minor\_number*.*release\_number*</span></span>

-   <span data-ttu-id="9323f-142">Les informations spécifiques au fournisseur peuvent suivre le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="9323f-142">Vendor-specific information may follow the version number.</span></span> <span data-ttu-id="9323f-143">Son format dépend de l’implémentation, mais un espace sépare toujours le numéro de version et les informations spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9323f-143">Its format depends on the implementation, but a space always separates the version number and the vendor-specific information.</span></span>
-   <span data-ttu-id="9323f-144">Toutes les chaînes se terminent par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="9323f-144">All strings are null-terminated.</span></span>

<span data-ttu-id="9323f-145">Si une erreur est générée, **glGetString** retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="9323f-145">If an error is generated, **glGetString** returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="9323f-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9323f-146">Requirements</span></span>



| <span data-ttu-id="9323f-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9323f-147">Requirement</span></span> | <span data-ttu-id="9323f-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="9323f-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9323f-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9323f-149">Minimum supported client</span></span><br/> | <span data-ttu-id="9323f-150">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9323f-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9323f-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9323f-151">Minimum supported server</span></span><br/> | <span data-ttu-id="9323f-152">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9323f-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9323f-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="9323f-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="9323f-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9323f-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9323f-155">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9323f-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="9323f-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9323f-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9323f-157">DLL</span><span class="sxs-lookup"><span data-stu-id="9323f-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9323f-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9323f-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9323f-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9323f-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9323f-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9323f-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9323f-161">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="9323f-161">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





