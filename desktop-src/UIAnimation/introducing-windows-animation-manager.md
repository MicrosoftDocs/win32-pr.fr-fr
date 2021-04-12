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
# <a name="update-the-animation-manager-and-draw-frames"></a><span data-ttu-id="df66e-105">Mettre à jour le gestionnaire d’animations et dessiner des frames</span><span class="sxs-lookup"><span data-stu-id="df66e-105">Update the Animation Manager and Draw Frames</span></span>

<span data-ttu-id="df66e-106">Chaque fois qu’une application planifie un Storyboard, l’application doit fournir l’heure actuelle au gestionnaire d’animations.</span><span class="sxs-lookup"><span data-stu-id="df66e-106">Each time an application schedules a storyboard, the application must supply the current time to the animation manager.</span></span> <span data-ttu-id="df66e-107">L’heure actuelle est également requise pour indiquer au gestionnaire d’animations de mettre à jour son état et de définir toutes les variables d’animation sur les valeurs interpolées appropriées.</span><span class="sxs-lookup"><span data-stu-id="df66e-107">The current time is also required when directing the animation manager to update its state and set all animation variables to the appropriate interpolated values.</span></span>

## <a name="overview"></a><span data-ttu-id="df66e-108">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="df66e-108">Overview</span></span>

<span data-ttu-id="df66e-109">Il existe deux configurations prises en charge par Windows animation : animation pilotée par les applications et animation pilotée par un minuteur.</span><span class="sxs-lookup"><span data-stu-id="df66e-109">There are two configurations supported by Windows Animation: application-driven animation and timer-driven animation.</span></span>

<span data-ttu-id="df66e-110">Pour utiliser l’animation pilotée par les applications dans votre application, vous devez mettre à jour le gestionnaire d’animations avant de dessiner chaque frame et utiliser un mécanisme approprié pour dessiner des frames suffisamment souvent pour l’animation.</span><span class="sxs-lookup"><span data-stu-id="df66e-110">To use application-driven animation in your application, you must update the animation manager before drawing each frame and use an appropriate mechanism to draw frames frequently enough for animation.</span></span> <span data-ttu-id="df66e-111">Une application utilisant une animation pilotée par application peut utiliser n’importe quel mécanisme pour déterminer l’heure actuelle, mais l’objet du minuteur d’animation Windows retourne une heure précise dans les unités acceptées par le gestionnaire d’animations.</span><span class="sxs-lookup"><span data-stu-id="df66e-111">An application using application-driven animation can use any mechanism to determine the current time, but the Windows Animation timer object returns a precise time in the units accepted by the animation manager.</span></span> <span data-ttu-id="df66e-112">Pour éviter tout dessin inutile quand aucune animation n’est lue, vous devez également fournir un gestionnaire d’événements Manager pour commencer à redessiner quand les animations sont planifiées et vérifier après chaque image si le rafraîchissement peut être suspendu.</span><span class="sxs-lookup"><span data-stu-id="df66e-112">To avoid unnecessary drawing when no animations are playing, you should also provide a manager event handler to start redrawing when animations are scheduled and check after each frame whether redrawing can be suspended.</span></span> <span data-ttu-id="df66e-113">Pour plus d’informations, consultez [animation pilotée](scenic-animation-api-overview.md)par les applications.</span><span class="sxs-lookup"><span data-stu-id="df66e-113">For more information, see [Application-Driven Animation](scenic-animation-api-overview.md).</span></span>

<span data-ttu-id="df66e-114">Dans la configuration pilotée par l’application, une application peut appeler la méthode [**IUIAnimationManager :: GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus) pour vérifier que les animations sont actuellement planifiées et continuer à dessiner des frames, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="df66e-114">In the application-driven configuration, an application can call the [**IUIAnimationManager::GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus) method to verify that animations are currently scheduled and continue to draw frames if they are.</span></span> <span data-ttu-id="df66e-115">Étant donné que le redessin s’arrête quand aucune animation n’est planifiée, il est nécessaire de le redémarrer la prochaine fois qu’une animation est planifiée.</span><span class="sxs-lookup"><span data-stu-id="df66e-115">Because redrawing stops when there are no animations scheduled, it is necessary to restart it the next time an animation is scheduled.</span></span> <span data-ttu-id="df66e-116">Une application peut inscrire un gestionnaire d’événements de gestionnaire pour être averti lorsque l’état du gestionnaire d’animations passe de inactif (aucune animation n’est actuellement planifiée) à occupé.</span><span class="sxs-lookup"><span data-stu-id="df66e-116">An application can register a manager event handler to be notified when the status of the animation manager changes from idle (no animations are currently scheduled) to busy.</span></span>

