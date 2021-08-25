---
description: Appeler des méthodes asynchrones
ms.assetid: 1d8688a5-d476-457d-a0ad-e4f106ac3484
title: Appeler des méthodes asynchrones
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a53f5f0a3062ad6af955fbbfdd8cd05c82b30271cf680d6434bc652d567325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959199"
---
# <a name="calling-asynchronous-methods"></a>Appeler des méthodes asynchrones

Dans Media Foundation, de nombreuses opérations sont exécutées de façon asynchrone. Les opérations asynchrones peuvent améliorer les performances, car elles ne bloquent pas le thread appelant. Une opération asynchrone dans Media Foundation est définie par une paire de méthodes avec la Convention d’affectation de noms **Begin..** . et **end...**. Ensemble, ces deux méthodes définissent une opération de lecture asynchrone sur le flux.

Pour démarrer une opération asynchrone, appelez la méthode **Begin** . La méthode **Begin** contient toujours au moins deux paramètres :

-   Pointeur vers l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) . L’application doit implémenter cette interface.
-   Pointeur vers un objet d’État facultatif.

L’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) avertit l’application lorsque l’opération est terminée. Pour obtenir un exemple d’implémentation de cette interface, consultez [implémentation du rappel asynchrone](implementing-the-asynchronous-callback.md). L’objet d’État est facultatif. S’il est spécifié, il doit implémenter l’interface **IUnknown** . Vous pouvez utiliser l’objet d’État pour stocker toutes les informations d’État requises par votre rappel. Si vous n’avez pas besoin d’informations d’État, vous pouvez définir ce paramètre sur la **valeur null**. La méthode **Begin** peut contenir des paramètres supplémentaires qui sont spécifiques à cette méthode.

Si la méthode **Begin** retourne un code d’échec, cela signifie que l’opération a échoué immédiatement et que le rappel n’est pas appelé. Si la méthode **Begin** réussit, cela signifie que l’opération est en attente et que le rappel est appelé lorsque l’opération se termine.

Par exemple, la méthode [**IMFByteStream :: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) démarre une opération de lecture asynchrone sur un flux d’octets :


```C++
    BYTE data[DATA_SIZE];
    ULONG cbRead = 0;

    CMyCallback *pCB = new (std::nothrow) CMyCallback(pStream, &hr);

    if (pCB == NULL)
    {
        hr = E_OUTOFMEMORY;
    }

    // Start an asynchronous request to read data.
    if (SUCCEEDED(hr))
    {
        hr = pStream->BeginRead(data, DATA_SIZE, pCB, NULL);
    }
```



La méthode de rappel est [**IMFAsyncCallback :: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke). Il possède un seul paramètre, *pAsyncResult*, qui est un pointeur vers l’interface [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) . Pour terminer l’opération asynchrone, appelez la méthode **end** qui correspond à la méthode **Begin** asynchrone. La méthode **end** prend toujours un pointeur **IMFAsyncResult** . Transmettez toujours le même pointeur que celui que vous avez reçu dans la méthode **Invoke** . L’opération asynchrone n’est pas terminée tant que vous n’avez pas appelé la méthode **end** . Vous pouvez appeler la méthode **end** à partir de la méthode **Invoke** , ou vous pouvez l’appeler à partir d’un autre thread.

Par exemple, pour terminer [**IMFByteStream :: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) sur un flux d’octets, appelez [**IMFByteStream :: EndRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endread):


```C++
    STDMETHODIMP Invoke(IMFAsyncResult* pResult)
    {
        m_hrStatus = m_pStream->EndRead(pResult, &m_cbRead);

        SetEvent(m_hEvent);

        return S_OK;
    }
```



La valeur de retour de la méthode **end** indique l’état de l’opération asynchrone. Dans la plupart des cas, votre application effectue un travail après l’exécution de l’opération asynchrone, qu’elle se termine correctement ou non. Vous disposez de plusieurs options :

-   Effectuez le travail à l’intérieur de la méthode [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) . Cette approche est acceptable tant que votre application ne bloque jamais le thread appelant ou n’attend rien à l’intérieur de la méthode **Invoke** . Si vous bloquez le thread appelant, vous risquez de bloquer le pipeline de diffusion en continu. Par exemple, vous pouvez mettre à jour certaines variables d’État, mais n’effectuez pas d’opération de lecture synchrone ou d’attente sur un objet Mutex.
-   Dans la méthode [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) , définissez un événement et retournez immédiatement. Le thread appelant de l’application attend l’événement et effectue le travail lorsque l’événement est signalé.
-   Dans la méthode [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) , publiez un message de fenêtre privée dans la fenêtre de votre application et revenez immédiatement. L’application effectue le travail sur sa boucle de message. (Veillez à poster le message en appelant **PostMessage**, et non **SendMessage**, car **SendMessage** peut bloquer le thread de rappel.)

Il est important de se souvenir que [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) est appelé à partir d’un autre thread. Votre application est chargée de s’assurer que tout travail effectué dans **Invoke** est thread-safe.

Par défaut, le thread qui appelle [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) n’émet aucune hypothèse sur le comportement de votre objet de rappel. Si vous le souhaitez, vous pouvez implémenter la méthode [**IMFAsyncCallback :: GetParameters**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters) pour retourner des informations sur votre implémentation de rappel. Sinon, cette méthode peut retourner **E \_ NOTIMPL**:


```C++
    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
```



Si vous avez spécifié un objet d’État dans la méthode **Begin** , vous pouvez le récupérer à l’intérieur de votre méthode de rappel en appelant [**IMFAsyncResult :: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Méthodes de rappel asynchrones](asynchronous-callback-methods.md)
</dt> </dl>

 

 



