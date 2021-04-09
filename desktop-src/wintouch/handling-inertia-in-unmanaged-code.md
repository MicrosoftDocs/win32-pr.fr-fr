---
title: Gestion de l’inertie dans du code non managé
description: Cette section explique comment utiliser l’interface IInertiaProcessor pour gérer l’inertie dans du code non managé.
ms.assetid: 3261b461-add2-4e92-9a51-b2d46630fb4f
keywords:
- Tactile Windows, inertie
- Tactile Windows, processeur de manipulation
- inertie, code non managé
- inertie, interface IInertiaProcessor
- inertie, processeur de manipulation
- processeur de manipulation, inertie
- Interface IInertiaProcessor, code non managé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3de56d06547f426de252a89ef5172df3fe4ca439
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028693"
---
# <a name="handling-inertia-in-unmanaged-code"></a>Gestion de l’inertie dans du code non managé

Cette section explique comment utiliser l’interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) pour gérer l’inertie dans du code non managé.

## <a name="overview"></a>Vue d’ensemble

Pour utiliser l’inertie dans du code non managé, vous devez implémenter des récepteurs d’événements à la fois pour le processeur de manipulation et le processeur d’inertie. Commencez par ajouter la prise en charge de manipulation à votre application, comme décrit dans la section Ajout de la [prise en charge de manipulation au code non managé](adding-manipulation-support-in-unmanaged-code.md). Notez que la prise en charge de la manipulation nécessite que vous utilisiez des messages tactiles plutôt que des messages de geste pour alimenter les données d’événement vers le processeur de manipulation. Une fois que vous avez manipulé le travail, vous devez également implémenter un deuxième récepteur d’événements pour les événements que l’interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) générera ou devra modifier votre récepteur d’événements existant pour prendre en charge les événements générés par les interfaces **IInertiaProcessor** et [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) . Dans le cadre de cet exemple, il est plus facile de démarrer à partir du récepteur d’événements créé pour la section qui ajoute la prise en charge de manipulation au code non managé et d’ajouter un second constructeur qui fonctionne avec le processeur d’inertie plutôt que le processeur de manipulation. De cette façon, l’implémentation du récepteur d’événements peut fonctionner pour le processeur de manipulation ou le processeur d’inertie. Outre l’ajout d’un second constructeur, le récepteur d’événements aura une variable qui indique s’il effectuera les opérations en fonction de l’entrée d’inertie plutôt que de manipuler l’entrée.

### <a name="add-inertia-support-to-a-manipulation-processor-event-sink"></a>Ajouter la prise en charge de l’inertie à un récepteur d’événements de processeur de manipulation

Le code suivant montre le nouveau constructeur de récepteur d’événements, les nouvelles variables membres pour une interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) et un indicateur qui spécifie si le récepteur est en extrapolation pour l’inertie.


```C++
    CManipulationEventSink(IManipulationProcessor *pManip, IInertiaProcessor *pInert, HWND hWnd);
    CManipulationEventSink(IInertiaProcessor *pInert, HWND hWnd);
```




```C++
    IInertiaProcessor*      m_pInert;
    BOOL fExtrapolating; 
```



Une fois que votre en-tête de classe a les nouveaux constructeurs et un indicateur spécifiant si vous utilisez l’extrapolation, vous pouvez implémenter votre récepteur d’événements pour avoir des blocs de gestion distincts pour les événements [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) et [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) . Le constructeur qui accepte un **IManipulationProcessor** et un **IInertiaProcessor** doit définir l’indicateur **fExtrapolating** sur false, ce qui indique qu’il s’agit d’un gestionnaire d’événements **IManipulationProcessor** . Le code suivant montre comment le constructeur pour un récepteur d’événements qui utilise le **IManipulationProcessor** peut être implémenté.


