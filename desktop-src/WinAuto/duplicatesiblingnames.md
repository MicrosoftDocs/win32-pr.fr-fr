---
title: DuplicateSiblingNames
description: DuplicateSiblingNames
ms.assetid: 4E9FFD16-EAC0-4778-8DEB-D179E2197411
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aed5a7caeadc34519988fe8a4a1f12ec4e05ce13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675874"
---
# <a name="duplicatesiblingnames"></a>DuplicateSiblingNames

## <a name="text"></a>Texte

Le nom frère dupliqué et le rôle \\ " {0} \\ " lèvent une ambiguïté entre les éléments.

## <a name="type"></a>Type

Error

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

 

 




