---
title: Ajout de la prise en charge de manipulation dans du code non managé
description: Cette section explique comment ajouter la prise en charge de manipulation au code non managé en implémentant un récepteur d’événements pour l' \_ interface IManipulationEvents.
ms.assetid: 7d8c6230-eaca-43c7-ad2f-651851b69d7f
keywords:
- Tactile Windows, manipulations
- Interface tactile Windows, _IManipulationEvents interface
- Tactile Windows, interface IManipulationProcessor
- manipulations, ajout de la prise en charge dans du code non managé
- manipulations, prise en charge du code non managé
- manipulations, prise en charge dans du code non managé
- manipulations, interface _IManipulationEvents
- manipulations, interface IManipulationProcessor
- Interface _IManipulationEvents, prise en charge de la manipulation dans du code non managé
- Interface IManipulationProcessor, prise en charge de la manipulation dans du code non managé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a2e000b6d3518c4e90eb5ae03b581e81037edf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102069"
---
# <a name="adding-manipulation-support-in-unmanaged-code"></a><span data-ttu-id="031d7-113">Ajout de la prise en charge de manipulation dans du code non managé</span><span class="sxs-lookup"><span data-stu-id="031d7-113">Adding Manipulation Support in Unmanaged Code</span></span>

<span data-ttu-id="031d7-114">Cette section explique comment ajouter la prise en charge de manipulation au code non managé en implémentant un récepteur d’événements pour l’interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .</span><span class="sxs-lookup"><span data-stu-id="031d7-114">This section explains how to add manipulation support to unmanaged code by implementing an event sink for the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface.</span></span>

<span data-ttu-id="031d7-115">L’image suivante présente l’architecture de manipulation.</span><span class="sxs-lookup"><span data-stu-id="031d7-115">The following image outlines the manipulation architecture.</span></span>

![illustration qui montre les messages tactiles Windows passés au processeur de manipulation d’un objet, qui gère les événements avec l' \- interface imanipulationevents](images/manipulation-arch.png)

<span data-ttu-id="031d7-117">Les données tactiles reçues des messages [**WM \_ Touch**](wm-touchdown.md) sont transmises au [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) avec l’ID de contact du message tactile.</span><span class="sxs-lookup"><span data-stu-id="031d7-117">Touch data that is received from [**WM\_TOUCH**](wm-touchdown.md) messages is passed to the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) together with the contact ID from the touch message.</span></span> <span data-ttu-id="031d7-118">En fonction de la séquence de messages, l’interface **IManipulationProcessor** calcule le type de transformation en cours d’exécution et les valeurs associées à cette transformation.</span><span class="sxs-lookup"><span data-stu-id="031d7-118">Based on the message sequence, the **IManipulationProcessor** interface will calculate what kind of transformation is being performed and what the values associated with this transformation are.</span></span> <span data-ttu-id="031d7-119">Le **IManipulationProcessor** génère ensuite des [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) qui sont gérés par un récepteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="031d7-119">The **IManipulationProcessor** will then generate [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) which are handled by an event sink.</span></span> <span data-ttu-id="031d7-120">Le récepteur d’événements peut ensuite utiliser ces valeurs pour effectuer des opérations personnalisées sur l’objet en cours de transformation.</span><span class="sxs-lookup"><span data-stu-id="031d7-120">The event sink can then use these values to perform custom operations on the object being transformed.</span></span>

<span data-ttu-id="031d7-121">Pour ajouter la prise en charge de manipulation à votre application, vous devez suivre les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="031d7-121">To add manipulation support to your application, you must follow these steps:</span></span>

