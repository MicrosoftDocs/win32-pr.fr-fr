---
title: Création d’un objet dans COM
description: Pour utiliser une interface COM, votre programme crée d’abord une instance d’un objet qui implémente cette interface.
ms.assetid: 75f2115d-d49d-4e4e-8f99-67a231559ba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f96e4d9c2afbac028bfcefffcec6a070c78c8b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381866"
---
# <a name="creating-an-object-in-com"></a><span data-ttu-id="3a8d1-103">Création d’un objet dans COM</span><span class="sxs-lookup"><span data-stu-id="3a8d1-103">Creating an Object in COM</span></span>

<span data-ttu-id="3a8d1-104">Une fois qu’un thread a initialisé la bibliothèque COM, il est possible que le thread utilise des interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-104">After a thread has initialized the COM library, it is safe for the thread to use COM interfaces.</span></span> <span data-ttu-id="3a8d1-105">Pour utiliser une interface COM, votre programme crée d’abord une instance d’un objet qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-105">To use a COM interface, your program first creates an instance of an object that implements that interface.</span></span>

<span data-ttu-id="3a8d1-106">En général, il existe deux façons de créer un objet COM :</span><span class="sxs-lookup"><span data-stu-id="3a8d1-106">In general, there are two ways to create a COM object:</span></span>

