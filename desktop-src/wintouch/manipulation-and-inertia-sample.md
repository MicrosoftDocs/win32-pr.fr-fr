---
title: Exemple de manipulation et d’inertie
description: l’exemple de Manipulation et d’inertie montre comment ajouter une prise en charge de l’interface tactile Windows aux applications natives basées sur Windows qui utilisent l’API tactile Windows.
ms.assetid: 6a6e2e39-026e-47a3-b936-16f6a740a3af
keywords:
- Windows Touch, exemples de code
- Windows Toucher, exemple de code
- Windows Toucher, manipulations
- Windows Toucher, inertie
- Windows Exemple tactile, manipulation et inertie
- Exemple de manipulation et d’inertie
- Windows Interface tactile, _IManipulationEventSink
- Windows Interface tactile, IManipulationProcessor
- Windows Interface tactile, IInertiaProcessor
- manipulations, exemple de code
- manipulations, exemples de code
- manipulations, interface _IManipulationEventSink
- manipulations, interface IManipulationProcessor
- inertie, exemple de code
- inertie, exemples de code
- inertie, interface IInertiaProcessor
- Interface _IManipulationEventSink
- Interface IManipulationProcessor, exemples de code
- Interface IManipulationProcessor, exemple de code
- Interface IInertiaProcessor, exemples de code
- Interface IInertiaProcessor, exemple de code
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 8b6471362d30b6efc9dfa0c4f07df70f014c8cb72866c92bbb04c9eb33463410
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840592"
---
# <a name="manipulation-and-inertia-sample"></a>Exemple de manipulation et d’inertie

l’exemple de Manipulation et d’inertie montre comment ajouter une prise en charge de l’interface tactile Windows aux applications natives basées sur Windows qui utilisent l’API tactile Windows. L’exemple implémente les fonctionnalités de base de l’API pour permettre la traduction, la rotation et la mise à l’échelle des objets et l’application des propriétés d’inertie. l’exemple montre également comment fournir à votre Windows des applications tactiles la prise en charge de base de la souris. L’illustration suivante montre l’apparence de l’exemple lorsqu’il s’exécute.

![capture d’écran montrant deux zones avec des dégradés dans l’exemple de manipulation et d’inertie](images/manip-inertia-sample.png)

les zones avec des dégradés peuvent être manipulées indépendamment par un utilisateur lorsqu’ils exécutent l’application à partir d’un ordinateur qui prend en charge Windows Touch.

## <a name="register-the-touch-window"></a>Inscrire la fenêtre tactile

avant de pouvoir recevoir des entrées tactiles, vous devez d’abord informer le système que votre application est une application Windows touch en appelant la fonction suivante :

```C++
   RegisterTouchWindow(g_hWnd, 0);
```

## <a name="implement-the-_imanipulationeventsink-interface"></a>Implémenter l’interface _IManipulationEventSink

Le récepteur d’événements [**_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) contient trois fonctions : [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta)et [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted). Ces fonctions de rappel sont utilisées par l’interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) et l’interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) pour retourner les valeurs calculées par les processeurs après l’appel des fonctions [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime), [**ProcessUpWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime), [**ProcessDownWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)et [**ProcessMoveWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime) . L’exemple de code suivant montre un exemple d’implémentation d’une interface **_IManipulationEvents** .