```C++
CManipulationEventSink::CManipulationEventSink(IManipulationProcessor *pManip, IInertiaProcessor *pInert, HWND hWnd)
{
    m_hWnd = hWnd;

    //Set initial ref count to 1.
    m_cRefCount = 1;

    fExtrapolating=FALSE;

    m_pManip = pManip;
    
    m_pInert = pInert;
    
    m_pManip->put_PivotRadius(-1);

    m_cStartedEventCount = 0;
    m_cDeltaEventCount = 0;
    m_cCompletedEventCount = 0;

    HRESULT hr = S_OK;

    //Get the container with the connection points.
    IConnectionPointContainer* spConnectionContainer;
    
    hr = pManip->QueryInterface(
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
```



Le code suivant montre comment le constructeur pour un récepteur d’événements qui utilise le [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) peut être implémenté. Ce constructeur affecte la valeur true à l’indicateur **fExtrapolating** , ce qui indique que cette instance de la classe de récepteur d’événements effectuera l’extrapolation et effectuera toutes les opérations de déplacement effectuées précédemment par les événements du processeur de manipulation.


```C++
CManipulationEventSink::CManipulationEventSink(IInertiaProcessor *pInert, HWND hWnd)
{
    m_hWnd = hWnd;

    m_pInert = pInert;
    //Set initial ref count to 1.
    m_cRefCount = 1;

    fExtrapolating=TRUE;

    m_cStartedEventCount = 0;
    m_cDeltaEventCount = 0;
    m_cCompletedEventCount = 0;

    HRESULT hr = S_OK;

    //Get the container with the connection points.
    IConnectionPointContainer* spConnectionContainer;
    
    hr = pInert->QueryInterface(
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
```



> [!Note]  
> L’implémentation de la classe du récepteur d’événements à partir du récepteur d’événements du processeur de manipulation est réutilisée comme récepteur d’événements pour le processeur d’inertie.

 

Maintenant, lorsque vous construisez cette classe, **CManipulationEventSink**, elle peut être construite en tant que récepteur d’événements pour un processeur de manipulation ou en tant que récepteur d’événements pour un processeur d’inertie. Lorsqu’il est construit en tant que récepteur d’événements du processeur d’inertie, l’indicateur **fExtrapolating** est défini sur true, ce qui indique que les événements de manipulation doivent être extrapolés.

> [!Note]  
> [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted) sera déclenchée par les interfaces [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) et [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .

 

Lorsque la manipulation démarre, les propriétés de l’interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) sont définies. Le code suivant montre comment l’événement Started est géré.


```C++
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationStarted( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y)
{
    m_cStartedEventCount ++;       

    // set origins in manipulation processor
    m_pInert->put_InitialOriginX(x);
    m_pInert->put_InitialOriginY(y);
    
    RECT screenRect;

    HWND desktop = GetDesktopWindow();
    GetClientRect(desktop, &screenRect);

    // physics settings
    // deceleration is units per square millisecond
    m_pInert->put_DesiredDeceleration(.1f);

    // set the boundaries        
    screenRect.left-= 1024;
    m_pInert->put_BoundaryLeft  ( static_cast<float>(screenRect.left   * 100));
    m_pInert->put_BoundaryTop   ( static_cast<float>(screenRect.top    * 100));
    m_pInert->put_BoundaryRight ( static_cast<float>(screenRect.right  * 100));
    m_pInert->put_BoundaryBottom( static_cast<float>(screenRect.bottom * 100));
    
    
    // Elastic boundaries - I set these to 90% of the screen 
    // so... 5% at left, 95% right, 5% top,  95% bottom
    // Values are whole numbers because units are in centipixels
    m_pInert->put_ElasticMarginLeft  (static_cast<float>(screenRect.left   * 5));
    m_pInert->put_ElasticMarginTop   (static_cast<float>(screenRect.top    * 5));
    m_pInert->put_ElasticMarginRight (static_cast<float>(screenRect.right  * 95));
    m_pInert->put_ElasticMarginBottom(static_cast<float>(screenRect.bottom * 95));
    
    
    return S_OK;
}
```



