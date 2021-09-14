---
title: Lire les valeurs de la variable d’animation
description: Chaque fois que votre application peint, elle doit lire les valeurs actuelles des variables d’animation qui représentent les caractéristiques visuelles à animer.
ms.assetid: 7abf084a-31f5-4e32-bfd1-e88fbc2bf63d
keywords:
- variables d’animation Windows animation, lecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16187547bb3efd99a2f45a8fcc0668a6b6603efe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192467"
---
# <a name="read-the-animation-variable-values"></a>Lire les valeurs de la variable d’animation

Chaque fois que votre application peint, elle doit lire les valeurs actuelles des variables d’animation qui représentent les caractéristiques visuelles à animer.

## <a name="overview"></a>Vue d’ensemble

Lors du dessin d’un frame, une application peut utiliser la méthode [**IUIAnimationVariable :: GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) ou [**IUIAnimationVariable :: GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) pour demander les valeurs de toutes les variables d’animation qui affecteront les visuels dans le frame. Il est possible d’insérer une variable d’animation sur une plage de valeurs ([**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) et [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)), et de demander que sa valeur soit arrondie à un entier à l’aide d’un schéma d’arrondi ([**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)) spécifié.

Au lieu de lire les valeurs de toutes les variables pour chaque frame, une application peut utiliser la méthode [**IUIAnimationVariable :: SetVariableChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariablechangehandler) ou [**IUIAnimationVariable :: SetVariableIntegerChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler) pour inscrire un ou plusieurs gestionnaires de modification de variable afin de recevoir des notifications uniquement en cas de modification de la valeur des variables ([**IUIAnimationVariableChangeHandler :: OnValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged)) ou de la valeur arrondie ([**IUIAnimationVariableIntegerChangeHandler :: OnIntegerValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged)). Pour identifier les variables passées aux gestionnaires de modification de variable, une application peut appliquer des balises à des variables à l’aide de la méthode [**IUIAnimationVariable :: SetTag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-settag) . Il s’agit d’objets (IUnknown \* ), de paires d’entiers qui sont interprétées par l’application.

## <a name="example-code"></a>Exemple de code

l’exemple de code suivant provient de Thumbnail. cpp dans l’exemple de présentation de la [grille](/windows/desktop/UIAnimation/grid-layout-sample)Windows Animation ; consultez la méthode CMainWindow :: Render. Elle utilise la méthode [**GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) pour lire les valeurs en tant que valeurs à virgule flottante.


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



l’exemple de code suivant est extrait de MainWindow. cpp dans l’exemple d' [animation pilotée par un](timer-driven-animation-sample.md)exemple d’animation Windows. consultez la méthode CMainWindow ::D rawBackground. Elle utilise la méthode [**GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) pour lire les valeurs sous la forme de valeurs entières.


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



## <a name="previous-step"></a>Étape précédente

Avant de commencer cette étape, vous devez avoir terminé cette étape : [mettre à jour le gestionnaire d’animations et dessiner des frames](introducing-windows-animation-manager.md).

## <a name="next-step"></a>étape suivante

À l’issue de cette étape, l’étape suivante consiste à [créer une table de montage séquentiel et à ajouter des transitions](updating---timer-driven-animation.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IUIAnimationVariable::GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue)
</dt> <dt>

[**IUIAnimationVariable :: GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue)
</dt> <dt>

[Windows Vue d’ensemble de l’animation](scenic-animation-api-overview.md)
</dt> </dl>

 

 