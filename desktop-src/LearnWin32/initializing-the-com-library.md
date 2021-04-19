---
title: Initialisation de la bibliothèque COM
description: Initialisation de la bibliothèque COM
ms.assetid: b044e146-8409-4f8d-87d3-52f21ebc2255
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 663cfb73455e118579f45710788ab72385ada335
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106511490"
---
# <a name="initializing-the-com-library"></a><span data-ttu-id="e9bf2-103">Initialisation de la bibliothèque COM</span><span class="sxs-lookup"><span data-stu-id="e9bf2-103">Initializing the COM Library</span></span>

<span data-ttu-id="e9bf2-104">Tout programme Windows utilisant COM doit initialiser la bibliothèque COM en appelant la fonction [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) .</span><span class="sxs-lookup"><span data-stu-id="e9bf2-104">Any Windows program that uses COM must initialize the COM library by calling the [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) function.</span></span> <span data-ttu-id="e9bf2-105">Chaque thread qui utilise une interface COM doit effectuer un appel distinct à cette fonction.</span><span class="sxs-lookup"><span data-stu-id="e9bf2-105">Each thread that uses a COM interface must make a separate call to this function.</span></span> <span data-ttu-id="e9bf2-106">**CoInitializeEx** a la signature suivante :</span><span class="sxs-lookup"><span data-stu-id="e9bf2-106">**CoInitializeEx** has the following signature:</span></span>


```C++
HRESULT CoInitializeEx(LPVOID pvReserved, DWORD dwCoInit);
```



<span data-ttu-id="e9bf2-107">Le premier paramètre est réservé et doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="e9bf2-107">The first parameter is reserved and must be **NULL**.</span></span> <span data-ttu-id="e9bf2-108">Le deuxième paramètre spécifie le modèle de thread utilisé par votre programme.</span><span class="sxs-lookup"><span data-stu-id="e9bf2-108">The second parameter specifies the threading model that your program will use.</span></span> <span data-ttu-id="e9bf2-109">COM prend en charge deux *modèles de thread* différents, *thread cloisonné et multithread* .</span><span class="sxs-lookup"><span data-stu-id="e9bf2-109">COM supports two different threading models, *apartment threaded* and *multithreaded*.</span></span> <span data-ttu-id="e9bf2-110">Si vous spécifiez un thread cloisonné, vous effectuez les garanties suivantes :</span><span class="sxs-lookup"><span data-stu-id="e9bf2-110">If you specify apartment threading, you are making the following guarantees:</span></span>

-   <span data-ttu-id="e9bf2-111">Vous allez accéder à chaque objet COM à partir d’un seul thread. vous ne partagez pas les pointeurs d’interface COM entre plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="e9bf2-111">You will access each COM object from a single thread; you will not share COM interface pointers between multiple threads.</span></span>
-   <span data-ttu-id="e9bf2-112">Le thread aura une boucle de message.</span><span class="sxs-lookup"><span data-stu-id="e9bf2-112">The thread will have a message loop.</span></span> <span data-ttu-id="e9bf2-113">(Voir [messages de fenêtre](window-messages.md) dans le module 1.)</span><span class="sxs-lookup"><span data-stu-id="e9bf2-113">(See [Window Messages](window-messages.md) in Module 1.)</span></span>

<span data-ttu-id="e9bf2-114">Si l’une de ces contraintes n’est pas vraie, utilisez le modèle multithread.</span><span class="sxs-lookup"><span data-stu-id="e9bf2-114">If either of these constraints is not true, use the multithreaded model.</span></span> <span data-ttu-id="e9bf2-115">Pour spécifier le modèle de thread, définissez l’un des indicateurs suivants dans le paramètre *dwCoInit* .</span><span class="sxs-lookup"><span data-stu-id="e9bf2-115">To specify the threading model, set one of the following flags in the *dwCoInit* parameter.</span></span>



| <span data-ttu-id="e9bf2-116">Indicateur</span><span class="sxs-lookup"><span data-stu-id="e9bf2-116">Flag</span></span>                          | <span data-ttu-id="e9bf2-117">Description</span><span class="sxs-lookup"><span data-stu-id="e9bf2-117">Description</span></span>         |
|-------------------------------|---------------------|
| <span data-ttu-id="e9bf2-118">**APARTMENTTHREADED coinit \_**</span><span class="sxs-lookup"><span data-stu-id="e9bf2-118">**COINIT\_APARTMENTTHREADED**</span></span> | <span data-ttu-id="e9bf2-119">Thread cloisonné.</span><span class="sxs-lookup"><span data-stu-id="e9bf2-119">Apartment threaded.</span></span> |
| <span data-ttu-id="e9bf2-120">**coinit \_ multithread**</span><span class="sxs-lookup"><span data-stu-id="e9bf2-120">**COINIT\_MULTITHREADED**</span></span>     | <span data-ttu-id="e9bf2-121">Multithread.</span><span class="sxs-lookup"><span data-stu-id="e9bf2-121">Multithreaded.</span></span>      |



 