-   <span data-ttu-id="3a8d1-107">Le module qui implémente l’objet peut fournir une fonction spécifiquement conçue pour créer des instances de cet objet.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-107">The module that implements the object might provide a function specifically designed to create instances of that object.</span></span>
-   <span data-ttu-id="3a8d1-108">En guise d’alternative, COM fournit une fonction de création générique nommée [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="3a8d1-108">Alternatively, COM provides a generic creation function named [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="3a8d1-109">Par exemple, prenez l' `Shape` objet hypothétique de la rubrique [qu’est-ce qu’une interface com ?](what-is-a-com-interface-.md).</span><span class="sxs-lookup"><span data-stu-id="3a8d1-109">For example, take the hypothetical `Shape` object from the topic [What Is a COM Interface?](what-is-a-com-interface-.md).</span></span> <span data-ttu-id="3a8d1-110">Dans cet exemple, l' `Shape` objet implémente une interface nommée `IDrawable` .</span><span class="sxs-lookup"><span data-stu-id="3a8d1-110">In that example, the `Shape` object implements an interface named `IDrawable`.</span></span> <span data-ttu-id="3a8d1-111">La bibliothèque de graphiques qui implémente l' `Shape` objet peut exporter une fonction avec la signature suivante.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-111">The graphics library that implements the `Shape` object might export a function with the following signature.</span></span>


```C++
// Not an actual Windows function. 

HRESULT CreateShape(IDrawable** ppShape);
```



<span data-ttu-id="3a8d1-112">À partir de cette fonction, vous pouvez créer un nouvel `Shape` objet comme suit.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-112">Given this function, you could create a new `Shape` object as follows.</span></span>


```C++
IDrawable *pShape;

HRESULT hr = CreateShape(&pShape);
if (SUCCEEDED(hr))
{
    // Use the Shape object.
}
else
{
    // An error occurred.
}
```



<span data-ttu-id="3a8d1-113">Le paramètre *ppShape* est de type pointeur vers pointeur vers `IDrawable` .</span><span class="sxs-lookup"><span data-stu-id="3a8d1-113">The *ppShape* parameter is of type pointer-to-pointer-to-`IDrawable`.</span></span> <span data-ttu-id="3a8d1-114">Si vous n’avez pas déjà vu ce modèle, l’indirection double peut être curieuse.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-114">If you have not seen this pattern before, the double indirection might be puzzling.</span></span>

<span data-ttu-id="3a8d1-115">Tenez compte des exigences de la `CreateShape` fonction.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-115">Consider the requirements of the `CreateShape` function.</span></span> <span data-ttu-id="3a8d1-116">La fonction doit renvoyer un `IDrawable` pointeur à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-116">The function must give an `IDrawable` pointer back to the caller.</span></span> <span data-ttu-id="3a8d1-117">Mais la valeur de retour de la fonction est déjà utilisée pour le code d’erreur/de réussite.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-117">But the function's return value is already used for the error/success code.</span></span> <span data-ttu-id="3a8d1-118">Par conséquent, le pointeur doit être retourné par l’intermédiaire d’un argument à la fonction.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-118">Therefore, the pointer must be returned through an argument to the function.</span></span> <span data-ttu-id="3a8d1-119">L’appelant passera une variable de type `IDrawable*` à la fonction, et la fonction remplacera cette variable par un nouveau `IDrawable` pointeur.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-119">The caller will pass a variable of type `IDrawable*` to the function, and the function will overwrite this variable with a new `IDrawable` pointer.</span></span> <span data-ttu-id="3a8d1-120">En C++, il existe deux façons pour une fonction de remplacer une valeur de paramètre : passer par référence ou passer par adresse.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-120">In C++, there are only two ways for a function to overwrite a parameter value: pass by reference, or pass by address.</span></span> <span data-ttu-id="3a8d1-121">COM utilise la dernière adresse, directe.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-121">COM uses the latter, pass-by-address.</span></span> <span data-ttu-id="3a8d1-122">Et l’adresse d’un pointeur est un pointeur vers un pointeur, donc le type de paramètre doit être `IDrawable**` .</span><span class="sxs-lookup"><span data-stu-id="3a8d1-122">And the address of a pointer is a pointer-to-a-pointer, so the parameter type must be `IDrawable**`.</span></span>

<span data-ttu-id="3a8d1-123">Voici un diagramme pour vous aider à visualiser ce qui se passe.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-123">Here is a diagram to help visualize what's going on.</span></span>

![diagramme qui montre une indirection de pointeur double](images/com03.png)

<span data-ttu-id="3a8d1-125">La `CreateShape` fonction utilise l’adresse de *pShape* ( `&pShape` ) pour écrire une nouvelle valeur de pointeur dans *pShape*.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-125">The `CreateShape` function uses the address of *pShape* (`&pShape`) to write a new pointer value to *pShape*.</span></span>

## <a name="cocreateinstance-a-generic-way-to-create-objects"></a><span data-ttu-id="3a8d1-126">CoCreateInstance : méthode générique pour créer des objets</span><span class="sxs-lookup"><span data-stu-id="3a8d1-126">CoCreateInstance: A Generic Way to Create Objects</span></span>

<span data-ttu-id="3a8d1-127">La fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) fournit un mécanisme générique pour la création d’objets.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-127">The [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function provides a generic mechanism for creating objects.</span></span> <span data-ttu-id="3a8d1-128">Pour comprendre **CoCreateInstance**, gardez à l’esprit que deux objets COM peuvent implémenter la même interface, et qu’un objet peut implémenter deux ou plusieurs interfaces.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-128">To understand **CoCreateInstance**, keep in mind that two COM objects can implement the same interface, and one object can implement two or more interfaces.</span></span> <span data-ttu-id="3a8d1-129">Par conséquent, une fonction générique qui crée des objets a besoin de deux éléments d’information.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-129">Thus, a generic function that creates objects needs two pieces of information.</span></span>

-   <span data-ttu-id="3a8d1-130">L’objet à créer.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-130">Which object to create.</span></span>
-   <span data-ttu-id="3a8d1-131">Interface à récupérer à partir de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-131">Which interface to get from the object.</span></span>

<span data-ttu-id="3a8d1-132">Mais comment faire pour indiquer ces informations lorsque nous appelons la fonction ?</span><span class="sxs-lookup"><span data-stu-id="3a8d1-132">But how do we indicate this information when we call the function?</span></span> <span data-ttu-id="3a8d1-133">Dans COM, un objet ou une interface est identifié en lui assignant un nombre 128 bits, appelé *identificateur global unique* (Guid).</span><span class="sxs-lookup"><span data-stu-id="3a8d1-133">In COM, an object or an interface is identified by assigning it a 128-bit number, called a *globally unique identifier* (GUID).</span></span> <span data-ttu-id="3a8d1-134">Les GUID sont générés d’une manière qui les rend effectivement uniques.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-134">GUIDs are generated in a way that makes them effectively unique.</span></span> <span data-ttu-id="3a8d1-135">Les GUID sont une solution au problème de la création d’identificateurs uniques sans autorité d’inscription centrale.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-135">GUIDs are a solution to the problem of how to create unique identifiers without a central registration authority.</span></span> <span data-ttu-id="3a8d1-136">Les GUID sont parfois appelés *identificateurs uniques universels* (UUID).</span><span class="sxs-lookup"><span data-stu-id="3a8d1-136">GUIDs are sometimes called *universally unique identifiers* (UUIDs).</span></span> <span data-ttu-id="3a8d1-137">Avant COM, elles étaient utilisées dans DCE/RPC (environnement de calcul distribué/appel de procédure distante).</span><span class="sxs-lookup"><span data-stu-id="3a8d1-137">Prior to COM, they were used in DCE/RPC (Distributed Computing Environment/Remote Procedure Call).</span></span> <span data-ttu-id="3a8d1-138">Plusieurs algorithmes existent pour la création de nouveaux GUID.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-138">Several algorithms exist for creating new GUIDs.</span></span> <span data-ttu-id="3a8d1-139">Tous ces algorithmes garantissent une unicité stricte, mais la probabilité de créer deux fois la même valeur GUID est très faible, en réalité zéro.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-139">Not all of these algorithms strictly guarantee uniqueness, but the probability of accidentally creating the same GUID value twice is extremely small—effectively zero.</span></span> <span data-ttu-id="3a8d1-140">Les GUID peuvent être utilisés pour identifier n’importe quel type d’entité, pas seulement les objets et les interfaces.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-140">GUIDs can be used to identify any sort of entity, not just objects and interfaces.</span></span> <span data-ttu-id="3a8d1-141">Toutefois, il s’agit de la seule utilisation qui nous concerne dans ce module.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-141">However, that is the only use that concerns us in this module.</span></span>

<span data-ttu-id="3a8d1-142">Par exemple, la `Shapes` bibliothèque peut déclarer deux constantes GUID :</span><span class="sxs-lookup"><span data-stu-id="3a8d1-142">For example, the `Shapes` library might declare two GUID constants:</span></span>


```C++
extern const GUID CLSID_Shape;
extern const GUID IID_IDrawable; 
```



<span data-ttu-id="3a8d1-143">(Vous pouvez supposer que les valeurs numériques 128 bits réelles pour ces constantes sont définies ailleurs.) La **\_ forme de CLSID** constante identifie l' `Shape` objet, tandis que le **\_ IDrawable IID** de constante identifie l' `IDrawable` interface.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-143">(You can assume that the actual 128-bit numeric values for these constants are defined elsewhere.) The constant **CLSID\_Shape** identifies the `Shape` object, while the constant **IID\_IDrawable** identifies the `IDrawable` interface.</span></span> <span data-ttu-id="3a8d1-144">Le préfixe « CLSID » signifie *identificateur de classe* et le préfixe *IID* signifie *identificateur d’interface*.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-144">The prefix "CLSID" stands for *class identifier*, and the prefix *IID* stands for *interface identifier*.</span></span> <span data-ttu-id="3a8d1-145">Il s’agit des conventions d’affectation de noms standard dans COM.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-145">These are standard naming conventions in COM.</span></span>

<span data-ttu-id="3a8d1-146">À partir de ces valeurs, vous devez créer une nouvelle instance de la façon suivante `Shape` :</span><span class="sxs-lookup"><span data-stu-id="3a8d1-146">Given these values, you would create a new `Shape` instance as follows:</span></span>


```C++
IDrawable *pShape;
hr = CoCreateInstance(CLSID_Shape, NULL, CLSCTX_INPROC_SERVER, IID_Drawable,
     reinterpret_cast<void**>(&pShape));

if (SUCCEEDED(hr))
{
    // Use the Shape object.
}
else
{
    // An error occurred.
}
```



<span data-ttu-id="3a8d1-147">La fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) a cinq paramètres.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-147">The [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function has five parameters.</span></span> <span data-ttu-id="3a8d1-148">Le premier et le quatrième paramètres sont l’identificateur de classe et l’identificateur d’interface.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-148">The first and fourth parameters are the class identifier and interface identifier.</span></span> <span data-ttu-id="3a8d1-149">En effet, ces paramètres indiquent à la fonction « créer l’objet de forme et me donnent un pointeur vers l’interface IDrawable ».</span><span class="sxs-lookup"><span data-stu-id="3a8d1-149">In effect, these parameters tell the function, "Create the Shape object, and give me a pointer to the IDrawable interface."</span></span>