```C++
#include "cmanipulationeventsink.h"
#include <math.h>

CManipulationEventSink::CManipulationEventSink(HWND hWnd, CDrawingObject *dObj, int iTimerId, BOOL inertia) {
    // Manipulation & Inertia Processors
    m_manip = NULL;
    m_inert = NULL;

    // Connection points for COM.
    m_pConPointContainer = NULL;
    m_pConnPoint = NULL;

    // Reference to an object associated with this event sink.
    m_dObj = dObj;

    // Handle to the window used for computing boundaries.
    m_hWnd = hWnd;

    // The unique timer id for this manipulation event sink.
    m_iTimerId = iTimerId;

    m_bInertia = inertia;

    m_cRefCount = 1;
}


CManipulationEventSink::~CManipulationEventSink()
{

}


HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationStarted(
    FLOAT x,
    FLOAT y)
{
    KillTimer(m_hWnd, m_iTimerId);

    return S_OK;
}

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta(
    FLOAT x,
    FLOAT y,
    FLOAT translationDeltaX,
    FLOAT translationDeltaY,
    FLOAT scaleDelta,
    FLOAT expansionDelta,
    FLOAT rotationDelta,
    FLOAT cumulativeTranslationX,
    FLOAT cumulativeTranslationY,
    FLOAT cumulativeScale,
    FLOAT cumulativeExpansion,
    FLOAT cumulativeRotation)
{
    FLOAT pivot = 0.0f;

    // Apply transformation based on rotationDelta (in radians).
    FLOAT rads = 180.0f / 3.14159f;
    m_dObj->Rotate(rotationDelta*rads, x, y);

    // Apply translation based on scaleDelta.
    m_dObj->Scale(scaleDelta);

    // Apply translation based on translationDelta.
    m_dObj->Translate(translationDeltaX, translationDeltaY);

    if(!m_bInertia)
    {
        // Set values for one-finger rotations.
        FLOAT fPivotRadius = (FLOAT)(sqrt(pow(m_dObj->GetWidth()/2, 2)
                           + pow(m_dObj->GetHeight()/2, 2)))*0.4f;
        FLOAT fPivotPtX    = m_dObj->GetCenterX();
        FLOAT fPivotPtY    = m_dObj->GetCenterY();

        m_manip->put_PivotPointX(fPivotPtX);
        m_manip->put_PivotPointY(fPivotPtY);
        m_manip->put_PivotRadius(fPivotRadius);
    }
    return S_OK;
}

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationCompleted(
    FLOAT x,
    FLOAT y,
    FLOAT cumulativeTranslationX,
    FLOAT cumulativeTranslationY,
    FLOAT cumulativeScale,
    FLOAT cumulativeExpansion,
    FLOAT cumulativeRotation)
{
    if(!m_bInertia)
    {
        SetupInertia();

        // Kick off timer that handles inertia.
        SetTimer(m_hWnd, m_iTimerId, DESIRED_MILLISECONDS, NULL);
    }
    else
    {
        // Stop timer that handles inertia.
        KillTimer(m_hWnd, m_iTimerId);
    }

    return S_OK;
}
```

## <a name="create-com-objects-and-set-up-the-imanipulationprocessor-and-iinertiaprocessor-interfaces"></a>Créer des objets COM et configurer les interfaces IManipulationProcessor et IInertiaProcessor

L’API fournit une implémentation des interfaces [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) et [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) . Vous devez créer une instance de et référencer les objets COM à partir du récepteur d’événements [**IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) qui a été implémenté précédemment.

## <a name="handle-wm_touch-messages"></a>Gérer les messages de WM_TOUCH

Les données d’entrée doivent être extraites des messages de [**WM_TOUCH**](wm-touchdown.md) , puis doivent être traitées ultérieurement pour alimenter le processeur de manipulation approprié.

```C++
switch (msg)
{
    case WM_TOUCH:

      iNumContacts = LOWORD(wParam);
      hInput       = (HTOUCHINPUT)lParam;
      pInputs      = new TOUCHINPUT[iNumContacts];

      // Get each touch input info and feed each
      // tagTOUCHINPUT into the process input handler.

      if(pInputs != NULL)
      {
          if(GetTouchInputInfo(hInput, iNumContacts,
               pInputs, sizeof(TOUCHINPUT)))
          {
              for(int i = 0; i < iNumContacts; i++)
              {
                  // Bring touch input info into client coordinates.
                  ptInputs.x = pInputs[i].x/100;
                  ptInputs.y = pInputs[i].y/100;
                  ScreenToClient(g_hWnd, &ptInputs);

                  pInputs[i].x = ptInputs.x;
                  pInputs[i].y = ptInputs.y;

                  g_ctDriver->ProcessInputEvent(pInputs[i]);
              }
          }
      }

      delete [] pInputs;
      break;
}
```

> [!Note]  
> Pour pouvoir utiliser la fonction [**ScreenToClient**](/windows/desktop/api/winuser/nf-winuser-screentoclient) , vous devez disposer d’une prise en charge des résolutions élevées dans votre application. Pour plus d’informations sur la prise en charge de la haute résolution, consultez la section [haute résolution]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) de MSDN.

## <a name="pass-touchinput-structures-to-the-appropriate-processor"></a>Passer les structures TOUCHINPUT au processeur approprié

Une fois les données extraites des messages [**WM_TOUCH**](wm-touchdown.md) à l’aide de la fonction [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) , alimentez les données dans le processeur de manipulation en appelant les fonctions [**ProcessUpWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime), [**ProcessDownWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)ou [**ProcessMoveWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime) , en fonction de l' **dwFlag** défini dans la structure [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) .

> [!Note]  
> Lorsque vous prenez en charge plusieurs manipulations, vous devez créer un processeur de manipulation si le **dwId** défini dans la structure [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) doit être utilisé pour envoyer les données à l’objet [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) correct.

