---
description: Ce programme montre comment vous pouvez générer une application qui capture les événements InkCollector en utilisant uniquement C++. Ce programme Co-crée un objet InkCollector pour activer l’écriture manuscrite dans la fenêtre. Elle affiche une boîte de message chaque fois qu’un événement Stroke est reçu.
ms.assetid: 91450559-ae47-457a-a709-b4e4e78bde22
title: Exemple de récepteurs d’événements C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e950254293b676088d8b281624c089b098e5dca8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517207"
---
# <a name="c-event-sinks-sample"></a><span data-ttu-id="c71df-105">Exemple de récepteurs d’événements C++</span><span class="sxs-lookup"><span data-stu-id="c71df-105">C++ Event Sinks Sample</span></span>

<span data-ttu-id="c71df-106">Ce programme montre comment vous pouvez générer une application qui capture les événements InkCollector en utilisant uniquement C++.</span><span class="sxs-lookup"><span data-stu-id="c71df-106">This program demonstrates how you can build an application that captures InkCollector events using only C++.</span></span> <span data-ttu-id="c71df-107">Ce programme Co-crée un objet [**InkCollector**](inkcollector-class.md) pour activer l’écriture manuscrite dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c71df-107">This program co-creates an [**InkCollector**](inkcollector-class.md) object to ink -enable the window.</span></span> <span data-ttu-id="c71df-108">Elle affiche une boîte de message chaque fois qu’un événement [**Stroke**](inkcollector-stroke.md) est reçu.</span><span class="sxs-lookup"><span data-stu-id="c71df-108">It displays a message box whenever a [**Stroke**](inkcollector-stroke.md) event is received.</span></span>

## <a name="defining-a-wrapper-for-ink-collector-events"></a><span data-ttu-id="c71df-109">Définition d’un wrapper pour les événements du collecteur d’encre</span><span class="sxs-lookup"><span data-stu-id="c71df-109">Defining a Wrapper for Ink Collector Events</span></span>

<span data-ttu-id="c71df-110">La `InkCollectorEvents` classe gère le passage des événements du collecteur d’encre du collecteur d’encre à l’utilisateur de cette classe.</span><span class="sxs-lookup"><span data-stu-id="c71df-110">The `InkCollectorEvents` Class handles passing ink collector events from the ink collector to the user of this class.</span></span> <span data-ttu-id="c71df-111">La `AdviseInkCollector` méthode Configure la connexion entre l’objet [**InkCollector**](inkcollector-class.md) et cette classe.</span><span class="sxs-lookup"><span data-stu-id="c71df-111">The `AdviseInkCollector` method sets up the connection between the [**InkCollector**](inkcollector-class.md) object and this class.</span></span> <span data-ttu-id="c71df-112">La `Invoke` méthode convertit la notification d’événement [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) en un appel à une fonction virtuelle que l’utilisateur de cette classe peut substituer pour traiter un événement particulier.</span><span class="sxs-lookup"><span data-stu-id="c71df-112">The `Invoke` method converts the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) event notification into a call to a virtual function that the user of this class can override to process a particular event.</span></span>

> [!Note]  
> <span data-ttu-id="c71df-113">Vous devez faire plus que remplacer la fonction virtuelle d’un gestionnaire d’événements pour obtenir cet événement.</span><span class="sxs-lookup"><span data-stu-id="c71df-113">You must do more than override the virtual function for an event handler to get that event.</span></span> <span data-ttu-id="c71df-114">Pour tous les événements sauf les événements par défaut, vous devez appeler la méthode [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest) du collecteur d’encre pour garantir l’obtention d’un événement.</span><span class="sxs-lookup"><span data-stu-id="c71df-114">For all but default events, you have to call the ink collector's [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest) method to guarantee getting an event.</span></span> <span data-ttu-id="c71df-115">Deuxièmement, cet objet marshale lui-même le thread libre, de sorte que tous les gestionnaires d’événements implémentés doivent également être libres de thread.</span><span class="sxs-lookup"><span data-stu-id="c71df-115">Secondly, this object marshals itself free threaded so all implemented event handlers need to be free threaded as well.</span></span> <span data-ttu-id="c71df-116">Il est particulièrement important d’utiliser des API Windows, ce qui peut entraîner un basculement vers un autre thread, car le gestionnaire d’événements n’est pas garanti s’exécuter sur le même thread que la fenêtre connectée au collecteur d’encre.</span><span class="sxs-lookup"><span data-stu-id="c71df-116">Of particular importance is using Windows APIs, which may cause a switch to another thread as the event handler is not guaranteed to be running on the same thread as the window connected with the ink collector.</span></span>

 


