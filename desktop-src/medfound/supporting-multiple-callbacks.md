---
description: Prise en charge de plusieurs rappels
ms.assetid: d57544cc-f16c-4415-9411-d06d6c16cb2f
title: Prise en charge de plusieurs rappels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 614d92a50101a5ed4e7c281dc76a3edce930fa06d68e11484dc89a3cad83de05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118057704"
---
# <a name="supporting-multiple-callbacks"></a>Prise en charge de plusieurs rappels

Si vous appelez plusieurs méthodes asynchrones, chacune d’elles requiert une implémentation distincte de [**IMFAsyncCallback :: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke). Toutefois, vous souhaiterez peut-être implémenter les rappels à l’intérieur d’une classe C++ unique. La classe ne pouvant avoir qu’une seule méthode **Invoke** , une solution consiste à fournir une classe d’assistance qui délègue les appels **Invoke** à une autre méthode sur une classe de conteneur.

Le code suivant illustre un modèle de classe nommé `AsyncCallback` , qui illustre cette approche.


```C++
//////////////////////////////////////////////////////////////////////////
//  AsyncCallback [template]
//
//  Description:
//  Helper class that routes IMFAsyncCallback::Invoke calls to a class
//  method on the parent class.
//
//  Usage:
//  Add this class as a member variable. In the parent class constructor,
//  initialize the AsyncCallback class like this:
//      m_cb(this, &CYourClass::OnInvoke)
//  where
//      m_cb       = AsyncCallback object
//      CYourClass = parent class
//      OnInvoke   = Method in the parent class to receive Invoke calls.
//
//  The parent's OnInvoke method (you can name it anything you like) must
//  have a signature that matches the InvokeFn typedef below.
//////////////////////////////////////////////////////////////////////////

// T: Type of the parent object
template<class T>
class AsyncCallback : public IMFAsyncCallback
{
public:
    typedef HRESULT (T::*InvokeFn)(IMFAsyncResult *pAsyncResult);

    AsyncCallback(T *pParent, InvokeFn fn) : m_pParent(pParent), m_pInvokeFn(fn)
    {
    }

    // IUnknown
    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] =
        {
            QITABENT(AsyncCallback, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }
    STDMETHODIMP_(ULONG) AddRef() {
        // Delegate to parent class.
        return m_pParent->AddRef();
    }
    STDMETHODIMP_(ULONG) Release() {
        // Delegate to parent class.
        return m_pParent->Release();
    }

    // IMFAsyncCallback methods
    STDMETHODIMP GetParameters(DWORD*, DWORD*)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }

    STDMETHODIMP Invoke(IMFAsyncResult* pAsyncResult)
    {
        return (m_pParent->*m_pInvokeFn)(pAsyncResult);
    }

    T *m_pParent;
    InvokeFn m_pInvokeFn;
};
```



Le paramètre de modèle est le nom de la classe de conteneur. Le `AsyncCallback` constructeur a deux paramètres : un pointeur vers la classe de conteneur et l’adresse d’une méthode de rappel sur la classe de conteneur. La classe de conteneur peut avoir plusieurs instances de la `AsyncCallback` classe en tant que variables membres, une pour chaque méthode asynchrone. Quand la classe de conteneur appelle une méthode asynchrone, elle utilise l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) de l' `AsyncCallback` objet approprié. Lorsque la `AsyncCallback` méthode [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) de l’objet est appelée, l’appel est délégué à la méthode correcte sur la classe de conteneur.

L' `AsyncCallback` objet délègue également des appels de **AddRef** et de **Release** à la classe de conteneur, de sorte que la classe de conteneur gère la durée de vie de l' `AsyncCallback` objet. Cela garantit que l' `AsyncCallback` objet n’est pas supprimé tant que l’objet conteneur lui-même n’est pas supprimé.

Le code suivant illustre l’utilisation de ce modèle :


```C++
#pragma warning( push )
#pragma warning( disable : 4355 )  // 'this' used in base member initializer list

class CMyObject : public IUnknown
{
public:

    CMyObject() : m_CB(this, &CMyObject::OnInvoke)
    {
        // Other initialization here.
    }

    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);


private:

    AsyncCallback<CMyObject>   m_CB;

    HRESULT OnInvoke(IMFAsyncResult *pAsyncResult);
};

#pragma warning( pop )
```



Dans cet exemple, la classe de conteneur est nommée `CMyObject` . La variable de membre *m \_ CB* est un `AsyncCallback` objet. Dans le `CMyObject` constructeur, la variable de membre *m \_ CB* est initialisée avec l’adresse de la `CMyObject::OnInvoke` méthode.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Méthodes de rappel asynchrones](asynchronous-callback-methods.md)
</dt> </dl>

 

 



