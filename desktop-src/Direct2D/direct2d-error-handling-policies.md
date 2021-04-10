---
title: Stratégies de gestion des erreurs Direct2D
description: Cette rubrique décrit les stratégies de gestion des erreurs Direct2D. Elle contient les sections suivantes.
ms.assetid: b5fa327a-a315-46fa-aa78-8a5733faae01
keywords:
- Direct2D, gestion des erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc930e7ee9e5b73b5f676103f45ffe25e4d4e61
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941275"
---
# <a name="direct2d-error-handling-policies"></a><span data-ttu-id="095c4-105">Stratégies de gestion des erreurs Direct2D</span><span class="sxs-lookup"><span data-stu-id="095c4-105">Direct2D Error Handling Policies</span></span>

<span data-ttu-id="095c4-106">Cette rubrique décrit les stratégies de gestion des erreurs Direct2D.</span><span class="sxs-lookup"><span data-stu-id="095c4-106">This topic describes the Direct2D error handling policies.</span></span> <span data-ttu-id="095c4-107">Elle contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="095c4-107">It contains the following sections.</span></span>

-   [<span data-ttu-id="095c4-108">Utilisation de HRESULT</span><span class="sxs-lookup"><span data-stu-id="095c4-108">Use of HRESULT</span></span>](#use-of-hresult)
-   [<span data-ttu-id="095c4-109">Valeur de retour des fonctions traitées par lot</span><span class="sxs-lookup"><span data-stu-id="095c4-109">Return Value of Batched Functions</span></span>](#return-value-of-batched-functions)
-   [<span data-ttu-id="095c4-110">Entrée non valide</span><span class="sxs-lookup"><span data-stu-id="095c4-110">Invalid Input</span></span>](#invalid-input)
    -   [<span data-ttu-id="095c4-111">Pointeur de sortie</span><span class="sxs-lookup"><span data-stu-id="095c4-111">Output Pointer</span></span>](#output-pointer)
    -   [<span data-ttu-id="095c4-112">Paramètre obligatoire</span><span class="sxs-lookup"><span data-stu-id="095c4-112">Required Parameter</span></span>](#required-parameter)
-   [<span data-ttu-id="095c4-113">RECTANGLEs d’entrée NaN et mal ordonnés</span><span class="sxs-lookup"><span data-stu-id="095c4-113">NaN and Poorly Ordered Input RECTs</span></span>](#nan-and-poorly-ordered-input-rects)
    -   [<span data-ttu-id="095c4-114">NaN comme entrée</span><span class="sxs-lookup"><span data-stu-id="095c4-114">NaN as Input</span></span>](#nan-as-input)
    -   [<span data-ttu-id="095c4-115">RECTo d’entrée mal ordonnés</span><span class="sxs-lookup"><span data-stu-id="095c4-115">Poorly Ordered Input RECTs</span></span>](#poorly-ordered-input-rects)

## <a name="use-of-hresult"></a><span data-ttu-id="095c4-116">Utilisation de HRESULT</span><span class="sxs-lookup"><span data-stu-id="095c4-116">Use of HRESULT</span></span>

<span data-ttu-id="095c4-117">Si une fonction n’est pas regroupée par lot et peut avoir un échec au moment de l’exécution, elle doit retourner **HRESULT** pour indiquer un échec.</span><span class="sxs-lookup"><span data-stu-id="095c4-117">If a function is not batched and can have a run-time failure, it should return **HRESULT** to indicate a failure.</span></span> <span data-ttu-id="095c4-118">Un échec au moment de l’exécution est un échec qui ne peut pas être évité au moment de la conception, par exemple en cas de mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="095c4-118">A run-time failure is any failure that cannot be avoided at design time, such as out of memory.</span></span>

## <a name="return-value-of-batched-functions"></a><span data-ttu-id="095c4-119">Valeur de retour des fonctions traitées par lot</span><span class="sxs-lookup"><span data-stu-id="095c4-119">Return Value of Batched Functions</span></span>

<span data-ttu-id="095c4-120">Les fonctions par lot dans Direct2D sont les fonctions traitées comme une unité unique lorsque [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) est appelé.</span><span class="sxs-lookup"><span data-stu-id="095c4-120">Batched functions in Direct2D are the functions that are processed as a single unit when [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) is called.</span></span> <span data-ttu-id="095c4-121">Il s’agit des commandes de dessin entre [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) et **EndDraw** ou des commandes sur [**GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink).</span><span class="sxs-lookup"><span data-stu-id="095c4-121">They are the drawing commands between [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) and **EndDraw** or commands on [**GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink).</span></span> <span data-ttu-id="095c4-122">Pour ces fonctions, des erreurs sont signalées au moment où le lot est terminé.</span><span class="sxs-lookup"><span data-stu-id="095c4-122">For these functions, errors are reported at the time the batch is completed.</span></span> <span data-ttu-id="095c4-123">L’erreur est retournée après **EndDraw** pour les commandes de dessin et après **fermeture** pour **GeometrySink**.</span><span class="sxs-lookup"><span data-stu-id="095c4-123">The error is returned after **EndDraw** for drawing commands, and after **Close** for **GeometrySink**.</span></span>

<span data-ttu-id="095c4-124">RenderTargets arrête le dessin si un état d’erreur est défini, mais une application peut appeler [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) pour réinitialiser l’état d’erreur et reprendre le dessin.</span><span class="sxs-lookup"><span data-stu-id="095c4-124">RenderTargets stop drawing if an error state is set, but an application can call [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) to reset the error state and resume drawing.</span></span>

<span data-ttu-id="095c4-125">Les fonctions **obtenir** et **définir** n’ont aucune valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="095c4-125">**Get** and **Set** functions have no return value.</span></span> <span data-ttu-id="095c4-126">Toutefois, si une fonction **définie** a une entrée non valide, la couche de débogage génère un message.</span><span class="sxs-lookup"><span data-stu-id="095c4-126">However, if a **Set** function has an invalid input, the debug layer generates a message.</span></span> <span data-ttu-id="095c4-127">Dans ce cas, aucun État d’erreur n’est défini et la fonction **Set** ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="095c4-127">In this case, no error state is set and the **Set** function does nothing.</span></span>

## <a name="invalid-input"></a><span data-ttu-id="095c4-128">Entrée non valide</span><span class="sxs-lookup"><span data-stu-id="095c4-128">Invalid Input</span></span>

<span data-ttu-id="095c4-129">Direct2D déréférence les pointeurs de sortie et les paramètres requis, ce qui entraîne des violations d’accès lorsque les pointeurs ne sont pas valides ou **null**.</span><span class="sxs-lookup"><span data-stu-id="095c4-129">Direct2D dereferences output pointers and required parameters which result in access violations when the pointers are invalid or **NULL**.</span></span>

### <a name="output-pointer"></a><span data-ttu-id="095c4-130">Pointeur de sortie</span><span class="sxs-lookup"><span data-stu-id="095c4-130">Output Pointer</span></span>

<span data-ttu-id="095c4-131">Direct2D déréférence un pointeur de sortie et l’assigne à **null** immédiatement lors de l’entrée dans la fonction.</span><span class="sxs-lookup"><span data-stu-id="095c4-131">Direct2D dereferences an output pointer and assigns it to **NULL** immediately upon entering the function.</span></span> <span data-ttu-id="095c4-132">Cela provoque une violation d’accès si un appelant passe **null** comme pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="095c4-132">This causes an access violation if a caller passes in **NULL** as the pointer to the return value.</span></span> <span data-ttu-id="095c4-133">Cette stratégie s’applique également aux tableaux de pointeurs.</span><span class="sxs-lookup"><span data-stu-id="095c4-133">This policy also applies to arrays of pointers.</span></span> <span data-ttu-id="095c4-134">Pour les autres paramètres de sortie, tels qu’un struct, le déréférencement se produit plus tard et entraîne également une violation d’accès.</span><span class="sxs-lookup"><span data-stu-id="095c4-134">For other output parameters, such as a struct, the dereference happens later and also results in an access violation.</span></span> <span data-ttu-id="095c4-135">Toutefois, il existe des méthodes qui ont des pointeurs de sortie facultatifs (autrement dit, [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw), [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)) qui n’entraînent pas de violation d’accès.</span><span class="sxs-lookup"><span data-stu-id="095c4-135">However, there are some methods that have optional output pointers (that is, [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw), [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)) that will not cause an access violation.</span></span>

### <a name="required-parameter"></a><span data-ttu-id="095c4-136">Paramètre obligatoire</span><span class="sxs-lookup"><span data-stu-id="095c4-136">Required Parameter</span></span>

<span data-ttu-id="095c4-137">Si **null** est passé à une fonction nécessitant une valeur valide, la fonction déréférence le pointeur incorrect qui entraîne une violation d’accès.</span><span class="sxs-lookup"><span data-stu-id="095c4-137">If **NULL** is passed to any function requiring a valid value, the function dereferences the bad pointer early resulting in an access violation.</span></span> <span data-ttu-id="095c4-138">Pour les paramètres d’entrée facultatifs, la valeur **null** est une valeur valide qui produit une valeur par défaut raisonnable.</span><span class="sxs-lookup"><span data-stu-id="095c4-138">For optional input parameters, **NULL** is a valid value that results in some reasonable default.</span></span>

## <a name="nan-and-poorly-ordered-input-rects"></a><span data-ttu-id="095c4-139">RECTANGLEs d’entrée NaN et mal ordonnés</span><span class="sxs-lookup"><span data-stu-id="095c4-139">NaN and Poorly Ordered Input RECTs</span></span>

<span data-ttu-id="095c4-140">Dans Direct2D, NaN est considéré comme une entrée valide et les RECTos d’entrée mal ordonnés sont triés.</span><span class="sxs-lookup"><span data-stu-id="095c4-140">In Direct2D, NaN is considered a valid input and poorly ordered input RECTs are sorted.</span></span>

### <a name="nan-as-input"></a><span data-ttu-id="095c4-141">NaN comme entrée</span><span class="sxs-lookup"><span data-stu-id="095c4-141">NaN as Input</span></span>

<span data-ttu-id="095c4-142">NaN est considéré comme une entrée valide, bien qu’il résulte généralement de la primitive qui contient le dessin NaN not Drawing.</span><span class="sxs-lookup"><span data-stu-id="095c4-142">NaN is considered a valid input, though it typically results in the primitive that contains the NaN not drawing.</span></span> <span data-ttu-id="095c4-143">L’API Direct2D ne fournit pas de filtrage explicite de NaN pour valider l’entrée.</span><span class="sxs-lookup"><span data-stu-id="095c4-143">The Direct2D API does not provide explicit filtering of NaN to validate input.</span></span>

### <a name="poorly-ordered-input-rects"></a><span data-ttu-id="095c4-144">RECTo d’entrée mal ordonnés</span><span class="sxs-lookup"><span data-stu-id="095c4-144">Poorly Ordered Input RECTs</span></span>

<span data-ttu-id="095c4-145">Les RECTos d’entrée mal classés sont triés de sorte que les angles supérieur, gauche et inférieur sont correctement spécifiés.</span><span class="sxs-lookup"><span data-stu-id="095c4-145">Poorly ordered input RECTs are sorted so that the top, left and bottom, right corners are correctly specified.</span></span> <span data-ttu-id="095c4-146">Pour la sortie, les rectangles vides se présentent comme suit : {Infinity, Infinity, FloatMax, FloatMax}.</span><span class="sxs-lookup"><span data-stu-id="095c4-146">For output, empty rectangles look like this: {Infinity, Infinity, FloatMax, FloatMax}.</span></span>

 

 