```C++
// Invoke translates from IDispatch to an event callout
//  that can be overriden by a subclass of this class.
STDMETHOD(Invoke)(
   DISPID dispidMember, 
    REFIID riid,
    LCID lcid, 
    WORD /*wFlags*/, 
    DISPPARAMS* pdispparams, 
    VARIANT* pvarResult,
    EXCEPINFO* /*pexcepinfo*/, 
    UINT* /*puArgErr*/)
{
    switch(dispidMember)
    {
        case DISPID_ICEStroke:
            Stroke(
                (IInkCursor*) pdispparams->rgvarg[2].pdispVal,
                (IInkStrokeDisp*) pdispparams->rgvarg[1].pdispVal,
                (VARIANT_BOOL *)pdispparams->rgvarg[0].pboolVal);
            break;
        ...
    }
    return S_OK;
}

virtual void Stroke(
    IInkCursor* Cursor,
    IInkStrokeDisp* Stroke,
    VARIANT_BOOL *Cancel)
{
    // This is a place holder designed to be overridden by
    //  user of this class.
    return;
}
...
```



<span data-ttu-id="c71df-117">La `Init` méthode appelle [CoCreateFreeThreadedMarshaler](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) pour configurer un marshaleur de thread libre.</span><span class="sxs-lookup"><span data-stu-id="c71df-117">The `Init` method calls [CoCreateFreeThreadedMarshaler](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) to set up a free threaded marshaler.</span></span>


```C++
// Init: set up free threaded marshaller.
HRESULT Init()
{
    return CoCreateFreeThreadedMarshaler(this, &m_punkFTM);
}
```



<span data-ttu-id="c71df-118">La `AdviseInkCollector` méthode Configure la connexion entre l’objet [**InkCollector**](inkcollector-class.md) et cette classe.</span><span class="sxs-lookup"><span data-stu-id="c71df-118">The `AdviseInkCollector` method sets up the connection between the [**InkCollector**](inkcollector-class.md) object and this class.</span></span> <span data-ttu-id="c71df-119">Il récupère tout d’abord un point de connexion au collecteur d’encres.</span><span class="sxs-lookup"><span data-stu-id="c71df-119">It first retrieves a connection point to the ink collector.</span></span> <span data-ttu-id="c71df-120">Il récupère ensuite un pointeur vers le `IInkCollectorEvents` afin qu’il puisse établir une connexion consultative au contrôle.</span><span class="sxs-lookup"><span data-stu-id="c71df-120">Then it retrieves a pointer to the `IInkCollectorEvents` so that it may establish an advisory connection to the control.</span></span>


```C++
// Set up connection between sink and InkCollector
HRESULT AdviseInkCollector(
    IInkCollector *pIInkCollector)
{
    // Get the connection point container
    IConnectionPointContainer *pIConnectionPointContainer;
    HRESULT hr = pIInkCollector->QueryInterface(IID_IConnectionPointContainer, (void **) &pIConnectionPointContainer);
        
    if (FAILED(hr))
        ...
    
    // Find the connection point for Ink Collector events
    hr = pIConnectionPointContainer->FindConnectionPoint(__uuidof(_IInkCollectorEvents), &m_pIConnectionPoint);
        
    if (SUCCEEDED(hr))
    {
        // Hook up sink to connection point
        hr = m_pIConnectionPoint->Advise(this, &m_dwCookie);
    }
    
    if (FAILED(hr))
        ...
    
    // Don't need the connection point container any more.
    pIConnectionPointContainer->Release();
    return hr;
}
```



