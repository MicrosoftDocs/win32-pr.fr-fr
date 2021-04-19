---
title: Gestion des erreurs dans COM (prise en main de Win32 et C++)
description: .
ms.assetid: 022ca652-59d2-4513-9d73-1c6d8688c478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505f8cfe6867db07da77616e6a94fdc257e32f3e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106511112"
---
# <a name="error-handling-in-com-get-started-with-win32-and-c"></a><span data-ttu-id="18dc1-103">Gestion des erreurs dans COM (prise en main de Win32 et C++)</span><span class="sxs-lookup"><span data-stu-id="18dc1-103">Error Handling in COM (Get Started with Win32 and C++)</span></span>

<span data-ttu-id="18dc1-104">COM utilise des valeurs **HRESULT** pour indiquer la réussite ou l’échec d’un appel de méthode ou de fonction.</span><span class="sxs-lookup"><span data-stu-id="18dc1-104">COM uses **HRESULT** values to indicate the success or failure of a method or function call.</span></span> <span data-ttu-id="18dc1-105">Divers en-têtes du kit de développement logiciel (SDK) définissent différentes constantes **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="18dc1-105">Various SDK headers define various **HRESULT** constants.</span></span> <span data-ttu-id="18dc1-106">Un ensemble commun de codes à l’ensemble du système est défini dans WinError. h.</span><span class="sxs-lookup"><span data-stu-id="18dc1-106">A common set of system-wide codes is defined in WinError.h.</span></span> <span data-ttu-id="18dc1-107">Le tableau suivant présente certains de ces codes de retour à l’ensemble du système.</span><span class="sxs-lookup"><span data-stu-id="18dc1-107">The following table shows some of those system-wide return codes.</span></span>



| <span data-ttu-id="18dc1-108">Constante</span><span class="sxs-lookup"><span data-stu-id="18dc1-108">Constant</span></span>            | <span data-ttu-id="18dc1-109">Valeur numérique</span><span class="sxs-lookup"><span data-stu-id="18dc1-109">Numeric value</span></span> | <span data-ttu-id="18dc1-110">Description</span><span class="sxs-lookup"><span data-stu-id="18dc1-110">Description</span></span>                                          |
|---------------------|---------------|------------------------------------------------------|
| <span data-ttu-id="18dc1-111">**\_ACCESSDENIED E**</span><span class="sxs-lookup"><span data-stu-id="18dc1-111">**E\_ACCESSDENIED**</span></span> | <span data-ttu-id="18dc1-112">0x80070005</span><span class="sxs-lookup"><span data-stu-id="18dc1-112">0x80070005</span></span>    | <span data-ttu-id="18dc1-113">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="18dc1-113">Access denied.</span></span>                                       |
| <span data-ttu-id="18dc1-114">**E \_ échec**</span><span class="sxs-lookup"><span data-stu-id="18dc1-114">**E\_FAIL**</span></span>         | <span data-ttu-id="18dc1-115">0x80004005</span><span class="sxs-lookup"><span data-stu-id="18dc1-115">0x80004005</span></span>    | <span data-ttu-id="18dc1-116">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="18dc1-116">Unspecified error.</span></span>                                   |
| <span data-ttu-id="18dc1-117">**E \_ INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="18dc1-117">**E\_INVALIDARG**</span></span>   | <span data-ttu-id="18dc1-118">0x80070057</span><span class="sxs-lookup"><span data-stu-id="18dc1-118">0x80070057</span></span>    | <span data-ttu-id="18dc1-119">Valeur de paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="18dc1-119">Invalid parameter value.</span></span>                             |
| <span data-ttu-id="18dc1-120">**\_OUTOFMEMORY E**</span><span class="sxs-lookup"><span data-stu-id="18dc1-120">**E\_OUTOFMEMORY**</span></span>  | <span data-ttu-id="18dc1-121">0x8007000E</span><span class="sxs-lookup"><span data-stu-id="18dc1-121">0x8007000E</span></span>    | <span data-ttu-id="18dc1-122">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="18dc1-122">Out of memory.</span></span>                                       |
| <span data-ttu-id="18dc1-123">**\_pointeur E**</span><span class="sxs-lookup"><span data-stu-id="18dc1-123">**E\_POINTER**</span></span>      | <span data-ttu-id="18dc1-124">0x80004003</span><span class="sxs-lookup"><span data-stu-id="18dc1-124">0x80004003</span></span>    | <span data-ttu-id="18dc1-125">La valeur **null** a été transmise de manière incorrecte pour une valeur de pointeur.</span><span class="sxs-lookup"><span data-stu-id="18dc1-125">**NULL** was passed incorrectly for a pointer value.</span></span> |
| <span data-ttu-id="18dc1-126">**E \_ inattendu**</span><span class="sxs-lookup"><span data-stu-id="18dc1-126">**E\_UNEXPECTED**</span></span>   | <span data-ttu-id="18dc1-127">0x8000FFFF</span><span class="sxs-lookup"><span data-stu-id="18dc1-127">0x8000FFFF</span></span>    | <span data-ttu-id="18dc1-128">Condition inattendue.</span><span class="sxs-lookup"><span data-stu-id="18dc1-128">Unexpected condition.</span></span>                                |
| <span data-ttu-id="18dc1-129">**\_OK**</span><span class="sxs-lookup"><span data-stu-id="18dc1-129">**S\_OK**</span></span>           | <span data-ttu-id="18dc1-130">0x0</span><span class="sxs-lookup"><span data-stu-id="18dc1-130">0x0</span></span>           | <span data-ttu-id="18dc1-131">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="18dc1-131">Success.</span></span>                                             |
| <span data-ttu-id="18dc1-132">**S \_ false**</span><span class="sxs-lookup"><span data-stu-id="18dc1-132">**S\_FALSE**</span></span>        | <span data-ttu-id="18dc1-133">0x1</span><span class="sxs-lookup"><span data-stu-id="18dc1-133">0x1</span></span>           | <span data-ttu-id="18dc1-134">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="18dc1-134">Success.</span></span>                                             |



 

