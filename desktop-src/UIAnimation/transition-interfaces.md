---
title: Interfaces de transition
description: cette section contient les spécifications de référence pour les interfaces du gestionnaire d’animations Windows qui prennent en charge les transitions.
ms.assetid: 581C853D-F213-4227-AC61-4ED2E5D4EF04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5791de6e2ca148e42ef836c8bb9be2d9dc96304df00a856b1bc036e05fca3fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119418599"
---
# <a name="transition-interfaces"></a>Interfaces de transition

cette section contient les spécifications de référence pour les interfaces du gestionnaire d’animations Windows qui prennent en charge les transitions.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                     | Description                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAnimationInterpolator**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator)<br/>                                   | Définit des méthodes pour créer un interpolateur personnalisé.<br/>                                                                                                                                                                                                             |
| [**IUIAnimationInterpolator2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator2)<br/>                                 | Étend l’interface [**IUIAnimationInterpolator**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator) qui définit des méthodes pour la création d’un interpolateur personnalisé. [**IUIAnimationInterpolator2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator2) prend en charge l’interpolation dans une dimension donnée. <br/>        |
| [**IUIAnimationPrimitiveInterpolation**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprimitiveinterpolation)<br/>               | Définit une méthode qui permet à un interpolateur personnalisé de fournir des informations de transition, sous la forme d’une courbe polynomiale cubique, au gestionnaire d’animations.<br/>                                                                                                        |
| [**IUIAnimationTransition**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition)<br/>                                       | Définit une transition qui détermine la manière dont une variable d’animation change dans le temps.<br/>                                                                                                                                                                             |
| [**IUIAnimationTransition2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition2)<br/>                                     | Étend l’interface [**IUIAnimationTransition**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition) qui définit une transition. Une transition [**IUIAnimationTransition2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition2) détermine la manière dont une variable d’animation change dans le temps dans une dimension donnée.<br/> |
| [**IUIAnimationTransitionFactory**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory)<br/>                         | Définit une méthode pour créer des transitions à partir d’interpolateurs personnalisés.<br/>                                                                                                                                                                                            |
| [**IUIAnimationTransitionFactory2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory2)<br/>                       | Définit une méthode pour créer des transitions à partir d’interpolateurs personnalisés.<br/>                                                                                                                                                                                            |
| [**IUIAnimationTransitionLibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)<br/>                         | Définit une bibliothèque de transitions standard. <br/>                                                                                                                                                                                                                     |
| [**IUIAnimationTransitionLibrary2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary2)<br/>                       | Définit une bibliothèque de transitions standard pour une dimension spécifiée.<br/>                                                                                                                                                                                            |
| [**IUIAnimationVariable**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariable)<br/>                                           | Définit une variable d’animation, qui représente un élément visuel qui peut être animé.<br/>                                                                                                                                                                          |
| [**IUIAnimationVariable2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariable2)<br/>                                         | Définit une variable d’animation, qui représente un élément visuel qui peut être animé dans plusieurs dimensions.<br/>                                                                                                                                                   |
| [**IUIAnimationVariableChangeHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablechangehandler)<br/>                 | Définit une méthode pour gérer les événements liés aux mises à jour des variables d’animation.<br/>                                                                                                                                                                                     |
| [**IUIAnimationVariableChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablechangehandler2)<br/>               | Définit une méthode pour gérer les événements de mise à jour des variables d’animation. [**IUIAnimationVariableChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablechangehandler2) gère les événements qui se produisent dans une dimension spécifiée.<br/>                                                            |
| [**IUIAnimationVariableIntegerChangeHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariableintegerchangehandler)<br/>   | Définit une méthode pour gérer les événements de mise à jour des variables d’animation.<br/>                                                                                                                                                                                                 |
| [**IUIAnimationVariableIntegerChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariableintegerchangehandler2)<br/> | Définit une méthode pour gérer les événements de mise à jour des variables d’animation. [**IUIAnimationVariableIntegerChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariableintegerchangehandler2) gère les événements qui se produisent dans une dimension spécifiée.<br/>                                              |
| [**IUIAnimationVariableCurveChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablecurvechangehandler2)<br/>     | Définit une méthode pour gérer les événements de mise à jour de la courbe d’animation. <br/>                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interfaces](windows-animation-reference.md)
</dt> </dl>

 

 





