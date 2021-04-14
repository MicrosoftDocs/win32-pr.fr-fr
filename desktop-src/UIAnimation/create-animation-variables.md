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
# <a name="create-animation-variables"></a>Créer des variables d’animation

Une application doit créer une variable d’animation pour chaque caractéristique visuelle qui doit être animée à l’aide de l’animation Windows.

## <a name="overview"></a>Vue d’ensemble

Les variables d’animation sont créées à l’aide du gestionnaire d’animations, et l’application doit conserver une référence à chaque fois que cela est nécessaire. En général, votre application crée chaque variable d’animation en même temps que l’objet visuel qu’elle anime.

Quand une variable d’animation est créée, sa valeur initiale doit être spécifiée. Par la suite, sa valeur ne peut être modifiée qu’en planifiant des storyboards qui l’animent.

Les variables d’animation sont passées en tant que paramètres lors de la construction des storyboards. par conséquent, l’application ne doit pas les libérer tant que les caractéristiques visuelles qu’elles représentent n’ont plus besoin d’être animées, en général lorsque les objets visuels associés sont sur le lieu d’être détruits.

## <a name="example-code"></a>Exemple de code

-   [Animer des couleurs](#animating-colors)
-   [Animation des coordonnées x et y](#animating-x-and-y-coordinates)

### <a name="animating-colors"></a>Animer des couleurs

L’exemple de code suivant provient de MainWindow. cpp dans l’animation Windows Samples animation [pilotée](application-driven-animation-sample.md) par l’application et [animation pilotée par un minuteur](timer-driven-animation-sample.md). Dans l’exemple, trois variables d’animation sont créées à l’aide de [**CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) pour représenter les couleurs d’arrière-plan. Le code utilise également les méthodes [**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) et [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound) pour contrôler la valeur de la variable d’animation.


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



Notez les définitions suivantes de MainWindow. h.


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



### <a name="animating-x-and-y-coordinates"></a>Animation des coordonnées x et y

L’exemple de code suivant est extrait de thumbnail. cpp dans l' [exemple de présentation](/windows/desktop/UIAnimation/grid-layout-sample)de la grille d’animation Windows. consultez la méthode CMainWindow :: CreateAnimationVariables. Deux variables d’animation sont créées pour représenter les coordonnées X et Y de chaque objet.


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



Notez les définitions suivantes de thumbnail. h.


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



Les variables d’animation sont des nombres à virgule flottante, mais leurs valeurs peuvent également être extraites en tant qu’entiers. Par défaut, chaque valeur est arrondie à l’entier le plus proche, mais il est possible de substituer le mode d’arrondi utilisé pour une variable. L’exemple de code suivant utilise la méthode [**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode) pour spécifier que les valeurs doivent toujours être arrondies à la valeur inférieure.


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



## <a name="previous-step"></a>Étape précédente

Avant de commencer cette étape, vous devez avoir terminé cette étape : [créer les objets d’animation principaux](adding-animation-to-an-application.md).

## <a name="next-step"></a>étape suivante

À l’issue de cette étape, l’étape suivante est : [mettre à jour le gestionnaire d’animations et dessiner des frames](introducing-windows-animation-manager.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IUIAnimationManager::CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable)
</dt> <dt>

[**IUIAnimationVariable::SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound)
</dt> <dt>

[**IUIAnimationVariable::SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)
</dt> <dt>

[**IUIAnimationVariable::SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)
</dt> <dt>

[Vue d’ensemble des animations Windows](scenic-animation-api-overview.md)
</dt> </dl>

 

 