---
description: Cette rubrique explique comment implémenter la journalisation des erreurs dans les services de modification DirectShow.
ms.assetid: c0b3b25c-ed03-4f78-9c53-0c0bcff1c60c
title: Création d’une classe de journalisation des erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db08971c7bf1a0024669935079b7a9403c429327
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515330"
---
# <a name="creating-an-error-logging-class"></a><span data-ttu-id="50f25-103">Création d’une classe de journalisation des erreurs</span><span class="sxs-lookup"><span data-stu-id="50f25-103">Creating an Error Logging Class</span></span>

<span data-ttu-id="50f25-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="50f25-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="50f25-105">Cette rubrique explique comment implémenter la journalisation des erreurs dans les [services de modification DirectShow](directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="50f25-105">This topic describes how to implement error logging in [DirectShow Editing Services](directshow-editing-services.md).</span></span>

<span data-ttu-id="50f25-106">Tout d’abord, déclarez une classe qui implémente la journalisation des erreurs.</span><span class="sxs-lookup"><span data-stu-id="50f25-106">First, declare a class that will implement error logging.</span></span> <span data-ttu-id="50f25-107">La classe hérite de l’interface [**IAMErrorLog**](iamerrorlog.md) .</span><span class="sxs-lookup"><span data-stu-id="50f25-107">The class inherits the [**IAMErrorLog**](iamerrorlog.md) interface.</span></span> <span data-ttu-id="50f25-108">Elle contient des déclarations pour les trois méthodes **IUnknown** et pour la méthode unique dans [IAMErrorLog](implementing-iamerrorlog.md).</span><span class="sxs-lookup"><span data-stu-id="50f25-108">It contains declarations for the three **IUnknown** methods, and for the single method in [IAMErrorLog](implementing-iamerrorlog.md).</span></span> <span data-ttu-id="50f25-109">La déclaration de classe se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="50f25-109">The class declaration is as follows:</span></span>


```C++
class CErrReporter : public IAMErrorLog
{
protected:
    long    m_lRef; // Reference count.

public:
    CErrReporter() { m_lRef = 0; }

    // IUnknown
    STDMETHOD(QueryInterface(REFIID, void**));
    STDMETHOD_(ULONG, AddRef());
    STDMETHOD_(ULONG, Release());

    // IAMErrorLog
    STDMETHOD(LogError(LONG, BSTR, LONG, HRESULT, VARIANT*));
};
```



<span data-ttu-id="50f25-110">La seule variable membre de la classe est m \_ lRef, qui contient le nombre de références de l’objet.</span><span class="sxs-lookup"><span data-stu-id="50f25-110">The only member variable in the class is m\_lRef, which holds the object's reference count.</span></span>

<span data-ttu-id="50f25-111">Ensuite, définissez les méthodes dans **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="50f25-111">Next, define the methods in **IUnknown**.</span></span> <span data-ttu-id="50f25-112">L’exemple suivant illustre une implémentation standard de ces méthodes :</span><span class="sxs-lookup"><span data-stu-id="50f25-112">The following example shows a standard implementation for these methods:</span></span>


```C++
STDMETHODIMP CErrReporter::QueryInterface(REFIID riid, void **ppv)
{
    if (ppv == NULL) return E_POINTER;

    *ppv = NULL;
    if (riid == IID_IUnknown)
        *ppv = static_cast<IUnknown*>(this);
    else if (riid == IID_IAMErrorLog)
        *ppv = static_cast<IAMErrorLog*>(this);
        
    else 
    return E_NOINTERFACE;

    AddRef();
    return S_OK;
}

STDMETHODIMP_(ULONG) CErrReporter::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

STDMETHODIMP_(ULONG) CErrReporter::Release()
{
    // Store the decremented count in a temporary
    // variable. 
    ULONG uCount = InterlockedDecrement(&m_lRef);
    if (uCount == 0)
    {
        delete this;
    }
    // Return the temporary variable, not the member
    // variable, for thread safety.
    return uCount;
}
```



<span data-ttu-id="50f25-113">Avec l’infrastructure COM en place, vous pouvez désormais implémenter l’interface **IAMErrorLog** .</span><span class="sxs-lookup"><span data-stu-id="50f25-113">With the COM framework in place, you can now implement the **IAMErrorLog** interface.</span></span> <span data-ttu-id="50f25-114">La section suivante décrit la procédure à suivre.</span><span class="sxs-lookup"><span data-stu-id="50f25-114">The next section describes how to do this.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50f25-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="50f25-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50f25-116">Journalisation des erreurs</span><span class="sxs-lookup"><span data-stu-id="50f25-116">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