1.  <span data-ttu-id="031d7-122">Implémentez un récepteur d’événements pour l’interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .</span><span class="sxs-lookup"><span data-stu-id="031d7-122">Implement an event sink for the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface.</span></span>
2.  <span data-ttu-id="031d7-123">Créer une instance d’une interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .</span><span class="sxs-lookup"><span data-stu-id="031d7-123">Create an instance of an [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span>
3.  <span data-ttu-id="031d7-124">Créez une instance de votre récepteur d’événements et configurez des événements tactiles.</span><span class="sxs-lookup"><span data-stu-id="031d7-124">Create an instance of your event sink and set up touch events.</span></span>
4.  <span data-ttu-id="031d7-125">Envoyer des données d’événement tactile au processeur de manipulation.</span><span class="sxs-lookup"><span data-stu-id="031d7-125">Send touch event data to the manipulation processor.</span></span>

<span data-ttu-id="031d7-126">Cette section explique les étapes que vous devez suivre pour ajouter la prise en charge de manipulation à votre application.</span><span class="sxs-lookup"><span data-stu-id="031d7-126">This section explains the steps that you must follow to add manipulation support to your application.</span></span> <span data-ttu-id="031d7-127">Le code est fourni à chaque étape pour vous aider à démarrer.</span><span class="sxs-lookup"><span data-stu-id="031d7-127">Code is provided at each step to get you started.</span></span>

> [!Note]  
> <span data-ttu-id="031d7-128">Vous ne pouvez pas utiliser les manipulations et les gestes en même temps, car les messages de mouvement et de toucher s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="031d7-128">You cannot use manipulations and gestures at the same time because gesture and touch messages are mutually exclusive.</span></span>

### <a name="implement-an-event-sink-for-_imanipualtionevents-interface"></a><span data-ttu-id="031d7-129">Implémenter un récepteur d’événements pour l' \_ interface IManipualtionEvents</span><span class="sxs-lookup"><span data-stu-id="031d7-129">Implement an Event Sink for \_IManipualtionEvents Interface</span></span>

<span data-ttu-id="031d7-130">Avant de pouvoir créer une instance de votre récepteur d’événements, vous devez créer une classe qui implémente l’interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="031d7-130">Before you can create an instance of your event sink, you must create a class that implements the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface for eventing.</span></span> <span data-ttu-id="031d7-131">Il s’agit de votre récepteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="031d7-131">This is your event sink.</span></span> <span data-ttu-id="031d7-132">Les événements générés par l’interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) sont gérés par votre récepteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="031d7-132">Events generated by the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface are handled by your event sink.</span></span> <span data-ttu-id="031d7-133">Le code suivant montre un exemple d’en-tête pour une classe qui hérite de l’interface **\_ IManipulationEvents** .</span><span class="sxs-lookup"><span data-stu-id="031d7-133">The following code shows an example header for a class that inherits the **\_IManipulationEvents** interface.</span></span>

```C++
// Manipulation Header Files
#include <comdef.h>
#include <manipulations.h>
#include <ocidl.h>

class CManipulationEventSink : _IManipulationEvents
{
public:
    CManipulationEventSink(IManipulationProcessor *manip, HWND hWnd);

    int GetStartedEventCount();
    int GetDeltaEventCount();
    int GetCompletedEventCount();
    double CManipulationEventSink::GetX();
    double CManipulationEventSink::GetY();        

    ~CManipulationEventSink();

    //////////////////////////////
    // IManipulationEvents methods
    //////////////////////////////
    virtual HRESULT STDMETHODCALLTYPE ManipulationStarted( 
        /* [in] */ FLOAT x,
        /* [in] */ FLOAT y);
    
    virtual HRESULT STDMETHODCALLTYPE ManipulationDelta( 
        /* [in] */ FLOAT x,
        /* [in] */ FLOAT y,
        /* [in] */ FLOAT translationDeltaX,
        /* [in] */ FLOAT translationDeltaY,
        /* [in] */ FLOAT scaleDelta,
        /* [in] */ FLOAT expansionDelta,
        /* [in] */ FLOAT rotationDelta,
        /* [in] */ FLOAT cumulativeTranslationX,
        /* [in] */ FLOAT cumulativeTranslationY,
        /* [in] */ FLOAT cumulativeScale,
        /* [in] */ FLOAT cumulativeExpansion,
        /* [in] */ FLOAT cumulativeRotation);
    
    virtual HRESULT STDMETHODCALLTYPE ManipulationCompleted( 
        /* [in] */ FLOAT x,
        /* [in] */ FLOAT y,
        /* [in] */ FLOAT cumulativeTranslationX,
        /* [in] */ FLOAT cumulativeTranslationY,
        /* [in] */ FLOAT cumulativeScale,
        /* [in] */ FLOAT cumulativeExpansion,
        /* [in] */ FLOAT cumulativeRotation);

    ////////////////////////////////////////////////////////////
    // IUnknown methods
    ////////////////////////////////////////////////////////////
    STDMETHOD_(ULONG, AddRef)(void);
    STDMETHOD_(ULONG, Release)(void);
    STDMETHOD(QueryInterface)(REFIID riid, LPVOID *ppvObj);

private:
    double m_fX;
    double m_fY;

    int m_cRefCount;
    int m_cStartedEventCount;
    int m_cDeltaEventCount;
    int m_cCompletedEventCount;

    IManipulationProcessor* m_pManip;

    IConnectionPointContainer* m_pConPointContainer;
    IConnectionPoint* m_pConnPoint;
    
    HWND m_hWnd;
};     
```

