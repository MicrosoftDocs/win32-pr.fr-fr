---
title: fonction glLineStipple (GL. h)
description: La fonction glLineStipple spécifie le modèle de stipple de ligne.
ms.assetid: 256d968c-9e72-4aec-9faf-afe70f1087a8
keywords:
- glLineStipple fonction OpenGL
topic_type:
- apiref
api_name:
- glLineStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b47202b25c0779a3daa0bd801900b1d29e0b37b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739797"
---
# <a name="gllinestipple-function"></a><span data-ttu-id="369ef-104">glLineStipple fonction)</span><span class="sxs-lookup"><span data-stu-id="369ef-104">glLineStipple function</span></span>

<span data-ttu-id="369ef-105">La fonction **glLineStipple** spécifie le modèle de stipple de ligne.</span><span class="sxs-lookup"><span data-stu-id="369ef-105">The **glLineStipple** function specifies the line stipple pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="369ef-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="369ef-106">Syntax</span></span>


```C++
void WINAPI glLineStipple(
   GLint    factor,
   GLushort pattern
);
```



## <a name="parameters"></a><span data-ttu-id="369ef-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="369ef-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="369ef-108">*factorisés*</span><span class="sxs-lookup"><span data-stu-id="369ef-108">*factor*</span></span> 
</dt> <dd>

<span data-ttu-id="369ef-109">Multiplicateur pour chaque bit dans le modèle stipple de la ligne.</span><span class="sxs-lookup"><span data-stu-id="369ef-109">A multiplier for each bit in the line stipple pattern.</span></span> <span data-ttu-id="369ef-110">Si *Factor* est égal à 3, par exemple, chaque bit du modèle sera utilisé trois fois avant l’utilisation du bit suivant dans le modèle.</span><span class="sxs-lookup"><span data-stu-id="369ef-110">If *factor* is 3, for example, each bit in the pattern will be used three times before the next bit in the pattern is used.</span></span> <span data-ttu-id="369ef-111">Le paramètre *Factor* est ancré à la plage \[ 1, 256 \] et prend par défaut la valeur un.</span><span class="sxs-lookup"><span data-stu-id="369ef-111">The *factor* parameter is clamped to the range \[1, 256\] and defaults to one.</span></span>

</dd> <dt>

<span data-ttu-id="369ef-112">*pattern*</span><span class="sxs-lookup"><span data-stu-id="369ef-112">*pattern*</span></span> 
</dt> <dd>

<span data-ttu-id="369ef-113">Entier 16 bits dont le modèle de bits détermine les fragments d’une ligne qui seront dessinés lorsque la ligne est pixellisée.</span><span class="sxs-lookup"><span data-stu-id="369ef-113">A 16-bit integer whose bit pattern determines which fragments of a line will be drawn when the line is rasterized.</span></span> <span data-ttu-id="369ef-114">Le bit zéro est utilisé en premier, et le modèle par défaut est All.</span><span class="sxs-lookup"><span data-stu-id="369ef-114">Bit zero is used first, and the default pattern is all ones.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="369ef-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="369ef-115">Return value</span></span>

<span data-ttu-id="369ef-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="369ef-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="369ef-117">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="369ef-117">Error codes</span></span>

<span data-ttu-id="369ef-118">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="369ef-118">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="369ef-119">Nom</span><span class="sxs-lookup"><span data-stu-id="369ef-119">Name</span></span>                                                                                                  | <span data-ttu-id="369ef-120">Signification</span><span class="sxs-lookup"><span data-stu-id="369ef-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="369ef-121"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="369ef-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="369ef-122">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="369ef-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="369ef-123">Notes</span><span class="sxs-lookup"><span data-stu-id="369ef-123">Remarks</span></span>

<span data-ttu-id="369ef-124">La fonction **glLineStipple** spécifie le modèle de stipple de ligne.</span><span class="sxs-lookup"><span data-stu-id="369ef-124">The **glLineStipple** function specifies the line stipple pattern.</span></span> <span data-ttu-id="369ef-125">La ligne stippling masque certains fragments produits par la pixellisation ; ces fragments ne seront pas dessinés.</span><span class="sxs-lookup"><span data-stu-id="369ef-125">Line stippling masks out certain fragments produced by rasterization; those fragments will not be drawn.</span></span> <span data-ttu-id="369ef-126">Le masquage est effectué à l’aide de trois paramètres : *le modèle de modèle stipple* de ligne de 16 bits, le *facteur* nombre de répétitions et *un compteur stipple* entier.</span><span class="sxs-lookup"><span data-stu-id="369ef-126">The masking is achieved by using three parameters: the 16-bit line stipple pattern *pattern*, the repeat count *factor*, and an integer stipple counter *s*.</span></span>