```C++
CoreObject* coCurrent = m_coHead;

while(coCurrent!=NULL && !bFoundObj)
{
    if(dwEvent & TOUCHEVENTF_DOWN)
    {
        DownEvent(coCurrent, inData, &bFoundObj);
    }
    else if(dwEvent & TOUCHEVENTF_MOVE)
    {
        MoveEvent(coCurrent, inData);
    }
    else if(dwEvent & TOUCHEVENTF_UP)
    {
        UpEvent(coCurrent, inData);
    }
    coCurrent = coCurrent->coNext;
}

VOID CComTouchDriver::DownEvent(CoreObject* coRef, tagTOUCHINPUT inData, BOOL* bFound) {
    DWORD dwPCursor = inData.dwID;
    DWORD dwPTime   = inData.dwTime;
    int x           = inData.x;
    int y           = inData.y;

    // Check that the user has touched within an object's region and fed to the object's manipulation processor.

    if(coRef->doDrawing->InRegion(x, y) &&
        !HasCursor(coRef, dwPCursor))
    {
        ...

        // Feed values to the Manipulation Processor.
        coRef->manipulationProc->ProcessDownWithTime(dwPCursor, (FLOAT)x, (FLOAT)y, dwPTime);

        ...
    }
}
```

## <a name="set-up-inertia-within-manipulationcompleted"></a>Configuration de l’inertie dans ManipulationCompleted

Après l’appel de la méthode [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) , l’objet [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) doit définir les valeurs de l’objet [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) lié à **IManipulationProcessor** pour appeler inertie. L’exemple de code suivant montre comment configurer l’objet **IInertiaProcessor** à partir de la méthode **IManipulationProcessor** **ManipulationCompleted**.

```C++
    int iVWidth       = GetSystemMetrics(SM_CXVIRTUALSCREEN);
    int iVHeight      = GetSystemMetrics(SM_CYVIRTUALSCREEN);

    RECT rc;
    GetClientRect(m_hWnd, &rc);
    FLOAT lCWidth     = (FLOAT)rc.right;
    FLOAT lCHeight    = (FLOAT)rc.bottom;

    // Set properties for inertia events.

    // Deceleration for tranlations in pixel / msec^2.
    m_inert->put_DesiredDeceleration(0.001f);

    // Deceleration for rotations in radians / msec^2.
    m_inert->put_DesiredAngularDeceleration(0.00001f);

    // Calculate borders and elastic margin to be set.
    // They are relative to the width and height of the object.

    FLOAT fHOffset = m_dObj->GetWidth()  * 0.5f;
    FLOAT fVOffset = m_dObj->GetHeight() * 0.5f;

    // Elastic margin is in pixels - note that it offsets the boundary.

    FLOAT fHElasticMargin = 25.0f;
    FLOAT fVElasticMargin = 25.0f;

    FLOAT fBoundaryLeft   = fHOffset + fHElasticMargin;
    FLOAT fBoundaryTop    = fVOffset + fVElasticMargin;
    FLOAT fBoundaryRight  = lCWidth - fHOffset - fHElasticMargin;
    FLOAT fBoundaryBottom = lCHeight - fVOffset - fVElasticMargin;

    // Set borders and elastic margin.

    m_inert->put_BoundaryLeft(fBoundaryLeft);
    m_inert->put_BoundaryTop(fBoundaryTop);
    m_inert->put_BoundaryRight(fBoundaryRight);
    m_inert->put_BoundaryBottom(fBoundaryBottom);

    m_inert->put_ElasticMarginLeft(fHElasticMargin);
    m_inert->put_ElasticMarginTop(fVElasticMargin);
    m_inert->put_ElasticMarginRight(fHElasticMargin);
    m_inert->put_ElasticMarginBottom(fVElasticMargin);

    // Set initial origins.

    m_inert->put_InitialOriginX(m_dObj->GetCenterX());
    m_inert->put_InitialOriginY(m_dObj->GetCenterY());

    FLOAT fVX;
    FLOAT fVY;
    FLOAT fVR;

    m_manip->GetVelocityX(&fVX);
    m_manip->GetVelocityY(&fVY);
    m_manip->GetAngularVelocity(&fVR);

    // Set initial velocities for inertia processor.

    m_inert->put_InitialVelocityX(fVX);
    m_inert->put_InitialVelocityY(fVY);
    m_inert->put_InitialAngularVelocity(fVR);
```

## <a name="clean-up-your-com-objects"></a>Nettoyer vos objets COM

Lorsque votre application se ferme, vous devez nettoyer vos objets COM. Le code suivant montre comment vous pouvez libérer les ressources qui ont été allouées dans l’exemple.

```C++
CComTouchDriver::~CComTouchDriver(VOID) {
    CoreObject* coCurrent = m_coHead;

    // Clean up COM objects.

    while(coCurrent!=NULL)
    {
        coCurrent->inertiaEventSink->Release();
        coCurrent->manipulationEventSink->Release();
        coCurrent->inertiaProc->Release();
        coCurrent->manipulationProc->Release();
        coCurrent = coCurrent->coNext;
    }
}
```

## <a name="related-topics"></a>Rubriques connexes

exemple d' [Application de manipulation multipoint](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulation/cpp), [de manipulation et d’inertie](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulationInertia/cpp), [Windows exemples tactiles](windows-touch-samples.md)