<span data-ttu-id="031d7-134">À partir de l’en-tête, vous devez créer une implémentation de l’interface d’événements afin que votre classe exécute les actions que vous souhaitez que le processeur de manipulation exécute.</span><span class="sxs-lookup"><span data-stu-id="031d7-134">Given the header, you must create an implementation of the events interface so that your class performs the actions that you want the manipulation processor to perform.</span></span> <span data-ttu-id="031d7-135">Le code suivant est un modèle qui implémente la fonctionnalité minimale d’un récepteur d’événements pour l’interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .</span><span class="sxs-lookup"><span data-stu-id="031d7-135">The following code is a template that implements the minimum functionality of an event sink for the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface.</span></span>

```C++
#include "stdafx.h"
#include "cmanipulationeventsink.h"

CManipulationEventSink::CManipulationEventSink(IManipulationProcessor *manip, HWND hWnd)
{
    m_hWnd = hWnd;

    //Set initial ref count to 1.
    m_cRefCount = 1;

    m_pManip = manip;
    m_pManip->put_PivotRadius(-1);

    m_cStartedEventCount = 0;
    m_cDeltaEventCount = 0;
    m_cCompletedEventCount = 0;

    HRESULT hr = S_OK;

    //Get the container with the connection points.
    IConnectionPointContainer* spConnectionContainer;
    
    hr = manip->QueryInterface(
      IID_IConnectionPointContainer, 
          (LPVOID*) &spConnectionContainer
        );
    //hr = manip->QueryInterface(&spConnectionContainer);
    if (spConnectionContainer == NULL){
        // something went wrong, try to gracefully quit
        
    }

    //Get a connection point.
    hr = spConnectionContainer->FindConnectionPoint(__uuidof(_IManipulationEvents), &m_pConnPoint);
    if (m_pConnPoint == NULL){
        // something went wrong, try to gracefully quit
    }

    DWORD dwCookie;

    //Advise.
    hr = m_pConnPoint->Advise(this, &dwCookie);
}

int CManipulationEventSink::GetStartedEventCount()
{
    return m_cStartedEventCount;
}

int CManipulationEventSink::GetDeltaEventCount()
{
    return m_cDeltaEventCount;
}

int CManipulationEventSink::GetCompletedEventCount()
{
    return m_cCompletedEventCount;
}

double CManipulationEventSink::GetX()
{
    return m_fX;
}

double CManipulationEventSink::GetY()
{
    return m_fY;
}

CManipulationEventSink::~CManipulationEventSink()
{
    //Cleanup.
}

///////////////////////////////////
//Implement IManipulationEvents
///////////////////////////////////

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationStarted( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y)
{
    m_cStartedEventCount ++;
    
    return S_OK;
}

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y,
    /* [in] */ FLOAT translationDeltaX,
    /* [in] */ FLOAT translationDeltaY,
    /* [in] */ FLOAT scaleDelta,
    /* [in] */ FLOAT expansionDelta,
    /* [in] */ FLOAT rotationDelta,
    /* [in] */ FLOAT cumulativeTranslationX,
    /* [in] */ FLOAT cumulativeTranslationY,
    /* [in] */ FLOAT cumulativeScale,
    /* [in] */ FLOAT cumulativeExpansion,
    /* [in] */ FLOAT cumulativeRotation)
{
    m_cDeltaEventCount ++;
    
    RECT rect;
        
    GetWindowRect(m_hWnd, &rect);
    
    int oldWidth =  rect.right-rect.left;
    int oldHeight = rect.bottom-rect.top;            

    // scale and translate the window size / position    
    MoveWindow(m_hWnd,                                                     // the window to move
               static_cast<int>(rect.left + (translationDeltaX / 100.0f)), // the x position
               static_cast<int>(rect.top + (translationDeltaY/100.0f)),    // the y position
               static_cast<int>(oldWidth * scaleDelta),                    // width
               static_cast<int>(oldHeight * scaleDelta),                   // height
               TRUE);                                                      // redraw
                     
    return S_OK;
}

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationCompleted( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y,
    /* [in] */ FLOAT cumulativeTranslationX,
    /* [in] */ FLOAT cumulativeTranslationY,
    /* [in] */ FLOAT cumulativeScale,
    /* [in] */ FLOAT cumulativeExpansion,
    /* [in] */ FLOAT cumulativeRotation)
{
    m_cCompletedEventCount ++;

    m_fX = x;
    m_fY = y;

    // place your code handler here to do any operations based on the manipulation   

    return S_OK;
}


/////////////////////////////////
//Implement IUnknown
/////////////////////////////////

ULONG CManipulationEventSink::AddRef(void) 
{
    return ++m_cRefCount;
}

ULONG CManipulationEventSink::Release(void)
{ 
    m_cRefCount --;

    if(0 == m_cRefCount) {
        delete this;
        return 0;
    }

    return m_cRefCount;
}

HRESULT CManipulationEventSink::QueryInterface(REFIID riid, LPVOID *ppvObj) 
{
    if (IID__IManipulationEvents == riid) {
        *ppvObj = (_IManipulationEvents *)(this); AddRef(); return S_OK;
    } else if (IID_IUnknown == riid) {
        *ppvObj = (IUnknown *)(this); AddRef(); return S_OK;
    } else {
        return E_NOINTERFACE;
    }
}         
```

