---
title: Erreur de rôle ARIA pour les éléments avec gestionnaires d’événements
description: Erreur de rôle ARIA pour les éléments avec gestionnaires d’événements
ms.assetid: 20BB874A-874B-4266-9C7B-49C07D4146DA
keywords:
- AriaContainerRoleErrorMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cebaa2e6f4526d0a1e820e60adc1d28439d3f361c7ffb58a0c4d855861ea46d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133992"
---
# <a name="aria-role-error-for-elements-with-event-handlers"></a>Erreur de rôle ARIA pour les éléments avec gestionnaires d’événements

## <a name="text"></a>Texte

L’élément a un gestionnaire d’événements mais le rôle WAI-ARIA valide n’est pas défini.

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

Cette erreur s’applique aux éléments qui ne disposent pas d’une initiative d’accessibilité Web implicite, accessible via le rôle WAI-ARIA.

Cette erreur indique qu’un élément a un gestionnaire d’événements de souris ou de clavier (**clic**, **MouseDown**, **MouseUp**, **MouseMove**, **mouseout**, **MouseOver**, **KeyUp**, **keyverser** ou **touche**), mais ne dispose pas de l’attribut de [**rôle**](https://developer.mozilla.org/docs/Web/HTML/Reference) défini et ne fait pas partie des balises HTML qui ont un rôle WAI-ARIA implicite (par exemple, **un, un** **bouton**, **img**, **entrée**, **Sélectionner**

La définition de l’attribut [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) pour les éléments interactifs qui n’ont pas de rôle implicite (par exemple, une balise **div** ) est nécessaire pour exposer les modèles de comportement de l’élément aux lecteurs d’écran et autres technologies d’assistance.

Pour corriger cette erreur, définissez l’attribut de [**rôle**](https://developer.mozilla.org/docs/Web/HTML/Reference) sur un rôle WAI-ARIA valide qui correspond au mieux aux modèles de comportement de cet élément et aux attributs requis. Par exemple, si une balise **div** fonctionne comme un bouton, affectez à l’attribut Role la valeur « Button ».

## <a name="example"></a>Exemple


```HTML
<!-- Setting role attribute allows screen readers to know it can be clicked -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




