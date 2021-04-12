---
title: Mettre à jour le gestionnaire d’animations et dessiner des frames
description: Chaque fois qu’une application planifie un Storyboard, l’application doit fournir l’heure actuelle au gestionnaire d’animations.
ms.assetid: c4f746c3-e47c-4b82-a41b-e2c0d177d097
keywords:
- objets du gestionnaire d’animations-Animation Windows, mise à jour
- objets de minuteur d’animation Windows animation, connexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9a48e8d6e273174e502c374727e69b61bc478d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031340"
---
# <a name="update-the-animation-manager-and-draw-frames"></a>Mettre à jour le gestionnaire d’animations et dessiner des frames

Chaque fois qu’une application planifie un Storyboard, l’application doit fournir l’heure actuelle au gestionnaire d’animations. L’heure actuelle est également requise pour indiquer au gestionnaire d’animations de mettre à jour son état et de définir toutes les variables d’animation sur les valeurs interpolées appropriées.

## <a name="overview"></a>Vue d’ensemble

Il existe deux configurations prises en charge par Windows animation : animation pilotée par les applications et animation pilotée par un minuteur.

Pour utiliser l’animation pilotée par les applications dans votre application, vous devez mettre à jour le gestionnaire d’animations avant de dessiner chaque frame et utiliser un mécanisme approprié pour dessiner des frames suffisamment souvent pour l’animation. Une application utilisant une animation pilotée par application peut utiliser n’importe quel mécanisme pour déterminer l’heure actuelle, mais l’objet du minuteur d’animation Windows retourne une heure précise dans les unités acceptées par le gestionnaire d’animations. Pour éviter tout dessin inutile quand aucune animation n’est lue, vous devez également fournir un gestionnaire d’événements Manager pour commencer à redessiner quand les animations sont planifiées et vérifier après chaque image si le rafraîchissement peut être suspendu. Pour plus d’informations, consultez [animation pilotée](scenic-animation-api-overview.md)par les applications.

Dans la configuration pilotée par l’application, une application peut appeler la méthode [**IUIAnimationManager :: GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus) pour vérifier que les animations sont actuellement planifiées et continuer à dessiner des frames, le cas échéant. Étant donné que le redessin s’arrête quand aucune animation n’est planifiée, il est nécessaire de le redémarrer la prochaine fois qu’une animation est planifiée. Une application peut inscrire un gestionnaire d’événements de gestionnaire pour être averti lorsque l’état du gestionnaire d’animations passe de inactif (aucune animation n’est actuellement planifiée) à occupé.

Pour utiliser une animation pilotée par minuterie dans votre application, vous devez connecter le gestionnaire d’animations à un minuteur d’animation et fournir un gestionnaire d’événements de minuterie. Lorsque le gestionnaire d’animations est connecté à un minuteur, le minuteur peut indiquer au gestionnaire quand l’état de l’animation doit être mis à jour à mesure que le temps progresse. L’application doit dessiner un frame pour chaque graduation de la minuterie. Le gestionnaire d’animations peut, à son tour, indiquer à la minuterie quand des animations sont lues, de sorte que la minuterie peut s’arrêter pendant les périodes d’inactivité lorsque le rafraîchissement est inutile. Pour éviter tout dessin inutile quand aucune animation n’est lue, vous devez configurer le minuteur pour qu’il se désactive automatiquement. Pour plus d’informations, consultez [animation pilotée par minuterie](scenic-animation-api-overview.md).

## <a name="example-code"></a>Exemple de code