<span data-ttu-id="e9bf2-122">Vous devez définir exactement l’un de ces indicateurs.</span><span class="sxs-lookup"><span data-stu-id="e9bf2-122">You must set exactly one of these flags.</span></span> <span data-ttu-id="e9bf2-123">En règle générale, un thread qui crée une fenêtre doit utiliser l’indicateur **coinit \_ APARTMENTTHREADED** et les autres threads doivent utiliser la **coinit \_ multithread**.</span><span class="sxs-lookup"><span data-stu-id="e9bf2-123">Generally, a thread that creates a window should use the **COINIT\_APARTMENTTHREADED** flag, and other threads should use **COINIT\_MULTITHREADED**.</span></span> <span data-ttu-id="e9bf2-124">Toutefois, certains composants COM requièrent un modèle de thread particulier.</span><span class="sxs-lookup"><span data-stu-id="e9bf2-124">However, some COM components require a particular threading model.</span></span> <span data-ttu-id="e9bf2-125">La documentation MSDN doit vous indiquer quand c’est le cas.</span><span class="sxs-lookup"><span data-stu-id="e9bf2-125">The MSDN documentation should tell you when that is the case.</span></span>

> [!Note]  
> <span data-ttu-id="e9bf2-126">En fait, même si vous spécifiez un thread cloisonné, il est toujours possible de partager des interfaces entre les threads, à l’aide d’une technique appelée *marshaling*.</span><span class="sxs-lookup"><span data-stu-id="e9bf2-126">Actually, even if you specify apartment threading, it is still possible to share interfaces between threads, by using a technique called *marshaling*.</span></span> <span data-ttu-id="e9bf2-127">Le marshaling n’entre pas dans le cadre de ce module.</span><span class="sxs-lookup"><span data-stu-id="e9bf2-127">Marshaling is beyond the scope of this module.</span></span> <span data-ttu-id="e9bf2-128">Le point important est qu’avec le thread cloisonné, vous ne devez jamais simplement copier un pointeur d’interface vers un autre thread.</span><span class="sxs-lookup"><span data-stu-id="e9bf2-128">The important point is that with apartment threading, you must never simply copy an interface pointer to another thread.</span></span> <span data-ttu-id="e9bf2-129">Pour plus d’informations sur les modèles de threads COM, consultez [processus, threads et Apartments](/windows/desktop/com/processes--threads--and-apartments).</span><span class="sxs-lookup"><span data-stu-id="e9bf2-129">For more information about the COM threading models, see [Processes, Threads, and Apartments](/windows/desktop/com/processes--threads--and-apartments).</span></span>

 

<span data-ttu-id="e9bf2-130">En plus des indicateurs déjà mentionnés, il est judicieux de définir l’indicateur **coinit \_ Disable \_ OLE1DDE** dans le paramètre *dwCoInit* .</span><span class="sxs-lookup"><span data-stu-id="e9bf2-130">In addition to the flags already mentioned, it is a good idea to set the **COINIT\_DISABLE\_OLE1DDE** flag in the *dwCoInit* parameter.</span></span> <span data-ttu-id="e9bf2-131">La définition de cet indicateur évite une surcharge liée à la liaison et à l’incorporation d’objets (OLE) 1,0, une technologie obsolète.</span><span class="sxs-lookup"><span data-stu-id="e9bf2-131">Setting this flag avoids some overhead associated with Object Linking and Embedding (OLE) 1.0, an obsolete technology.</span></span>

<span data-ttu-id="e9bf2-132">Voici comment initialiser COM pour le thread cloisonné :</span><span class="sxs-lookup"><span data-stu-id="e9bf2-132">Here is how you would initialize COM for apartment threading:</span></span>


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
```



<span data-ttu-id="e9bf2-133">Le type de retour **HRESULT** contient un code d’erreur ou de réussite.</span><span class="sxs-lookup"><span data-stu-id="e9bf2-133">The **HRESULT** return type contains an error or success code.</span></span> <span data-ttu-id="e9bf2-134">Nous allons examiner la gestion des erreurs COM dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="e9bf2-134">We'll look at COM error handling in the next section.</span></span>

## <a name="uninitializing-the-com-library"></a><span data-ttu-id="e9bf2-135">Désinitialisation de la bibliothèque COM</span><span class="sxs-lookup"><span data-stu-id="e9bf2-135">Uninitializing the COM Library</span></span>

<span data-ttu-id="e9bf2-136">Pour chaque appel réussi à [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), vous devez appeler [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) avant que le thread ne se termine.</span><span class="sxs-lookup"><span data-stu-id="e9bf2-136">For every successful call to [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), you must call [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) before the thread exits.</span></span> <span data-ttu-id="e9bf2-137">Cette fonction n’accepte aucun paramètre et n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="e9bf2-137">This function takes no parameters and has no return value.</span></span>


```C++
CoUninitialize();
```



## <a name="next"></a><span data-ttu-id="e9bf2-138">Suivant</span><span class="sxs-lookup"><span data-stu-id="e9bf2-138">Next</span></span>

[<span data-ttu-id="e9bf2-139">Codes d’erreur dans COM</span><span class="sxs-lookup"><span data-stu-id="e9bf2-139">Error Codes in COM</span></span>](error-codes-in-com.md)

 

 