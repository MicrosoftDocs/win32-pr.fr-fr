---
title: DuplicateSiblingNames
description: DuplicateSiblingNames
ms.assetid: 4E9FFD16-EAC0-4778-8DEB-D179E2197411
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d18f0e04ed0b2aba3b0637ca8535e2ca5a18110ee29edb397fc250944035f895
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115329"
---
# <a name="duplicatesiblingnames"></a>DuplicateSiblingNames

## <a name="text"></a>Texte

Le nom frère dupliqué et le rôle \\ " {0} \\ " lèvent une ambiguïté entre les éléments.

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

Un élément a le même nom et le même rôle/ControlType qu’un autre élément.

Ce problème peut entraîner une confusion, car les lecteurs d’écran lisent le même texte pour tous les éléments portant le même nom et le même rôle/ControlType.

## <a name="possible-causes"></a>Causes possibles

-   Le nom de l’élément contient le texte Role/ControlType.
-   Le nom de l’élément ou le nom de son parent n’est pas défini ou n’est pas défini correctement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IAccessible :: \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Propriété Name](name-property.md)
</dt> <dt>

[**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement.CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