<span data-ttu-id="df66e-117">Pour utiliser une animation pilotée par minuterie dans votre application, vous devez connecter le gestionnaire d’animations à un minuteur d’animation et fournir un gestionnaire d’événements de minuterie.</span><span class="sxs-lookup"><span data-stu-id="df66e-117">To use timer-driven animation in your application, you must connect the animation manager to an animation timer and provide a timer event handler.</span></span> <span data-ttu-id="df66e-118">Lorsque le gestionnaire d’animations est connecté à un minuteur, le minuteur peut indiquer au gestionnaire quand l’état de l’animation doit être mis à jour à mesure que le temps progresse.</span><span class="sxs-lookup"><span data-stu-id="df66e-118">When the animation manager is connected to a timer, the timer can tell the manager when the animation state should be updated as time progresses.</span></span> <span data-ttu-id="df66e-119">L’application doit dessiner un frame pour chaque graduation de la minuterie.</span><span class="sxs-lookup"><span data-stu-id="df66e-119">The application should draw a frame for each timer tick.</span></span> <span data-ttu-id="df66e-120">Le gestionnaire d’animations peut, à son tour, indiquer à la minuterie quand des animations sont lues, de sorte que la minuterie peut s’arrêter pendant les périodes d’inactivité lorsque le rafraîchissement est inutile.</span><span class="sxs-lookup"><span data-stu-id="df66e-120">The animation manager can in turn tell the timer when there are animations playing, so the timer can shut itself off during idle periods when redrawing is unnecessary.</span></span> <span data-ttu-id="df66e-121">Pour éviter tout dessin inutile quand aucune animation n’est lue, vous devez configurer le minuteur pour qu’il se désactive automatiquement.</span><span class="sxs-lookup"><span data-stu-id="df66e-121">To avoid unnecessary drawing when no animations are playing, you should configure the timer to disable itself automatically.</span></span> <span data-ttu-id="df66e-122">Pour plus d’informations, consultez [animation pilotée par minuterie](scenic-animation-api-overview.md).</span><span class="sxs-lookup"><span data-stu-id="df66e-122">For more information, see [Timer-Driven Animation](scenic-animation-api-overview.md).</span></span>

## <a name="example-code"></a><span data-ttu-id="df66e-123">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="df66e-123">Example Code</span></span>