-   [Animation pilotée par les applications](#application-driven-animation)
-   [Animation pilotée par minuterie](#timer-driven-animation)

### <a name="application-driven-animation"></a>Animation Application-Driven

L’exemple de code suivant provient de ManagerEventHandler. h à partir [des exemples d’animation Windows](application-driven-animation-sample.md) et de la [disposition de grille](/windows/desktop/UIAnimation/grid-layout-sample). Il définit le gestionnaire d’événements du gestionnaire.


```C++
#include "UIAnimationHelper.h"

// Event handler object for manager status changes

class CManagerEventHandler :
    public CUIAnimationManagerEventHandlerBase<CManagerEventHandler>
{
public:

    static HRESULT
    CreateInstance
    (
        CMainWindow *pMainWindow,
        IUIAnimationManagerEventHandler **ppManagerEventHandler
    ) throw()
    {
        CManagerEventHandler *pManagerEventHandler;
        HRESULT hr = CUIAnimationCallbackBase::CreateInstance(
            ppManagerEventHandler,
            &pManagerEventHandler
            );
        if (SUCCEEDED(hr))
        {
            pManagerEventHandler->m_pMainWindow = pMainWindow;
        }
        
        return hr;
    }

    // IUIAnimationManagerEventHandler

    IFACEMETHODIMP
    OnManagerStatusChanged
    (
        UI_ANIMATION_MANAGER_STATUS newStatus,
        UI_ANIMATION_MANAGER_STATUS previousStatus
    )
    {
        HRESULT hr = S_OK;

        if (newStatus == UI_ANIMATION_MANAGER_BUSY)
        {
            hr = m_pMainWindow->Invalidate();
        }

        return hr;
    }

    ...

};
```



L’exemple de code suivant est extrait de MainWindow. cpp de l’exemple d' [animation pilotée par l’application](application-driven-animation-sample.md)Windows. consultez CMainWindow :: InitializeAnimation. Cet exemple crée une instance du gestionnaire d’événements Manager à l’aide de la méthode [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) et la transmet au gestionnaire d’animations à l’aide de la méthode [**IUIAnimationManager :: SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler) .


```C++
// Create and set the ManagerEventHandler to start updating when animations are scheduled

IUIAnimationManagerEventHandler *pManagerEventHandler;
HRESULT hr = CManagerEventHandler::CreateInstance(
    this,
    &pManagerEventHandler
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationManager->SetManagerEventHandler(
        pManagerEventHandler
        );
    pManagerEventHandler->Release();
}
```



Étant donné que le gestionnaire d’événements Manager conserve une référence à l’objet fenêtre principale, le gestionnaire d’événements Manager doit être effacé (en passant la **valeur null** à [**SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)) ou le gestionnaire d’animations doit être complètement libéré avant que la fenêtre principale soit détruite.

L’exemple de code suivant est extrait de MainWindow. cpp dans l’exemple d' [animation pilotée par l’application](application-driven-animation-sample.md)Windows. consultez la méthode CMainWindow :: OnPaint. Elle appelle la méthode [**IUIAnimationManager :: getTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime) pour récupérer l’heure dans les unités requises par la méthode [**IUIAnimationManager :: Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update) .


```C++
// Update the animation manager with the current time

UI_ANIMATION_SECONDS secondsNow;
HRESULT hr = m_pAnimationTimer->GetTime(
    &secondsNow
    );

if (SUCCEEDED(hr))
{
    hr = m_pAnimationManager->Update(
        secondsNow
        );

    ...

}
```



L’exemple de code suivant provient de MainWindow. cpp [des exemples d’animation Windows](application-driven-animation-sample.md) et de la [disposition en grille](/windows/desktop/UIAnimation/grid-layout-sample). consultez la méthode CMainWindow :: OnPaint. Il part du principe que l’application utilise une API Graphics qui se synchronise automatiquement avec la fréquence d’actualisation de l’analyse (par exemple Direct2D avec ses paramètres par défaut), auquel cas un appel à la fonction [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) est suffisant pour garantir que le code de peinture sera appelé à nouveau lorsqu’il sera temps de dessiner le frame suivant. Au lieu d’appeler **InvalidateRect** de manière inconditionnelle, il est préférable de vérifier s’il existe encore des animations planifiées à l’aide de [**GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus).


```C++
// Read the values of the animation variables and draw the client area

hr = DrawClientArea();
if (SUCCEEDED(hr))
{          
    // Continue redrawing the client area as long as there are animations scheduled
    UI_ANIMATION_MANAGER_STATUS status;
    hr = m_pAnimationManager->GetStatus(
        &status
        );
    if (SUCCEEDED(hr))
    {
        if (status == UI_ANIMATION_MANAGER_BUSY)
        {
            InvalidateRect(
                m_hwnd,
                NULL,
                FALSE
                );
        }
    }
}
```



### <a name="timer-driven-animation"></a>Animation Timer-Driven

L’exemple de code suivant est extrait de TimerEventHandler. h de l’exemple d' [animation pilotée par une](timer-driven-animation-sample.md)Animation Windows. L’exemple de code définit le gestionnaire d’événements du minuteur, qui invalide la zone cliente de la fenêtre pour provoquer un redessin après chaque mise à jour de l’état de l’animation.


```C++
#include "UIAnimationHelper.h"

// Event handler object for timer events

class CTimerEventHandler :
    public CUIAnimationTimerEventHandlerBase<CTimerEventHandler>
{
public:

    static HRESULT
    CreateInstance
    (
        CMainWindow *pMainWindow,
        IUIAnimationTimerEventHandler **ppTimerEventHandler
    ) throw()
    {
        CTimerEventHandler *pTimerEventHandler;
        HRESULT hr = CUIAnimationCallbackBase::CreateInstance(
            ppTimerEventHandler,
            &pTimerEventHandler
            );

        if (SUCCEEDED(hr))
        {
            pTimerEventHandler->m_pMainWindow = pMainWindow;
        }
        
        return hr;
    }

    // IUIAnimationTimerEventHandler

    IFACEMETHODIMP
    OnPreUpdate()
    {
        return S_OK;
    }

    IFACEMETHODIMP
    OnPostUpdate()
    {
        HRESULT hr = m_pMainWindow->Invalidate();

        return hr;
    }

    IFACEMETHODIMP
    OnRenderingTooSlow
    (
        UINT32 /* fps */
    )
    {
        return S_OK;
    }

    ...

};
```



L’exemple de code suivant est extrait de MainWindow. cpp de l’exemple d' [animation pilotée par une](timer-driven-animation-sample.md)Animation Windows. consultez CMainWindow :: InitializeAnimation. Cet exemple crée une instance du gestionnaire d’événements du minuteur à l’aide de la méthode [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) et la transmet au minuteur à l’aide de la méthode [**IUIAnimationTimer :: SetTimerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimereventhandler) . Étant donné que le gestionnaire d’événements du minuteur conserve une référence à l’objet de fenêtre principale, le gestionnaire d’événements du minuteur doit être effacé (en transmettant **null** à **SetTimerEventHandler**) ou le minuteur a été complètement libéré avant la destruction de la fenêtre principale.


```C++
// Create and set the timer event handler

IUIAnimationTimerEventHandler *pTimerEventHandler;
hr = CTimerEventHandler::CreateInstance(
    this,
    &pTimerEventHandler
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationTimer->SetTimerEventHandler(
        pTimerEventHandler
        );
    pTimerEventHandler->Release();
}
```



L’exemple de code suivant est extrait de MainWindow. cpp dans l’exemple d' [animation pilotée par une](timer-driven-animation-sample.md)Animation Windows. consultez la méthode CMainWindow :: InitializeAnimation. Elle appelle la méthode [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur l’objet du gestionnaire d’animations pour obtenir un pointeur vers [**IUIAnimationTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimerupdatehandler), puis connecte les objets [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)) et [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)) en définissant le gestionnaire d’animations comme gestionnaire de mise à jour de la minuterie à l’aide de la méthode [**IUIAnimationTimer :: SetTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler) . Notez qu’il n’est pas nécessaire d’effacer explicitement cette connexion ; la connexion est effacée en toute sécurité après que l’application a libéré le gestionnaire d’animations et le minuteur d’animation.


```C++
// Connect the animation manager to the timer

IUIAnimationTimerUpdateHandler *pTimerUpdateHandler;
hr = m_pAnimationManager->QueryInterface(
    IID_PPV_ARGS(&pTimerUpdateHandler)
    );

if (SUCCEEDED(hr))
{
    hr = m_pAnimationTimer->SetTimerUpdateHandler(
        pTimerUpdateHandler
        UI_ANIMATION_IDLE_BEHAVIOR_DISABLE  // timer will shut itself off when there are no animations playing
        );
    pTimerUpdateHandler->Release();
    if (SUCCEEDED(hr))
    {
        // Create and set the timer event handler

        ...

    }
}
```



Si **la \_ \_ \_ \_ désactivation du comportement inactif d’animation d’interface utilisateur** n’est pas utilisée, il est également nécessaire d’activer le minuteur pour le démarrer.

## <a name="previous-step"></a>Étape précédente

Avant de commencer cette étape, vous devez avoir terminé cette étape : [créer des variables d’animation](create-animation-variables.md).

## <a name="next-step"></a>étape suivante

À l’issue de cette étape, l’étape suivante est : [lire les valeurs de la variable d’animation](updating---application-driven-animation.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IUIAnimationManager :: GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus)
</dt> <dt>

[**IUIAnimationManager::SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)
</dt> <dt>

[**IUIAnimationManager :: Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update)
</dt> <dt>

[**IUIAnimationTimer :: GetTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[**IUIAnimationTimer::SetTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler)
</dt> <dt>

[**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))
</dt> <dt>

[**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))
</dt> <dt>

[Vue d’ensemble des animations Windows](scenic-animation-api-overview.md)
</dt> </dl>

 

 