<span data-ttu-id="031d7-136">Portez une attention particulière aux implémentations des méthodes [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta)et [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) dans la classe.</span><span class="sxs-lookup"><span data-stu-id="031d7-136">Pay extra attention to implementations of [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta), and [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) methods in the class.</span></span> <span data-ttu-id="031d7-137">Il s’agit des méthodes les plus probables dans l’interface, qui nécessitent l’exécution d’opérations basées sur les informations de manipulation transmises dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="031d7-137">These are the most likely methods in the interface that will require you to perform operations based on the manipulation information that is passed around in the event.</span></span> <span data-ttu-id="031d7-138">Notez également que le deuxième paramètre dans le constructeur est l’objet utilisé dans les manipulations d’événements.</span><span class="sxs-lookup"><span data-stu-id="031d7-138">Note also that the second parameter in the constructor is the object that is used in the event manipulations.</span></span> <span data-ttu-id="031d7-139">Dans le code utilisé pour produire l’exemple, le hWnd de l’application est envoyé au constructeur afin qu’il puisse être repositionné et redimensionné.</span><span class="sxs-lookup"><span data-stu-id="031d7-139">In the code used for producing the sample, the hWnd for the application is sent to the constructor so that it can be repositioned and resized.</span></span>

### <a name="create-an-instance-of-an-imanipulationprocessor-interface"></a><span data-ttu-id="031d7-140">Créer une instance d’une interface IManipulationProcessor</span><span class="sxs-lookup"><span data-stu-id="031d7-140">Create an instance of an IManipulationProcessor Interface</span></span>

