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
# <a name="writing-an-asynchronous-method"></a>Écriture d’une méthode asynchrone

Cette rubrique explique comment implémenter une méthode asynchrone dans Microsoft Media Foundation.

Les méthodes asynchrones sont omniprésentes dans le pipeline Media Foundation. Les méthodes asynchrones facilitent la répartition du travail entre plusieurs threads. Il est particulièrement important d’effectuer des e/s de manière asynchrone, de sorte que la lecture à partir d’un fichier ou d’un réseau ne bloque pas le reste du pipeline.

Si vous écrivez une source multimédia ou un récepteur multimédia, il est essentiel de gérer correctement les opérations asynchrones, car les performances de votre composant ont un impact sur l’ensemble du pipeline.

> [!Note]  
> Les transformations de Media Foundation (MFTs) utilisent des méthodes synchrones par défaut.

 

### <a name="work-queues-for-asynchronous-operations"></a>Files d’attente de travail pour les opérations asynchrones

Dans Media Foundation, il existe une relation étroite entre les [méthodes de rappel asynchrones](asynchronous-callback-methods.md) et les [files d’attente de travail](work-queues.md). Une file d’attente de travail est une abstraction pour déplacer le travail du thread de l’appelant vers un thread de travail. Pour effectuer un travail sur une file d’attente de travail, procédez comme suit :

1.  Implémentez l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .
2.  Appelez [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) pour créer un objet de *résultat* . L’objet de résultat expose le [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult). L’objet de résultat contient trois pointeurs :

    -   Pointeur vers l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) de l’appelant.
    -   Pointeur facultatif vers un objet d’État. S’il est spécifié, l’objet d’État doit implémenter **IUnknown**.
    -   Pointeur facultatif vers un objet privé. S’il est spécifié, cet objet doit également implémenter **IUnknown**.

    Les deux derniers pointeurs peuvent avoir la **valeur null**. Dans le cas contraire, utilisez-les pour stocker des informations sur l’opération asynchrone.

3.  Appelez [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) pour effectuer la file d’attente vers l’élément de travail.
4.  Le thread de file d’attente de travail appelle votre méthode [**IMFAsyncCallback :: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) .
5.  Effectuez le travail à l’intérieur de votre méthode [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) . Le paramètre *pAsyncResult* de cette méthode est le pointeur [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) de l’étape 2. Utilisez ce pointeur pour récupérer l’objet d’État et l’objet privé :
    -   Pour accéder à l’objet d’État, appelez [**IMFAsyncResult :: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).
    -   Pour accéder à l’objet privé, appelez [**IMFAsyncResult :: GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject).

Vous pouvez également combiner les étapes 2 et 3 en appelant la fonction [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) . En interne, cette fonction appelle [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) pour créer l’objet de résultat.

Le diagramme suivant montre les relations entre l’appelant, l’objet de résultat, l’objet d’État et l’objet privé.

![Diagramme montrant un objet de résultat asynchrone](images/workqueues01.png)

Le diagramme de séquence suivant montre comment un objet met en file d’attente un élément de travail. Lorsque le thread de file d’attente de travail appelle [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), l’objet effectue l’opération asynchrone sur ce thread.

![Diagramme montrant comment un objet met en file d’attente un élément de travail](images/workqueues02.png)

Il est important de se souvenir que [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) est appelé à partir d’un thread qui appartient à la file d’attente de travail. Votre implémentation de **Invoke** doit être thread-safe. En outre, si vous utilisez la file d’attente de travail de la plateforme (**MFASYNC \_ callback \_ Queue \_ standard**), il est essentiel de ne jamais bloquer le thread, car cela peut bloquer l’intégralité du pipeline Media Foundation du traitement des données. Si vous devez effectuer une opération qui se bloque ou prend beaucoup de temps, utilisez une file d’attente de travail privée. Pour créer une file d’attente de travail privée, appelez [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue). Tout composant de pipeline qui effectue des opérations d’e/s doit éviter de bloquer les appels d’e/s pour la même raison. L’interface [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) fournit une abstraction utile pour les e/s de fichier asynchrones.

### <a name="implementing-the-beginend-pattern"></a>Implémentation de BEGIN. ../end... Répétition

Comme décrit dans [appel de méthodes asynchrones](calling-asynchronous-methods.md), les méthodes asynchrones dans Media Foundation utilisent souvent la méthode **Begin...** / **Fin....** répétition. Dans ce modèle, une opération asynchrone utilise deux méthodes avec des signatures similaires à ce qui suit :