<span data-ttu-id="18dc1-135">Toutes les constantes avec le préfixe « E \_ » sont des codes d’erreur.</span><span class="sxs-lookup"><span data-stu-id="18dc1-135">All of the constants with the prefix "E\_" are error codes.</span></span> <span data-ttu-id="18dc1-136">Les constantes **s \_ OK** et **s \_ false** sont les deux codes de réussite.</span><span class="sxs-lookup"><span data-stu-id="18dc1-136">The constants **S\_OK** and **S\_FALSE** are both success codes.</span></span> <span data-ttu-id="18dc1-137">Il se peut que 99% des méthodes COM retournent **S \_ OK** quand elles ont été correctement exécutées, mais n’autorisent pas ce fait à vous tromper.</span><span class="sxs-lookup"><span data-stu-id="18dc1-137">Probably 99% of COM methods return **S\_OK** when they succeed; but do not let this fact mislead you.</span></span> <span data-ttu-id="18dc1-138">Une méthode peut retourner d’autres codes de réussite, donc toujours tester les erreurs à l’aide de la macro [**Succeeded**](/windows/desktop/api/winerror/nf-winerror-succeeded) ou [**failed**](/windows/desktop/api/winerror/nf-winerror-failed) .</span><span class="sxs-lookup"><span data-stu-id="18dc1-138">A method might return other success codes, so always test for errors by using the [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) or [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro.</span></span> <span data-ttu-id="18dc1-139">L’exemple de code suivant montre une méthode incorrecte et la bonne façon de tester la réussite d’un appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="18dc1-139">The following example code shows the wrong way and the right way to test for the success of a function call.</span></span>


```C++
// Wrong.
HRESULT hr = SomeFunction();
if (hr != S_OK)
{
    printf("Error!\n"); // Bad. hr might be another success code.
}

// Right.
HRESULT hr = SomeFunction();
if (FAILED(hr))
{
    printf("Error!\n"); 
}
```



<span data-ttu-id="18dc1-140">Le code de réussite **S \_ false** mérite de mentionner.</span><span class="sxs-lookup"><span data-stu-id="18dc1-140">The success code **S\_FALSE** deserves mention.</span></span> <span data-ttu-id="18dc1-141">Certaines méthodes utilisent **S \_ false** pour signifier, à peu près, une condition négative qui n’est pas un échec.</span><span class="sxs-lookup"><span data-stu-id="18dc1-141">Some methods use **S\_FALSE** to mean, roughly, a negative condition that is not a failure.</span></span> <span data-ttu-id="18dc1-142">Il peut également indiquer un « no-op », la méthode a réussi, mais n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="18dc1-142">It can also indicate a "no-op"—the method succeeded, but had no effect.</span></span> <span data-ttu-id="18dc1-143">Par exemple, la fonction [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) retourne **S \_ false** si vous l’appelez une deuxième fois à partir du même thread.</span><span class="sxs-lookup"><span data-stu-id="18dc1-143">For example, the [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) function returns **S\_FALSE** if you call it a second time from the same thread.</span></span> <span data-ttu-id="18dc1-144">Si vous avez besoin de faire la distinction entre **s \_ OK** et **s \_ false** dans votre code, vous devez tester la valeur directement, mais utilisez toujours l' [**échec**](/windows/desktop/api/winerror/nf-winerror-failed) ou le [**succès**](/windows/desktop/api/winerror/nf-winerror-succeeded) pour gérer les cas restants, comme illustré dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="18dc1-144">If you need to differentiate between **S\_OK** and **S\_FALSE** in your code, you should test the value directly, but still use [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) or [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) to handle the remaining cases, as shown in the following example code.</span></span>


```C++
if (hr == S_FALSE)
{
    // Handle special case.
}
else if (SUCCEEDED(hr))
{
    // Handle general success case.
}
else
{
    // Handle errors.
    printf("Error!\n"); 
}
```



<span data-ttu-id="18dc1-145">Certaines valeurs **HRESULT** sont spécifiques à une fonctionnalité particulière ou à un sous-système de Windows.</span><span class="sxs-lookup"><span data-stu-id="18dc1-145">Some **HRESULT** values are specific to a particular feature or subsystem of Windows.</span></span> <span data-ttu-id="18dc1-146">Par exemple, l’API graphique Direct2D définit le code d’erreur **D2DERR \_ \_ \_ format de pixel non pris en charge**, ce qui signifie que le programme a utilisé un format de pixel non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="18dc1-146">For example, the Direct2D graphics API defines the error code **D2DERR\_UNSUPPORTED\_PIXEL\_FORMAT**, which means that the program used an unsupported pixel format.</span></span> <span data-ttu-id="18dc1-147">La documentation MSDN fournit souvent une liste de codes d’erreur spécifiques qu’une méthode peut retourner.</span><span class="sxs-lookup"><span data-stu-id="18dc1-147">MSDN documentation often gives a list of specific error codes that a method might return.</span></span> <span data-ttu-id="18dc1-148">Toutefois, vous ne devez pas considérer que ces listes sont définitives.</span><span class="sxs-lookup"><span data-stu-id="18dc1-148">However, you should not consider these lists to be definitive.</span></span> <span data-ttu-id="18dc1-149">Une méthode peut toujours retourner une valeur **HRESULT** qui n’est pas indiquée dans la documentation.</span><span class="sxs-lookup"><span data-stu-id="18dc1-149">A method can always return an **HRESULT** value that is not listed in the documentation.</span></span> <span data-ttu-id="18dc1-150">Là encore, utilisez les macros ayant [**réussi**](/windows/desktop/api/winerror/nf-winerror-succeeded) et [**échoué**](/windows/desktop/api/winerror/nf-winerror-failed) .</span><span class="sxs-lookup"><span data-stu-id="18dc1-150">Again, use the [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) and [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macros.</span></span> <span data-ttu-id="18dc1-151">Si vous testez un code d’erreur spécifique, incluez également un cas par défaut.</span><span class="sxs-lookup"><span data-stu-id="18dc1-151">If you test for a specific error code, include a default case as well.</span></span>


```C++
if (hr == D2DERR_UNSUPPORTED_PIXEL_FORMAT)
{
    // Handle the specific case of an unsupported pixel format.
}
else if (FAILED(hr))
{
    // Handle other errors.
}
```



## <a name="patterns-for-error-handling"></a><span data-ttu-id="18dc1-152">Modèles pour la gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="18dc1-152">Patterns for Error Handling</span></span>

<span data-ttu-id="18dc1-153">Cette section présente certains modèles pour la gestion structurée des erreurs COM.</span><span class="sxs-lookup"><span data-stu-id="18dc1-153">This section looks at some patterns for handling COM errors in a structured way.</span></span> <span data-ttu-id="18dc1-154">Chaque modèle présente des avantages et des inconvénients.</span><span class="sxs-lookup"><span data-stu-id="18dc1-154">Each pattern has advantages and disadvantages.</span></span> <span data-ttu-id="18dc1-155">Dans une certaine mesure, le choix est une question de saveur.</span><span class="sxs-lookup"><span data-stu-id="18dc1-155">To some extent, the choice is a matter of taste.</span></span> <span data-ttu-id="18dc1-156">Si vous travaillez sur un projet existant, il a peut-être déjà des instructions de codage qui découpent un style particulier.</span><span class="sxs-lookup"><span data-stu-id="18dc1-156">If you work on an existing project, it might already have coding guidelines that proscribe a particular style.</span></span> <span data-ttu-id="18dc1-157">Quel que soit le modèle que vous adoptez, le code fiable obéit aux règles suivantes.</span><span class="sxs-lookup"><span data-stu-id="18dc1-157">Regardless of which pattern you adopt, robust code will obey the following rules.</span></span>

-   <span data-ttu-id="18dc1-158">Pour chaque méthode ou fonction qui retourne un **HRESULT**, vérifiez la valeur de retour avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="18dc1-158">For every method or function that returns an **HRESULT**, check the return value before proceeding.</span></span>
-   <span data-ttu-id="18dc1-159">Libérer des ressources une fois qu’elles sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="18dc1-159">Release resources after they are used.</span></span>
-   <span data-ttu-id="18dc1-160">N’essayez pas d’accéder à des ressources non valides ou non initialisées, telles que des pointeurs **null** .</span><span class="sxs-lookup"><span data-stu-id="18dc1-160">Do not attempt to access invalid or uninitialized resources, such as **NULL** pointers.</span></span>
-   <span data-ttu-id="18dc1-161">N’essayez pas d’utiliser une ressource après l’avoir libérée.</span><span class="sxs-lookup"><span data-stu-id="18dc1-161">Do not try to use a resource after you release it.</span></span>

<span data-ttu-id="18dc1-162">Avec ces règles à l’esprit, Voici quatre modèles pour la gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="18dc1-162">With these rules in mind, here are four patterns for handling errors.</span></span>

-   [<span data-ttu-id="18dc1-163">IFS imbriqué</span><span class="sxs-lookup"><span data-stu-id="18dc1-163">Nested ifs</span></span>](#nested-ifs)
-   [<span data-ttu-id="18dc1-164">IFS en cascade</span><span class="sxs-lookup"><span data-stu-id="18dc1-164">Cascading ifs</span></span>](#cascading-ifs)
-   [<span data-ttu-id="18dc1-165">Sauter en cas d’échec</span><span class="sxs-lookup"><span data-stu-id="18dc1-165">Jump on Fail</span></span>](#jump-on-fail)
-   [<span data-ttu-id="18dc1-166">Lever en cas d’échec</span><span class="sxs-lookup"><span data-stu-id="18dc1-166">Throw on Fail</span></span>](#throw-on-fail)

### <a name="nested-ifs"></a><span data-ttu-id="18dc1-167">IFS imbriqué</span><span class="sxs-lookup"><span data-stu-id="18dc1-167">Nested ifs</span></span>

<span data-ttu-id="18dc1-168">Après chaque appel qui retourne un **HRESULT**, utilisez une instruction **If** pour tester la réussite.</span><span class="sxs-lookup"><span data-stu-id="18dc1-168">After every call that returns an **HRESULT**, use an **if** statement to test for success.</span></span> <span data-ttu-id="18dc1-169">Ensuite, placez l’appel de méthode suivant dans la portée de l’instruction **If** .</span><span class="sxs-lookup"><span data-stu-id="18dc1-169">Then, put the next method call within the scope of the **if** statement.</span></span> <span data-ttu-id="18dc1-170">Plus d’instructions **If** peuvent être imbriquées aussi profondément que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="18dc1-170">More **if** statements can be nested as deeply as needed.</span></span> <span data-ttu-id="18dc1-171">Les exemples de code précédents de ce module ont tous utilisé ce modèle, mais ici encore :</span><span class="sxs-lookup"><span data-stu-id="18dc1-171">The previous code examples in this module have all used this pattern, but here it is again:</span></span>


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                // Use pItem (not shown). 
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    return hr;
}
```



<span data-ttu-id="18dc1-172">Avantages</span><span class="sxs-lookup"><span data-stu-id="18dc1-172">Advantages</span></span>

-   <span data-ttu-id="18dc1-173">Les variables peuvent être déclarées avec une étendue minimale.</span><span class="sxs-lookup"><span data-stu-id="18dc1-173">Variables can be declared with minimal scope.</span></span> <span data-ttu-id="18dc1-174">Par exemple, *pItem* n’est pas déclaré tant qu’il n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="18dc1-174">For example, *pItem* is not declared until it is used.</span></span>
-   <span data-ttu-id="18dc1-175">Dans chaque instruction **If** , certains invariants sont vrais : tous les appels précédents ont réussi et toutes les ressources acquises sont toujours valides.</span><span class="sxs-lookup"><span data-stu-id="18dc1-175">Within each **if** statement, certain invariants are true: All previous calls have succeeded, and all acquired resources are still valid.</span></span> <span data-ttu-id="18dc1-176">Dans l’exemple précédent, lorsque le programme atteint l’instruction **If** la plus profonde, *pItem* et *pFileOpen* sont reconnus comme étant valides.</span><span class="sxs-lookup"><span data-stu-id="18dc1-176">In the previous example, when the program reaches the innermost **if** statement, both *pItem* and *pFileOpen* are known to be valid.</span></span>
-   <span data-ttu-id="18dc1-177">Il est clair quand il faut libérer des pointeurs d’interface et d’autres ressources.</span><span class="sxs-lookup"><span data-stu-id="18dc1-177">It is clear when to release interface pointers and other resources.</span></span> <span data-ttu-id="18dc1-178">Vous publiez une ressource à la fin de l’instruction **If** qui suit immédiatement l’appel qui a acquis la ressource.</span><span class="sxs-lookup"><span data-stu-id="18dc1-178">You release a resource at the end of the **if** statement that immediately follows the call that acquired the resource.</span></span>

<span data-ttu-id="18dc1-179">Inconvénients</span><span class="sxs-lookup"><span data-stu-id="18dc1-179">Disadvantages</span></span>

-   <span data-ttu-id="18dc1-180">Certaines personnes recherchent une imbrication profonde difficile à lire.</span><span class="sxs-lookup"><span data-stu-id="18dc1-180">Some people find deep nesting hard to read.</span></span>
-   <span data-ttu-id="18dc1-181">La gestion des erreurs est mélangée à d’autres instructions de création de branche et de bouclage.</span><span class="sxs-lookup"><span data-stu-id="18dc1-181">Error handling is mixed in with other branching and looping statements.</span></span> <span data-ttu-id="18dc1-182">Cela peut rendre la logique de programme globale plus difficile à suivre.</span><span class="sxs-lookup"><span data-stu-id="18dc1-182">This can make the overall program logic harder to follow.</span></span>

### <a name="cascading-ifs"></a><span data-ttu-id="18dc1-183">IFS en cascade</span><span class="sxs-lookup"><span data-stu-id="18dc1-183">Cascading ifs</span></span>

<span data-ttu-id="18dc1-184">Après chaque appel de méthode, utilisez une instruction **If** pour tester la réussite.</span><span class="sxs-lookup"><span data-stu-id="18dc1-184">After each method call, use an **if** statement to test for success.</span></span> <span data-ttu-id="18dc1-185">Si la méthode est réussie, placez l’appel de méthode suivant à l’intérieur du bloc **If** .</span><span class="sxs-lookup"><span data-stu-id="18dc1-185">If the method succeeds, place the next method call inside the **if** block.</span></span> <span data-ttu-id="18dc1-186">Mais au lieu d’imbriquer d’autres instructions **If** , placez chaque test [**réussi**](/windows/desktop/api/winerror/nf-winerror-succeeded) suivant après le bloc **If** précédent.</span><span class="sxs-lookup"><span data-stu-id="18dc1-186">But instead of nesting further **if** statements, place each subsequent [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) test after the previous **if** block.</span></span> <span data-ttu-id="18dc1-187">Si une méthode échoue, tous les tests **réussis** restants échouent uniquement jusqu’à ce que le bas de la fonction soit atteint.</span><span class="sxs-lookup"><span data-stu-id="18dc1-187">If any method fails, all the remaining **SUCCEEDED** tests simply fail until the bottom of the function is reached.</span></span>


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->GetResult(&pItem);
    }
    if (SUCCEEDED(hr))
    {
        // Use pItem (not shown).
    }

    // Clean up.
    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
    return hr;
}
```



<span data-ttu-id="18dc1-188">Dans ce modèle, vous libérez des ressources à la fin de la fonction.</span><span class="sxs-lookup"><span data-stu-id="18dc1-188">In this pattern, you release resources at the very end of the function.</span></span> <span data-ttu-id="18dc1-189">Si une erreur se produit, certains pointeurs peuvent être non valides lorsque la fonction se termine.</span><span class="sxs-lookup"><span data-stu-id="18dc1-189">If an error occurs, some pointers might be invalid when the function exits.</span></span> <span data-ttu-id="18dc1-190">L’appel de [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur un pointeur non valide entraîne un blocage du programme (ou pire). vous devez donc initialiser tous les pointeurs vers la **valeur null** et vérifier s’ils ont la **valeur null** avant de les libérer.</span><span class="sxs-lookup"><span data-stu-id="18dc1-190">Calling [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on an invalid pointer will crash the program (or worse), so you must initialize all pointers to **NULL** and check whether they are **NULL** before releasing them.</span></span> <span data-ttu-id="18dc1-191">Cet exemple utilise la `SafeRelease` fonction ; les pointeurs intelligents sont également un bon choix.</span><span class="sxs-lookup"><span data-stu-id="18dc1-191">This example uses the `SafeRelease` function; smart pointers are also a good choice.</span></span>

<span data-ttu-id="18dc1-192">Si vous utilisez ce modèle, vous devez faire attention aux constructions de boucle.</span><span class="sxs-lookup"><span data-stu-id="18dc1-192">If you use this pattern, you must be careful with loop constructs.</span></span> <span data-ttu-id="18dc1-193">À l’intérieur d’une boucle, arrêter à partir de la boucle en cas d’échec d’un appel.</span><span class="sxs-lookup"><span data-stu-id="18dc1-193">Inside a loop, break from the loop if any call fails.</span></span>

<span data-ttu-id="18dc1-194">Avantages</span><span class="sxs-lookup"><span data-stu-id="18dc1-194">Advantages</span></span>

-   <span data-ttu-id="18dc1-195">Ce modèle crée moins d’imbrication que le modèle « IFS imbriqué ».</span><span class="sxs-lookup"><span data-stu-id="18dc1-195">This pattern creates less nesting than the "nested ifs" pattern.</span></span>
-   <span data-ttu-id="18dc1-196">Le workflow de contrôle global est plus facile à voir.</span><span class="sxs-lookup"><span data-stu-id="18dc1-196">Overall control flow is easier to see.</span></span>
-   <span data-ttu-id="18dc1-197">Les ressources sont libérées à un seul point du code.</span><span class="sxs-lookup"><span data-stu-id="18dc1-197">Resources are released at one point in the code.</span></span>

<span data-ttu-id="18dc1-198">Inconvénients</span><span class="sxs-lookup"><span data-stu-id="18dc1-198">Disadvantages</span></span>

-   <span data-ttu-id="18dc1-199">Toutes les variables doivent être déclarées et initialisées en haut de la fonction.</span><span class="sxs-lookup"><span data-stu-id="18dc1-199">All variables must be declared and initialized at the top of the function.</span></span>
-   <span data-ttu-id="18dc1-200">Si un appel échoue, la fonction effectue plusieurs vérifications d’erreurs inutiles au lieu de quitter la fonction immédiatement.</span><span class="sxs-lookup"><span data-stu-id="18dc1-200">If a call fails, the function makes multiple unneeded error checks, instead of exiting the function immediately.</span></span>
-   <span data-ttu-id="18dc1-201">Étant donné que le déroulement du contrôle continue via la fonction après une défaillance, vous devez faire attention dans le corps de la fonction et non pas pour accéder aux ressources non valides.</span><span class="sxs-lookup"><span data-stu-id="18dc1-201">Because the flow of control continues through the function after a failure, you must be careful throughout the body of the function not to access invalid resources.</span></span>
-   <span data-ttu-id="18dc1-202">Les erreurs à l’intérieur d’une boucle requièrent un cas particulier.</span><span class="sxs-lookup"><span data-stu-id="18dc1-202">Errors inside a loop require a special case.</span></span>

### <a name="jump-on-fail"></a><span data-ttu-id="18dc1-203">Sauter en cas d’échec</span><span class="sxs-lookup"><span data-stu-id="18dc1-203">Jump on Fail</span></span>

<span data-ttu-id="18dc1-204">Après chaque appel de méthode, tester l’échec (pas de succès).</span><span class="sxs-lookup"><span data-stu-id="18dc1-204">After each method call, test for failure (not success).</span></span> <span data-ttu-id="18dc1-205">En cas d’échec, accédez à une étiquette près du bas de la fonction.</span><span class="sxs-lookup"><span data-stu-id="18dc1-205">On failure, jump to a label near the bottom of the function.</span></span> <span data-ttu-id="18dc1-206">Après l’étiquette, mais avant de quitter la fonction, libérez des ressources.</span><span class="sxs-lookup"><span data-stu-id="18dc1-206">After the label, but before exiting the function, release resources.</span></span>


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pFileOpen->Show(NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pFileOpen->GetResult(&pItem);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use pItem (not shown).

done:
    // Clean up.
    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
    return hr;
}
```



<span data-ttu-id="18dc1-207">Avantages</span><span class="sxs-lookup"><span data-stu-id="18dc1-207">Advantages</span></span>

-   <span data-ttu-id="18dc1-208">Le workflow de contrôle global est facile à voir.</span><span class="sxs-lookup"><span data-stu-id="18dc1-208">The overall control flow is easy to see.</span></span>
-   <span data-ttu-id="18dc1-209">À chaque point du code après un [**échec**](/windows/desktop/api/winerror/nf-winerror-failed) de vérification, si vous n’avez pas sauté l’étiquette, il est garanti que tous les appels précédents ont réussi.</span><span class="sxs-lookup"><span data-stu-id="18dc1-209">At every point in the code after a [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) check, if you have not jumped to the label, it is guaranteed that all the previous calls have succeeded.</span></span>
-   <span data-ttu-id="18dc1-210">Les ressources sont libérées à un seul emplacement dans le code.</span><span class="sxs-lookup"><span data-stu-id="18dc1-210">Resources are released at one place in the code.</span></span>

<span data-ttu-id="18dc1-211">Inconvénients</span><span class="sxs-lookup"><span data-stu-id="18dc1-211">Disadvantages</span></span>

-   <span data-ttu-id="18dc1-212">Toutes les variables doivent être déclarées et initialisées en haut de la fonction.</span><span class="sxs-lookup"><span data-stu-id="18dc1-212">All variables must be declared and initialized at the top of the function.</span></span>
-   <span data-ttu-id="18dc1-213">Certains programmeurs n’aiment pas utiliser **goto** dans leur code.</span><span class="sxs-lookup"><span data-stu-id="18dc1-213">Some programmers do not like to use **goto** in their code.</span></span> <span data-ttu-id="18dc1-214">(Toutefois, il convient de noter que cette utilisation de **goto** est très structurée ; le code ne passe jamais en dehors de l’appel de fonction actuel.)</span><span class="sxs-lookup"><span data-stu-id="18dc1-214">(However, it should be noted that this use of **goto** is highly structured; the code never jumps outside the current function call.)</span></span>
-   <span data-ttu-id="18dc1-215">les instructions **goto** ignorent les initialiseurs.</span><span class="sxs-lookup"><span data-stu-id="18dc1-215">**goto** statements skip initializers.</span></span>

### <a name="throw-on-fail"></a><span data-ttu-id="18dc1-216">Lever en cas d’échec</span><span class="sxs-lookup"><span data-stu-id="18dc1-216">Throw on Fail</span></span>

<span data-ttu-id="18dc1-217">Au lieu d’accéder à une étiquette, vous pouvez lever une exception en cas d’échec d’une méthode.</span><span class="sxs-lookup"><span data-stu-id="18dc1-217">Rather than jump to a label, you can throw an exception when a method fails.</span></span> <span data-ttu-id="18dc1-218">Cela peut générer un style plus idiomatique C++ si vous êtes utilisé pour écrire du code sécurisé à l’exception.</span><span class="sxs-lookup"><span data-stu-id="18dc1-218">This can produce a more idiomatic style of C++ if you are used to writing exception-safe code.</span></span>


```C++
#include <comdef.h>  // Declares _com_error

inline void throw_if_fail(HRESULT hr)
{
    if (FAILED(hr))
    {
        throw _com_error(hr);
    }
}

void ShowDialog()
{
    try
    {
        CComPtr<IFileOpenDialog> pFileOpen;
        throw_if_fail(CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen)));

        throw_if_fail(pFileOpen->Show(NULL));

        CComPtr<IShellItem> pItem;
        throw_if_fail(pFileOpen->GetResult(&pItem));

        // Use pItem (not shown).
    }
    catch (_com_error err)
    {
        // Handle error.
    }
}
```



<span data-ttu-id="18dc1-219">Notez que cet exemple utilise la classe **CComPtr** pour gérer les pointeurs d’interface.</span><span class="sxs-lookup"><span data-stu-id="18dc1-219">Notice that this example uses the **CComPtr** class to manage interface pointers.</span></span> <span data-ttu-id="18dc1-220">En général, si votre code lève des exceptions, vous devez suivre le modèle RAII (Resource Acquisition Is Initialization).</span><span class="sxs-lookup"><span data-stu-id="18dc1-220">Generally, if your code throws exceptions, you should follow the RAII (Resource Acquisition is Initialization) pattern.</span></span> <span data-ttu-id="18dc1-221">Autrement dit, chaque ressource doit être gérée par un objet dont le destructeur garantit que la ressource est libérée correctement.</span><span class="sxs-lookup"><span data-stu-id="18dc1-221">That is, every resource should be managed by an object whose destructor guarantees that the resource is correctly released.</span></span> <span data-ttu-id="18dc1-222">Si une exception est levée, il est garanti que le destructeur est appelé.</span><span class="sxs-lookup"><span data-stu-id="18dc1-222">If an exception is thrown, the destructor is guaranteed to be invoked.</span></span> <span data-ttu-id="18dc1-223">Dans le cas contraire, votre programme peut provoquer des fuites de ressources.</span><span class="sxs-lookup"><span data-stu-id="18dc1-223">Otherwise, your program might leak resources.</span></span>

<span data-ttu-id="18dc1-224">Avantages</span><span class="sxs-lookup"><span data-stu-id="18dc1-224">Advantages</span></span>

-   <span data-ttu-id="18dc1-225">Compatible avec le code existant qui utilise la gestion des exceptions.</span><span class="sxs-lookup"><span data-stu-id="18dc1-225">Compatible with existing code that uses exception handling.</span></span>
-   <span data-ttu-id="18dc1-226">Compatible avec les bibliothèques C++ qui lèvent des exceptions, telles que la bibliothèque STL (Standard Template Library).</span><span class="sxs-lookup"><span data-stu-id="18dc1-226">Compatible with C++ libraries that throw exceptions, such as the Standard Template Library (STL).</span></span>

<span data-ttu-id="18dc1-227">Inconvénients</span><span class="sxs-lookup"><span data-stu-id="18dc1-227">Disadvantages</span></span>

-   <span data-ttu-id="18dc1-228">Requiert des objets C++ pour gérer des ressources telles que la mémoire ou les handles de fichiers.</span><span class="sxs-lookup"><span data-stu-id="18dc1-228">Requires C++ objects to manage resources such as memory or file handles.</span></span>
-   <span data-ttu-id="18dc1-229">Nécessite une bonne compréhension de la manière d’écrire du code sécurisé contre les exceptions.</span><span class="sxs-lookup"><span data-stu-id="18dc1-229">Requires a good understanding of how to write exception-safe code.</span></span>

## <a name="next"></a><span data-ttu-id="18dc1-230">Suivant</span><span class="sxs-lookup"><span data-stu-id="18dc1-230">Next</span></span>

[<span data-ttu-id="18dc1-231">Module 3. Graphiques Windows</span><span class="sxs-lookup"><span data-stu-id="18dc1-231">Module 3. Windows Graphics</span></span>](module-3---windows-graphics.md)

 

 