<span data-ttu-id="031d7-141">Dans le code où vous allez utiliser des manipulations, vous devez créer une instance d’une interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .</span><span class="sxs-lookup"><span data-stu-id="031d7-141">In the code where you will use manipulations, you must create an instance of an [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span> <span data-ttu-id="031d7-142">Tout d’abord, vous devez ajouter la prise en charge de la classe demanipulations.</span><span class="sxs-lookup"><span data-stu-id="031d7-142">First you must add support for the manipulations class.</span></span> <span data-ttu-id="031d7-143">Le code suivant montre comment effectuer cette opération dans votre classe.</span><span class="sxs-lookup"><span data-stu-id="031d7-143">The following code shows how you can do this in your class.</span></span>

```C++
//Include windows.h for touch events
#include "windows.h"  

// Manipulation implementation file
#include <manipulations_i.c>
    
// Smart Pointer to a global reference of a manipulation processor, event sink
IManipulationProcessor* g_pIManipProc;     
```

<span data-ttu-id="031d7-144">Une fois que vous avez la variable pour le processeur de manipulation et que vous avez inclus les en-têtes pour les manipulations, vous devez créer une instance de l’interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .</span><span class="sxs-lookup"><span data-stu-id="031d7-144">After you have your variable for the manipulation processor and you have included the headers for manipulations, you have to create an instance of the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span> <span data-ttu-id="031d7-145">Il s’agit d’un objet COM.</span><span class="sxs-lookup"><span data-stu-id="031d7-145">This is a COM object.</span></span> <span data-ttu-id="031d7-146">Par conséquent, vous devez appeler [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), puis créer une instance de votre référence à **IManipulationProcessor**.</span><span class="sxs-lookup"><span data-stu-id="031d7-146">Therefore, you must call [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), and then create an instance of your reference to the **IManipulationProcessor**.</span></span> <span data-ttu-id="031d7-147">Le code suivant montre comment vous pouvez créer une instance de cette interface.</span><span class="sxs-lookup"><span data-stu-id="031d7-147">The following code shows how you can create an instance of this interface.</span></span>

```C++
   HRESULT hr = CoInitialize(0);
        
   hr = CoCreateInstance(CLSID_ManipulationProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIManipProc)
   );
```

### <a name="create-an-instance-of-your-event-sink-and-set-up-touch-events"></a><span data-ttu-id="031d7-148">Créer une instance de votre récepteur d’événements et configurer des événements tactiles</span><span class="sxs-lookup"><span data-stu-id="031d7-148">Create an instance of your Event Sink and set up Touch Events</span></span>

<span data-ttu-id="031d7-149">Incluez la définition de votre classe de récepteur d’événements à votre code, puis ajoutez une variable pour la classe de récepteur d’événements de manipulation.</span><span class="sxs-lookup"><span data-stu-id="031d7-149">Include the definition for your event sink class to your code and then add a variable for the manipulation event sink class.</span></span> <span data-ttu-id="031d7-150">L’exemple de code suivant comprend l’en-tête de l’implémentation de la classe et configure une variable globale pour stocker le récepteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="031d7-150">The following code example includes the header for the class implementation and sets up a global variable to store the event sink.</span></span>

```C++
//Include your definition of the event sink, CManipulationEventSink.h in this case
#include "CManipulationEventSink.h"    
     
// Set up a variable to point to the manipulation event sink implementation class    
CManipulationEventSink* g_pManipulationEventSink;   
```

<span data-ttu-id="031d7-151">Une fois que vous avez la variable et que vous avez inclus votre définition pour la nouvelle classe de récepteur d’événements, vous pouvez construire la classe à l’aide du processeur de manipulation que vous avez configuré à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="031d7-151">After you have the variable and have included your definition for the new event sink class, you can construct the class by using the manipulation processor that you have set up in the previous step.</span></span> <span data-ttu-id="031d7-152">Le code suivant montre comment créer une instance de cette classe à partir de **OnInitDialog**.</span><span class="sxs-lookup"><span data-stu-id="031d7-152">The following code shows how an instance of this class would be created from **OnInitDialog**.</span></span>

```C++
   g_pManipulationEventSink = new CManipulationEventSink(g_pIManipProc, hWnd);


   RegisterTouchWindow(hWnd, 0);  
```

> [!Note]  
> <span data-ttu-id="031d7-153">La façon dont vous créez une instance de votre récepteur d’événements dépend de ce que vous effectuez avec les données de manipulation.</span><span class="sxs-lookup"><span data-stu-id="031d7-153">The way that you create an instance of your event sink depends on what you are doing with the manipulation data.</span></span> <span data-ttu-id="031d7-154">Dans la plupart des cas, vous allez créer un récepteur d’événements de processeur de manipulation qui n’a pas le même constructeur que cet exemple.</span><span class="sxs-lookup"><span data-stu-id="031d7-154">In most cases, you will create a manipulation processor event sink that does not have the same constructor as this example.</span></span>

### <a name="send-touch-event-data-to-the-manipulation-processor"></a><span data-ttu-id="031d7-155">Envoyer des données d’événement tactile au processeur de manipulation</span><span class="sxs-lookup"><span data-stu-id="031d7-155">Send Touch Event Data to the Manipulation Processor</span></span>

<span data-ttu-id="031d7-156">Maintenant que votre processeur de manipulation et votre récepteur d’événements sont configurés, vous devez alimenter les données tactiles vers le processeur de manipulation pour déclencher des événements de manipulation.</span><span class="sxs-lookup"><span data-stu-id="031d7-156">Now that you have your manipulation processor and event sink set up, you must feed touch data to the manipulation processor to trigger manipulation events.</span></span>

> [!Note]  
> <span data-ttu-id="031d7-157">Il s’agit de la même procédure que celle décrite dans [prise en main avec les messages tactiles Windows](getting-started-with-multi-touch-messages.md).</span><span class="sxs-lookup"><span data-stu-id="031d7-157">This is the same procedure as discussed in [Getting Started with Windows Touch Messages](getting-started-with-multi-touch-messages.md).</span></span>

<span data-ttu-id="031d7-158">Tout d’abord, vous allez créer du code pour décoder les messages [**WM \_ Touch**](wm-touchdown.md) et les envoyer à l’interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) pour déclencher des événements.</span><span class="sxs-lookup"><span data-stu-id="031d7-158">First, you will create some code to decode the [**WM\_TOUCH**](wm-touchdown.md) messages and send them to the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface to raise events.</span></span> <span data-ttu-id="031d7-159">Le code suivant montre un exemple d’implémentation qui est appelé à partir de la méthode **WndProc** et retourne une **LRESULT** pour la messagerie.</span><span class="sxs-lookup"><span data-stu-id="031d7-159">The following code shows an example implementation that is called from the **WndProc** method and return an **LRESULT** for messaging.</span></span>