<span data-ttu-id="c71df-121">La `UnadviseInkCollector` méthode libère les connexions de l’objet au contrôle.</span><span class="sxs-lookup"><span data-stu-id="c71df-121">The `UnadviseInkCollector` method releases the connections the object has to the control.</span></span>


```C++
// Remove the connection of the sink to the Ink Collector
HRESULT UnadviseInkCollector()
{
    HRESULT hr = m_pIConnectionPoint->Unadvise(m_dwCookie);m_pIConnectionPoint->Release();
m_pIConnectionPoint = NULL;
    return hr;
}
```



## <a name="defining-an-ink-collector-events-handler"></a><span data-ttu-id="c71df-122">Définition d’un gestionnaire d’événements du collecteur d’encre</span><span class="sxs-lookup"><span data-stu-id="c71df-122">Defining an Ink Collector Events Handler</span></span>

<span data-ttu-id="c71df-123">La classe CMyInkEvents remplace le comportement par défaut du gestionnaire d’événements [**Stroke**](inkcollector-stroke.md) de la classe InkCollectorEvents.</span><span class="sxs-lookup"><span data-stu-id="c71df-123">The CMyInkEvents Class overrides the default behavior of the [**Stroke**](inkcollector-stroke.md) event handler of the InkCollectorEvents Class.</span></span> <span data-ttu-id="c71df-124">La méthode Stroke affiche une boîte de message lorsque le [**InkCollector**](inkcollector-class.md) reçoit un événement **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="c71df-124">The Stroke method displays a message box when the [**InkCollector**](inkcollector-class.md) receives a **Stroke** event.</span></span>


```C++
class CMyInkEvents : public InkCollectorEvents
{
public:

    // Event: Stroke
    virtual void Stroke(
        IInkCursor* Cursor,
        IInkStrokeDisp* Stroke,
        VARIANT_BOOL *Cancel)
    {
        // Demonstrate that the event notification was received.
        MessageBox(m_hWnd, "Stroke Event", "Event Received", MB_OK);
    }
    
    CMyInkEvents()
    {
        m_hWnd = NULL;
    }
    
    HRESULT Init(
        HWND hWnd)
    {
        m_hWnd = hWnd;
        return InkCollectorEvents::Init();
    }    
    
    HWND m_hWnd;
};
```



## <a name="defining-an-ink-collector-wrapper"></a><span data-ttu-id="c71df-125">Définition d’un wrapper du collecteur d’encre</span><span class="sxs-lookup"><span data-stu-id="c71df-125">Defining an Ink Collector Wrapper</span></span>

<span data-ttu-id="c71df-126">La méthode Init de la classe CMyInkCollector déclare et initialise un objet CMyInkEvents.</span><span class="sxs-lookup"><span data-stu-id="c71df-126">The CMyInkCollector Class's Init method declares and initializes a CMyInkEvents object.</span></span> <span data-ttu-id="c71df-127">Il crée ensuite un objet [**InkCollector**](inkcollector-class.md) et associe le collecteur d’encre et le gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="c71df-127">It then creates an [**InkCollector**](inkcollector-class.md) object and associates the ink collector and the event handler.</span></span> <span data-ttu-id="c71df-128">Enfin, le **InkCollector** est attaché à la fenêtre et activé.</span><span class="sxs-lookup"><span data-stu-id="c71df-128">Finally, the **InkCollector** is attached to the window and enabled.</span></span>