<span data-ttu-id="369ef-127">Le compteur *s* est remis à zéro chaque fois que [**glBegin**](glbegin.md) est appelé, et avant que chaque segment de ligne d’une séquence **glBegin**( \_ lignes GL)/**glEnd** soit généré.</span><span class="sxs-lookup"><span data-stu-id="369ef-127">Counter *s* is reset to zero whenever [**glBegin**](glbegin.md) is called, and before each line segment of a **glBegin**(GL\_LINES)/**glEnd** sequence is generated.</span></span> <span data-ttu-id="369ef-128">Il est incrémenté après la génération de chaque fragment d’un segment de ligne avec alias de largeur d’unité, ou après la génération *de chaque fragment* d’un segment de ligne de largeur *i* .</span><span class="sxs-lookup"><span data-stu-id="369ef-128">It is incremented after each fragment of a unit width aliased line segment is generated, or after each *i* fragments of an *i* width line segment are generated.</span></span> <span data-ttu-id="369ef-129">Les fragments *i* associés à Count *s* sont masqués si le bit de *motif* (  /  *facteur* s) mod 16 est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="369ef-129">The *i* fragments associated with count *s* are masked out if *pattern* bit (*s* / *factor*) mod 16 is zero.</span></span> <span data-ttu-id="369ef-130">Dans le cas contraire, ces fragments sont envoyés au trame.</span><span class="sxs-lookup"><span data-stu-id="369ef-130">Otherwise these fragments are sent to the framebuffer.</span></span> <span data-ttu-id="369ef-131">Le bit zéro du *modèle* est le bit le moins significatif.</span><span class="sxs-lookup"><span data-stu-id="369ef-131">Bit zero of *pattern* is the least significant bit.</span></span>

<span data-ttu-id="369ef-132">Les lignes avec un alias sont traitées comme une séquence de rectangles de *largeur* 1x à des fins de stippling.</span><span class="sxs-lookup"><span data-stu-id="369ef-132">Antialiased lines are treated as a sequence of 1x *width* rectangles for purposes of stippling.</span></span> <span data-ttu-id="369ef-133">Rectangle *s* est pixellisé ou non en fonction de la règle de fragmentation décrite pour les lignes avec alias ; elle compte des rectangles plutôt que des groupes de fragments.</span><span class="sxs-lookup"><span data-stu-id="369ef-133">Rectangle *s* is rasterized or not based on the fragment rule described for aliased lines; it counts rectangles rather than groups of fragments.</span></span>

<span data-ttu-id="369ef-134">La ligne stippling est activée ou désactivée à l’aide de [**glEnable**](glenable.md) et **glDisable** avec l’argument, \_ ligne \_ STIPPLE.</span><span class="sxs-lookup"><span data-stu-id="369ef-134">Line stippling is enabled or disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_LINE\_STIPPLE.</span></span> <span data-ttu-id="369ef-135">Quand cette option est activée, le modèle de stipple de ligne est appliqué comme décrit ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="369ef-135">When enabled, the line stipple pattern is applied as described above.</span></span> <span data-ttu-id="369ef-136">Quand elle est désactivée, elle est comme si le modèle était tous des.</span><span class="sxs-lookup"><span data-stu-id="369ef-136">When disabled, it is as if the pattern were all ones.</span></span> <span data-ttu-id="369ef-137">Au départ, la ligne stippling est désactivée.</span><span class="sxs-lookup"><span data-stu-id="369ef-137">Initially, line stippling is disabled.</span></span>

<span data-ttu-id="369ef-138">Les fonctions suivantes récupèrent les informations relatives à **glLineStipple**:</span><span class="sxs-lookup"><span data-stu-id="369ef-138">The following functions retrieve information related to **glLineStipple**:</span></span>

<span data-ttu-id="369ef-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument \_ modèle de \_ STIPPLE de ligne de GL \_</span><span class="sxs-lookup"><span data-stu-id="369ef-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LINE\_STIPPLE\_PATTERN</span></span>

<span data-ttu-id="369ef-140">**glGet** avec argument GL \_ line \_ STIPPLE \_ REPEAT</span><span class="sxs-lookup"><span data-stu-id="369ef-140">**glGet** with argument GL\_LINE\_STIPPLE\_REPEAT</span></span>

<span data-ttu-id="369ef-141">[**glIsEnabled**](glisenabled.md) avec argument GL \_ ligne \_ STIPPLE</span><span class="sxs-lookup"><span data-stu-id="369ef-141">[**glIsEnabled**](glisenabled.md) with argument GL\_LINE\_STIPPLE</span></span>

## <a name="requirements"></a><span data-ttu-id="369ef-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="369ef-142">Requirements</span></span>



| <span data-ttu-id="369ef-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="369ef-143">Requirement</span></span> | <span data-ttu-id="369ef-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="369ef-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="369ef-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="369ef-145">Minimum supported client</span></span><br/> | <span data-ttu-id="369ef-146">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="369ef-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="369ef-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="369ef-147">Minimum supported server</span></span><br/> | <span data-ttu-id="369ef-148">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="369ef-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="369ef-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="369ef-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="369ef-150"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="369ef-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="369ef-151">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="369ef-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="369ef-152"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="369ef-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="369ef-153">DLL</span><span class="sxs-lookup"><span data-stu-id="369ef-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="369ef-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="369ef-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="369ef-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="369ef-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="369ef-156">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="369ef-156">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="369ef-157">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="369ef-157">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="369ef-158">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="369ef-158">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="369ef-159">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="369ef-159">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> </dl>

 

 





