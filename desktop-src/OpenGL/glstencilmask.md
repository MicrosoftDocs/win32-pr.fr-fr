---
title: fonction glStencilMask (GL. h)
description: La fonction glStencilMask contrôle l’écriture de bits individuels dans les plans de gabarit.
ms.assetid: c586f9db-bad5-4f06-a194-a8d979842d0c
keywords:
- glStencilMask fonction OpenGL
topic_type:
- apiref
api_name:
- glStencilMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e63790fa30e88abbde6e1ba47e624c6caf2dcfc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106399"
---
# <a name="glstencilmask-function"></a><span data-ttu-id="31b5b-104">glStencilMask fonction)</span><span class="sxs-lookup"><span data-stu-id="31b5b-104">glStencilMask function</span></span>

<span data-ttu-id="31b5b-105">La fonction **glStencilMask** contrôle l’écriture de bits individuels dans les plans de gabarit.</span><span class="sxs-lookup"><span data-stu-id="31b5b-105">The **glStencilMask** function controls the writing of individual bits in the stencil planes.</span></span>

## <a name="syntax"></a><span data-ttu-id="31b5b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31b5b-106">Syntax</span></span>


```C++
void WINAPI glStencilMask(
   GLuint mask
);
```



## <a name="parameters"></a><span data-ttu-id="31b5b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31b5b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31b5b-108">*mask*</span><span class="sxs-lookup"><span data-stu-id="31b5b-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="31b5b-109">Masque de bits permettant d’activer et de désactiver l’écriture de bits individuels dans les plans de gabarit.</span><span class="sxs-lookup"><span data-stu-id="31b5b-109">A bit mask to enable and disable writing of individual bits in the stencil planes.</span></span> <span data-ttu-id="31b5b-110">Initialement, le masque est tous les éléments.</span><span class="sxs-lookup"><span data-stu-id="31b5b-110">Initially, the mask is all ones.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31b5b-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="31b5b-111">Return value</span></span>

<span data-ttu-id="31b5b-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="31b5b-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="31b5b-113">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="31b5b-113">Error codes</span></span>

<span data-ttu-id="31b5b-114">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="31b5b-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="31b5b-115">Nom</span><span class="sxs-lookup"><span data-stu-id="31b5b-115">Name</span></span>                                                                                                  | <span data-ttu-id="31b5b-116">Signification</span><span class="sxs-lookup"><span data-stu-id="31b5b-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="31b5b-117"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="31b5b-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="31b5b-118">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="31b5b-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="31b5b-119">Notes</span><span class="sxs-lookup"><span data-stu-id="31b5b-119">Remarks</span></span>

<span data-ttu-id="31b5b-120">La fonction **glStencilMask** contrôle l’écriture de bits individuels dans les plans de gabarit.</span><span class="sxs-lookup"><span data-stu-id="31b5b-120">The **glStencilMask** function controls the writing of individual bits in the stencil planes.</span></span> <span data-ttu-id="31b5b-121">Les *n* bits les moins significatifs du *masque*, où *n* est le nombre de bits dans la mémoire tampon du stencil, spécifient un masque.</span><span class="sxs-lookup"><span data-stu-id="31b5b-121">The least significant *n* bits of *mask*, where *n* is the number of bits in the stencil buffer, specify a mask.</span></span> <span data-ttu-id="31b5b-122">Chaque fois qu’un seul apparaît dans le masque, le bit correspondant dans la mémoire tampon du stencil est rendu accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="31b5b-122">Wherever a one appears in the mask, the corresponding bit in the stencil buffer is made writable.</span></span> <span data-ttu-id="31b5b-123">Lorsqu’un zéro s’affiche, le bit est protégé en écriture.</span><span class="sxs-lookup"><span data-stu-id="31b5b-123">Where a zero appears, the bit is write-protected.</span></span> <span data-ttu-id="31b5b-124">Initialement, tous les bits sont activés pour l’écriture.</span><span class="sxs-lookup"><span data-stu-id="31b5b-124">Initially, all bits are enabled for writing.</span></span>

<span data-ttu-id="31b5b-125">Les fonctions suivantes récupèrent les informations relatives à **glStencilMask**:</span><span class="sxs-lookup"><span data-stu-id="31b5b-125">The following functions retrieve information related to **glStencilMask**:</span></span>

<span data-ttu-id="31b5b-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument \_ WRITEMASK de gabarit \_</span><span class="sxs-lookup"><span data-stu-id="31b5b-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_WRITEMASK</span></span>

<span data-ttu-id="31b5b-127">glGet avec arguments de stencil de la comptabilité GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="31b5b-127">glGet with argument GL\_STENCIL\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="31b5b-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31b5b-128">Requirements</span></span>



| <span data-ttu-id="31b5b-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31b5b-129">Requirement</span></span> | <span data-ttu-id="31b5b-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="31b5b-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31b5b-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31b5b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="31b5b-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31b5b-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="31b5b-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31b5b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="31b5b-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31b5b-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="31b5b-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="31b5b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="31b5b-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="31b5b-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="31b5b-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="31b5b-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="31b5b-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31b5b-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="31b5b-139">DLL</span><span class="sxs-lookup"><span data-stu-id="31b5b-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31b5b-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31b5b-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31b5b-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31b5b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31b5b-142">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="31b5b-142">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="31b5b-143">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="31b5b-143">**glColorMask**</span></span>](glcolormask.md)
</dt> <dt>

[<span data-ttu-id="31b5b-144">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="31b5b-144">**glDepthMask**</span></span>](gldepthmask.md)
</dt> <dt>

[<span data-ttu-id="31b5b-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="31b5b-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="31b5b-146">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="31b5b-146">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="31b5b-147">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="31b5b-147">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> <dt>

[<span data-ttu-id="31b5b-148">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="31b5b-148">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





