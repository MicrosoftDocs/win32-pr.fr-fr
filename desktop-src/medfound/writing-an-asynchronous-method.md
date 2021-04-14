---
description: Cette rubrique explique comment implémenter une méthode asynchrone dans Microsoft Media Foundation.
ms.assetid: cd94280d-7267-4d35-8333-aa4a5bd81b73
title: Écriture d’une méthode asynchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d8360d0c15fe25661b8cd0f0f5adc9768db8ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320270"
---
# <a name="writing-an-asynchronous-method"></a><span data-ttu-id="69765-103">Écriture d’une méthode asynchrone</span><span class="sxs-lookup"><span data-stu-id="69765-103">Writing an Asynchronous Method</span></span>

<span data-ttu-id="69765-104">Cette rubrique explique comment implémenter une méthode asynchrone dans Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="69765-104">This topic describes how to implement an asynchronous method in Microsoft Media Foundation.</span></span>

<span data-ttu-id="69765-105">Les méthodes asynchrones sont omniprésentes dans le pipeline Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="69765-105">Asynchronous methods are ubiquitous in the Media Foundation pipeline.</span></span> <span data-ttu-id="69765-106">Les méthodes asynchrones facilitent la répartition du travail entre plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="69765-106">Asynchronous methods make it easier to distribute work among several threads.</span></span> <span data-ttu-id="69765-107">Il est particulièrement important d’effectuer des e/s de manière asynchrone, de sorte que la lecture à partir d’un fichier ou d’un réseau ne bloque pas le reste du pipeline.</span><span class="sxs-lookup"><span data-stu-id="69765-107">It is particularly important to perform I/O asynchronously, so that reading from a file or network does not block the rest of the pipeline.</span></span>

<span data-ttu-id="69765-108">Si vous écrivez une source multimédia ou un récepteur multimédia, il est essentiel de gérer correctement les opérations asynchrones, car les performances de votre composant ont un impact sur l’ensemble du pipeline.</span><span class="sxs-lookup"><span data-stu-id="69765-108">If you are writing a media source or media sink, it is crucial to handle asynchronous operations correctly, because your component's performance has an impact on the entire pipeline.</span></span>

> [!Note]  
> <span data-ttu-id="69765-109">Les transformations de Media Foundation (MFTs) utilisent des méthodes synchrones par défaut.</span><span class="sxs-lookup"><span data-stu-id="69765-109">Media Foundation transforms (MFTs) use synchronous methods by default.</span></span>

 

### <a name="work-queues-for-asynchronous-operations"></a><span data-ttu-id="69765-110">Files d’attente de travail pour les opérations asynchrones</span><span class="sxs-lookup"><span data-stu-id="69765-110">Work Queues For Asynchronous Operations</span></span>

<span data-ttu-id="69765-111">Dans Media Foundation, il existe une relation étroite entre les [méthodes de rappel asynchrones](asynchronous-callback-methods.md) et les [files d’attente de travail](work-queues.md).</span><span class="sxs-lookup"><span data-stu-id="69765-111">In Media Foundation, there is a close relationship between [Asynchronous Callback Methods](asynchronous-callback-methods.md) and [Work Queues](work-queues.md).</span></span> <span data-ttu-id="69765-112">Une file d’attente de travail est une abstraction pour déplacer le travail du thread de l’appelant vers un thread de travail.</span><span class="sxs-lookup"><span data-stu-id="69765-112">A work queue is an abstraction for moving work from the caller's thread to a worker thread.</span></span> <span data-ttu-id="69765-113">Pour effectuer un travail sur une file d’attente de travail, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="69765-113">To perform work on a work queue, do the following:</span></span>

1.  <span data-ttu-id="69765-114">Implémentez l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="69765-114">Implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
2.  <span data-ttu-id="69765-115">Appelez [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) pour créer un objet de *résultat* .</span><span class="sxs-lookup"><span data-stu-id="69765-115">Call [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) to create a *result* object.</span></span> <span data-ttu-id="69765-116">L’objet de résultat expose le [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult).</span><span class="sxs-lookup"><span data-stu-id="69765-116">The result object exposes the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult).</span></span> <span data-ttu-id="69765-117">L’objet de résultat contient trois pointeurs :</span><span class="sxs-lookup"><span data-stu-id="69765-117">The result object contains three pointers:</span></span>

    -   <span data-ttu-id="69765-118">Pointeur vers l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="69765-118">A pointer to the caller's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
    -   <span data-ttu-id="69765-119">Pointeur facultatif vers un objet d’État.</span><span class="sxs-lookup"><span data-stu-id="69765-119">An optional pointer to a state object.</span></span> <span data-ttu-id="69765-120">S’il est spécifié, l’objet d’État doit implémenter **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="69765-120">If specified, the state object must implement **IUnknown**.</span></span>
    -   <span data-ttu-id="69765-121">Pointeur facultatif vers un objet privé.</span><span class="sxs-lookup"><span data-stu-id="69765-121">An optional pointer to a private object.</span></span> <span data-ttu-id="69765-122">S’il est spécifié, cet objet doit également implémenter **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="69765-122">If specified, this object also must implement **IUnknown**.</span></span>

    <span data-ttu-id="69765-123">Les deux derniers pointeurs peuvent avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="69765-123">The last two pointers can be **NULL**.</span></span> <span data-ttu-id="69765-124">Dans le cas contraire, utilisez-les pour stocker des informations sur l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="69765-124">Otherwise, use them to hold information about the asynchronous operation.</span></span>

