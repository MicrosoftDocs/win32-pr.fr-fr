---
title: fonction glGetError (GL. h)
description: La fonction glGetError retourne des informations sur l’erreur.
ms.assetid: 18f0368f-054f-4b84-8397-3f9ee4aa07fa
keywords:
- glGetError fonction OpenGL
topic_type:
- apiref
api_name:
- glGetError
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c0abf6ec03ca0c29ede3b7d396db375fd06ac6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942683"
---
# <a name="glgeterror-function"></a><span data-ttu-id="be8b4-104">glGetError fonction)</span><span class="sxs-lookup"><span data-stu-id="be8b4-104">glGetError function</span></span>

<span data-ttu-id="be8b4-105">La fonction **glGetError** retourne des informations sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="be8b4-105">The **glGetError** function returns error information.</span></span>

## <a name="syntax"></a><span data-ttu-id="be8b4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be8b4-106">Syntax</span></span>


```C++
GLenum WINAPI glGetError(void);
```



## <a name="parameters"></a><span data-ttu-id="be8b4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be8b4-107">Parameters</span></span>

<span data-ttu-id="be8b4-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="be8b4-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="be8b4-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="be8b4-109">Return value</span></span>

<span data-ttu-id="be8b4-110">La fonction **glGetError** retourne l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="be8b4-110">The **glGetError** function returns one of the following error codes.</span></span>



| <span data-ttu-id="be8b4-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="be8b4-111">Return code</span></span>                                                                                           | <span data-ttu-id="be8b4-112">Description</span><span class="sxs-lookup"><span data-stu-id="be8b4-112">Description</span></span>                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="be8b4-113"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="be8b4-113"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="be8b4-114">Une valeur inacceptable est spécifiée pour un argument énuméré.</span><span class="sxs-lookup"><span data-stu-id="be8b4-114">An unacceptable value is specified for an enumerated argument.</span></span> <span data-ttu-id="be8b4-115">La fonction incriminée est ignorée, ce qui n’a aucun effet secondaire que de définir l’indicateur d’erreur.</span><span class="sxs-lookup"><span data-stu-id="be8b4-115">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>         |
| <dl> <span data-ttu-id="be8b4-116"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="be8b4-116"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="be8b4-117">Un argument numérique est hors limites.</span><span class="sxs-lookup"><span data-stu-id="be8b4-117">A numeric argument is out of range.</span></span> <span data-ttu-id="be8b4-118">La fonction incriminée est ignorée, ce qui n’a aucun effet secondaire que de définir l’indicateur d’erreur.</span><span class="sxs-lookup"><span data-stu-id="be8b4-118">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>                                    |
| <dl> <span data-ttu-id="be8b4-119"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="be8b4-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="be8b4-120">L’opération spécifiée n’est pas autorisée dans l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="be8b4-120">The specified operation is not allowed in the current state.</span></span> <span data-ttu-id="be8b4-121">La fonction incriminée est ignorée, ce qui n’a aucun effet secondaire que de définir l’indicateur d’erreur.</span><span class="sxs-lookup"><span data-stu-id="be8b4-121">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>           |
| <dl> <span data-ttu-id="be8b4-122"><dt>**GL- \_ aucune \_ erreur**</dt></span><span class="sxs-lookup"><span data-stu-id="be8b4-122"><dt>**GL\_NO\_ERROR**</dt></span></span> </dl>          | <span data-ttu-id="be8b4-123">Aucune erreur n’a été enregistrée.</span><span class="sxs-lookup"><span data-stu-id="be8b4-123">No error has been recorded.</span></span> <span data-ttu-id="be8b4-124">La valeur de cette constante symbolique est garantie égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="be8b4-124">The value of this symbolic constant is guaranteed to be zero.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="be8b4-125"><dt>**dépassement de capacité de la \_ pile GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="be8b4-125"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="be8b4-126">Cette fonction provoquerait un dépassement de capacité de la pile.</span><span class="sxs-lookup"><span data-stu-id="be8b4-126">This function would cause a stack overflow.</span></span> <span data-ttu-id="be8b4-127">La fonction incriminée est ignorée, ce qui n’a aucun effet secondaire que de définir l’indicateur d’erreur.</span><span class="sxs-lookup"><span data-stu-id="be8b4-127">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>                            |
| <dl> <span data-ttu-id="be8b4-128"><dt>**DÉPASSEMENT de capacité de la \_ pile GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="be8b4-128"><dt>**GL\_STACK\_UNDERFLOW**</dt></span></span> </dl>   | <span data-ttu-id="be8b4-129">Cette fonction provoque un dépassement de capacité négatif de la pile.</span><span class="sxs-lookup"><span data-stu-id="be8b4-129">This function would cause a stack underflow.</span></span> <span data-ttu-id="be8b4-130">La fonction incriminée est ignorée, ce qui n’a aucun effet secondaire que de définir l’indicateur d’erreur.</span><span class="sxs-lookup"><span data-stu-id="be8b4-130">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>                           |
| <dl> <span data-ttu-id="be8b4-131"><dt>**\_mémoire insuffisante \_ du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="be8b4-131"><dt>**GL\_OUT\_OF\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="be8b4-132">Il n’y a pas assez de mémoire pour exécuter la fonction.</span><span class="sxs-lookup"><span data-stu-id="be8b4-132">There is not enough memory left to execute the function.</span></span> <span data-ttu-id="be8b4-133">L’état de OpenGL n’est pas défini, à l’exception de l’état des indicateurs d’erreur, après l’enregistrement de cette erreur.</span><span class="sxs-lookup"><span data-stu-id="be8b4-133">The state of OpenGL is undefined, except for the state of the error flags, after this error is recorded.</span></span><br/> |



 