Dans cet exemple, les deltas de manipulation sont utilisés pour déplacer la fenêtre. Le code suivant montre comment l’événement Delta est géré.


```C++
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
    MoveWindow(m_hWnd,                                              // the window to move
        static_cast<int>(rect.left + (translationDeltaX / 100.0f)), // the x position
        static_cast<int>(rect.top + (translationDeltaY/100.0f)),    // the y position
        static_cast<int>(oldWidth * scaleDelta),                    // width
        static_cast<int>(oldHeight * scaleDelta),                   // height
        TRUE);                                                      // redraw
                     
    return S_OK;
}
```



Dans cet exemple, la manipulation des événements terminés démarre ou arrête un minuteur qui appellera le [**processus**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process) sur l’interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) . Le code suivant montre comment l’événement de manipulation terminée est géré.


```C++
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
    
    if (fExtrapolating){
        //Inertia Complete, stop the timer used for processing      
        KillTimer(m_hWnd,0);        
    }else{ 
        // setup velocities for inertia processor
        float vX = 0.0f;
        float vY = 0.0f;
        float vA = 0.0f;
        m_pManip->GetVelocityX(&vX);
        m_pManip->GetVelocityY(&vY);
        m_pManip->GetAngularVelocity(&vA);

        // complete any previous processing
        m_pInert->Complete();
        
        // Reset sets the  initial timestamp
        m_pInert->Reset();
                
        // 
        m_pInert->put_InitialVelocityX(vX);
        m_pInert->put_InitialVelocityY(vY);        
        
        m_pInert->put_InitialOriginX(x);
        m_pInert->put_InitialOriginY(y);
        
           
        // Start a timer
        SetTimer(m_hWnd,0, 50, 0);        
    }

    return S_OK;
}
```



Le code suivant montre comment vous pouvez interpréter les messages **\_ du minuteur WM** dans **WndProc** pour effectuer des appels au [**processus**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process) sur l’interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .


```C++
case WM_TIMER:       
  if (g_pIInertProc){
    BOOL b;       
    g_pIInertProc->Process(&b);        
  }
  break;
```



### <a name="coinitialize-the-inertia-processor-and-manipulation-processor-and-initialize-the-event-sinks"></a>Coinitialisez le processeur d’inertie et le processeur de manipulation et initialisez les récepteurs d’événements.

Après avoir modifié le récepteur d’événements pour qu’il prenne en charge à la fois [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) et [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor), vous êtes prêt à initialiser les récepteurs d’événements et à les configurer pour qu’ils s’exécutent à partir de votre application. Le code suivant montre comment les pointeurs d’interface sont alloués.


```C++
//Include windows.h for touch events
#include "windows.h"  

// Manipulation implementation file
#include <manipulations_i.c>
    
// Smart Pointer to a global reference of a manipulation processor, event sink
IManipulationProcessor* g_pIManipProc;
IInertiaProcessor*      g_pIInertProc;
```



L’exemple de code suivant montre comment instancier vos interfaces.


```C++
   HRESULT hr = CoInitialize(0);
        
   hr = CoCreateInstance(CLSID_ManipulationProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIManipProc)
   );
   
   hr = CoCreateInstance(CLSID_InertiaProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIInertProc)
   );
```



L’exemple de code suivant montre comment construire vos récepteurs d’événements en fonction des pointeurs d’interface et enregistrer la fenêtre pour l’entrée tactile.


```C++
   g_pManipulationEventSink = new CManipulationEventSink(g_pIManipProc, g_pIInertProc, hWnd);
   g_pManipulationEventSink = new CManipulationEventSink(g_pIInertProc, hWnd);


   RegisterTouchWindow(hWnd, 0);  
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inertie](getting-started-with-inertia.md)
</dt> </dl>

 

 




