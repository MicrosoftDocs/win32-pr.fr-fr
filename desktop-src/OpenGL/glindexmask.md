---
title: fonction glIndexMask (GL. h)
description: La fonction glIndexMask contrôle l’écriture de bits individuels dans les mémoires tampons d’index de couleurs.
ms.assetid: f4b5df36-390f-4254-95fb-98589750a11b
keywords:
- glIndexMask fonction OpenGL
topic_type:
- apiref
api_name:
- glIndexMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d426cb1f4bb2e794bef53853d0336db1d64b263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509302"
---
# <a name="glindexmask-function"></a><span data-ttu-id="661da-104">glIndexMask fonction)</span><span class="sxs-lookup"><span data-stu-id="661da-104">glIndexMask function</span></span>

<span data-ttu-id="661da-105">La fonction **glIndexMask** contrôle l’écriture de bits individuels dans les mémoires tampons d’index de couleurs.</span><span class="sxs-lookup"><span data-stu-id="661da-105">The **glIndexMask** function controls the writing of individual bits in the color-index buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="661da-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="661da-106">Syntax</span></span>


```C++
void WINAPI glIndexMask(
   GLuint mask
);
```



## <a name="parameters"></a><span data-ttu-id="661da-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="661da-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="661da-108">*mask*</span><span class="sxs-lookup"><span data-stu-id="661da-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="661da-109">Masque de bits permettant d’activer et de désactiver l’écriture de bits individuels dans les mémoires tampons d’index de couleurs.</span><span class="sxs-lookup"><span data-stu-id="661da-109">A bit mask to enable and disable the writing of individual bits in the color-index buffers.</span></span> <span data-ttu-id="661da-110">Initialement, le masque est tous les éléments.</span><span class="sxs-lookup"><span data-stu-id="661da-110">Initially, the mask is all ones.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="661da-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="661da-111">Return value</span></span>

<span data-ttu-id="661da-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="661da-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="661da-113">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="661da-113">Error codes</span></span>

<span data-ttu-id="661da-114">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="661da-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="661da-115">Nom</span><span class="sxs-lookup"><span data-stu-id="661da-115">Name</span></span>                                                                                                  | <span data-ttu-id="661da-116">Signification</span><span class="sxs-lookup"><span data-stu-id="661da-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="661da-117"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="661da-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="661da-118">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="661da-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="661da-119">Notes</span><span class="sxs-lookup"><span data-stu-id="661da-119">Remarks</span></span>

<span data-ttu-id="661da-120">La fonction **glIndexMask** contrôle l’écriture de bits individuels dans les mémoires tampons d’index de couleurs.</span><span class="sxs-lookup"><span data-stu-id="661da-120">The **glIndexMask** function controls the writing of individual bits in the color-index buffers.</span></span> <span data-ttu-id="661da-121">Les *n* bits les moins significatifs du *masque*, où *1* est le nombre de bits dans une mémoire tampon d’index de couleurs, spécifiez un masque.</span><span class="sxs-lookup"><span data-stu-id="661da-121">The least significant *n* bits of *mask*, where *1* is the number of bits in a color-index buffer, specify a mask.</span></span> <span data-ttu-id="661da-122">Chaque fois qu’un point apparaît dans le masque, le bit correspondant dans la mémoire tampon d’index de couleurs (ou mémoires tampons) est rendu accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="661da-122">Wherever a one appears in the mask, the corresponding bit in the color-index buffer (or buffers) is made writable.</span></span> <span data-ttu-id="661da-123">Lorsqu’un zéro s’affiche, le bit est protégé en écriture.</span><span class="sxs-lookup"><span data-stu-id="661da-123">Where a zero appears, the bit is write-protected.</span></span>

<span data-ttu-id="661da-124">Ce masque est utilisé uniquement en mode d’index de couleurs, et il affecte uniquement les mémoires tampons actuellement sélectionnées pour l’écriture (voir [**glDrawBuffer**](gldrawbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="661da-124">This mask is used only in color-index mode, and it affects only the buffers currently selected for writing (see [**glDrawBuffer**](gldrawbuffer.md)).</span></span> <span data-ttu-id="661da-125">Initialement, tous les bits sont activés pour l’écriture.</span><span class="sxs-lookup"><span data-stu-id="661da-125">Initially, all bits are enabled for writing.</span></span>

<span data-ttu-id="661da-126">La fonction suivante récupère des informations relatives à **glIndexMask**:</span><span class="sxs-lookup"><span data-stu-id="661da-126">The following function retrieves information related to **glIndexMask**:</span></span>

<span data-ttu-id="661da-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ index \_ WRITEMASK</span><span class="sxs-lookup"><span data-stu-id="661da-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_INDEX\_WRITEMASK</span></span>

## <a name="requirements"></a><span data-ttu-id="661da-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="661da-128">Requirements</span></span>



| <span data-ttu-id="661da-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="661da-129">Requirement</span></span> | <span data-ttu-id="661da-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="661da-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="661da-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="661da-131">Minimum supported client</span></span><br/> | <span data-ttu-id="661da-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="661da-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="661da-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="661da-133">Minimum supported server</span></span><br/> | <span data-ttu-id="661da-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="661da-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="661da-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="661da-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="661da-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="661da-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="661da-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="661da-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="661da-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="661da-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="661da-139">DLL</span><span class="sxs-lookup"><span data-stu-id="661da-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="661da-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="661da-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="661da-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="661da-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="661da-142">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="661da-142">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="661da-143">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="661da-143">**glDepthMask**</span></span>](gldepthmask.md)
</dt> <dt>

[<span data-ttu-id="661da-144">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="661da-144">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="661da-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="661da-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="661da-146">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="661da-146">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="661da-147">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="661da-147">**glStencilMask**</span></span>](glstencilmask.md)
</dt> </dl>

 

 





