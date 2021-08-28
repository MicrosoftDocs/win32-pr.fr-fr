---
title: UiaNameLengthTooLong
description: UiaNameLengthTooLong
ms.assetid: 01AF3F1E-9A3F-48B4-8219-6E80BAFC82EE
keywords:
- Identificateur UIA_NamePropertyId AutomationElement. NameProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eec235897680cde3b024a67745b923e989cfc68db3b154be260c9dcd3510ba10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993969"
---
# <a name="uianamelengthtoolong"></a>UiaNameLengthTooLong

## <a name="text"></a>Texte

Le nom de l’élément ne doit pas retourner une chaîne de plus de {0} caractères

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

Le nom d’un élément contient trop de caractères. Par exemple, la méthode [**IUIAutomationElement :: CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) utilisée pour récupérer le nom UIA d’un élément retourne une chaîne supérieure à la limite.

Ce problème provoque des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car un élément peut avoir un nom non significatif et non intuitif.

## <a name="possible-causes"></a>Causes possibles

Un nom ou une étiquette n’est pas assigné à l’élément ou à son parent.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




