---
title: Gestion de la durée de vie d’un objet
description: Découvrez comment gérer les méthodes AddRef et Release pour contrôler la durée de vie d’un objet.
ms.assetid: 0e522ded-8976-4cdd-9a61-eae7834c896b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 495e657863150612e5b8efa21fff0b00c7a936b9
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104559970"
---
# <a name="managing-the-lifetime-of-an-object"></a><span data-ttu-id="d47dd-103">Gestion de la durée de vie d’un objet</span><span class="sxs-lookup"><span data-stu-id="d47dd-103">Managing the Lifetime of an Object</span></span>

<span data-ttu-id="d47dd-104">Il existe une règle pour les interfaces COM que nous n’avons pas encore mentionnées.</span><span class="sxs-lookup"><span data-stu-id="d47dd-104">There is a rule for COM interfaces that we have not yet mentioned.</span></span> <span data-ttu-id="d47dd-105">Chaque interface COM doit hériter, directement ou indirectement, d’une interface nommée [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="d47dd-105">Every COM interface must inherit, directly or indirectly, from an interface named [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="d47dd-106">Cette interface fournit des fonctionnalités de base que tous les objets COM doivent prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="d47dd-106">This interface provides some baseline capabilities that all COM objects must support.</span></span>

<span data-ttu-id="d47dd-107">L’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) définit trois méthodes :</span><span class="sxs-lookup"><span data-stu-id="d47dd-107">The [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface defines three methods:</span></span>

-   <span data-ttu-id="d47dd-108">[**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="d47dd-108">[**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span>
-   [<span data-ttu-id="d47dd-109">**AddRef**</span><span class="sxs-lookup"><span data-stu-id="d47dd-109">**AddRef**</span></span>](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref)
-   [<span data-ttu-id="d47dd-110">**Libérer**</span><span class="sxs-lookup"><span data-stu-id="d47dd-110">**Release**</span></span>](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)

<span data-ttu-id="d47dd-111">La méthode [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) permet à un programme d’interroger les fonctionnalités de l’objet au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="d47dd-111">The [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method enables a program to query the capabilities of the object at run time.</span></span> <span data-ttu-id="d47dd-112">Pour plus d’informations à ce sujet, nous allons [demander un objet pour une interface](asking-an-object-for-an-interface.md).</span><span class="sxs-lookup"><span data-stu-id="d47dd-112">We'll say more about that in the next topic, [Asking an Object for an Interface](asking-an-object-for-an-interface.md).</span></span> <span data-ttu-id="d47dd-113">Les méthodes [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) et [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sont utilisées pour contrôler la durée de vie d’un objet.</span><span class="sxs-lookup"><span data-stu-id="d47dd-113">The [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) methods are used to control the lifetime of an object.</span></span> <span data-ttu-id="d47dd-114">Il s’agit de l’objet de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="d47dd-114">This is the subject of this topic.</span></span>

## <a name="reference-counting"></a><span data-ttu-id="d47dd-115">Décompte de références</span><span class="sxs-lookup"><span data-stu-id="d47dd-115">Reference Counting</span></span>

<span data-ttu-id="d47dd-116">À un moment donné, un programme peut allouer et libérer des ressources.</span><span class="sxs-lookup"><span data-stu-id="d47dd-116">Whatever else a program might do, at some point it will allocate and free resources.</span></span> <span data-ttu-id="d47dd-117">L’allocation d’une ressource est simple.</span><span class="sxs-lookup"><span data-stu-id="d47dd-117">Allocating a resource is easy.</span></span> <span data-ttu-id="d47dd-118">Il est difficile de savoir quand libérer la ressource, surtout si la durée de vie de la ressource s’étend au-delà de la portée actuelle.</span><span class="sxs-lookup"><span data-stu-id="d47dd-118">Knowing when to free the resource is hard, especially if the lifetime of the resource extends beyond the current scope.</span></span> <span data-ttu-id="d47dd-119">Ce problème n’est pas propre à COM.</span><span class="sxs-lookup"><span data-stu-id="d47dd-119">This problem is not unique to COM.</span></span> <span data-ttu-id="d47dd-120">Tout programme qui alloue de la mémoire du tas doit résoudre le même problème.</span><span class="sxs-lookup"><span data-stu-id="d47dd-120">Any program that allocates heap memory must solve the same problem.</span></span> <span data-ttu-id="d47dd-121">Par exemple, C++ utilise des destructeurs automatiques, tandis que C# et Java utilisent garbage collection.</span><span class="sxs-lookup"><span data-stu-id="d47dd-121">For example, C++ uses automatic destructors, while C# and Java use garbage collection.</span></span> <span data-ttu-id="d47dd-122">COM utilise une approche appelée *décompte de références*.</span><span class="sxs-lookup"><span data-stu-id="d47dd-122">COM uses an approach called *reference counting*.</span></span>

<span data-ttu-id="d47dd-123">Chaque objet COM gère un nombre interne.</span><span class="sxs-lookup"><span data-stu-id="d47dd-123">Every COM object maintains an internal count.</span></span> <span data-ttu-id="d47dd-124">C’est ce que l’on appelle le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="d47dd-124">This is known as the reference count.</span></span> <span data-ttu-id="d47dd-125">Le nombre de références effectue le suivi du nombre de références à l’objet actuellement actives.</span><span class="sxs-lookup"><span data-stu-id="d47dd-125">The reference count tracks how many references to the object are currently active.</span></span> <span data-ttu-id="d47dd-126">Lorsque le nombre de références chute à zéro, l’objet se supprime lui-même.</span><span class="sxs-lookup"><span data-stu-id="d47dd-126">When the number of references drops to zero, the object deletes itself.</span></span> <span data-ttu-id="d47dd-127">La dernière partie est la plus intéressante : l’objet se supprime lui-même.</span><span class="sxs-lookup"><span data-stu-id="d47dd-127">The last part is worth repeating: The object deletes itself.</span></span> <span data-ttu-id="d47dd-128">Le programme ne supprime jamais l’objet de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="d47dd-128">The program never explicitly deletes the object.</span></span>

<span data-ttu-id="d47dd-129">Voici les règles pour le décompte de références :</span><span class="sxs-lookup"><span data-stu-id="d47dd-129">Here are the rules for reference counting:</span></span>

-   <span data-ttu-id="d47dd-130">Lorsque l’objet est créé pour la première fois, son nombre de références est 1.</span><span class="sxs-lookup"><span data-stu-id="d47dd-130">When the object is first created, its reference count is 1.</span></span> <span data-ttu-id="d47dd-131">À ce stade, le programme a un seul pointeur vers l’objet.</span><span class="sxs-lookup"><span data-stu-id="d47dd-131">At this point, the program has a single pointer to the object.</span></span>
-   <span data-ttu-id="d47dd-132">Le programme peut créer une nouvelle référence en dupliquant (copiant) le pointeur.</span><span class="sxs-lookup"><span data-stu-id="d47dd-132">The program can create a new reference by duplicating (copying) the pointer.</span></span> <span data-ttu-id="d47dd-133">Lorsque vous copiez le pointeur, vous devez appeler la méthode [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d47dd-133">When you copy the pointer, you must call the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) method of the object.</span></span> <span data-ttu-id="d47dd-134">Cette méthode incrémente le nombre de références d’une unité.</span><span class="sxs-lookup"><span data-stu-id="d47dd-134">This method increments the reference count by one.</span></span>
-   <span data-ttu-id="d47dd-135">Lorsque vous avez terminé d’utiliser un pointeur vers l’objet, vous devez appeler [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="d47dd-135">When you are finished using a pointer to the object, you must call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="d47dd-136">La méthode **Release** décrémente le nombre de références d’une unité.</span><span class="sxs-lookup"><span data-stu-id="d47dd-136">The **Release** method decrements the reference count by one.</span></span> <span data-ttu-id="d47dd-137">Il invalide également le pointeur.</span><span class="sxs-lookup"><span data-stu-id="d47dd-137">It also invalidates the pointer.</span></span> <span data-ttu-id="d47dd-138">N’utilisez pas le pointeur une fois que vous avez appelé **Release**.</span><span class="sxs-lookup"><span data-stu-id="d47dd-138">Do not use the pointer again after you call **Release**.</span></span> <span data-ttu-id="d47dd-139">(Si vous avez d’autres pointeurs vers le même objet, vous pouvez continuer à utiliser ces pointeurs.)</span><span class="sxs-lookup"><span data-stu-id="d47dd-139">(If you have other pointers to the same object, you can continue to use those pointers.)</span></span>
-   <span data-ttu-id="d47dd-140">Quand vous avez appelé [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) avec chaque pointeur, le nombre de références d’objet de l’objet atteint zéro, et l’objet se supprime lui-même.</span><span class="sxs-lookup"><span data-stu-id="d47dd-140">When you have called [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) with every pointer, the object reference count of the object reaches zero, and the object deletes itself.</span></span>

<span data-ttu-id="d47dd-141">Le diagramme suivant illustre un cas simple mais classique.</span><span class="sxs-lookup"><span data-stu-id="d47dd-141">The following diagram shows a simple but typical case.</span></span>

![Diagramme qui montre un cas simple de décompte de références.](images/com04.png)

<span data-ttu-id="d47dd-143">Le programme crée un objet et stocke un pointeur (*p*) sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="d47dd-143">The program creates an object and stores a pointer (*p*) to the object.</span></span> <span data-ttu-id="d47dd-144">À ce stade, le nombre de références est 1.</span><span class="sxs-lookup"><span data-stu-id="d47dd-144">At this point, the reference count is 1.</span></span> <span data-ttu-id="d47dd-145">Quand le programme a fini d’utiliser le pointeur, il appelle [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="d47dd-145">When the program is finished using the pointer, it calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="d47dd-146">Le décompte de références est décrémenté à zéro et l’objet se supprime lui-même.</span><span class="sxs-lookup"><span data-stu-id="d47dd-146">The reference count is decremented to zero, and the object deletes itself.</span></span> <span data-ttu-id="d47dd-147">Désormais, *p* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d47dd-147">Now *p* is invalid.</span></span> <span data-ttu-id="d47dd-148">L’utilisation de *p* pour d’autres appels de méthode est une erreur.</span><span class="sxs-lookup"><span data-stu-id="d47dd-148">It is an error to use *p* for any further method calls.</span></span>

<span data-ttu-id="d47dd-149">Le diagramme suivant montre un exemple plus complexe.</span><span class="sxs-lookup"><span data-stu-id="d47dd-149">The next diagram shows a more complex example.</span></span>

![illustration illustrant le décompte de références](images/com05.png)

<span data-ttu-id="d47dd-151">Ici, le programme crée un objet et stocke le pointeur *p*, comme précédemment.</span><span class="sxs-lookup"><span data-stu-id="d47dd-151">Here, the program creates an object and stores the pointer *p*, as before.</span></span> <span data-ttu-id="d47dd-152">Ensuite, le programme copie *p* vers une nouvelle variable, *q*.</span><span class="sxs-lookup"><span data-stu-id="d47dd-152">Next, the program copies *p* to a new variable, *q*.</span></span> <span data-ttu-id="d47dd-153">À ce stade, le programme doit appeler [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) pour incrémenter le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="d47dd-153">At this point, the program must call [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) to increment the reference count.</span></span> <span data-ttu-id="d47dd-154">Le décompte de références est maintenant 2 et il existe deux pointeurs valides pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="d47dd-154">The reference count is now 2, and there are two valid pointers to the object.</span></span> <span data-ttu-id="d47dd-155">Supposons maintenant que le programme a fini d’utiliser *p*.</span><span class="sxs-lookup"><span data-stu-id="d47dd-155">Now suppose that the program is finished using *p*.</span></span> <span data-ttu-id="d47dd-156">Le programme appelle [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), le décompte de références atteint 1 et *p* n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="d47dd-156">The program calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), the reference count goes to 1, and *p* is no longer valid.</span></span> <span data-ttu-id="d47dd-157">Toutefois, *q* est toujours valide.</span><span class="sxs-lookup"><span data-stu-id="d47dd-157">However, *q* is still valid.</span></span> <span data-ttu-id="d47dd-158">Plus tard, le programme se termine à l’aide de *q*.</span><span class="sxs-lookup"><span data-stu-id="d47dd-158">Later, the program finishes using *q*.</span></span> <span data-ttu-id="d47dd-159">Par conséquent, il appelle à nouveau la **version** .</span><span class="sxs-lookup"><span data-stu-id="d47dd-159">Therefore, it calls **Release** again.</span></span> <span data-ttu-id="d47dd-160">Le décompte de références atteint zéro, et l’objet se supprime lui-même.</span><span class="sxs-lookup"><span data-stu-id="d47dd-160">The reference count goes to zero, and the object deletes itself.</span></span>

<span data-ttu-id="d47dd-161">Vous vous demandez peut-être pourquoi le programme copiera *p*.</span><span class="sxs-lookup"><span data-stu-id="d47dd-161">You might wonder why the program would copy *p*.</span></span> <span data-ttu-id="d47dd-162">Il existe deux raisons principales : tout d’abord, vous souhaiterez peut-être stocker le pointeur dans une structure de données, telle qu’une liste.</span><span class="sxs-lookup"><span data-stu-id="d47dd-162">There are two main reasons: First, you might want to store the pointer in a data structure, such as a list.</span></span> <span data-ttu-id="d47dd-163">Deuxièmement, vous souhaiterez peut-être conserver le pointeur au-delà de la portée actuelle de la variable d’origine.</span><span class="sxs-lookup"><span data-stu-id="d47dd-163">Second, you might want to keep the pointer beyond the current scope of the original variable.</span></span> <span data-ttu-id="d47dd-164">Par conséquent, vous pouvez la copier dans une nouvelle variable avec une portée plus étendue.</span><span class="sxs-lookup"><span data-stu-id="d47dd-164">Therefore, you would copy it to a new variable with wider scope.</span></span>

<span data-ttu-id="d47dd-165">L’un des avantages du décompte de références est que vous pouvez partager des pointeurs entre différentes sections de code, sans que les différents chemins de code ne coordonnent la suppression de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d47dd-165">One advantage of reference counting is that you can share pointers across different sections of code, without the various code paths coordinating to delete the object.</span></span> <span data-ttu-id="d47dd-166">Au lieu de cela, chaque chemin de code appelle simplement [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) quand ce chemin de code est effectué à l’aide de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d47dd-166">Instead, each code path merely calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) when that code path is done using the object.</span></span> <span data-ttu-id="d47dd-167">L’objet gère sa suppression à l’heure correcte.</span><span class="sxs-lookup"><span data-stu-id="d47dd-167">The object handles deleting itself at the correct time.</span></span>

## <a name="example"></a><span data-ttu-id="d47dd-168">Exemple</span><span class="sxs-lookup"><span data-stu-id="d47dd-168">Example</span></span>

<span data-ttu-id="d47dd-169">Voici à nouveau le code de l' [exemple de boîte de dialogue Ouvrir](example--the-open-dialog-box.md) .</span><span class="sxs-lookup"><span data-stu-id="d47dd-169">Here is the code from the [Open dialog box example](example--the-open-dialog-box.md) again.</span></span>

```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED |
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    IFileOpenDialog *pFileOpen;

    hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL,
            IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                PWSTR pszFilePath;
                hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
                if (SUCCEEDED(hr))
                {
                    MessageBox(NULL, pszFilePath, L&quot;File Path&quot;, MB_OK);
                    CoTaskMemFree(pszFilePath);
                }
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    CoUninitialize();
}
````

<span data-ttu-id="d47dd-170">Le décompte de références se produit à deux emplacements dans ce code.</span><span class="sxs-lookup"><span data-stu-id="d47dd-170">Reference counting occurs in two places in this code.</span></span> <span data-ttu-id="d47dd-171">Tout d’abord, si le programme crée correctement l’objet de boîte de dialogue d’élément commun, il doit appeler [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur le pointeur *pFileOpen* .</span><span class="sxs-lookup"><span data-stu-id="d47dd-171">First, if program successfully creates the Common Item Dialog object, it must call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on the *pFileOpen* pointer.</span></span>

```C++
hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL, 
        IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

if (SUCCEEDED(hr))
{
    // ...
    pFileOpen->Release();
}
```

<span data-ttu-id="d47dd-172">Deuxièmement, lorsque la méthode [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) retourne un pointeur vers l’interface [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) , le programme doit appeler [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur le pointeur *pItem* .</span><span class="sxs-lookup"><span data-stu-id="d47dd-172">Second, when the [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) method returns a pointer to the [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) interface, the program must call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on the *pItem* pointer.</span></span>

```C++
hr = pFileOpen->GetResult(&pItem);

if (SUCCEEDED(hr))
{
    // ...
    pItem->Release();
}
```

<span data-ttu-id="d47dd-173">Notez que dans les deux cas, l’appel de [**version**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) est la dernière chose qui se produit avant que le pointeur ne soit hors de portée.</span><span class="sxs-lookup"><span data-stu-id="d47dd-173">Notice that in both cases, the [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) call is the last thing that happens before the pointer goes out of scope.</span></span> <span data-ttu-id="d47dd-174">Notez également que **Release** est appelé uniquement après que vous avez testé la réussite de **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d47dd-174">Also notice that **Release** is called only after you test the **HRESULT** for success.</span></span> <span data-ttu-id="d47dd-175">Par exemple, si l’appel à [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) échoue, le pointeur *pFileOpen* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d47dd-175">For example, if the call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) fails, the *pFileOpen* pointer is not valid.</span></span> <span data-ttu-id="d47dd-176">Par conséquent, il serait erroné d’appeler **Release** sur le pointeur.</span><span class="sxs-lookup"><span data-stu-id="d47dd-176">Therefore, it would be an error to call **Release** on the pointer.</span></span>

## <a name="next"></a><span data-ttu-id="d47dd-177">Suivant</span><span class="sxs-lookup"><span data-stu-id="d47dd-177">Next</span></span>

[<span data-ttu-id="d47dd-178">Demande d’un objet pour une interface</span><span class="sxs-lookup"><span data-stu-id="d47dd-178">Asking an Object for an Interface</span></span>](asking-an-object-for-an-interface.md)