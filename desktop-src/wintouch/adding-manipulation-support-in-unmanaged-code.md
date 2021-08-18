---
title: Ajout de la prise en charge de manipulation dans du code non managé
description: Cette section explique comment ajouter la prise en charge de manipulation au code non managé en implémentant un récepteur d’événements pour l' \_ interface IManipulationEvents.
ms.assetid: 7d8c6230-eaca-43c7-ad2f-651851b69d7f
keywords:
- Windows Toucher, manipulations
- Windows Interface tactile, _IManipulationEvents
- Windows Interface tactile, IManipulationProcessor
- manipulations, ajout de la prise en charge dans du code non managé
- manipulations, prise en charge du code non managé
- manipulations, prise en charge dans du code non managé
- manipulations, interface _IManipulationEvents
- manipulations, interface IManipulationProcessor
- Interface _IManipulationEvents, prise en charge de la manipulation dans du code non managé
- Interface IManipulationProcessor, prise en charge de la manipulation dans du code non managé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ff526c128b6da83fae3a74b88cd3bb21bc3a81c507c0a76a7c70dbddc5f76d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709999"
---
# <a name="adding-manipulation-support-in-unmanaged-code"></a>Ajout de la prise en charge de manipulation dans du code non managé

Cette section explique comment ajouter la prise en charge de manipulation au code non managé en implémentant un récepteur d’événements pour l’interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .

L’image suivante présente l’architecture de manipulation.

![illustration qui montre les messages tactiles Windows passés au processeur de manipulation d’un objet, qui gère les événements avec l' \- interface imanipulationevents](images/manipulation-arch.png)

Les données tactiles reçues des messages [**WM \_ Touch**](wm-touchdown.md) sont transmises au [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) avec l’ID de contact du message tactile. En fonction de la séquence de messages, l’interface **IManipulationProcessor** calcule le type de transformation en cours d’exécution et les valeurs associées à cette transformation. Le **IManipulationProcessor** génère ensuite des [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) qui sont gérés par un récepteur d’événements. Le récepteur d’événements peut ensuite utiliser ces valeurs pour effectuer des opérations personnalisées sur l’objet en cours de transformation.

Pour ajouter la prise en charge de manipulation à votre application, vous devez suivre les étapes suivantes :

1.  Implémentez un récepteur d’événements pour l’interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .
2.  Créer une instance d’une interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .
3.  Créez une instance de votre récepteur d’événements et configurez des événements tactiles.
4.  Envoyer des données d’événement tactile au processeur de manipulation.

Cette section explique les étapes que vous devez suivre pour ajouter la prise en charge de manipulation à votre application. Le code est fourni à chaque étape pour vous aider à démarrer.

> [!Note]  
> Vous ne pouvez pas utiliser les manipulations et les gestes en même temps, car les messages de mouvement et de toucher s’excluent mutuellement.

### <a name="implement-an-event-sink-for-_imanipualtionevents-interface"></a>Implémenter un récepteur d’événements pour l' \_ interface IManipualtionEvents

Avant de pouvoir créer une instance de votre récepteur d’événements, vous devez créer une classe qui implémente l’interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) pour l’événement. Il s’agit de votre récepteur d’événements. Les événements générés par l’interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) sont gérés par votre récepteur d’événements. Le code suivant montre un exemple d’en-tête pour une classe qui hérite de l’interface **\_ IManipulationEvents** .

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

À partir de l’en-tête, vous devez créer une implémentation de l’interface d’événements afin que votre classe exécute les actions que vous souhaitez que le processeur de manipulation exécute. Le code suivant est un modèle qui implémente la fonctionnalité minimale d’un récepteur d’événements pour l’interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .

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

Portez une attention particulière aux implémentations des méthodes [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta)et [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) dans la classe. Il s’agit des méthodes les plus probables dans l’interface, qui nécessitent l’exécution d’opérations basées sur les informations de manipulation transmises dans l’événement. Notez également que le deuxième paramètre dans le constructeur est l’objet utilisé dans les manipulations d’événements. Dans le code utilisé pour produire l’exemple, le hWnd de l’application est envoyé au constructeur afin qu’il puisse être repositionné et redimensionné.

