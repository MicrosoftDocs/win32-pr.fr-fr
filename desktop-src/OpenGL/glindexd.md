---
title: fonction glIndexd (GL. h)
description: La fonction glIndexd définit l’index de couleur actuel.
ms.assetid: 4cd72d32-e796-4c94-94cb-591f1ee3b26e
keywords:
- glIndexd fonction OpenGL
topic_type:
- apiref
api_name:
- glIndexd
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5d1e7cce6ad2ae39e5ca107ef89b3b86147596e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941831"
---
# <a name="glindexd-function"></a><span data-ttu-id="d5e8d-104">glIndexd fonction)</span><span class="sxs-lookup"><span data-stu-id="d5e8d-104">glIndexd function</span></span>

<span data-ttu-id="d5e8d-105">La fonction **glIndexd** définit l’index de couleur actuel.</span><span class="sxs-lookup"><span data-stu-id="d5e8d-105">The **glIndexd** function sets the current color index.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5e8d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5e8d-106">Syntax</span></span>


```C++
void WINAPI glIndexd(
   GLdouble c
);
```



## <a name="parameters"></a><span data-ttu-id="d5e8d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5e8d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5e8d-108">*c*</span><span class="sxs-lookup"><span data-stu-id="d5e8d-108">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="d5e8d-109">Nouvelle valeur pour l’index de couleur actuel.</span><span class="sxs-lookup"><span data-stu-id="d5e8d-109">The new value for the current color index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5e8d-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d5e8d-110">Return value</span></span>

<span data-ttu-id="d5e8d-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d5e8d-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5e8d-112">Notes</span><span class="sxs-lookup"><span data-stu-id="d5e8d-112">Remarks</span></span>

<span data-ttu-id="d5e8d-113">La fonction **glIndexd** met à jour l’index de couleurs actuel (à valeur unique).</span><span class="sxs-lookup"><span data-stu-id="d5e8d-113">The **glIndexd** function updates the current (single-valued) color index.</span></span> <span data-ttu-id="d5e8d-114">Il accepte un argument : la nouvelle valeur pour l’index de couleur actuel.</span><span class="sxs-lookup"><span data-stu-id="d5e8d-114">It takes one argument: the new value for the current color index.</span></span>

<span data-ttu-id="d5e8d-115">L’index actuel est stocké sous la forme d’une valeur à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="d5e8d-115">The current index is stored as a floating-point value.</span></span> <span data-ttu-id="d5e8d-116">Les valeurs entières sont converties directement en valeurs à virgule flottante, sans mappage spécial.</span><span class="sxs-lookup"><span data-stu-id="d5e8d-116">Integer values are converted directly to floating-point values, with no special mapping.</span></span>

<span data-ttu-id="d5e8d-117">Les valeurs d’index situées en dehors de la plage représentable de la mémoire tampon d’index de couleurs ne sont pas ancrées.</span><span class="sxs-lookup"><span data-stu-id="d5e8d-117">Index values outside the representable range of the color-index buffer are not clamped.</span></span> <span data-ttu-id="d5e8d-118">Toutefois, avant qu’un index ne soit déformé (s’il est activé) et écrit dans le trame, il est converti au format à virgule fixe.</span><span class="sxs-lookup"><span data-stu-id="d5e8d-118">However, before an index is dithered (if enabled) and written to the framebuffer, it is converted to fixed-point format.</span></span> <span data-ttu-id="d5e8d-119">Tous les bits de la partie entière de la valeur à virgule fixe résultante qui ne correspondent pas aux bits dans le trame sont masqués.</span><span class="sxs-lookup"><span data-stu-id="d5e8d-119">Any bits in the integer portion of the resulting fixed-point value that do not correspond to bits in the framebuffer are masked out.</span></span>

<span data-ttu-id="d5e8d-120">L’index actuel peut être mis à jour à tout moment.</span><span class="sxs-lookup"><span data-stu-id="d5e8d-120">The current index can be updated at any time.</span></span> <span data-ttu-id="d5e8d-121">En particulier, **glIndexd** peut être appelé entre un appel à [**glBegin**](/windows/desktop/OpenGL/glbegin) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="d5e8d-121">In particular, **glIndexd** can be called between a call to [**glBegin**](/windows/desktop/OpenGL/glbegin) and the corresponding call to [**glEnd**](glend.md).</span></span>

<span data-ttu-id="d5e8d-122">La fonction suivante récupère des informations relatives à **glIndexd**:</span><span class="sxs-lookup"><span data-stu-id="d5e8d-122">The following function retrieves information related to **glIndexd**:</span></span>

<span data-ttu-id="d5e8d-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Current \_ index</span><span class="sxs-lookup"><span data-stu-id="d5e8d-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_INDEX</span></span>

## <a name="requirements"></a><span data-ttu-id="d5e8d-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5e8d-124">Requirements</span></span>



| <span data-ttu-id="d5e8d-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5e8d-125">Requirement</span></span> | <span data-ttu-id="d5e8d-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5e8d-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5e8d-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5e8d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d5e8d-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5e8d-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d5e8d-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5e8d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d5e8d-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5e8d-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d5e8d-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="d5e8d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5e8d-132"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5e8d-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d5e8d-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d5e8d-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="d5e8d-134"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5e8d-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d5e8d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d5e8d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5e8d-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5e8d-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5e8d-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5e8d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5e8d-138">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="d5e8d-138">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d5e8d-139">**glColor**</span><span class="sxs-lookup"><span data-stu-id="d5e8d-139">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="d5e8d-140">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="d5e8d-140">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d5e8d-141">**glGet**</span><span class="sxs-lookup"><span data-stu-id="d5e8d-141">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