3.  <span data-ttu-id="69765-125">Appelez [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) pour effectuer la file d’attente vers l’élément de travail.</span><span class="sxs-lookup"><span data-stu-id="69765-125">Call [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) to queue to the work item.</span></span>
4.  <span data-ttu-id="69765-126">Le thread de file d’attente de travail appelle votre méthode [**IMFAsyncCallback :: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) .</span><span class="sxs-lookup"><span data-stu-id="69765-126">The work-queue thread calls your [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method.</span></span>
5.  <span data-ttu-id="69765-127">Effectuez le travail à l’intérieur de votre méthode [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) .</span><span class="sxs-lookup"><span data-stu-id="69765-127">Do the work inside your [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method.</span></span> <span data-ttu-id="69765-128">Le paramètre *pAsyncResult* de cette méthode est le pointeur [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) de l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="69765-128">The *pAsyncResult* parameter of this method is the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) pointer from step 2.</span></span> <span data-ttu-id="69765-129">Utilisez ce pointeur pour récupérer l’objet d’État et l’objet privé :</span><span class="sxs-lookup"><span data-stu-id="69765-129">Use this pointer to get the state object and private object:</span></span>
    -   <span data-ttu-id="69765-130">Pour accéder à l’objet d’État, appelez [**IMFAsyncResult :: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).</span><span class="sxs-lookup"><span data-stu-id="69765-130">To get the state object, call [**IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).</span></span>
    -   <span data-ttu-id="69765-131">Pour accéder à l’objet privé, appelez [**IMFAsyncResult :: GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject).</span><span class="sxs-lookup"><span data-stu-id="69765-131">To get the private object, call [**IMFAsyncResult::GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject).</span></span>

<span data-ttu-id="69765-132">Vous pouvez également combiner les étapes 2 et 3 en appelant la fonction [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) .</span><span class="sxs-lookup"><span data-stu-id="69765-132">As an alternative, you can combine steps 2 and 3 by calling the [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) function.</span></span> <span data-ttu-id="69765-133">En interne, cette fonction appelle [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) pour créer l’objet de résultat.</span><span class="sxs-lookup"><span data-stu-id="69765-133">Internally, this function calls [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) to create the result object.</span></span>

<span data-ttu-id="69765-134">Le diagramme suivant montre les relations entre l’appelant, l’objet de résultat, l’objet d’État et l’objet privé.</span><span class="sxs-lookup"><span data-stu-id="69765-134">The following diagram shows the relationships between the caller, the result object, the state object, and the private object.</span></span>

![Diagramme montrant un objet de résultat asynchrone](images/workqueues01.png)

<span data-ttu-id="69765-136">Le diagramme de séquence suivant montre comment un objet met en file d’attente un élément de travail.</span><span class="sxs-lookup"><span data-stu-id="69765-136">The following sequence diagram shows how an object queues a work item.</span></span> <span data-ttu-id="69765-137">Lorsque le thread de file d’attente de travail appelle [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), l’objet effectue l’opération asynchrone sur ce thread.</span><span class="sxs-lookup"><span data-stu-id="69765-137">When the work-queue thread calls [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), the object performs the asynchronous operation on that thread.</span></span>

![Diagramme montrant comment un objet met en file d’attente un élément de travail](images/workqueues02.png)

<span data-ttu-id="69765-139">Il est important de se souvenir que [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) est appelé à partir d’un thread qui appartient à la file d’attente de travail.</span><span class="sxs-lookup"><span data-stu-id="69765-139">It is important to remember [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) is called from a thread that is owned by the work queue.</span></span> <span data-ttu-id="69765-140">Votre implémentation de **Invoke** doit être thread-safe.</span><span class="sxs-lookup"><span data-stu-id="69765-140">Your implementation of **Invoke** must be thread safe.</span></span> <span data-ttu-id="69765-141">En outre, si vous utilisez la file d’attente de travail de la plateforme (**MFASYNC \_ callback \_ Queue \_ standard**), il est essentiel de ne jamais bloquer le thread, car cela peut bloquer l’intégralité du pipeline Media Foundation du traitement des données.</span><span class="sxs-lookup"><span data-stu-id="69765-141">In addition, if you use the platform work queue (**MFASYNC\_CALLBACK\_QUEUE\_STANDARD**), it is critical that you never block the thread, because that can block the entire Media Foundation pipeline from processing data.</span></span> <span data-ttu-id="69765-142">Si vous devez effectuer une opération qui se bloque ou prend beaucoup de temps, utilisez une file d’attente de travail privée.</span><span class="sxs-lookup"><span data-stu-id="69765-142">If you need to perform an operation that will block or take a long time to complete, use a private work queue.</span></span> <span data-ttu-id="69765-143">Pour créer une file d’attente de travail privée, appelez [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).</span><span class="sxs-lookup"><span data-stu-id="69765-143">To create a private work queue, call [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).</span></span> <span data-ttu-id="69765-144">Tout composant de pipeline qui effectue des opérations d’e/s doit éviter de bloquer les appels d’e/s pour la même raison.</span><span class="sxs-lookup"><span data-stu-id="69765-144">Any pipeline component that performs I/O operations should avoid blocking I/O calls for the same reason.</span></span> <span data-ttu-id="69765-145">L’interface [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) fournit une abstraction utile pour les e/s de fichier asynchrones.</span><span class="sxs-lookup"><span data-stu-id="69765-145">The [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface provides a useful abstraction for asynchronous file I/O.</span></span>

### <a name="implementing-the-beginend-pattern"></a><span data-ttu-id="69765-146">Implémentation de BEGIN. ../end... Répétition</span><span class="sxs-lookup"><span data-stu-id="69765-146">Implementing the Begin.../End... Pattern</span></span>

<span data-ttu-id="69765-147">Comme décrit dans [appel de méthodes asynchrones](calling-asynchronous-methods.md), les méthodes asynchrones dans Media Foundation utilisent souvent la méthode **Begin...** / **Fin....** répétition.</span><span class="sxs-lookup"><span data-stu-id="69765-147">As described in [Calling Asynchronous Methods](calling-asynchronous-methods.md), asynchronous methods in Media Foundation often use the **Begin...**/**End....** pattern.</span></span> <span data-ttu-id="69765-148">Dans ce modèle, une opération asynchrone utilise deux méthodes avec des signatures similaires à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="69765-148">In this pattern, an asynchronous operation uses two methods with signatures similar to the following:</span></span>

``` syntax
// Starts the asynchronous operation.
HRESULT BeginX(IMFAsyncCallback *pCallback, IUnknown *punkState);

// Completes the asynchronous operation. 
// Call this method from inside the caller's Invoke method.
HRESULT EndX(IMFAsyncResult *pResult);
```

<span data-ttu-id="69765-149">Pour rendre la méthode véritablement asynchrone, l’implémentation de **BeginX** doit effectuer le travail réel sur un autre thread.</span><span class="sxs-lookup"><span data-stu-id="69765-149">To make the method truly asynchronous, the implementation of **BeginX** must perform the actual work on another thread.</span></span> <span data-ttu-id="69765-150">C’est là que les files d’attente de travail entrent dans l’image.</span><span class="sxs-lookup"><span data-stu-id="69765-150">This is where work queues come into the picture.</span></span> <span data-ttu-id="69765-151">Dans les étapes qui suivent, l' *appelant* est le code qui appelle **BeginX** et **EndX**.</span><span class="sxs-lookup"><span data-stu-id="69765-151">In the steps that follow, the *caller* is the code that calls **BeginX** and **EndX**.</span></span> <span data-ttu-id="69765-152">Il peut s’agir d’une application ou du pipeline Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="69765-152">This might be an application or the Media Foundation pipeline.</span></span> <span data-ttu-id="69765-153">Le *composant* est le code qui implémente **BeginX** et **EndX**.</span><span class="sxs-lookup"><span data-stu-id="69765-153">The *component* is the code that implements **BeginX** and **EndX**.</span></span>

1.  <span data-ttu-id="69765-154">L’appelant appelle **Begin...**, en passant un pointeur vers l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="69765-154">The caller calls **Begin...**, passing in a pointer to the caller's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
2.  <span data-ttu-id="69765-155">Le composant crée un objet de résultat asynchrone.</span><span class="sxs-lookup"><span data-stu-id="69765-155">The component creates a new asynchronous result object.</span></span> <span data-ttu-id="69765-156">Cet objet stocke l’interface de rappel et l’objet d’état de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="69765-156">This object stores the caller's callback interface and state object.</span></span> <span data-ttu-id="69765-157">En règle générale, il stocke également toutes les informations d’État privé dont le composant a besoin pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="69765-157">Typically, it also stores any private state information that the component needs to complete the operation.</span></span> <span data-ttu-id="69765-158">L’objet de résultat de cette étape est intitulé « résultat 1 » dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="69765-158">The result object from this step is labeled "Result 1" in the next diagram.</span></span>
3.  <span data-ttu-id="69765-159">Le composant crée un deuxième objet de résultat.</span><span class="sxs-lookup"><span data-stu-id="69765-159">The component creates a second result object.</span></span> <span data-ttu-id="69765-160">Cet objet de résultat stocke deux pointeurs : le premier objet de résultat et l’interface de rappel de l’appelé.</span><span class="sxs-lookup"><span data-stu-id="69765-160">This result object stores two pointers: The first result object, and the callback interface of the callee.</span></span> <span data-ttu-id="69765-161">Cet objet de résultat est intitulé « résultat 2 » dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="69765-161">This result object is labeled "Result 2" in the next diagram.</span></span>
4.  <span data-ttu-id="69765-162">Le composant appelle [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) pour effectuer la mise en file d’attente d’un nouvel élément de travail.</span><span class="sxs-lookup"><span data-stu-id="69765-162">The component calls [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) to queue a new work item.</span></span>
5.  <span data-ttu-id="69765-163">Dans la méthode [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) , le composant effectue le travail asynchrone.</span><span class="sxs-lookup"><span data-stu-id="69765-163">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, the component does the asynchronous work.</span></span>
6.  <span data-ttu-id="69765-164">Le composant appelle [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) pour appeler la méthode de rappel de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="69765-164">The component calls [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) to invoke the caller's callback method.</span></span>
7.  <span data-ttu-id="69765-165">L’appelant appelle la méthode **EndX** .</span><span class="sxs-lookup"><span data-stu-id="69765-165">The caller calls the **EndX** method.</span></span>

![Diagramme montrant comment un objet implémente le modèle Begin/End](images/workqueues03.png)

## <a name="asynchronous-method-example"></a><span data-ttu-id="69765-167">Exemple de méthode asynchrone</span><span class="sxs-lookup"><span data-stu-id="69765-167">Asynchronous Method Example</span></span>

<span data-ttu-id="69765-168">Pour illustrer cette discussion, nous allons utiliser un exemple de fictif.</span><span class="sxs-lookup"><span data-stu-id="69765-168">To illustrate this discussion, we will use a contrived example.</span></span> <span data-ttu-id="69765-169">Prenons l’exemple d’une méthode asynchrone pour calculer une racine carrée :</span><span class="sxs-lookup"><span data-stu-id="69765-169">Consider an asynchronous method for computing a square root:</span></span>


```C++
    HRESULT BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState);
    HRESULT EndSquareRoot(IMFAsyncResult *pResult, double *pVal);
```



<span data-ttu-id="69765-170">Le paramètre *x* de `BeginSquareRoot` est la valeur dont la racine carrée sera calculée.</span><span class="sxs-lookup"><span data-stu-id="69765-170">The *x* parameter of `BeginSquareRoot` is the value whose square root will be calculated.</span></span> <span data-ttu-id="69765-171">La racine carrée est retournée dans le paramètre *pval* de `EndSquareRoot` .</span><span class="sxs-lookup"><span data-stu-id="69765-171">The square root is returned in the *pVal* parameter of `EndSquareRoot`.</span></span>

<span data-ttu-id="69765-172">Voici la déclaration d’une classe qui implémente ces deux méthodes :</span><span class="sxs-lookup"><span data-stu-id="69765-172">Here is the declaration of a class that implements these two methods:</span></span>


```C++
class SqrRoot : public IMFAsyncCallback
{
    LONG    m_cRef;
    double  m_sqrt;

    HRESULT DoCalculateSquareRoot(AsyncOp *pOp);

public:

    SqrRoot() : m_cRef(1)
    {

    }

    HRESULT BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState);
    HRESULT EndSquareRoot(IMFAsyncResult *pResult, double *pVal);

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(SqrRoot, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    // IMFAsyncCallback methods.

    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;  
    }
    // Invoke is where the work is performed.
    STDMETHODIMP Invoke(IMFAsyncResult* pResult);
};
```



<span data-ttu-id="69765-173">La `SqrRoot` classe implémente [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) afin qu’elle puisse placer l’opération racine carrée sur une file d’attente de travail.</span><span class="sxs-lookup"><span data-stu-id="69765-173">The `SqrRoot` class implements [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) so that it can put the square root operation on a work queue.</span></span> <span data-ttu-id="69765-174">La `DoCalculateSquareRoot` méthode est la méthode de classe privée qui calcule la racine carrée.</span><span class="sxs-lookup"><span data-stu-id="69765-174">The `DoCalculateSquareRoot` method is the private class method that calculates the square root.</span></span> <span data-ttu-id="69765-175">Cette méthode sera appelée à partir du thread de la file d’attente de travail.</span><span class="sxs-lookup"><span data-stu-id="69765-175">This method will be called from the work queue thread.</span></span>

<span data-ttu-id="69765-176">Tout d’abord, nous avons besoin d’un moyen de stocker la valeur de *x*, afin qu’elle puisse être récupérée lorsque le thread de file d’attente de travail appelle `SqrRoot::Invoke` .</span><span class="sxs-lookup"><span data-stu-id="69765-176">First, we need a way to store the value of *x*, so that it can be retrieved when the work queue thread calls `SqrRoot::Invoke`.</span></span> <span data-ttu-id="69765-177">Voici une classe simple qui stocke les informations :</span><span class="sxs-lookup"><span data-stu-id="69765-177">Here is a simple class that stores the information:</span></span>


```C++
class AsyncOp : public IUnknown
{
    LONG    m_cRef;

public:

    double  m_value;

    AsyncOp(double val) : m_cRef(1), m_value(val) { }

    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(AsyncOp, IUnknown),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }
};
```



<span data-ttu-id="69765-178">Cette classe implémente **IUnknown** afin qu’il puisse être stocké dans un objet de résultat.</span><span class="sxs-lookup"><span data-stu-id="69765-178">This class implements **IUnknown** so that it can be stored in a result object.</span></span>

<span data-ttu-id="69765-179">Le code suivant implémente la `BeginSquareRoot` méthode :</span><span class="sxs-lookup"><span data-stu-id="69765-179">The following code implements the `BeginSquareRoot` method:</span></span>


```C++
HRESULT SqrRoot::BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState)
{
    AsyncOp *pOp = new (std::nothrow) AsyncOp(x);
    if (pOp == NULL)
    {
        return E_OUTOFMEMORY;
    }

    IMFAsyncResult *pResult = NULL;

    // Create the inner result object. This object contains pointers to:
    // 
    //   1. The caller's callback interface and state object. 
    //   2. The AsyncOp object, which contains the operation data.
    //

    HRESULT hr = MFCreateAsyncResult(pOp, pCB, pState, &pResult);

    if (SUCCEEDED(hr))
    {
        // Queue a work item. The work item contains pointers to:
        // 
        // 1. The callback interface of the SqrRoot object.
        // 2. The inner result object.

        hr = MFPutWorkItem(MFASYNC_CALLBACK_QUEUE_STANDARD, this, pResult);

        pResult->Release();
    }

    return hr;
}
```



<span data-ttu-id="69765-180">Ce code effectue les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="69765-180">This code does the following:</span></span>

1.  <span data-ttu-id="69765-181">Crée une nouvelle instance de la `AsyncOp` classe pour contenir la valeur de *x*.</span><span class="sxs-lookup"><span data-stu-id="69765-181">Creates a new instance of the `AsyncOp` class to hold the value of *x*.</span></span>
2.  <span data-ttu-id="69765-182">Appelle [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) pour créer un objet de résultat.</span><span class="sxs-lookup"><span data-stu-id="69765-182">Calls [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) to create a result object.</span></span> <span data-ttu-id="69765-183">Cet objet contient plusieurs pointeurs :</span><span class="sxs-lookup"><span data-stu-id="69765-183">This object holds several pointers:</span></span>
    -   <span data-ttu-id="69765-184">Pointeur vers l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="69765-184">A pointer to the caller's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
    -   <span data-ttu-id="69765-185">Pointeur vers l’objet d’état de l’appelant (*pState*).</span><span class="sxs-lookup"><span data-stu-id="69765-185">A pointer to the caller's state object (*pState*).</span></span>
    -   <span data-ttu-id="69765-186">Pointeur vers l'objet `AsyncOp`.</span><span class="sxs-lookup"><span data-stu-id="69765-186">A pointer to the `AsyncOp` object.</span></span>
3.  <span data-ttu-id="69765-187">Appelle [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) pour effectuer la mise en file d’attente d’un nouvel élément de travail.</span><span class="sxs-lookup"><span data-stu-id="69765-187">Calls [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) to queue a new work item.</span></span> <span data-ttu-id="69765-188">Cet appel crée implicitement un objet de résultat externe, qui contient les pointeurs suivants :</span><span class="sxs-lookup"><span data-stu-id="69765-188">This call implicitly creates an outer result object, which holds the following pointers:</span></span>
    -   <span data-ttu-id="69765-189">Pointeur vers l' `SqrRoot` interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="69765-189">A pointer to the `SqrRoot` object's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
    -   <span data-ttu-id="69765-190">Pointeur vers l’objet de résultat interne de l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="69765-190">A pointer to the inner result object from step 2.</span></span>

<span data-ttu-id="69765-191">Le code suivant implémente la `SqrRoot::Invoke` méthode :</span><span class="sxs-lookup"><span data-stu-id="69765-191">The following code implements the `SqrRoot::Invoke` method:</span></span>


```C++
// Invoke is called by the work queue. This is where the object performs the
// asynchronous operation.

STDMETHODIMP SqrRoot::Invoke(IMFAsyncResult* pResult)
{
    HRESULT hr = S_OK;

    IUnknown *pState = NULL;
    IUnknown *pUnk = NULL;
    IMFAsyncResult *pCallerResult = NULL;

    AsyncOp *pOp = NULL; 

    // Get the asynchronous result object for the application callback. 

    hr = pResult->GetState(&pState);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pState->QueryInterface(IID_PPV_ARGS(&pCallerResult));
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the object that holds the state information for the asynchronous method.
    hr = pCallerResult->GetObject(&pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    pOp = static_cast<AsyncOp*>(pUnk);

    // Do the work.

    hr = DoCalculateSquareRoot(pOp);

done:
    // Signal the application.
    if (pCallerResult)
    {
        pCallerResult->SetStatus(hr);
        MFInvokeCallback(pCallerResult);
    }

    SafeRelease(&pState);
    SafeRelease(&pUnk);
    SafeRelease(&pCallerResult);
    return S_OK;
}
```



<span data-ttu-id="69765-192">Cette méthode obtient l’objet de résultat interne et l' `AsyncOp` objet.</span><span class="sxs-lookup"><span data-stu-id="69765-192">This method gets the inner result object and the `AsyncOp` object.</span></span> <span data-ttu-id="69765-193">Ensuite, il passe l' `AsyncOp` objet à `DoCalculateSquareRoot` .</span><span class="sxs-lookup"><span data-stu-id="69765-193">Then it passes the `AsyncOp` object to `DoCalculateSquareRoot`.</span></span> <span data-ttu-id="69765-194">Enfin, il appelle [**IMFAsyncResult :: SetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-setstatus) pour définir le code d’État et [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) pour appeler la méthode de rappel de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="69765-194">Finally, it calls [**IMFAsyncResult::SetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-setstatus) to set the status code and [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) to invoke the caller's callback method.</span></span>

<span data-ttu-id="69765-195">La `DoCalculateSquareRoot` méthode fait exactement ce que vous attendez :</span><span class="sxs-lookup"><span data-stu-id="69765-195">The `DoCalculateSquareRoot` method does exactly what you would expect:</span></span>


```C++
HRESULT SqrRoot::DoCalculateSquareRoot(AsyncOp *pOp)
{
    pOp->m_value = sqrt(pOp->m_value);

    return S_OK;
}
```



<span data-ttu-id="69765-196">Quand la méthode de rappel de l’appelant est appelée, il incombe à l’appelant d’appeler la méthode **end...** , dans ce cas, `EndSquareRoot` .</span><span class="sxs-lookup"><span data-stu-id="69765-196">When the caller's callback method is invoked, it is the caller's responsibility to call the **End...** method—in this case, `EndSquareRoot`.</span></span> <span data-ttu-id="69765-197">La `EndSquareRoot` méthode est la manière dont l’appelant récupère le résultat de l’opération asynchrone, qui, dans cet exemple, est la racine carrée calculée.</span><span class="sxs-lookup"><span data-stu-id="69765-197">The `EndSquareRoot` is how the caller retrieves the result of the asynchronous operation, which in this example is the computed square root.</span></span> <span data-ttu-id="69765-198">Ces informations sont stockées dans l’objet de résultat :</span><span class="sxs-lookup"><span data-stu-id="69765-198">This information is stored in the result object:</span></span>


```C++
HRESULT SqrRoot::EndSquareRoot(IMFAsyncResult *pResult, double *pVal)
{
    *pVal = 0;

    IUnknown *pUnk = NULL;

    HRESULT hr = pResult->GetStatus();

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pResult->GetObject(&pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    AsyncOp *pOp = static_cast<AsyncOp*>(pUnk);

    // Get the result.
    *pVal = pOp->m_value;

done:
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="operation-queues"></a><span data-ttu-id="69765-199">Files d’attente d’opérations</span><span class="sxs-lookup"><span data-stu-id="69765-199">Operation Queues</span></span>

<span data-ttu-id="69765-200">Jusqu’à présent, il a été tacitement supposé qu’une opération asynchrone pouvait être effectuée à tout moment, quel que soit l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="69765-200">So far, it has been tacitly assumed that an asynchronous operation could be done at any time, regardless of the object's current state.</span></span> <span data-ttu-id="69765-201">Par exemple, considérez ce qui se passe si une application appelle `BeginSquareRoot` alors qu’un appel antérieur à la même méthode est toujours en attente.</span><span class="sxs-lookup"><span data-stu-id="69765-201">For example, consider what happens if an application calls `BeginSquareRoot` while an earlier call to the same method is still pending.</span></span> <span data-ttu-id="69765-202">La `SqrRoot` classe peut faire en file d’attente le nouvel élément de travail avant la fin de l’élément de travail précédent.</span><span class="sxs-lookup"><span data-stu-id="69765-202">The `SqrRoot` class might queue the new work item before the previous work item is done.</span></span> <span data-ttu-id="69765-203">Toutefois, il n’est pas garanti que les files d’attente de travail sérialisent les éléments de travail.</span><span class="sxs-lookup"><span data-stu-id="69765-203">However, work queues are not guaranteed to serialize work items.</span></span> <span data-ttu-id="69765-204">Rappelez-vous qu’une file d’attente de travail peut utiliser plusieurs threads pour distribuer des éléments de travail.</span><span class="sxs-lookup"><span data-stu-id="69765-204">Recall that a work queue can use more than one thread to dispatch work items.</span></span> <span data-ttu-id="69765-205">Dans un environnement multithread, un élément de travail peut être appelé avant la fin de l’opération précédente.</span><span class="sxs-lookup"><span data-stu-id="69765-205">In a multithreaded environment, a work item might be invoked before the previous one has completed.</span></span> <span data-ttu-id="69765-206">Les éléments de travail peuvent même être appelés dans le désordre, si un changement de contexte se produit juste avant l’appel du rappel.</span><span class="sxs-lookup"><span data-stu-id="69765-206">Work items can even be invoked out of order, if a context switch happens to occur just before the callback is invoked.</span></span>

<span data-ttu-id="69765-207">Pour cette raison, il est de la responsabilité de l’objet de sérialiser les opérations sur lui-même, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="69765-207">For this reason, it is the object's responsibility to serialize operations on itself, if required.</span></span> <span data-ttu-id="69765-208">En d’autres termes, si l’objet exige que l’opération *a* se termine avant que l’opération *b* puisse démarrer, l’objet ne doit pas mettre en file d’attente un élément de travail pour *b* tant que l’opération *a n’est* pas terminée.</span><span class="sxs-lookup"><span data-stu-id="69765-208">In other words, if the object requires operation *A* to finish before operation *B* can start, the object must not queue a work item for *B* until operation *A* has completed.</span></span> <span data-ttu-id="69765-209">Un objet peut répondre à cette exigence en ayant sa propre file d’attente d’opérations en attente.</span><span class="sxs-lookup"><span data-stu-id="69765-209">An object can meet this requirement by having its own queue of pending operations.</span></span> <span data-ttu-id="69765-210">Lorsqu’une méthode asynchrone est appelée sur l’objet, l’objet place la demande dans sa propre file d’attente.</span><span class="sxs-lookup"><span data-stu-id="69765-210">When an asynchronous method is called on the object, the object puts the request on its own queue.</span></span> <span data-ttu-id="69765-211">À mesure que chaque opération asynchrone est terminée, l’objet extrait la requête suivante à partir de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="69765-211">As each asynchronous operation is completed, the object pulls the next request from the queue.</span></span> <span data-ttu-id="69765-212">L' [exemple MPEG1Source](mpeg1source-sample.md) montre comment implémenter une telle file d’attente.</span><span class="sxs-lookup"><span data-stu-id="69765-212">The [MPEG1Source Sample](mpeg1source-sample.md) shows an example of how to implement such a queue.</span></span>

<span data-ttu-id="69765-213">Une méthode unique peut impliquer plusieurs opérations asynchrones, en particulier lors de l’utilisation d’appels d’e/s.</span><span class="sxs-lookup"><span data-stu-id="69765-213">A single method might involve several asynchronous operations, particularly when I/O calls are used.</span></span> <span data-ttu-id="69765-214">Lorsque vous implémentez des méthodes asynchrones, réfléchissez soigneusement aux exigences de sérialisation.</span><span class="sxs-lookup"><span data-stu-id="69765-214">When you implement asynchronous methods, think carefully about serialization requirements.</span></span> <span data-ttu-id="69765-215">Par exemple, est-il valide pour l’objet de démarrer une nouvelle opération alors qu’une demande d’e/s précédente est toujours en attente ?</span><span class="sxs-lookup"><span data-stu-id="69765-215">For example, is it valid for the object to start a new operation while a previous I/O request is still pending?</span></span> <span data-ttu-id="69765-216">Si la nouvelle opération modifie l’état interne de l’objet, que se passe-t-il lorsqu’une requête d’e/s précédente se termine et retourne des données qui peuvent maintenant être obsolètes ?</span><span class="sxs-lookup"><span data-stu-id="69765-216">If the new operation changes the object's internal state, what happens when a previous I/O request completes and returns data that might now be stale?</span></span> <span data-ttu-id="69765-217">Un diagramme d’état correct peut aider à identifier les transitions d’état valides.</span><span class="sxs-lookup"><span data-stu-id="69765-217">A good state diagram can help to identify the valid state transitions.</span></span>

## <a name="cross-thread-and-cross-process-considerations"></a><span data-ttu-id="69765-218">Considérations inter-threads et inter-processus</span><span class="sxs-lookup"><span data-stu-id="69765-218">Cross-Thread and Cross-Process Considerations</span></span>

<span data-ttu-id="69765-219">Les files d’attente de travail n’utilisent pas le marshaling COM pour marshaler des pointeurs d’interface à travers les limites de thread.</span><span class="sxs-lookup"><span data-stu-id="69765-219">Work queues do not use COM marshaling to marshal interface pointers across thread boundaries.</span></span> <span data-ttu-id="69765-220">Par conséquent, même si un objet est inscrit en tant que thread cloisonné ou si le thread d’application est entré dans un thread cloisonné (STA, Single-Threaded Apartment), les rappels [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) sont appelés à partir d’un thread différent.</span><span class="sxs-lookup"><span data-stu-id="69765-220">Therefore, even if an object is registered as apartment-threaded or the application thread has entered a single-threaded apartment (STA), [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) callbacks will be invoked from a different thread.</span></span> <span data-ttu-id="69765-221">Dans tous les cas, tous les composants de pipeline Media Foundation doivent utiliser le modèle de thread « both ».</span><span class="sxs-lookup"><span data-stu-id="69765-221">In any case, all Media Foundation pipeline components should use the "Both" threading model.</span></span>

<span data-ttu-id="69765-222">Certaines interfaces dans Media Foundation définissent des versions distantes de certaines méthodes asynchrones.</span><span class="sxs-lookup"><span data-stu-id="69765-222">Some interfaces in Media Foundation define remote versions of some asynchronous methods.</span></span> <span data-ttu-id="69765-223">Quand l’une de ces méthodes est appelée à travers les limites du processus, la DLL proxy/stub Media Foundation appelle la version distante de la méthode, qui effectue le marshaling personnalisé des paramètres de la méthode.</span><span class="sxs-lookup"><span data-stu-id="69765-223">When one of these methods is called across process boundaries, the Media Foundation proxy/stub DLL calls the remote version of the method, which performs custom marshaling of the method parameters.</span></span> <span data-ttu-id="69765-224">Dans le processus distant, le stub traduit le rappel dans la méthode locale sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="69765-224">In the remote process, the stub translates the call back into the local method on the object.</span></span> <span data-ttu-id="69765-225">Ce processus est transparent pour l’application et l’objet distant.</span><span class="sxs-lookup"><span data-stu-id="69765-225">This process is transparent to both the application and the remote object.</span></span> <span data-ttu-id="69765-226">Ces méthodes de marshaling personnalisées sont fournies principalement pour les objets qui sont chargés dans le chemin d’accès de média protégé (PMP).</span><span class="sxs-lookup"><span data-stu-id="69765-226">These custom marshaling methods are provided primarily for objects that are loaded in the protected media path (PMP).</span></span> <span data-ttu-id="69765-227">Pour plus d’informations sur le PMP, consultez [chemin d’accès au média protégé](protected-media-path.md).</span><span class="sxs-lookup"><span data-stu-id="69765-227">For more information about the PMP, see [Protected Media Path](protected-media-path.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="69765-228">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="69765-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69765-229">Méthodes de rappel asynchrones</span><span class="sxs-lookup"><span data-stu-id="69765-229">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)
</dt> <dt>

[<span data-ttu-id="69765-230">Files d’attente de travail</span><span class="sxs-lookup"><span data-stu-id="69765-230">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 