### <a name="create-an-instance-of-an-imanipulationprocessor-interface"></a>Créer une instance d’une interface IManipulationProcessor

Dans le code où vous allez utiliser des manipulations, vous devez créer une instance d’une interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) . Tout d’abord, vous devez ajouter la prise en charge de la classe demanipulations. Le code suivant montre comment effectuer cette opération dans votre classe.

```C++
//Include windows.h for touch events
#include "windows.h"  

// Manipulation implementation file
#include <manipulations_i.c>
    
// Smart Pointer to a global reference of a manipulation processor, event sink
IManipulationProcessor* g_pIManipProc;     
```

Une fois que vous avez la variable pour le processeur de manipulation et que vous avez inclus les en-têtes pour les manipulations, vous devez créer une instance de l’interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) . Il s’agit d’un objet COM. Par conséquent, vous devez appeler [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), puis créer une instance de votre référence à **IManipulationProcessor**. Le code suivant montre comment vous pouvez créer une instance de cette interface.

```C++
   HRESULT hr = CoInitialize(0);
        
   hr = CoCreateInstance(CLSID_ManipulationProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIManipProc)
   );
```

### <a name="create-an-instance-of-your-event-sink-and-set-up-touch-events"></a>Créer une instance de votre récepteur d’événements et configurer des événements tactiles

Incluez la définition de votre classe de récepteur d’événements à votre code, puis ajoutez une variable pour la classe de récepteur d’événements de manipulation. L’exemple de code suivant comprend l’en-tête de l’implémentation de la classe et configure une variable globale pour stocker le récepteur d’événements.

```C++
//Include your definition of the event sink, CManipulationEventSink.h in this case
#include "CManipulationEventSink.h"    
     
// Set up a variable to point to the manipulation event sink implementation class    
CManipulationEventSink* g_pManipulationEventSink;   
```

Une fois que vous avez la variable et que vous avez inclus votre définition pour la nouvelle classe de récepteur d’événements, vous pouvez construire la classe à l’aide du processeur de manipulation que vous avez configuré à l’étape précédente. Le code suivant montre comment créer une instance de cette classe à partir de **OnInitDialog**.

```C++
   g_pManipulationEventSink = new CManipulationEventSink(g_pIManipProc, hWnd);


   RegisterTouchWindow(hWnd, 0);  
```

> [!Note]  
> La façon dont vous créez une instance de votre récepteur d’événements dépend de ce que vous effectuez avec les données de manipulation. Dans la plupart des cas, vous allez créer un récepteur d’événements de processeur de manipulation qui n’a pas le même constructeur que cet exemple.

### <a name="send-touch-event-data-to-the-manipulation-processor"></a>Envoyer des données d’événement tactile au processeur de manipulation

Maintenant que votre processeur de manipulation et votre récepteur d’événements sont configurés, vous devez alimenter les données tactiles vers le processeur de manipulation pour déclencher des événements de manipulation.

> [!Note]  
> il s’agit de la même procédure que celle décrite dans [Prise en main avec des Messages tactiles Windows](getting-started-with-multi-touch-messages.md).

Tout d’abord, vous allez créer du code pour décoder les messages [**WM \_ Touch**](wm-touchdown.md) et les envoyer à l’interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) pour déclencher des événements. Le code suivant montre un exemple d’implémentation qui est appelé à partir de la méthode **WndProc** et retourne une **LRESULT** pour la messagerie.

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

Maintenant que vous disposez d’une méthode utilitaire pour décoder le message [**WM \_ Touch**](wm-touchdown.md) , vous devez transmettre les messages **WM \_ Touch** à la fonction utilitaire à partir de votre méthode **WndProc** . Le code suivant montre comment procéder.

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

Les méthodes personnalisées que vous avez implémentées dans votre récepteur d’événements doivent maintenant fonctionner. Dans cet exemple, la touche de la fenêtre est déplacée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Manipulations](getting-started-with-manipulations.md)
</dt> </dl>


 