```C++
// Handle all initializaton
HRESULT Init(
HWND hWnd)
{
    // Initialize event sink. This consists of setting
    //  up the free threaded marshaler.
    HRESULT hr = m_InkEvents.Init(hWnd);

    if (FAILED(hr))
        ...

    // Create the ink collector
    hr = CoCreateInstance(CLSID_InkCollector, NULL, CLSCTX_ALL, IID_IInkCollector, (void **) &m_pInkCollector);

    if (FAILED(hr))
        ...

    // Set up connection between Ink Collector and our event sink
    hr = m_InkEvents.AdviseInkCollector(m_pInkCollector);

    if (FAILED(hr))
        ...

    // Attach Ink Collector to window
    hr = m_pInkCollector->put_hWnd((long) hWnd);

    if (FAILED(hr))
        ...

    // Allow Ink Collector to receive input.
    return m_pInkCollector->put_Enabled(VARIANT_TRUE);
}
```



## <a name="accessing-the-tablet-pc-interfaces-and-the-wrapper-classes"></a><span data-ttu-id="c71df-129">Accès aux interfaces Tablet PC et aux classes wrapper</span><span class="sxs-lookup"><span data-stu-id="c71df-129">Accessing the Tablet PC Interfaces and the Wrapper Classes</span></span>

<span data-ttu-id="c71df-130">Tout d’abord, incluez les en-têtes pour les interfaces d’automatisation Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="c71df-130">First, include the headers for Tablet PC Automation interfaces.</span></span> <span data-ttu-id="c71df-131">Celles-ci sont installées avec le <entity type="reg"/> Kit de développement Microsoft Windows <entity type="reg"/> XP Tablet PC Edition 1,7.</span><span class="sxs-lookup"><span data-stu-id="c71df-131">These are installed with the Microsoft<entity type="reg"/> Windows<entity type="reg"/> XP Tablet PC Edition Development Kit 1.7.</span></span>


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



<span data-ttu-id="c71df-132">Ensuite, incluez les en-têtes des classes wrapper et le gestionnaire d’événements [**InkCollector**](inkcollector-class.md) a été défini.</span><span class="sxs-lookup"><span data-stu-id="c71df-132">Then, include the headers for the wrapper classes and [**InkCollector**](inkcollector-class.md) event handler was defined.</span></span>


```C++
#include "TpcConpt.h"
#include "EventSink.h"
```



## <a name="calling-the-wrapper-classes"></a><span data-ttu-id="c71df-133">Appel des classes wrapper</span><span class="sxs-lookup"><span data-stu-id="c71df-133">Calling the Wrapper Classes</span></span>

<span data-ttu-id="c71df-134">Lorsque la fenêtre est créée, la procédure de fenêtre crée un wrapper du collecteur d’encre et initialise le wrapper.</span><span class="sxs-lookup"><span data-stu-id="c71df-134">When the window is created, the Window procedure creates an ink collector wrapper and initializes the wrapper.</span></span> <span data-ttu-id="c71df-135">Lorsque la fenêtre est détruite, la procédure de fenêtre supprime le wrapper du collecteur d’encre.</span><span class="sxs-lookup"><span data-stu-id="c71df-135">When the window is destroyed, the Window procedure deletes the ink collector wrapper.</span></span> <span data-ttu-id="c71df-136">Le wrapper du collecteur d’encres gère la création et la suppression de son gestionnaire d’événements associé.</span><span class="sxs-lookup"><span data-stu-id="c71df-136">The ink collector wrapper handles the creation and deletion of its associated event handler.</span></span>


```C++
case WM_CREATE:

    // Allocate and initialize memory for object
    pmic = new CMyInkCollector();

    if (pmic != NULL)
    {
        // Real initialization. This consists of creating
        //  an ink collector object and attaching it to
        //  the current window. 
        if (SUCCEEDED(pmic->Init(hWnd)))
        {
            return 0;
        }
        
        // Failure free resources.
        delete pmic;
        pmic = NULL;
    }
    
    return -1;
...
case WM_DESTROY:
    // The destructor for the object handles releasing the
    //  InkCollector and disconnecting the InkCollector
    //  from the object's event sink. 
    delete pmic;
    pmic = NULL;
    PostQuitMessage(0);
    break;
```



 

 