<span data-ttu-id="3a8d1-150">Affectez au second paramètre la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-150">Set the second parameter to **NULL**.</span></span> <span data-ttu-id="3a8d1-151">(Pour plus d’informations sur la signification de ce paramètre, consultez la rubrique [Aggregation](/windows/desktop/com/aggregation) dans la documentation com.) Le troisième paramètre prend un ensemble d’indicateurs dont l’objectif principal est de spécifier le *contexte d’exécution* de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-151">(For more information about the meaning of this parameter, see the topic [Aggregation](/windows/desktop/com/aggregation) in the COM documentation.) The third parameter takes a set of flags whose main purpose is to specify the *execution context* for the object.</span></span> <span data-ttu-id="3a8d1-152">Le contexte d’exécution spécifie si l’objet s’exécute dans le même processus que l’application ; dans un processus différent sur le même ordinateur ; ou sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-152">The execution context specifies whether the object runs in the same process as the application; in a different process on the same computer; or on a remote computer.</span></span> <span data-ttu-id="3a8d1-153">Le tableau suivant indique les valeurs les plus courantes pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-153">The following table shows the most common values for this parameter.</span></span>



| <span data-ttu-id="3a8d1-154">Indicateur</span><span class="sxs-lookup"><span data-stu-id="3a8d1-154">Flag</span></span>                       | <span data-ttu-id="3a8d1-155">Description</span><span class="sxs-lookup"><span data-stu-id="3a8d1-155">Description</span></span>                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a8d1-156">**\_serveur INPROC \_ CLSCTX**</span><span class="sxs-lookup"><span data-stu-id="3a8d1-156">**CLSCTX\_INPROC\_SERVER**</span></span> | <span data-ttu-id="3a8d1-157">Même processus.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-157">Same process.</span></span>                                                                                                                                                      |
| <span data-ttu-id="3a8d1-158">**\_serveur local \_ CLSCTX**</span><span class="sxs-lookup"><span data-stu-id="3a8d1-158">**CLSCTX\_LOCAL\_SERVER**</span></span>  | <span data-ttu-id="3a8d1-159">Processus différent, même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-159">Different process, same computer.</span></span>                                                                                                                                  |
| <span data-ttu-id="3a8d1-160">**\_serveur distant \_ CLSCTX**</span><span class="sxs-lookup"><span data-stu-id="3a8d1-160">**CLSCTX\_REMOTE\_SERVER**</span></span> | <span data-ttu-id="3a8d1-161">Ordinateur différent.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-161">Different computer.</span></span>                                                                                                                                                |
| <span data-ttu-id="3a8d1-162">**CLSCTX \_ tout**</span><span class="sxs-lookup"><span data-stu-id="3a8d1-162">**CLSCTX\_ALL**</span></span>            | <span data-ttu-id="3a8d1-163">Utilisez l’option la plus efficace prise en charge par l’objet.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-163">Use the most efficient option that the object supports.</span></span> <span data-ttu-id="3a8d1-164">(Le classement, du plus efficace au moins efficace, est : in-process, out-of-process et Cross-Computer.)</span><span class="sxs-lookup"><span data-stu-id="3a8d1-164">(The ranking, from most efficient to least efficient, is: in-process, out-of-process, and cross-computer.)</span></span> |



 