```C++
LRESULT OnTouch(HWND hWnd, WPARAM wParam, LPARAM lParam )
{
  UINT cInputs = LOWORD(wParam);
  PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
  
  BOOL bHandled = FALSE;
  
  if (NULL != pInputs) {
    if (GetTouchInputInfo((HTOUCHINPUT)lParam,
      cInputs,
      pInputs,
      sizeof(TOUCHINPUT))) {      
      for (UINT i=0; i<cInputs; i++){
        if (pInputs[i].dwFlags & TOUCHEVENTF_DOWN){
            g_pIManipProc->ProcessDown(pInputs[i].dwID, static_cast<FLOAT>(pInputs[i].x), static_cast<FLOAT>(pInputs[i].y));
            bHandled = TRUE;
        }
        if (pInputs[i].dwFlags & TOUCHEVENTF_UP){
            g_pIManipProc->ProcessUp(pInputs[i].dwID, static_cast<FLOAT>(pInputs[i].x), static_cast<FLOAT>(pInputs[i].y));
            bHandled = TRUE;
        }
        if (pInputs[i].dwFlags & TOUCHEVENTF_MOVE){
            g_pIManipProc->ProcessMove(pInputs[i].dwID, static_cast<FLOAT>(pInputs[i].x), static_cast<FLOAT>(pInputs[i].y));
            bHandled = TRUE;
        }
      }      
    } else {
      // GetLastError() and error handling
    }
    delete [] pInputs;
  } else {
    // error handling, presumably out of memory
  }
  if (bHandled){
    // if you don't want to pass to DefWindowProc, close the touch input handle
    if (!CloseTouchInputHandle((HTOUCHINPUT)lParam)) {
        // error handling
    }
    return 0;
  }else{
    return DefWindowProc(hWnd, WM_TOUCH, wParam, lParam);
  }
}
```

<span data-ttu-id="031d7-160">Maintenant que vous disposez d’une méthode utilitaire pour décoder le message [**WM \_ Touch**](wm-touchdown.md) , vous devez transmettre les messages **WM \_ Touch** à la fonction utilitaire à partir de votre méthode **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="031d7-160">Now that you have a utility method for decoding the [**WM\_TOUCH**](wm-touchdown.md) message, you must pass the **WM\_TOUCH** messages to the utility function from your **WndProc** method.</span></span> <span data-ttu-id="031d7-161">Le code suivant montre comment procéder.</span><span class="sxs-lookup"><span data-stu-id="031d7-161">The following code shows how you can do this.</span></span>

```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {
    case WM_COMMAND:
        wmId    = LOWORD(wParam);
        wmEvent = HIWORD(wParam);
        // Parse the menu selections:
        switch (wmId)
        {
        case IDM_ABOUT:
            DialogBox(hInst, MAKEINTRESOURCE(IDD_ABOUTBOX), hWnd, About);
            break;
        case IDM_EXIT:
            DestroyWindow(hWnd);
            break;
        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
        }
        break;
    case WM_TOUCH:
        return OnTouch(hWnd, wParam, lParam);
    case WM_PAINT:
        hdc = BeginPaint(hWnd, &ps);
        // TODO: Add any drawing code here...
        EndPaint(hWnd, &ps);
        break;
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```

<span data-ttu-id="031d7-162">Les méthodes personnalisées que vous avez implémentées dans votre récepteur d’événements doivent maintenant fonctionner.</span><span class="sxs-lookup"><span data-stu-id="031d7-162">The custom methods that you have implemented in your event sink should now work.</span></span> <span data-ttu-id="031d7-163">Dans cet exemple, la touche de la fenêtre est déplacée.</span><span class="sxs-lookup"><span data-stu-id="031d7-163">In this example, touching the window will move it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="031d7-164">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="031d7-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="031d7-165">Manipulations</span><span class="sxs-lookup"><span data-stu-id="031d7-165">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>


 