---
title: fonction glAddSwapHintRectWIN (GL. h)
description: La fonction de rappel glAddSwapHintRectWIN spécifie un ensemble de rectangles à copier par SwapBuffers.
ms.assetid: f242e755-8e8a-471a-9884-47efa22a3de6
keywords:
- glAddSwapHintRectWIN fonction OpenGL
topic_type:
- apiref
api_name:
- glAddSwapHintRectWIN
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae3e10c2f51ff8d7c9763ff1dad7d09d800cd60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384832"
---
# <a name="gladdswaphintrectwin-function"></a><span data-ttu-id="707c9-104">glAddSwapHintRectWIN fonction)</span><span class="sxs-lookup"><span data-stu-id="707c9-104">glAddSwapHintRectWIN function</span></span>

<span data-ttu-id="707c9-105">La fonction de rappel **glAddSwapHintRectWIN** spécifie un ensemble de rectangles à copier par [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span><span class="sxs-lookup"><span data-stu-id="707c9-105">The **glAddSwapHintRectWIN** callback function specifies a set of rectangles that are to be copied by [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span></span>

## <a name="syntax"></a><span data-ttu-id="707c9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="707c9-106">Syntax</span></span>


```C++
void WINAPI glAddSwapHintRectWIN(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="707c9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="707c9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="707c9-108">*x*</span><span class="sxs-lookup"><span data-stu-id="707c9-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="707c9-109">Coordonnée *x*(en coordonnées de la fenêtre) de l’angle inférieur gauche du rectangle de la zone de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="707c9-109">The *x*-coordinate (in window coordinates) of the lower-left corner of the hint region rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="707c9-110">*y*</span><span class="sxs-lookup"><span data-stu-id="707c9-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="707c9-111">Coordonnée *y*(dans les coordonnées de la fenêtre) de l’angle inférieur gauche du rectangle de la zone d’indicateur.</span><span class="sxs-lookup"><span data-stu-id="707c9-111">The *y*-coordinate (in window coordinates) of the lower-left corner of the hint region rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="707c9-112">*width*</span><span class="sxs-lookup"><span data-stu-id="707c9-112">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="707c9-113">Largeur du rectangle de la zone d’indicateur.</span><span class="sxs-lookup"><span data-stu-id="707c9-113">The width of the hint region rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="707c9-114">*height*</span><span class="sxs-lookup"><span data-stu-id="707c9-114">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="707c9-115">Hauteur du rectangle de la zone de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="707c9-115">The height of the hint region rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="707c9-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="707c9-116">Return value</span></span>

<span data-ttu-id="707c9-117">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="707c9-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="707c9-118">Notes</span><span class="sxs-lookup"><span data-stu-id="707c9-118">Remarks</span></span>

<span data-ttu-id="707c9-119">La fonction **glAddSwapHintRectWIN** accélère l’animation en réduisant la quantité de redessin entre les frames.</span><span class="sxs-lookup"><span data-stu-id="707c9-119">The **glAddSwapHintRectWIN** function speeds up animation by reducing the amount of repainting between frames.</span></span> <span data-ttu-id="707c9-120">Avec **glAddSwapHintRectWIN**, vous spécifiez un ensemble de zones rectangulaires que vous souhaitez copier lorsque vous appelez [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span><span class="sxs-lookup"><span data-stu-id="707c9-120">With **glAddSwapHintRectWIN**, you specify a set of rectangular areas that you want copied when you call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span></span> <span data-ttu-id="707c9-121">Lorsque vous ne spécifiez pas de rectangles avec **glAddSwapHintRectWIN** avant d’appeler **SwapBuffers**, la totalité du trame est permutée.</span><span class="sxs-lookup"><span data-stu-id="707c9-121">When you do not specify any rectangles with **glAddSwapHintRectWIN** before calling **SwapBuffers**, the entire framebuffer is swapped.</span></span> <span data-ttu-id="707c9-122">L’utilisation de **glAddSwapHintRectWIN** pour copier uniquement les parties modifiées de la mémoire tampon peut augmenter considérablement les performances de **SwapBuffers**, en particulier lorsque **SwapBuffers** est implémenté dans le logiciel.</span><span class="sxs-lookup"><span data-stu-id="707c9-122">Using **glAddSwapHintRectWIN** to copy only changed parts of the buffer can significantly increase the performance of **SwapBuffers**, especially when **SwapBuffers** is implemented in software.</span></span>

<span data-ttu-id="707c9-123">La fonction **glAddSwapHintRectWIN** ajoute un rectangle à la région de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="707c9-123">The **glAddSwapHintRectWIN** function adds a rectangle to the hint region.</span></span> <span data-ttu-id="707c9-124">Lorsque l' \_ \_ indicateur de copie d’échange PFD de la structure de format de pixel [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) est défini, **SwapBuffers** utilise cette région pour découper la copie de la mémoire tampon d’arrière-plan dans la mémoire tampon d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="707c9-124">When the PFD\_SWAP\_COPY flag of the [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) pixel format structure is set, **SwapBuffers** uses this region to clip the copying of the back buffer to the front buffer.</span></span> <span data-ttu-id="707c9-125">Vous ne spécifiez pas la \_ \_ copie d’échange PFD ; elle est définie par le matériel de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="707c9-125">You don't specify PFD\_SWAP\_COPY; it is set by capable hardware.</span></span> <span data-ttu-id="707c9-126">La région de l’indicateur est effacée après chaque appel à **SwapBuffers**.</span><span class="sxs-lookup"><span data-stu-id="707c9-126">The hint region is cleared after each call to **SwapBuffers**.</span></span> <span data-ttu-id="707c9-127">Avec certaines configurations matérielles, **SwapBuffers** peut ignorer la région de l’indicateur et échanger la totalité de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="707c9-127">With some hardware configurations, **SwapBuffers** can ignore the hint region and exchange the entire buffer.</span></span> <span data-ttu-id="707c9-128">**SwapBuffers** est implémenté par le système, et non par l’application.</span><span class="sxs-lookup"><span data-stu-id="707c9-128">**SwapBuffers** is implemented by the system, not by the application.</span></span>

<span data-ttu-id="707c9-129">OpenGL conserve une région d’indication distincte pour chaque fenêtre.</span><span class="sxs-lookup"><span data-stu-id="707c9-129">OpenGL maintains a separate hint region for each window.</span></span> <span data-ttu-id="707c9-130">Quand vous appelez **glAddSwapHintRectWIN** sur n’importe quel contexte de rendu associé à une fenêtre, les rectangles d’indicateurs sont combinés dans une seule région.</span><span class="sxs-lookup"><span data-stu-id="707c9-130">When you call **glAddSwapHintRectWIN** on any rendering contexts associated with a window, the hint rectangles are combined into a single region.</span></span>

<span data-ttu-id="707c9-131">Appelez **glAddSwapHintRectWIN** avec un rectangle englobant pour chaque objet dessiné pour un frame et pour chaque rectangle effacé pour effacer les objets Frame précédents.</span><span class="sxs-lookup"><span data-stu-id="707c9-131">Call **glAddSwapHintRectWIN** with a bounding rectangle for each object drawn for a frame and for each rectangle cleared to erase previous frame objects.</span></span>

> [!Note]  
> <span data-ttu-id="707c9-132">La fonction **glAddSwapHintRectWIN** est une fonction d’extension qui ne fait pas partie de la bibliothèque OpenGL standard, mais qui fait partie de l’extension de l’indicateur de remplacement de Win pour le GL \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="707c9-132">The **glAddSwapHintRectWIN** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_WIN\_swap\_hint extension.</span></span> <span data-ttu-id="707c9-133">Pour vérifier si votre implémentation d’OpenGL prend en charge **glAddSwapHintRectWIN**, appelez **glGetString**( \_ Extensions GL).</span><span class="sxs-lookup"><span data-stu-id="707c9-133">To check whether your implementation of OpenGL supports **glAddSwapHintRectWIN**, call **glGetString**(GL\_EXTENSIONS).</span></span> <span data-ttu-id="707c9-134">Si elle retourne l' \_ \_ indicateur de remplacement du GL Win \_ , **glAddSwapHintRectWIN** est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="707c9-134">If it returns GL\_WIN\_swap\_hint, **glAddSwapHintRectWIN** is supported.</span></span> <span data-ttu-id="707c9-135">Pour obtenir l’adresse d’une fonction d’extension, appelez **wglGetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="707c9-135">To obtain the address of an extension function, call **wglGetProcAddress**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="707c9-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="707c9-136">Requirements</span></span>



| <span data-ttu-id="707c9-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="707c9-137">Requirement</span></span> | <span data-ttu-id="707c9-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="707c9-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="707c9-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="707c9-139">Minimum supported client</span></span><br/> | <span data-ttu-id="707c9-140">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="707c9-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="707c9-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="707c9-141">Minimum supported server</span></span><br/> | <span data-ttu-id="707c9-142">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="707c9-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="707c9-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="707c9-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="707c9-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="707c9-144"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="707c9-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="707c9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="707c9-146">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="707c9-146">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="707c9-147">**PIXELFORMATDESCRIPTOR**</span><span class="sxs-lookup"><span data-stu-id="707c9-147">**PIXELFORMATDESCRIPTOR**</span></span>](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)
</dt> <dt>

[<span data-ttu-id="707c9-148">**SwapBuffers**</span><span class="sxs-lookup"><span data-stu-id="707c9-148">**SwapBuffers**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)
</dt> <dt>

[<span data-ttu-id="707c9-149">**wglGetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="707c9-149">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