-   [<span data-ttu-id="df66e-124">Animation pilotée par les applications</span><span class="sxs-lookup"><span data-stu-id="df66e-124">Application-Driven Animation</span></span>](#application-driven-animation)
-   [<span data-ttu-id="df66e-125">Animation pilotée par minuterie</span><span class="sxs-lookup"><span data-stu-id="df66e-125">Timer-Driven Animation</span></span>](#timer-driven-animation)

### <a name="application-driven-animation"></a><span data-ttu-id="df66e-126">Animation Application-Driven</span><span class="sxs-lookup"><span data-stu-id="df66e-126">Application-Driven Animation</span></span>

<span data-ttu-id="df66e-127">L’exemple de code suivant provient de ManagerEventHandler. h à partir [des exemples d’animation Windows](application-driven-animation-sample.md) et de la [disposition de grille](/windows/desktop/UIAnimation/grid-layout-sample).</span><span class="sxs-lookup"><span data-stu-id="df66e-127">The following example code is taken from ManagerEventHandler.h from the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Grid Layout](/windows/desktop/UIAnimation/grid-layout-sample).</span></span> <span data-ttu-id="df66e-128">Il définit le gestionnaire d’événements du gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="df66e-128">It defines the manager event handler.</span></span>


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



<span data-ttu-id="df66e-129">L’exemple de code suivant est extrait de MainWindow. cpp de l’exemple d' [animation pilotée par l’application](application-driven-animation-sample.md)Windows. consultez CMainWindow :: InitializeAnimation.</span><span class="sxs-lookup"><span data-stu-id="df66e-129">The following example code is taken from MainWindow.cpp from the Windows Animation sample [Application-Driven Animation](application-driven-animation-sample.md); see CMainWindow::InitializeAnimation.</span></span> <span data-ttu-id="df66e-130">Cet exemple crée une instance du gestionnaire d’événements Manager à l’aide de la méthode [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) et la transmet au gestionnaire d’animations à l’aide de la méthode [**IUIAnimationManager :: SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler) .</span><span class="sxs-lookup"><span data-stu-id="df66e-130">This example creates an instance of the manager event handler using the [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) method and passes it to the animation manager using the [**IUIAnimationManager::SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler) method.</span></span>


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



<span data-ttu-id="df66e-131">Étant donné que le gestionnaire d’événements Manager conserve une référence à l’objet fenêtre principale, le gestionnaire d’événements Manager doit être effacé (en passant la **valeur null** à [**SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)) ou le gestionnaire d’animations doit être complètement libéré avant que la fenêtre principale soit détruite.</span><span class="sxs-lookup"><span data-stu-id="df66e-131">Because the manager event handler retains a reference to the main window object, the manager event handler should be cleared (by passing **NULL** to [**SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)) or the animation manager should be completely released before the main window is destroyed.</span></span>

<span data-ttu-id="df66e-132">L’exemple de code suivant est extrait de MainWindow. cpp dans l’exemple d' [animation pilotée par l’application](application-driven-animation-sample.md)Windows. consultez la méthode CMainWindow :: OnPaint.</span><span class="sxs-lookup"><span data-stu-id="df66e-132">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Application-Driven Animation](application-driven-animation-sample.md); see the CMainWindow::OnPaint method.</span></span> <span data-ttu-id="df66e-133">Elle appelle la méthode [**IUIAnimationManager :: getTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime) pour récupérer l’heure dans les unités requises par la méthode [**IUIAnimationManager :: Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update) .</span><span class="sxs-lookup"><span data-stu-id="df66e-133">It calls the [**IUIAnimationManager::GetTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime) method to retrieve the time in the units required by the [**IUIAnimationManager::Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update) method.</span></span>


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



<span data-ttu-id="df66e-134">L’exemple de code suivant provient de MainWindow. cpp [des exemples d’animation Windows](application-driven-animation-sample.md) et de la [disposition en grille](/windows/desktop/UIAnimation/grid-layout-sample). consultez la méthode CMainWindow :: OnPaint.</span><span class="sxs-lookup"><span data-stu-id="df66e-134">The following example code is taken from MainWindow.cpp from the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Grid Layout](/windows/desktop/UIAnimation/grid-layout-sample); see the CMainWindow::OnPaint method.</span></span> <span data-ttu-id="df66e-135">Il part du principe que l’application utilise une API Graphics qui se synchronise automatiquement avec la fréquence d’actualisation de l’analyse (par exemple Direct2D avec ses paramètres par défaut), auquel cas un appel à la fonction [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) est suffisant pour garantir que le code de peinture sera appelé à nouveau lorsqu’il sera temps de dessiner le frame suivant.</span><span class="sxs-lookup"><span data-stu-id="df66e-135">It assumes that the application is using a graphics API that automatically synchronizes to the monitor refresh rate (such as Direct2D with its default settings), in which case a call to the [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) function is enough to ensure that the painting code will be called again when it is time to draw the next frame.</span></span> <span data-ttu-id="df66e-136">Au lieu d’appeler **InvalidateRect** de manière inconditionnelle, il est préférable de vérifier s’il existe encore des animations planifiées à l’aide de [**GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus).</span><span class="sxs-lookup"><span data-stu-id="df66e-136">Rather than call **InvalidateRect** unconditionally, it is better to check if there are still any animations scheduled using [**GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus).</span></span>


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



### <a name="timer-driven-animation"></a><span data-ttu-id="df66e-137">Animation Timer-Driven</span><span class="sxs-lookup"><span data-stu-id="df66e-137">Timer-Driven Animation</span></span>

<span data-ttu-id="df66e-138">L’exemple de code suivant est extrait de TimerEventHandler. h de l’exemple d' [animation pilotée par une](timer-driven-animation-sample.md)Animation Windows.</span><span class="sxs-lookup"><span data-stu-id="df66e-138">The following example code is taken from TimerEventHandler.h from the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md).</span></span> <span data-ttu-id="df66e-139">L’exemple de code définit le gestionnaire d’événements du minuteur, qui invalide la zone cliente de la fenêtre pour provoquer un redessin après chaque mise à jour de l’état de l’animation.</span><span class="sxs-lookup"><span data-stu-id="df66e-139">The example code defines the timer event handler, which invalidates the window's client area to cause a repaint after each update of the animation state.</span></span>


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



<span data-ttu-id="df66e-140">L’exemple de code suivant est extrait de MainWindow. cpp de l’exemple d' [animation pilotée par une](timer-driven-animation-sample.md)Animation Windows. consultez CMainWindow :: InitializeAnimation.</span><span class="sxs-lookup"><span data-stu-id="df66e-140">The following example code is taken from MainWindow.cpp from the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see CMainWindow::InitializeAnimation.</span></span> <span data-ttu-id="df66e-141">Cet exemple crée une instance du gestionnaire d’événements du minuteur à l’aide de la méthode [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) et la transmet au minuteur à l’aide de la méthode [**IUIAnimationTimer :: SetTimerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimereventhandler) .</span><span class="sxs-lookup"><span data-stu-id="df66e-141">This example creates an instance of the timer event handler using the [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) method and passes it to the timer using the [**IUIAnimationTimer::SetTimerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimereventhandler) method.</span></span> <span data-ttu-id="df66e-142">Étant donné que le gestionnaire d’événements du minuteur conserve une référence à l’objet de fenêtre principale, le gestionnaire d’événements du minuteur doit être effacé (en transmettant **null** à **SetTimerEventHandler**) ou le minuteur a été complètement libéré avant la destruction de la fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="df66e-142">Because the timer event handler retains a reference to the main window object, the timer event handler should be cleared (by passing **NULL** to **SetTimerEventHandler**) or the timer completely released before the main window is destroyed.</span></span>


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



