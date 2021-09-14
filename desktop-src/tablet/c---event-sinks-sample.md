---
description: Ce programme montre comment vous pouvez générer une application qui capture les événements InkCollector en utilisant uniquement C++. Ce programme Co-crée un objet InkCollector pour activer l’écriture manuscrite dans la fenêtre. Elle affiche une boîte de message chaque fois qu’un événement Stroke est reçu.
ms.assetid: 91450559-ae47-457a-a709-b4e4e78bde22
title: Exemple de récepteurs d’événements C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e950254293b676088d8b281624c089b098e5dca8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294055"
---
# <a name="c-event-sinks-sample"></a>Exemple de récepteurs d’événements C++

Ce programme montre comment vous pouvez générer une application qui capture les événements InkCollector en utilisant uniquement C++. Ce programme Co-crée un objet [**InkCollector**](inkcollector-class.md) pour activer l’écriture manuscrite dans la fenêtre. Elle affiche une boîte de message chaque fois qu’un événement [**Stroke**](inkcollector-stroke.md) est reçu.

## <a name="defining-a-wrapper-for-ink-collector-events"></a>Définition d’un wrapper pour les événements du collecteur d’encre

La `InkCollectorEvents` classe gère le passage des événements du collecteur d’encre du collecteur d’encre à l’utilisateur de cette classe. La `AdviseInkCollector` méthode Configure la connexion entre l’objet [**InkCollector**](inkcollector-class.md) et cette classe. La `Invoke` méthode convertit la notification d’événement [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) en un appel à une fonction virtuelle que l’utilisateur de cette classe peut substituer pour traiter un événement particulier.

> [!Note]  
> Vous devez faire plus que remplacer la fonction virtuelle d’un gestionnaire d’événements pour obtenir cet événement. Pour tous les événements sauf les événements par défaut, vous devez appeler la méthode [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest) du collecteur d’encre pour garantir l’obtention d’un événement. Deuxièmement, cet objet marshale lui-même le thread libre, de sorte que tous les gestionnaires d’événements implémentés doivent également être libres de thread. il est particulièrement important d’utiliser des api Windows, ce qui peut entraîner un basculement vers un autre thread, car le gestionnaire d’événements n’est pas garanti s’exécuter sur le même thread que la fenêtre connectée au collecteur d’encre.

 


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



La `Init` méthode appelle [CoCreateFreeThreadedMarshaler](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) pour configurer un marshaleur de thread libre.


```C++
// Init: set up free threaded marshaller.
HRESULT Init()
{
    return CoCreateFreeThreadedMarshaler(this, &m_punkFTM);
}
```



La `AdviseInkCollector` méthode Configure la connexion entre l’objet [**InkCollector**](inkcollector-class.md) et cette classe. Il récupère tout d’abord un point de connexion au collecteur d’encres. Il récupère ensuite un pointeur vers le `IInkCollectorEvents` afin qu’il puisse établir une connexion consultative au contrôle.


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



La `UnadviseInkCollector` méthode libère les connexions de l’objet au contrôle.


```C++
// Remove the connection of the sink to the Ink Collector
HRESULT UnadviseInkCollector()
{
    HRESULT hr = m_pIConnectionPoint->Unadvise(m_dwCookie);m_pIConnectionPoint->Release();
m_pIConnectionPoint = NULL;
    return hr;
}
```



## <a name="defining-an-ink-collector-events-handler"></a>Définition d’un gestionnaire d’événements du collecteur d’encre

La classe CMyInkEvents remplace le comportement par défaut du gestionnaire d’événements [**Stroke**](inkcollector-stroke.md) de la classe InkCollectorEvents. La méthode Stroke affiche une boîte de message lorsque le [**InkCollector**](inkcollector-class.md) reçoit un événement **Stroke** .


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



## <a name="defining-an-ink-collector-wrapper"></a>Définition d’un wrapper du collecteur d’encre

La méthode Init de la classe CMyInkCollector déclare et initialise un objet CMyInkEvents. Il crée ensuite un objet [**InkCollector**](inkcollector-class.md) et associe le collecteur d’encre et le gestionnaire d’événements. Enfin, le **InkCollector** est attaché à la fenêtre et activé.


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



## <a name="accessing-the-tablet-pc-interfaces-and-the-wrapper-classes"></a>Accès aux interfaces Tablet PC et aux classes wrapper

Tout d’abord, incluez les en-têtes pour les interfaces d’automatisation Tablet PC. celles-ci sont installées avec le <entity type="reg"/> Kit de développement Microsoft Windows <entity type="reg"/> XP Tablet PC Edition 1,7.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



Ensuite, incluez les en-têtes des classes wrapper et le gestionnaire d’événements [**InkCollector**](inkcollector-class.md) a été défini.


```C++
#include "TpcConpt.h"
#include "EventSink.h"
```



## <a name="calling-the-wrapper-classes"></a>Appel des classes wrapper

Lorsque la fenêtre est créée, la procédure de fenêtre crée un wrapper du collecteur d’encre et initialise le wrapper. Lorsque la fenêtre est détruite, la procédure de fenêtre supprime le wrapper du collecteur d’encre. Le wrapper du collecteur d’encres gère la création et la suppression de son gestionnaire d’événements associé.


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



 

 
