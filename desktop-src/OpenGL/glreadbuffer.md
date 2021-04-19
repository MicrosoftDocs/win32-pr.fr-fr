---
title: fonction glReadBuffer (GL. h)
description: La fonction glReadBuffer sélectionne une source de mémoire tampon de couleur pour les pixels.
ms.assetid: 734153fa-e809-4b70-867e-55e46ab95712
keywords:
- glReadBuffer fonction OpenGL
topic_type:
- apiref
api_name:
- glReadBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f0e88cdcb2b1b3257b23606f8160e0986584db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512597"
---
# <a name="glreadbuffer-function"></a><span data-ttu-id="71213-104">glReadBuffer fonction)</span><span class="sxs-lookup"><span data-stu-id="71213-104">glReadBuffer function</span></span>

<span data-ttu-id="71213-105">La fonction **glReadBuffer** sélectionne une source de mémoire tampon de couleur pour les pixels.</span><span class="sxs-lookup"><span data-stu-id="71213-105">The **glReadBuffer** function selects a color buffer source for pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="71213-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71213-106">Syntax</span></span>


```C++
void WINAPI glReadBuffer(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="71213-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71213-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71213-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="71213-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="71213-109">Mémoire tampon de couleur.</span><span class="sxs-lookup"><span data-stu-id="71213-109">A color buffer.</span></span> <span data-ttu-id="71213-110">Les valeurs acceptées sont le préversion GL, le préversion GL, l’arrière-plan du GL, l’arrière-plan du GL, le \_ \_ \_ \_ \_ \_ \_ \_ \_ rectus GL, le \_ verso, le GL à \_ gauche, \_ le GL droit et le GL des, \_ où *i* est compris entre 0 et le GL des tampons au niveau  \_ \_ 1.</span><span class="sxs-lookup"><span data-stu-id="71213-110">Accepted values are GL\_FRONT\_LEFT, GL\_FRONT\_RIGHT, GL\_BACK\_LEFT, GL\_BACK\_RIGHT, GL\_FRONT, GL\_BACK, GL\_LEFT, GL\_RIGHT, and GL\_AUX *i*, where *i* is between 0 and GL\_AUX\_BUFFERS 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71213-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="71213-111">Return value</span></span>

<span data-ttu-id="71213-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="71213-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="71213-113">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="71213-113">Error codes</span></span>

<span data-ttu-id="71213-114">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="71213-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="71213-115">Nom</span><span class="sxs-lookup"><span data-stu-id="71213-115">Name</span></span>                                                                                                  | <span data-ttu-id="71213-116">Signification</span><span class="sxs-lookup"><span data-stu-id="71213-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="71213-117"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="71213-117"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="71213-118">le *mode* ne faisait pas partie des douze (ou plus) valeurs acceptées.</span><span class="sxs-lookup"><span data-stu-id="71213-118">*mode* was not an one of the twelve (or more) accepted values.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="71213-119"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="71213-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="71213-120">le *mode* a spécifié une mémoire tampon qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="71213-120">*mode* specified a buffer that does not exist.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="71213-121"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="71213-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="71213-122">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="71213-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="71213-123">Notes</span><span class="sxs-lookup"><span data-stu-id="71213-123">Remarks</span></span>

<span data-ttu-id="71213-124">La fonction **glReadBuffer** spécifie une mémoire tampon de couleur comme source pour les commandes [**glReadPixels**](glreadpixels.md) et [**glCopyPixels**](glcopypixels.md) suivantes.</span><span class="sxs-lookup"><span data-stu-id="71213-124">The **glReadBuffer** function specifies a color buffer as the source for subsequent [**glReadPixels**](glreadpixels.md) and [**glCopyPixels**](glcopypixels.md) commands.</span></span> <span data-ttu-id="71213-125">Le paramètre *mode* accepte une ou plusieurs valeurs prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="71213-125">The *mode* parameter accepts one of twelve or more predefined values.</span></span> <span data-ttu-id="71213-126">(GL \_ AUX0 via GL \_ AUX3 sont toujours définis.) Dans un système entièrement configuré, les préversions GL \_ , GL gauche et GL vers l’avant-plan de la zone de préversion de la mémoire tampon de l’avant-plan, le préversion \_ \_ \_ GL \_ \_ et \_ \_ \_ \_ le nom de la mémoire tampon d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="71213-126">(GL\_AUX0 through GL\_AUX3 are always defined.) In a fully configured system, GL\_FRONT, GL\_LEFT, and GL\_FRONT\_LEFT all name the front-left buffer, GL\_FRONT\_RIGHT and GL\_RIGHT name the front-right buffer, and GL\_BACK\_LEFT and GL\_BACK name the back-left buffer.</span></span>

<span data-ttu-id="71213-127">Les configurations à double mise en mémoire tampon non stéréo n’ont qu’une seule partie de l’avant-gauche et une mémoire tampon en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="71213-127">Nonstereo double-buffered configurations have only a front-left and a back-left buffer.</span></span> <span data-ttu-id="71213-128">Les configurations à une seule mise en mémoire tampon ont un avant-plan et une mémoire tampon de l’avant-plan si elle est stéréo, et seulement une mémoire tampon en avant-gauche si elle est non stéréo.</span><span class="sxs-lookup"><span data-stu-id="71213-128">Single-buffered configurations have a front-left and a front-right buffer if stereo, and only a front-left buffer if nonstereo.</span></span> <span data-ttu-id="71213-129">La spécification d’une mémoire tampon inexistante dans **glReadBuffer** est une erreur.</span><span class="sxs-lookup"><span data-stu-id="71213-129">It is an error to specify a nonexistent buffer to **glReadBuffer**.</span></span>

<span data-ttu-id="71213-130">Par défaut, le *mode* est \_ recto GL dans les configurations à une seule mise en mémoire tampon, et le GL \_ revient dans les configurations à double mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="71213-130">By default, *mode* is GL\_FRONT in single-buffered configurations, and GL\_BACK in double-buffered configurations.</span></span>

<span data-ttu-id="71213-131">La fonction suivante récupère des informations relatives à **glReadBuffer**:</span><span class="sxs-lookup"><span data-stu-id="71213-131">The following function retrieves information related to **glReadBuffer**:</span></span>

<span data-ttu-id="71213-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL de lecture de la \_ \_ mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="71213-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_READ\_BUFFER</span></span>

## <a name="requirements"></a><span data-ttu-id="71213-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71213-133">Requirements</span></span>



| <span data-ttu-id="71213-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71213-134">Requirement</span></span> | <span data-ttu-id="71213-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="71213-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71213-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71213-136">Minimum supported client</span></span><br/> | <span data-ttu-id="71213-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71213-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="71213-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71213-138">Minimum supported server</span></span><br/> | <span data-ttu-id="71213-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71213-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="71213-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="71213-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="71213-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="71213-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="71213-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="71213-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="71213-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71213-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="71213-144">DLL</span><span class="sxs-lookup"><span data-stu-id="71213-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71213-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71213-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71213-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71213-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71213-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="71213-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="71213-148">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="71213-148">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="71213-149">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="71213-149">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="71213-150">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="71213-150">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="71213-151">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="71213-151">**glReadPixels**</span></span>](glreadpixels.md)
</dt> </dl>

 

 





