---
title: Lire les valeurs de la variable d’animation
description: Chaque fois que votre application peint, elle doit lire les valeurs actuelles des variables d’animation qui représentent les caractéristiques visuelles à animer.
ms.assetid: 7abf084a-31f5-4e32-bfd1-e88fbc2bf63d
keywords:
- variables d’animation Windows animation, lecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16187547bb3efd99a2f45a8fcc0668a6b6603efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512742"
---
# <a name="read-the-animation-variable-values"></a><span data-ttu-id="8e37b-104">Lire les valeurs de la variable d’animation</span><span class="sxs-lookup"><span data-stu-id="8e37b-104">Read the Animation Variable Values</span></span>

<span data-ttu-id="8e37b-105">Chaque fois que votre application peint, elle doit lire les valeurs actuelles des variables d’animation qui représentent les caractéristiques visuelles à animer.</span><span class="sxs-lookup"><span data-stu-id="8e37b-105">Each time your application paints, it should read the current values of the animation variables that represent the visual characteristics to be animated.</span></span>

## <a name="overview"></a><span data-ttu-id="8e37b-106">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="8e37b-106">Overview</span></span>

<span data-ttu-id="8e37b-107">Lors du dessin d’un frame, une application peut utiliser la méthode [**IUIAnimationVariable :: GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) ou [**IUIAnimationVariable :: GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) pour demander les valeurs de toutes les variables d’animation qui affecteront les visuels dans le frame.</span><span class="sxs-lookup"><span data-stu-id="8e37b-107">When drawing a frame, an application can use the [**IUIAnimationVariable::GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) or [**IUIAnimationVariable::GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) method to request the values of any animation variables that will affect visuals within the frame.</span></span> <span data-ttu-id="8e37b-108">Il est possible d’insérer une variable d’animation sur une plage de valeurs ([**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) et [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)), et de demander que sa valeur soit arrondie à un entier à l’aide d’un schéma d’arrondi ([**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)) spécifié.</span><span class="sxs-lookup"><span data-stu-id="8e37b-108">It is possible to clip an animation variable to a range of values ([**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) and [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)), and to request its value be rounded to an integer using a specified rounding scheme ([**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)).</span></span>

<span data-ttu-id="8e37b-109">Au lieu de lire les valeurs de toutes les variables pour chaque frame, une application peut utiliser la méthode [**IUIAnimationVariable :: SetVariableChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariablechangehandler) ou [**IUIAnimationVariable :: SetVariableIntegerChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler) pour inscrire un ou plusieurs gestionnaires de modification de variable afin de recevoir des notifications uniquement en cas de modification de la valeur des variables ([**IUIAnimationVariableChangeHandler :: OnValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged)) ou de la valeur arrondie ([**IUIAnimationVariableIntegerChangeHandler :: OnIntegerValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged)).</span><span class="sxs-lookup"><span data-stu-id="8e37b-109">Instead of reading the values of all variables for every frame, an application can use the [**IUIAnimationVariable::SetVariableChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariablechangehandler) or [**IUIAnimationVariable::SetVariableIntegerChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler) method to register one or more variable change handlers to receive notifications only when there is a change to the variables' value ([**IUIAnimationVariableChangeHandler::OnValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged)) or rounded value ([**IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged)).</span></span> <span data-ttu-id="8e37b-110">Pour identifier les variables passées aux gestionnaires de modification de variable, une application peut appliquer des balises à des variables à l’aide de la méthode [**IUIAnimationVariable :: SetTag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-settag) .</span><span class="sxs-lookup"><span data-stu-id="8e37b-110">To identify the variables passed to variable change handlers, an application can apply tags to variables using the [**IUIAnimationVariable::SetTag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-settag) method.</span></span> <span data-ttu-id="8e37b-111">Il s’agit d’objets (IUnknown \* ), de paires d’entiers qui sont interprétées par l’application.</span><span class="sxs-lookup"><span data-stu-id="8e37b-111">These are object (IUnknown\*), integer pairs that are interpreted by the application.</span></span>

## <a name="example-code"></a><span data-ttu-id="8e37b-112">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="8e37b-112">Example Code</span></span>

