---
description: Prise en charge de plusieurs rappels
ms.assetid: d57544cc-f16c-4415-9411-d06d6c16cb2f
title: Prise en charge de plusieurs rappels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b77a15899488e44ea3c1499b11af65894d47483c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755261"
---
# <a name="supporting-multiple-callbacks"></a><span data-ttu-id="6350c-103">Prise en charge de plusieurs rappels</span><span class="sxs-lookup"><span data-stu-id="6350c-103">Supporting Multiple Callbacks</span></span>

<span data-ttu-id="6350c-104">Si vous appelez plusieurs méthodes asynchrones, chacune d’elles requiert une implémentation distincte de [**IMFAsyncCallback :: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span><span class="sxs-lookup"><span data-stu-id="6350c-104">If you call more than one asynchronous method, each one requires a separate implementation of [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span></span> <span data-ttu-id="6350c-105">Toutefois, vous souhaiterez peut-être implémenter les rappels à l’intérieur d’une classe C++ unique.</span><span class="sxs-lookup"><span data-stu-id="6350c-105">However, you might want to implement the callbacks inside a single C++ class.</span></span> <span data-ttu-id="6350c-106">La classe ne pouvant avoir qu’une seule méthode **Invoke** , une solution consiste à fournir une classe d’assistance qui délègue les appels **Invoke** à une autre méthode sur une classe de conteneur.</span><span class="sxs-lookup"><span data-stu-id="6350c-106">The class can have only one **Invoke** method, so one solution is to provide a helper class that delegates **Invoke** calls to another method on a container class.</span></span>

<span data-ttu-id="6350c-107">Le code suivant illustre un modèle de classe nommé `AsyncCallback` , qui illustre cette approche.</span><span class="sxs-lookup"><span data-stu-id="6350c-107">The following code shows a class template named `AsyncCallback`, which demonstrates this approach.</span></span>


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



<span data-ttu-id="6350c-108">Le paramètre de modèle est le nom de la classe de conteneur.</span><span class="sxs-lookup"><span data-stu-id="6350c-108">The template parameter is the name of container class.</span></span> <span data-ttu-id="6350c-109">Le `AsyncCallback` constructeur a deux paramètres : un pointeur vers la classe de conteneur et l’adresse d’une méthode de rappel sur la classe de conteneur.</span><span class="sxs-lookup"><span data-stu-id="6350c-109">The `AsyncCallback` constructor has two parameters: a pointer to the container class, and the address of a callback method on the container class.</span></span> <span data-ttu-id="6350c-110">La classe de conteneur peut avoir plusieurs instances de la `AsyncCallback` classe en tant que variables membres, une pour chaque méthode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="6350c-110">The container class can have multiple instances of the `AsyncCallback` class as member variables, one for each asynchronous method.</span></span> <span data-ttu-id="6350c-111">Quand la classe de conteneur appelle une méthode asynchrone, elle utilise l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) de l' `AsyncCallback` objet approprié.</span><span class="sxs-lookup"><span data-stu-id="6350c-111">When the container class calls an asynchronous method, it use the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface of the appropriate `AsyncCallback` object.</span></span> <span data-ttu-id="6350c-112">Lorsque la `AsyncCallback` méthode [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) de l’objet est appelée, l’appel est délégué à la méthode correcte sur la classe de conteneur.</span><span class="sxs-lookup"><span data-stu-id="6350c-112">When the `AsyncCallback` object's [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method is called, the call is delegated to the correct method on the container class.</span></span>

<span data-ttu-id="6350c-113">L' `AsyncCallback` objet délègue également des appels de **AddRef** et de **Release** à la classe de conteneur, de sorte que la classe de conteneur gère la durée de vie de l' `AsyncCallback` objet.</span><span class="sxs-lookup"><span data-stu-id="6350c-113">The `AsyncCallback` object also delegates **AddRef** and **Release** calls to the container class, so the container class manages the lifetime of the `AsyncCallback` object.</span></span> <span data-ttu-id="6350c-114">Cela garantit que l' `AsyncCallback` objet n’est pas supprimé tant que l’objet conteneur lui-même n’est pas supprimé.</span><span class="sxs-lookup"><span data-stu-id="6350c-114">This guarantees that the `AsyncCallback` object will not be deleted until the container object itself is deleted.</span></span>

<span data-ttu-id="6350c-115">Le code suivant illustre l’utilisation de ce modèle :</span><span class="sxs-lookup"><span data-stu-id="6350c-115">The following code shows how to use this template:</span></span>


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



<span data-ttu-id="6350c-116">Dans cet exemple, la classe de conteneur est nommée `CMyObject` .</span><span class="sxs-lookup"><span data-stu-id="6350c-116">In this example, the container class is named `CMyObject`.</span></span> <span data-ttu-id="6350c-117">La variable de membre *m \_ CB* est un `AsyncCallback` objet.</span><span class="sxs-lookup"><span data-stu-id="6350c-117">The *m\_CB* member variable is a `AsyncCallback` object.</span></span> <span data-ttu-id="6350c-118">Dans le `CMyObject` constructeur, la variable de membre *m \_ CB* est initialisée avec l’adresse de la `CMyObject::OnInvoke` méthode.</span><span class="sxs-lookup"><span data-stu-id="6350c-118">In the `CMyObject` constructor, the *m\_CB* member variable is initialized with the address of the `CMyObject::OnInvoke` method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6350c-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6350c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6350c-120">Méthodes de rappel asynchrones</span><span class="sxs-lookup"><span data-stu-id="6350c-120">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)
</dt> </dl>

 

 