<span data-ttu-id="be8b4-134">Notez que **glGetError** retourne \_ une opération GL non valide \_ si elle est appelée entre un appel à [**glBegin**](glbegin.md) et son appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="be8b4-134">Note that **glGetError** returns GL\_INVALID\_OPERATION if it is called between a call to [**glBegin**](glbegin.md) and its corresponding call to [**glEnd**](glend.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="be8b4-135">Notes</span><span class="sxs-lookup"><span data-stu-id="be8b4-135">Remarks</span></span>

<span data-ttu-id="be8b4-136">Chaque erreur détectable est assignée à un code numérique et à un nom symbolique.</span><span class="sxs-lookup"><span data-stu-id="be8b4-136">Each detectable error is assigned a numeric code and symbolic name.</span></span> <span data-ttu-id="be8b4-137">Lorsqu’une erreur se produit, l’indicateur d’erreur est défini sur la valeur de code d’erreur appropriée.</span><span class="sxs-lookup"><span data-stu-id="be8b4-137">When an error occurs, the error flag is set to the appropriate error code value.</span></span> <span data-ttu-id="be8b4-138">Aucune autre erreur n’est enregistrée tant que **glGetError** n’est pas appelé, le code d’erreur est retourné et l’indicateur est réinitialisé sur GL \_ no \_ Error.</span><span class="sxs-lookup"><span data-stu-id="be8b4-138">No other errors are recorded until **glGetError** is called, the error code is returned, and the flag is reset to GL\_NO\_ERROR.</span></span> <span data-ttu-id="be8b4-139">Si un appel à **glGetError** retourne GL \_ no \_ Error, aucune erreur détectable n’est survenue depuis le dernier appel à **glGetError** ou depuis que OpenGL a été initialisé.</span><span class="sxs-lookup"><span data-stu-id="be8b4-139">If a call to **glGetError** returns GL\_NO\_ERROR, there has been no detectable error since the last call to **glGetError**, or since OpenGL was initialized.</span></span>

<span data-ttu-id="be8b4-140">Pour permettre les implémentations distribuées, il peut y avoir plusieurs indicateurs d’erreur.</span><span class="sxs-lookup"><span data-stu-id="be8b4-140">To allow for distributed implementations, there may be several error flags.</span></span> <span data-ttu-id="be8b4-141">Si un indicateur d’erreur unique a enregistré une erreur, la valeur de cet indicateur est retournée et cet indicateur est réinitialisé sur GL \_ no \_ Error quand **glGetError** est appelé.</span><span class="sxs-lookup"><span data-stu-id="be8b4-141">If any single error flag has recorded an error, the value of that flag is returned and that flag is reset to GL\_NO\_ERROR when **glGetError** is called.</span></span> <span data-ttu-id="be8b4-142">Si plusieurs indicateurs ont enregistré une erreur, **glGetError** retourne et efface une valeur d’indicateur d’erreur arbitraire.</span><span class="sxs-lookup"><span data-stu-id="be8b4-142">If more than one flag has recorded an error, **glGetError** returns and clears an arbitrary error flag value.</span></span> <span data-ttu-id="be8b4-143">Si tous les indicateurs d’erreur doivent être réinitialisés, vous devez toujours appeler **glGetError** dans une boucle jusqu’à ce qu’il retourne GL \_ no \_ Error.</span><span class="sxs-lookup"><span data-stu-id="be8b4-143">If all error flags are to be reset, you should always call **glGetError** in a loop until it returns GL\_NO\_ERROR.</span></span>

<span data-ttu-id="be8b4-144">Initialement, tous les indicateurs d’erreur sont définis sur GL \_ no \_ Error.</span><span class="sxs-lookup"><span data-stu-id="be8b4-144">Initially, all error flags are set to GL\_NO\_ERROR.</span></span>

<span data-ttu-id="be8b4-145">Lorsqu’un indicateur d’erreur est défini, les résultats d’une opération OpenGL ne sont pas définis uniquement si la \_ mémoire insuffisante du GL s’est \_ \_ produite.</span><span class="sxs-lookup"><span data-stu-id="be8b4-145">When an error flag is set, results of an OpenGL operation are undefined only if GL\_OUT\_OF\_MEMORY has occurred.</span></span> <span data-ttu-id="be8b4-146">Dans tous les autres cas, la fonction qui génère l’erreur est ignorée et n’a aucun effet sur l’État OpenGL ou le contenu trame.</span><span class="sxs-lookup"><span data-stu-id="be8b4-146">In all other cases, the function generating the error is ignored and has no effect on the OpenGL state or framebuffer contents.</span></span>

## <a name="requirements"></a><span data-ttu-id="be8b4-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be8b4-147">Requirements</span></span>



| <span data-ttu-id="be8b4-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be8b4-148">Requirement</span></span> | <span data-ttu-id="be8b4-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="be8b4-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be8b4-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be8b4-150">Minimum supported client</span></span><br/> | <span data-ttu-id="be8b4-151">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be8b4-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="be8b4-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be8b4-152">Minimum supported server</span></span><br/> | <span data-ttu-id="be8b4-153">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be8b4-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="be8b4-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="be8b4-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="be8b4-155"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="be8b4-155"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="be8b4-156">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="be8b4-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="be8b4-157"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be8b4-157"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="be8b4-158">DLL</span><span class="sxs-lookup"><span data-stu-id="be8b4-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be8b4-159"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be8b4-159"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be8b4-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be8b4-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be8b4-161">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="be8b4-161">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="be8b4-162">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="be8b4-162">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





