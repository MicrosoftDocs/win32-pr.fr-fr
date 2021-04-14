---
title: Créer des variables d’animation
description: Une application doit créer une variable d’animation pour chaque caractéristique visuelle qui doit être animée à l’aide de l’animation Windows.
ms.assetid: 360aa157-cb50-400a-b373-45885410469d
keywords:
- variables d’animation Windows animation, création
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c059a924e22700bb4abd794435ad708a2775a9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382487"
---
# <a name="create-animation-variables"></a><span data-ttu-id="26874-104">Créer des variables d’animation</span><span class="sxs-lookup"><span data-stu-id="26874-104">Create Animation Variables</span></span>

<span data-ttu-id="26874-105">Une application doit créer une variable d’animation pour chaque caractéristique visuelle qui doit être animée à l’aide de l’animation Windows.</span><span class="sxs-lookup"><span data-stu-id="26874-105">An application must create an animation variable for each visual characteristic that is to be animated using Windows Animation.</span></span>

## <a name="overview"></a><span data-ttu-id="26874-106">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="26874-106">Overview</span></span>

<span data-ttu-id="26874-107">Les variables d’animation sont créées à l’aide du gestionnaire d’animations, et l’application doit conserver une référence à chaque fois que cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="26874-107">Animation variables are created using the animation manager, and the application should retain a reference to each for as long as it is needed.</span></span> <span data-ttu-id="26874-108">En général, votre application crée chaque variable d’animation en même temps que l’objet visuel qu’elle anime.</span><span class="sxs-lookup"><span data-stu-id="26874-108">Your application will generally create each animation variable at the same time as the visual object it animates.</span></span>

<span data-ttu-id="26874-109">Quand une variable d’animation est créée, sa valeur initiale doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="26874-109">When an animation variable is created, its initial value must be specified.</span></span> <span data-ttu-id="26874-110">Par la suite, sa valeur ne peut être modifiée qu’en planifiant des storyboards qui l’animent.</span><span class="sxs-lookup"><span data-stu-id="26874-110">Thereafter, its value can only be altered by scheduling storyboards that animate it.</span></span>

<span data-ttu-id="26874-111">Les variables d’animation sont passées en tant que paramètres lors de la construction des storyboards. par conséquent, l’application ne doit pas les libérer tant que les caractéristiques visuelles qu’elles représentent n’ont plus besoin d’être animées, en général lorsque les objets visuels associés sont sur le lieu d’être détruits.</span><span class="sxs-lookup"><span data-stu-id="26874-111">Animation variables are passed as parameters when storyboards are constructed, so the application should not release them until the visual characteristics they represent no longer need to be animated, typically when the associated visual objects are about to be destroyed.</span></span>

## <a name="example-code"></a><span data-ttu-id="26874-112">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="26874-112">Example Code</span></span>