<span data-ttu-id="3a8d1-165">La documentation d’un composant particulier peut vous indiquer le contexte d’exécution pris en charge par l’objet.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-165">The documentation for a particular component might tell you which execution context the object supports.</span></span> <span data-ttu-id="3a8d1-166">Si ce n’est pas le cas, utilisez **CLSCTX \_ All**.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-166">If not, use **CLSCTX\_ALL**.</span></span> <span data-ttu-id="3a8d1-167">Si vous demandez un contexte d’exécution que l’objet ne prend pas en charge, la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) retourne le code d’erreur **RegDB \_ E \_ CLASSNOTREG**.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-167">If you request an execution context that the object does not support, the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function returns the error code **REGDB\_E\_CLASSNOTREG**.</span></span> <span data-ttu-id="3a8d1-168">Ce code d’erreur peut également indiquer que le CLSID ne correspond à aucun composant inscrit sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-168">This error code can also indicate that the CLSID does not correspond to any component registered on the user's computer.</span></span>

<span data-ttu-id="3a8d1-169">Le cinquième paramètre de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) reçoit un pointeur vers l’interface.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-169">The fifth parameter to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) receives a pointer to the interface.</span></span> <span data-ttu-id="3a8d1-170">Comme **CoCreateInstance** est un mécanisme générique, ce paramètre ne peut pas être fortement typé.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-170">Because **CoCreateInstance** is a generic mechanism, this parameter cannot be strongly typed.</span></span> <span data-ttu-id="3a8d1-171">Au lieu de cela, le type de données est **void \* \*** et l’appelant doit contraindre l’adresse du pointeur en **type \* \* void** .</span><span class="sxs-lookup"><span data-stu-id="3a8d1-171">Instead, the data type is **void\*\***, and the caller must coerce the address of the pointer to a **void\*\*** type.</span></span> <span data-ttu-id="3a8d1-172">C’est l’objectif de la **\_ conversion réinterprétée** dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-172">That is the purpose of the **reinterpret\_cast** in the previous example.</span></span>

