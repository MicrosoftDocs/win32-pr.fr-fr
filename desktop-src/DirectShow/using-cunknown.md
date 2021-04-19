---
description: DirectShow implémente IUnknown dans une classe de base appelée CUnknown.
ms.assetid: 1fc74db6-c23a-464f-b9fa-b19d7e8672b7
title: Utilisation de CUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1758065e8d618bf6ca74b37d98b0a8b5425919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523289"
---
# <a name="using-cunknown"></a><span data-ttu-id="db0fb-103">Utilisation de CUnknown</span><span class="sxs-lookup"><span data-stu-id="db0fb-103">Using CUnknown</span></span>

<span data-ttu-id="db0fb-104">DirectShow implémente [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) dans une classe de base appelée [**CUnknown**](cunknown.md).</span><span class="sxs-lookup"><span data-stu-id="db0fb-104">DirectShow implements [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) in a base class called [**CUnknown**](cunknown.md).</span></span> <span data-ttu-id="db0fb-105">Vous pouvez utiliser **CUnknown** pour dériver d’autres classes, en substituant uniquement les méthodes qui changent d’un composant à l’autre.</span><span class="sxs-lookup"><span data-stu-id="db0fb-105">You can use **CUnknown** to derive other classes, overriding only the methods that change across components.</span></span> <span data-ttu-id="db0fb-106">La plupart des autres classes de base de DirectShow dérivant de **CUnknown**, votre composant peut hériter directement de **CUnknown** ou d’une autre classe de base.</span><span class="sxs-lookup"><span data-stu-id="db0fb-106">Most of the other base classes in DirectShow derive from **CUnknown**, so your component can inherit directly from **CUnknown** or from another base class.</span></span>

## <a name="inondelegatingunknown"></a><span data-ttu-id="db0fb-107">INonDelegatingUnknown</span><span class="sxs-lookup"><span data-stu-id="db0fb-107">INonDelegatingUnknown</span></span>