-   [<span data-ttu-id="26874-113">Animer des couleurs</span><span class="sxs-lookup"><span data-stu-id="26874-113">Animating Colors</span></span>](#animating-colors)
-   [<span data-ttu-id="26874-114">Animation des coordonnées x et y</span><span class="sxs-lookup"><span data-stu-id="26874-114">Animating x and y Coordinates</span></span>](#animating-x-and-y-coordinates)

### <a name="animating-colors"></a><span data-ttu-id="26874-115">Animer des couleurs</span><span class="sxs-lookup"><span data-stu-id="26874-115">Animating Colors</span></span>

<span data-ttu-id="26874-116">L’exemple de code suivant provient de MainWindow. cpp dans l’animation Windows Samples animation [pilotée](application-driven-animation-sample.md) par l’application et [animation pilotée par un minuteur](timer-driven-animation-sample.md).</span><span class="sxs-lookup"><span data-stu-id="26874-116">The following example code is taken from MainWindow.cpp in the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Timer-Driven Animation](timer-driven-animation-sample.md).</span></span> <span data-ttu-id="26874-117">Dans l’exemple, trois variables d’animation sont créées à l’aide de [**CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) pour représenter les couleurs d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="26874-117">In the example, three animation variables are created using [**CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) to represent background colors.</span></span> <span data-ttu-id="26874-118">Le code utilise également les méthodes [**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) et [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound) pour contrôler la valeur de la variable d’animation.</span><span class="sxs-lookup"><span data-stu-id="26874-118">The code also uses the [**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) and [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound) methods to control the value of the animation variable.</span></span>


```
const DOUBLE INITIAL_RED = COLOR_MAX;
const DOUBLE INITIAL_GREEN = COLOR_MAX;
const DOUBLE INITIAL_BLUE = COLOR_MAX;

HRESULT hr = m_pAnimationManager->CreateAnimationVariable(
    INITIAL_RED,
    &m_pAnimationVariableRed
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationVariableRed->SetLowerBound(COLOR_MIN);
    if (SUCCEEDED(hr))
    {
        hr = m_pAnimationVariableRed->SetUpperBound(COLOR_MAX);
        if (SUCCEEDED(hr))
        {
            hr = m_pAnimationManager->CreateAnimationVariable(
                INITIAL_GREEN,
                &m_pAnimationVariableGreen
                );
            if (SUCCEEDED(hr))
            {
                hr = m_pAnimationVariableGreen->SetLowerBound(COLOR_MIN);
                if (SUCCEEDED(hr))
                {
                    hr = m_pAnimationVariableGreen->SetUpperBound(COLOR_MAX);
                    if (SUCCEEDED(hr))
                    {
                        hr = m_pAnimationManager->CreateAnimationVariable(
                            INITIAL_BLUE,
                            &m_pAnimationVariableBlue
                            );
                        if (SUCCEEDED(hr))
                        {
                            hr = m_pAnimationVariableBlue->SetLowerBound(COLOR_MIN);
                            if (SUCCEEDED(hr))
                            {
                                hr = m_pAnimationVariableBlue->SetUpperBound(COLOR_MAX);
                            }
                        }
                    }
                }
            }
        }
    }
}
```



<span data-ttu-id="26874-119">Notez les définitions suivantes de MainWindow. h.</span><span class="sxs-lookup"><span data-stu-id="26874-119">Note the following definitions from MainWindow.h.</span></span>


```
class CMainWindow
{

    ...

private:

    // Animated Variables

    IUIAnimationVariable *m_pAnimationVariableRed;
    IUIAnimationVariable *m_pAnimationVariableGreen;
    IUIAnimationVariable *m_pAnimationVariableBlue;

    ...

};
```



### <a name="animating-x-and-y-coordinates"></a><span data-ttu-id="26874-120">Animation des coordonnées x et y</span><span class="sxs-lookup"><span data-stu-id="26874-120">Animating x and y Coordinates</span></span>

<span data-ttu-id="26874-121">L’exemple de code suivant est extrait de thumbnail. cpp dans l' [exemple de présentation](/windows/desktop/UIAnimation/grid-layout-sample)de la grille d’animation Windows. consultez la méthode CMainWindow :: CreateAnimationVariables.</span><span class="sxs-lookup"><span data-stu-id="26874-121">The following example code is taken from Thumbnail.cpp in the Windows Animation [Grid Layout Sample](/windows/desktop/UIAnimation/grid-layout-sample); see the CMainWindow::CreateAnimationVariables method.</span></span> <span data-ttu-id="26874-122">Deux variables d’animation sont créées pour représenter les coordonnées X et Y de chaque objet.</span><span class="sxs-lookup"><span data-stu-id="26874-122">Two animation variables are created to represent the X and Y coordinates of each object.</span></span>


```C++
// Create the animation variables for the x and y coordinates

hr = m_pAnimationManager->CreateAnimationVariable(
    xInitial,
    &m_pAnimationVariableX
    );

if (SUCCEEDED(hr))
{
    hr = m_pAnimationManager->CreateAnimationVariable(
        yInitial,
        &m_pAnimationVariableY
        );

    ...

}
```



<span data-ttu-id="26874-123">Notez les définitions suivantes de thumbnail. h.</span><span class="sxs-lookup"><span data-stu-id="26874-123">Note the following definitions from Thumbnail.h.</span></span>


```
class CThumbnail
{
public:

    ...

    // X and Y Animation Variables

    IUIAnimationVariable *m_pAnimationVariableX;
    IUIAnimationVariable *m_pAnimationVariableY;

    ...

};
```



<span data-ttu-id="26874-124">Les variables d’animation sont des nombres à virgule flottante, mais leurs valeurs peuvent également être extraites en tant qu’entiers.</span><span class="sxs-lookup"><span data-stu-id="26874-124">Animation variables are floating-point numbers, but their values can be fetched as integers, too.</span></span> <span data-ttu-id="26874-125">Par défaut, chaque valeur est arrondie à l’entier le plus proche, mais il est possible de substituer le mode d’arrondi utilisé pour une variable.</span><span class="sxs-lookup"><span data-stu-id="26874-125">By default, each value will be rounded to the nearest integer, but it is possible to override the rounding mode used for a variable.</span></span> <span data-ttu-id="26874-126">L’exemple de code suivant utilise la méthode [**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode) pour spécifier que les valeurs doivent toujours être arrondies à la valeur inférieure.</span><span class="sxs-lookup"><span data-stu-id="26874-126">The following example code uses the [**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode) method to specify that the values should always be rounded down.</span></span>


```C++
hr = m_pAnimationVariableX->SetRoundingMode(
    UI_ANIMATION_ROUNDING_MODE_FLOOR
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationVariableY->SetRoundingMode(
        UI_ANIMATION_ROUNDING_MODE_FLOOR
        );

    ...

}
```



## <a name="previous-step"></a><span data-ttu-id="26874-127">Étape précédente</span><span class="sxs-lookup"><span data-stu-id="26874-127">Previous Step</span></span>

<span data-ttu-id="26874-128">Avant de commencer cette étape, vous devez avoir terminé cette étape : [créer les objets d’animation principaux](adding-animation-to-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="26874-128">Before starting this step, you should have completed this step: [Create the Main Animation Objects](adding-animation-to-an-application.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="26874-129">étape suivante</span><span class="sxs-lookup"><span data-stu-id="26874-129">Next Step</span></span>

<span data-ttu-id="26874-130">À l’issue de cette étape, l’étape suivante est : [mettre à jour le gestionnaire d’animations et dessiner des frames](introducing-windows-animation-manager.md).</span><span class="sxs-lookup"><span data-stu-id="26874-130">After completing this step, the next step is: [Update the Animation Manager and Draw Frames](introducing-windows-animation-manager.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="26874-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="26874-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26874-132">**IUIAnimationManager::CreateAnimationVariable**</span><span class="sxs-lookup"><span data-stu-id="26874-132">**IUIAnimationManager::CreateAnimationVariable**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable)
</dt> <dt>

[<span data-ttu-id="26874-133">**IUIAnimationVariable::SetLowerBound**</span><span class="sxs-lookup"><span data-stu-id="26874-133">**IUIAnimationVariable::SetLowerBound**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound)
</dt> <dt>

[<span data-ttu-id="26874-134">**IUIAnimationVariable::SetRoundingMode**</span><span class="sxs-lookup"><span data-stu-id="26874-134">**IUIAnimationVariable::SetRoundingMode**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)
</dt> <dt>

[<span data-ttu-id="26874-135">**IUIAnimationVariable::SetUpperBound**</span><span class="sxs-lookup"><span data-stu-id="26874-135">**IUIAnimationVariable::SetUpperBound**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)
</dt> <dt>

[<span data-ttu-id="26874-136">Vue d’ensemble des animations Windows</span><span class="sxs-lookup"><span data-stu-id="26874-136">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 