<span data-ttu-id="8e37b-113">L’exemple de code suivant est extrait de thumbnail. cpp dans l’exemple de [Présentation](/windows/desktop/UIAnimation/grid-layout-sample)de la grille Windows animation ; consultez la méthode CMainWindow :: Render.</span><span class="sxs-lookup"><span data-stu-id="8e37b-113">The following example code is taken from Thumbnail.cpp in the Windows Animation sample [Grid Layout](/windows/desktop/UIAnimation/grid-layout-sample); see the CMainWindow::Render method.</span></span> <span data-ttu-id="8e37b-114">Elle utilise la méthode [**GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) pour lire les valeurs en tant que valeurs à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="8e37b-114">It uses the [**GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) method to read the values as floating-point values.</span></span>


```C++
// Get the x-coordinate and y-coordinate animation variable values

DOUBLE x=0;
hr = m_pAnimationVariableX->GetValue(&x);
if (SUCCEEDED(hr))
{
    DOUBLE y=0;
    hr = m_pAnimationVariableY->GetValue(&y);
    if (SUCCEEDED(hr))
    {
        // Draw the object

        ...

    }
}
```



<span data-ttu-id="8e37b-115">L’exemple de code suivant est extrait de MainWindow. cpp dans l’exemple d' [animation pilotée par une](timer-driven-animation-sample.md)Animation Windows. consultez la méthode CMainWindow ::D rawBackground.</span><span class="sxs-lookup"><span data-stu-id="8e37b-115">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see the CMainWindow::DrawBackground method.</span></span> <span data-ttu-id="8e37b-116">Elle utilise la méthode [**GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) pour lire les valeurs sous la forme de valeurs entières.</span><span class="sxs-lookup"><span data-stu-id="8e37b-116">It uses the [**GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) method to read the values as integer values.</span></span>


```C++
// Get the RGB animation variable values

INT32 red;
HRESULT hr = m_pAnimationVariableRed->GetIntegerValue(
    &red
    );
if (SUCCEEDED(hr))
{
    INT32 green;
    hr = m_pAnimationVariableGreen->GetIntegerValue(
        &green
        );
    if (SUCCEEDED(hr))
    {
        INT32 blue;
        hr = m_pAnimationVariableBlue->GetIntegerValue(
            &blue
            );
        if (SUCCEEDED(hr))
        {
            // Set the RGB of the background brush to the new animated value

            ...
                
            // Paint the background

            ...

        }
    }

    ...

}
```



## <a name="previous-step"></a><span data-ttu-id="8e37b-117">Étape précédente</span><span class="sxs-lookup"><span data-stu-id="8e37b-117">Previous Step</span></span>

<span data-ttu-id="8e37b-118">Avant de commencer cette étape, vous devez avoir terminé cette étape : [mettre à jour le gestionnaire d’animations et dessiner des frames](introducing-windows-animation-manager.md).</span><span class="sxs-lookup"><span data-stu-id="8e37b-118">Before starting this step, you should have completed this step: [Update the Animation Manager and Draw Frames](introducing-windows-animation-manager.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="8e37b-119">étape suivante</span><span class="sxs-lookup"><span data-stu-id="8e37b-119">Next Step</span></span>

<span data-ttu-id="8e37b-120">À l’issue de cette étape, l’étape suivante consiste à [créer une table de montage séquentiel et à ajouter des transitions](updating---timer-driven-animation.md).</span><span class="sxs-lookup"><span data-stu-id="8e37b-120">After completing this step, the next step is: [Create a Storyboard and Add Transitions](updating---timer-driven-animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e37b-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8e37b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e37b-122">**IUIAnimationVariable::GetIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="8e37b-122">**IUIAnimationVariable::GetIntegerValue**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue)
</dt> <dt>

[<span data-ttu-id="8e37b-123">**IUIAnimationVariable :: GetValue**</span><span class="sxs-lookup"><span data-stu-id="8e37b-123">**IUIAnimationVariable::GetValue**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue)
</dt> <dt>

[<span data-ttu-id="8e37b-124">Vue d’ensemble des animations Windows</span><span class="sxs-lookup"><span data-stu-id="8e37b-124">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 