``` syntax
// Starts the asynchronous operation.
HRESULT BeginX(IMFAsyncCallback *pCallback, IUnknown *punkState);

// Completes the asynchronous operation. 
// Call this method from inside the caller's Invoke method.
HRESULT EndX(IMFAsyncResult *pResult);
```

Pour rendre la méthode véritablement asynchrone, l’implémentation de **BeginX** doit effectuer le travail réel sur un autre thread. C’est là que les files d’attente de travail entrent dans l’image. Dans les étapes qui suivent, l' *appelant* est le code qui appelle **BeginX** et **EndX**. Il peut s’agir d’une application ou du pipeline Media Foundation. Le *composant* est le code qui implémente **BeginX** et **EndX**.

1.  L’appelant appelle **Begin...**, en passant un pointeur vers l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) de l’appelant.
2.  Le composant crée un objet de résultat asynchrone. Cet objet stocke l’interface de rappel et l’objet d’état de l’appelant. En règle générale, il stocke également toutes les informations d’État privé dont le composant a besoin pour terminer l’opération. L’objet de résultat de cette étape est intitulé « résultat 1 » dans le diagramme suivant.
3.  Le composant crée un deuxième objet de résultat. Cet objet de résultat stocke deux pointeurs : le premier objet de résultat et l’interface de rappel de l’appelé. Cet objet de résultat est intitulé « résultat 2 » dans le diagramme suivant.
4.  Le composant appelle [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) pour effectuer la mise en file d’attente d’un nouvel élément de travail.
5.  Dans la méthode [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) , le composant effectue le travail asynchrone.
6.  Le composant appelle [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) pour appeler la méthode de rappel de l’appelant.
7.  L’appelant appelle la méthode **EndX** .

![Diagramme montrant comment un objet implémente le modèle Begin/End](images/workqueues03.png)

## <a name="asynchronous-method-example"></a>Exemple de méthode asynchrone

Pour illustrer cette discussion, nous allons utiliser un exemple de fictif. Prenons l’exemple d’une méthode asynchrone pour calculer une racine carrée :


```C++
    HRESULT BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState);
    HRESULT EndSquareRoot(IMFAsyncResult *pResult, double *pVal);
```



Le paramètre *x* de `BeginSquareRoot` est la valeur dont la racine carrée sera calculée. La racine carrée est retournée dans le paramètre *pval* de `EndSquareRoot` .

Voici la déclaration d’une classe qui implémente ces deux méthodes :


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



La `SqrRoot` classe implémente [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) afin qu’elle puisse placer l’opération racine carrée sur une file d’attente de travail. La `DoCalculateSquareRoot` méthode est la méthode de classe privée qui calcule la racine carrée. Cette méthode sera appelée à partir du thread de la file d’attente de travail.

Tout d’abord, nous avons besoin d’un moyen de stocker la valeur de *x*, afin qu’elle puisse être récupérée lorsque le thread de file d’attente de travail appelle `SqrRoot::Invoke` . Voici une classe simple qui stocke les informations :


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



Cette classe implémente **IUnknown** afin qu’il puisse être stocké dans un objet de résultat.

Le code suivant implémente la `BeginSquareRoot` méthode :


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



Ce code effectue les actions suivantes :

1.  Crée une nouvelle instance de la `AsyncOp` classe pour contenir la valeur de *x*.
2.  Appelle [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) pour créer un objet de résultat. Cet objet contient plusieurs pointeurs :
    -   Pointeur vers l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) de l’appelant.
    -   Pointeur vers l’objet d’état de l’appelant (*pState*).
    -   Pointeur vers l'objet `AsyncOp`.
3.  Appelle [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) pour effectuer la mise en file d’attente d’un nouvel élément de travail. Cet appel crée implicitement un objet de résultat externe, qui contient les pointeurs suivants :
    -   Pointeur vers l' `SqrRoot` interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) de l’objet.
    -   Pointeur vers l’objet de résultat interne de l’étape 2.

Le code suivant implémente la `SqrRoot::Invoke` méthode :


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



Cette méthode obtient l’objet de résultat interne et l' `AsyncOp` objet. Ensuite, il passe l' `AsyncOp` objet à `DoCalculateSquareRoot` . Enfin, il appelle [**IMFAsyncResult :: SetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-setstatus) pour définir le code d’État et [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) pour appeler la méthode de rappel de l’appelant.

