---
title: UiaNameShouldNotContainControlType
description: UiaNameShouldNotContainControlType
ms.assetid: 96F7A5FC-1879-4706-9E67-5B43D57F7281
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6178ca4cd4c4b2ed0deb0070116b597ba3bd1bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839722"
---
# <a name="uianameshouldnotcontaincontroltype"></a>UiaNameShouldNotContainControlType

## <a name="text"></a>Texte

Le nom de l’élément ( {0} ) ne doit pas contenir le texte du ControlType ( {1} )

## <a name="type"></a>Type

Avertissement

## <a name="description"></a>Description

Le nom d’un élément intègre son type de contrôle UIA. Par exemple, cet avertissement peut se produire si la propriété de nom UIA pour un élément avec le type de contrôle Button est définie sur « My Button ».

Ce problème provoque des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car le type de contrôle est lu deux fois, ou il peut être non significatif ou non intuitif pour les utilisateurs.

## <a name="possible-causes"></a>Causes possibles

-   Un nom ou une étiquette n’est pas assigné à l’élément ou à son parent.
-   L’élément ou son parent a un nom par défaut qui n’a pas été révisé à un nom convivial. Par exemple, bouton 1.
-   Un développeur ne sait pas que les lecteurs d’écran lisent les noms et les types de contrôle.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




