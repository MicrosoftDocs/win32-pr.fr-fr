---
description: Vue d’ensemble de l’utilisation d’Active Accessibility pour exposer du texte.
ms.assetid: c04ade90-5f17-4e16-b82b-c99230000954
title: Utilisation de Active Accessibility pour exposer du texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d475a8c576e109f47be7b5a3d61cddf543038d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516863"
---
# <a name="using-active-accessibility-to-expose-text"></a>Utilisation de Active Accessibility pour exposer du texte

Les applications peuvent utiliser Microsoft Active Accessibility pour exposer du texte. Toutefois, l’interface [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible) définie par les versions antérieures de Active Accessibility n’est pas optimisée pour exposer de grandes quantités de texte enrichi. Les versions ultérieures définissent des interfaces qui sont optimisées pour exposer de grandes quantités de texte et d’attributs textuels.

Pour exposer un texte de grandes quantités, créez des objets COM (Component Object Model) distincts qui prennent en charge [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible), ou éléments enfants, pour représenter chaque exécution de texte. Une exécution est une ligne ou une partie d’une ligne qui partage la même mise en forme.

Active Accessibility expose uniquement le texte et son emplacement, mais n’a aucun mécanisme pour exposer la mise en forme du texte. Malgré ces limitations, certains programmes utilisent Active Accessibility pour exposer du texte. Par exemple, Microsoft Internet Explorer et Microsoft Visual Studio utilisent tous les deux Active Accessibility pour exposer de grandes quantités de texte.

Pour plus d’informations sur l’exposition de texte à l’aide de Active Accessibility, consultez [accessibilité](../accessibility/accessibility.md).

 

 