<span data-ttu-id="3a8d1-173">Il est essentiel de vérifier la valeur de retour de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="3a8d1-173">It is crucial to check the return value of [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="3a8d1-174">Si la fonction retourne un code d’erreur, le pointeur d’interface COM n’est pas valide et toute tentative de déréférencement peut entraîner le blocage de votre programme.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-174">If the function returns an error code, the COM interface pointer is invalid, and attempting to dereference it can cause your program to crash.</span></span>

<span data-ttu-id="3a8d1-175">En interne, la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) utilise diverses techniques pour créer un objet.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-175">Internally, the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function uses various techniques to create an object.</span></span> <span data-ttu-id="3a8d1-176">Dans le cas le plus simple, il recherche l’identificateur de classe dans le registre.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-176">In the simplest case, it looks up the class identifier in the registry.</span></span> <span data-ttu-id="3a8d1-177">L’entrée de registre pointe vers un fichier DLL ou EXE qui implémente l’objet.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-177">The registry entry points to a DLL or EXE that implements the object.</span></span> <span data-ttu-id="3a8d1-178">**CoCreateInstance** peut également utiliser des informations provenant d’un catalogue com+ ou d’un manifeste côte à côte (SxS).</span><span class="sxs-lookup"><span data-stu-id="3a8d1-178">**CoCreateInstance** can also use information from a COM+ catalog or a side-by-side (SxS) manifest.</span></span> <span data-ttu-id="3a8d1-179">Quels que soient les détails, les détails sont transparents pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-179">Regardless, the details are transparent to the caller.</span></span> <span data-ttu-id="3a8d1-180">Pour plus d’informations sur les détails internes de **CoCreateInstance**, consultez [clients et serveurs com](/windows/desktop/com/com-clients-and-servers).</span><span class="sxs-lookup"><span data-stu-id="3a8d1-180">For more information about the internal details of **CoCreateInstance**, see [COM Clients and Servers](/windows/desktop/com/com-clients-and-servers).</span></span>

<span data-ttu-id="3a8d1-181">L' `Shapes` exemple que nous utilisons est quelque peu fictif. passons maintenant à un exemple concret de com en action : affichage de la boîte de dialogue **ouvrir** pour que l’utilisateur sélectionne un fichier.</span><span class="sxs-lookup"><span data-stu-id="3a8d1-181">The `Shapes` example that we have been using is somewhat contrived, so now let's turn to a real-world example of COM in action: displaying the **Open** dialog box for the user to select a file.</span></span>

## <a name="next"></a><span data-ttu-id="3a8d1-182">Suivant</span><span class="sxs-lookup"><span data-stu-id="3a8d1-182">Next</span></span>

[<span data-ttu-id="3a8d1-183">Exemple : la boîte de dialogue Ouvrir</span><span class="sxs-lookup"><span data-stu-id="3a8d1-183">Example: The Open Dialog Box</span></span>](example--the-open-dialog-box.md)

 

 