La `DoCalculateSquareRoot` méthode fait exactement ce que vous attendez :


```C++
HRESULT SqrRoot::DoCalculateSquareRoot(AsyncOp *pOp)
{
    pOp->m_value = sqrt(pOp->m_value);

    return S_OK;
}
```



Quand la méthode de rappel de l’appelant est appelée, il incombe à l’appelant d’appeler la méthode **end...** , dans ce cas, `EndSquareRoot` . La `EndSquareRoot` méthode est la manière dont l’appelant récupère le résultat de l’opération asynchrone, qui, dans cet exemple, est la racine carrée calculée. Ces informations sont stockées dans l’objet de résultat :


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



## <a name="operation-queues"></a>Files d’attente d’opérations

Jusqu’à présent, il a été tacitement supposé qu’une opération asynchrone pouvait être effectuée à tout moment, quel que soit l’état actuel de l’objet. Par exemple, considérez ce qui se passe si une application appelle `BeginSquareRoot` alors qu’un appel antérieur à la même méthode est toujours en attente. La `SqrRoot` classe peut faire en file d’attente le nouvel élément de travail avant la fin de l’élément de travail précédent. Toutefois, il n’est pas garanti que les files d’attente de travail sérialisent les éléments de travail. Rappelez-vous qu’une file d’attente de travail peut utiliser plusieurs threads pour distribuer des éléments de travail. Dans un environnement multithread, un élément de travail peut être appelé avant la fin de l’opération précédente. Les éléments de travail peuvent même être appelés dans le désordre, si un changement de contexte se produit juste avant l’appel du rappel.

Pour cette raison, il est de la responsabilité de l’objet de sérialiser les opérations sur lui-même, si nécessaire. En d’autres termes, si l’objet exige que l’opération *a* se termine avant que l’opération *b* puisse démarrer, l’objet ne doit pas mettre en file d’attente un élément de travail pour *b* tant que l’opération *a n’est* pas terminée. Un objet peut répondre à cette exigence en ayant sa propre file d’attente d’opérations en attente. Lorsqu’une méthode asynchrone est appelée sur l’objet, l’objet place la demande dans sa propre file d’attente. À mesure que chaque opération asynchrone est terminée, l’objet extrait la requête suivante à partir de la file d’attente. L' [exemple MPEG1Source](mpeg1source-sample.md) montre comment implémenter une telle file d’attente.

Une méthode unique peut impliquer plusieurs opérations asynchrones, en particulier lors de l’utilisation d’appels d’e/s. Lorsque vous implémentez des méthodes asynchrones, réfléchissez soigneusement aux exigences de sérialisation. Par exemple, est-il valide pour l’objet de démarrer une nouvelle opération alors qu’une demande d’e/s précédente est toujours en attente ? Si la nouvelle opération modifie l’état interne de l’objet, que se passe-t-il lorsqu’une requête d’e/s précédente se termine et retourne des données qui peuvent maintenant être obsolètes ? Un diagramme d’état correct peut aider à identifier les transitions d’état valides.

## <a name="cross-thread-and-cross-process-considerations"></a>Considérations inter-threads et inter-processus

Les files d’attente de travail n’utilisent pas le marshaling COM pour marshaler des pointeurs d’interface à travers les limites de thread. Par conséquent, même si un objet est inscrit en tant que thread cloisonné ou si le thread d’application est entré dans un thread cloisonné (STA, Single-Threaded Apartment), les rappels [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) sont appelés à partir d’un thread différent. Dans tous les cas, tous les composants de pipeline Media Foundation doivent utiliser le modèle de thread « both ».

Certaines interfaces dans Media Foundation définissent des versions distantes de certaines méthodes asynchrones. Quand l’une de ces méthodes est appelée à travers les limites du processus, la DLL proxy/stub Media Foundation appelle la version distante de la méthode, qui effectue le marshaling personnalisé des paramètres de la méthode. Dans le processus distant, le stub traduit le rappel dans la méthode locale sur l’objet. Ce processus est transparent pour l’application et l’objet distant. Ces méthodes de marshaling personnalisées sont fournies principalement pour les objets qui sont chargés dans le chemin d’accès de média protégé (PMP). Pour plus d’informations sur le PMP, consultez [chemin d’accès au média protégé](protected-media-path.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Méthodes de rappel asynchrones](asynchronous-callback-methods.md)
</dt> <dt>

[Files d’attente de travail](work-queues.md)
</dt> </dl>

 

 