<span data-ttu-id="df66e-143">L’exemple de code suivant est extrait de MainWindow. cpp dans l’exemple d' [animation pilotée par une](timer-driven-animation-sample.md)Animation Windows. consultez la méthode CMainWindow :: InitializeAnimation.</span><span class="sxs-lookup"><span data-stu-id="df66e-143">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see the CMainWindow::InitializeAnimation method.</span></span> <span data-ttu-id="df66e-144">Elle appelle la méthode [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur l’objet du gestionnaire d’animations pour obtenir un pointeur vers [**IUIAnimationTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimerupdatehandler), puis connecte les objets [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)) et [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)) en définissant le gestionnaire d’animations comme gestionnaire de mise à jour de la minuterie à l’aide de la méthode [**IUIAnimationTimer :: SetTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler) .</span><span class="sxs-lookup"><span data-stu-id="df66e-144">It calls the [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the animation manager object to get a pointer to [**IUIAnimationTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimerupdatehandler), then connects the [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)) and [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)) objects by setting the animation manager as the timer's update handler using the [**IUIAnimationTimer::SetTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler) method.</span></span> <span data-ttu-id="df66e-145">Notez qu’il n’est pas nécessaire d’effacer explicitement cette connexion ; la connexion est effacée en toute sécurité après que l’application a libéré le gestionnaire d’animations et le minuteur d’animation.</span><span class="sxs-lookup"><span data-stu-id="df66e-145">Note that it is not necessary to explicitly clear this connection; the connection is cleared safely after the application releases both the animation manager and the animation timer.</span></span>


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



<span data-ttu-id="df66e-146">Si **la \_ \_ \_ \_ désactivation du comportement inactif d’animation d’interface utilisateur** n’est pas utilisée, il est également nécessaire d’activer le minuteur pour le démarrer.</span><span class="sxs-lookup"><span data-stu-id="df66e-146">If **UI\_ANIMATION\_IDLE\_BEHAVIOR\_DISABLE** is not used, it is also necessary to enable the timer to start it ticking.</span></span>

## <a name="previous-step"></a><span data-ttu-id="df66e-147">Étape précédente</span><span class="sxs-lookup"><span data-stu-id="df66e-147">Previous Step</span></span>

<span data-ttu-id="df66e-148">Avant de commencer cette étape, vous devez avoir terminé cette étape : [créer des variables d’animation](create-animation-variables.md).</span><span class="sxs-lookup"><span data-stu-id="df66e-148">Before starting this step, you should have completed this step: [Create Animation Variables](create-animation-variables.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="df66e-149">étape suivante</span><span class="sxs-lookup"><span data-stu-id="df66e-149">Next Step</span></span>

<span data-ttu-id="df66e-150">À l’issue de cette étape, l’étape suivante est : [lire les valeurs de la variable d’animation](updating---application-driven-animation.md).</span><span class="sxs-lookup"><span data-stu-id="df66e-150">After completing this step, the next step is: [Read the Animation Variable Values](updating---application-driven-animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="df66e-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="df66e-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df66e-152">**IUIAnimationManager :: GetStatus**</span><span class="sxs-lookup"><span data-stu-id="df66e-152">**IUIAnimationManager::GetStatus**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus)
</dt> <dt>

[<span data-ttu-id="df66e-153">**IUIAnimationManager::SetManagerEventHandler**</span><span class="sxs-lookup"><span data-stu-id="df66e-153">**IUIAnimationManager::SetManagerEventHandler**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)
</dt> <dt>

[<span data-ttu-id="df66e-154">**IUIAnimationManager :: Update**</span><span class="sxs-lookup"><span data-stu-id="df66e-154">**IUIAnimationManager::Update**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update)
</dt> <dt>

[<span data-ttu-id="df66e-155">**IUIAnimationTimer :: GetTime**</span><span class="sxs-lookup"><span data-stu-id="df66e-155">**IUIAnimationTimer::GetTime**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[<span data-ttu-id="df66e-156">**IUIAnimationTimer::SetTimerUpdateHandler**</span><span class="sxs-lookup"><span data-stu-id="df66e-156">**IUIAnimationTimer::SetTimerUpdateHandler**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler)
</dt> <dt>

<span data-ttu-id="df66e-157">[**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="df66e-157">[**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="df66e-158">[**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="df66e-158">[**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="df66e-159">Vue d’ensemble des animations Windows</span><span class="sxs-lookup"><span data-stu-id="df66e-159">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 