<span data-ttu-id="db0fb-108">[**CUnknown**](cunknown.md) implémente [**INonDelegatingUnknown**](inondelegatingunknown.md).</span><span class="sxs-lookup"><span data-stu-id="db0fb-108">[**CUnknown**](cunknown.md) implements [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span> <span data-ttu-id="db0fb-109">Il gère les nombres de références en interne et, dans la plupart des cas, votre classe dérivée peut hériter des deux méthodes de décompte de références sans modification.</span><span class="sxs-lookup"><span data-stu-id="db0fb-109">It manages reference counts internally, and in most situations your derived class can inherit the two reference-counting methods with no change.</span></span> <span data-ttu-id="db0fb-110">Sachez que **CUnknown** se supprime lui-même lorsque le nombre de références est atteint de zéro.</span><span class="sxs-lookup"><span data-stu-id="db0fb-110">Be aware that **CUnknown** deletes itself when the reference count drops to zero.</span></span> <span data-ttu-id="db0fb-111">En revanche, vous devez substituer [**CUnknown :: NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md), car la méthode dans la classe de base retourne E \_ nointerface si elle reçoit un IID autre que IID \_ IUnknown.</span><span class="sxs-lookup"><span data-stu-id="db0fb-111">On the other hand, you must override [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md), because the method in the base class returns E\_NOINTERFACE if it receives any IID other than IID\_IUnknown.</span></span> <span data-ttu-id="db0fb-112">Dans votre classe dérivée, testez les IID d’interfaces que vous prenez en charge, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="db0fb-112">In your derived class, test for the IIDs of interfaces that you support, as shown in the following example:</span></span>


```C++
STDMETHODIMP NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    if (riid == IID_ISomeInterface)
    {
        return GetInterface((ISomeInterface*)this, ppv);
    }
    // Default: Call parent class method. 
    // The CUnknown class must be in the inheritance chain.
    return CParentClass::NonDelegatingQueryInterface(riid, ppv);
}
```



<span data-ttu-id="db0fb-113">La fonction utilitaire [**GetInterface**](getinterface.md) (voir [**fonctions d’assistance com**](com-helper-functions.md)) définit le pointeur, incrémente le décompte de références de manière thread-safe et retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="db0fb-113">The utility function [**GetInterface**](getinterface.md) (see [**COM Helper Functions**](com-helper-functions.md)) sets the pointer, increments the reference count in a thread-safe way, and returns S\_OK.</span></span> <span data-ttu-id="db0fb-114">Dans le cas par défaut, appelez la méthode de la classe de base et retournez le résultat.</span><span class="sxs-lookup"><span data-stu-id="db0fb-114">In the default case, call the base class method and return the result.</span></span> <span data-ttu-id="db0fb-115">Si vous dérivez à partir d’une autre classe de base, appelez sa méthode [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="db0fb-115">If you derive from another base class, call its [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method instead.</span></span> <span data-ttu-id="db0fb-116">Cela vous permet de prendre en charge toutes les interfaces prises en charge par la classe parente.</span><span class="sxs-lookup"><span data-stu-id="db0fb-116">This enables you to support all the interfaces that the parent class supports.</span></span>

## <a name="iunknown"></a><span data-ttu-id="db0fb-117">IUnknown</span><span class="sxs-lookup"><span data-stu-id="db0fb-117">IUnknown</span></span>

<span data-ttu-id="db0fb-118">Comme indiqué précédemment, la version de la délégation de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) est la même pour chaque composant, car elle ne fait rien d’autre que d’appeler l’instance correcte de la version de nondelegating.</span><span class="sxs-lookup"><span data-stu-id="db0fb-118">As mentioned earlier, the delegating version of [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) is the same for every component, because it does nothing more than invoke the correct instance of the nondelegating version.</span></span> <span data-ttu-id="db0fb-119">Pour plus de commodité, le fichier d’en-tête ComBase. h contient une macro, [**déclarez \_ IUnknown**](declare-iunknown.md), qui déclare les trois méthodes de délégation comme des méthodes Inline.</span><span class="sxs-lookup"><span data-stu-id="db0fb-119">For convenience, the header file Combase.h contains a macro, [**DECLARE\_IUNKNOWN**](declare-iunknown.md), which declares the three delegating methods as inline methods.</span></span> <span data-ttu-id="db0fb-120">Il se développe jusqu’au code suivant :</span><span class="sxs-lookup"><span data-stu-id="db0fb-120">It expands to the following code:</span></span>


```C++
STDMETHODIMP QueryInterface(REFIID riid, void **ppv) {      
    return GetOwner()->QueryInterface(riid,ppv);            
};                                                          
STDMETHODIMP_(ULONG) AddRef() {                             
    return GetOwner()->AddRef();                            
};                                                          
STDMETHODIMP_(ULONG) Release() {                            
    return GetOwner()->Release();                           
};
```



<span data-ttu-id="db0fb-121">La fonction utilitaire [**CUnknown :: GetOwner**](cunknown-getowner.md) récupère un pointeur vers l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) du composant qui possède ce composant.</span><span class="sxs-lookup"><span data-stu-id="db0fb-121">The utility function [**CUnknown::GetOwner**](cunknown-getowner.md) retrieves a pointer to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the component that owns this component.</span></span> <span data-ttu-id="db0fb-122">Pour un composant agrégé, le propriétaire est le composant externe.</span><span class="sxs-lookup"><span data-stu-id="db0fb-122">For an aggregated component, the owner is the outer component.</span></span> <span data-ttu-id="db0fb-123">Dans le cas contraire, le composant se trouve lui-même.</span><span class="sxs-lookup"><span data-stu-id="db0fb-123">Otherwise, the component owns itself.</span></span> <span data-ttu-id="db0fb-124">Incluez la \_ macro DECLARE IUnknown dans la section public de votre définition de classe.</span><span class="sxs-lookup"><span data-stu-id="db0fb-124">Include the DECLARE\_IUNKNOWN macro in the public section of your class definition.</span></span>

## <a name="class-constructor"></a><span data-ttu-id="db0fb-125">Constructeur de classe</span><span class="sxs-lookup"><span data-stu-id="db0fb-125">Class Constructor</span></span>

<span data-ttu-id="db0fb-126">Votre constructeur de classe doit appeler la méthode de constructeur pour la classe parente, en plus de tout ce qu’il fait, qui est spécifique à votre classe.</span><span class="sxs-lookup"><span data-stu-id="db0fb-126">Your class constructor should invoke the constructor method for the parent class, in addition to anything it does that is specific to your class.</span></span> <span data-ttu-id="db0fb-127">L’exemple suivant est une méthode de constructeur typique :</span><span class="sxs-lookup"><span data-stu-id="db0fb-127">The following example is a typical constructor method:</span></span>


```C++
CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
    : CUnknown(tszName, pUnk, phr)
{ 
    /* Other initializations */ 
};
```



<span data-ttu-id="db0fb-128">La méthode prend les paramètres suivants, qu’elle transmet directement à la méthode du constructeur [**CUnknown**](cunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="db0fb-128">The method takes the following parameters, which it passes directly to the [**CUnknown**](cunknown.md) constructor method.</span></span>

-   <span data-ttu-id="db0fb-129">*tszName* spécifie un nom pour le composant.</span><span class="sxs-lookup"><span data-stu-id="db0fb-129">*tszName* specifies a name for the component.</span></span>
-   <span data-ttu-id="db0fb-130">*punk* est un pointeur vers l’agrégation [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="db0fb-130">*pUnk* is a pointer to the aggregating [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span>
-   <span data-ttu-id="db0fb-131">*pHr* est un pointeur vers une valeur HRESULT indiquant la réussite ou l’échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="db0fb-131">*pHr* is a pointer to an HRESULT value, indicating the success or failure of the method.</span></span>

## <a name="summary"></a><span data-ttu-id="db0fb-132">Résumé</span><span class="sxs-lookup"><span data-stu-id="db0fb-132">Summary</span></span>

<span data-ttu-id="db0fb-133">L’exemple suivant montre une classe dérivée qui prend en charge [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) et une interface hypothétique nommée ISomeInterface :</span><span class="sxs-lookup"><span data-stu-id="db0fb-133">The following example shows a derived class that supports [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) and a hypothetical interface named ISomeInterface:</span></span>


```C++
class CMyComponent : public CUnknown, public ISomeInterface
{
public:

    DECLARE_IUNKNOWN;

    STDMETHODIMP NonDelegatingQueryInterface(REFIID riid, void **ppv)
    {
        if( riid == IID_ISomeInterface )
        {
            return GetInterface((ISomeInterface*)this, ppv);
        }
        return CUnknown::NonDelegatingQueryInterface(riid, ppv);
    }

    CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
        : CUnknown(tszName, pUnk, phr)
    { 
        /* Other initializations */ 
    };

    // More declarations will be added later.
};
```



<span data-ttu-id="db0fb-134">Cet exemple illustre les points suivants :</span><span class="sxs-lookup"><span data-stu-id="db0fb-134">This example illustrates the following points:</span></span>

-   <span data-ttu-id="db0fb-135">La classe [**CUnknown**](cunknown.md) implémente l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="db0fb-135">The [**CUnknown**](cunknown.md) class implements the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="db0fb-136">Le nouveau composant hérite de **CUnknown** et de toutes les interfaces que le composant prend en charge.</span><span class="sxs-lookup"><span data-stu-id="db0fb-136">The new component inherits from **CUnknown** and from any interfaces that the component supports.</span></span> <span data-ttu-id="db0fb-137">Le composant peut dériver à la place d’une autre classe de base qui hérite de **CUnknown**.</span><span class="sxs-lookup"><span data-stu-id="db0fb-137">The component could derive instead from another base class that inherits from **CUnknown**.</span></span>
-   <span data-ttu-id="db0fb-138">La macro [**Declare \_ IUnknown**](declare-iunknown.md) déclare les méthodes [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) de délégation comme des méthodes Inline.</span><span class="sxs-lookup"><span data-stu-id="db0fb-138">The [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro declares the delegating [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) methods as inline methods.</span></span>
-   <span data-ttu-id="db0fb-139">La classe [**CUnknown**](cunknown.md) fournit l’implémentation pour [**INonDelegatingUnknown**](inondelegatingunknown.md).</span><span class="sxs-lookup"><span data-stu-id="db0fb-139">The [**CUnknown**](cunknown.md) class provides the implementation for [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span>
-   <span data-ttu-id="db0fb-140">Pour prendre en charge une interface autre que [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), la classe dérivée doit substituer la méthode [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) et tester l’IID de la nouvelle interface.</span><span class="sxs-lookup"><span data-stu-id="db0fb-140">To support an interface other than [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), the derived class must override the [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method and test for the IID of the new interface.</span></span>
-   <span data-ttu-id="db0fb-141">Le constructeur de classe appelle la méthode de constructeur pour [**CUnknown**](cunknown.md).</span><span class="sxs-lookup"><span data-stu-id="db0fb-141">The class constructor invokes the constructor method for [**CUnknown**](cunknown.md).</span></span>

<span data-ttu-id="db0fb-142">L’étape suivante de l’écriture d’un filtre consiste à permettre à une application de créer de nouvelles instances du composant.</span><span class="sxs-lookup"><span data-stu-id="db0fb-142">The next step in writing a filter is to enable an application to create new instances of the component.</span></span> <span data-ttu-id="db0fb-143">Cela nécessite une compréhension des dll et de leur relation avec les fabriques de classes et les méthodes de constructeur de classe.</span><span class="sxs-lookup"><span data-stu-id="db0fb-143">This requires an understanding of DLLs and their relation to class factories and class constructor methods.</span></span> <span data-ttu-id="db0fb-144">Pour plus d’informations, voir [How to Create a DirectShow Filter dll](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="db0fb-144">For more information, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="db0fb-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="db0fb-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db0fb-146">Comment implémenter IUnknown</span><span class="sxs-lookup"><span data-stu-id="db0fb-146">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 
