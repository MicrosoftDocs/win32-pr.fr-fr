---
title: Sélection des objets enfants
description: Les clients appellent la méthode IAccessible accSelect pour modifier la sélection ou le focus clavier parmi les enfants d’un objet. Les constantes SELFLAG spécifiées avec l’appel définissent l’opération à effectuer.
ms.assetid: 5e7ad1e9-b1b2-4e76-93e8-b58251930621
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d6f898f7da7beb047d3e781ad46cf383b3dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309497"
---
# <a name="selecting-child-objects"></a>Sélection des objets enfants

Les clients appellent la méthode [**IAccessible :: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) pour modifier la sélection ou le focus clavier parmi les enfants d’un objet. Les [constantes SELFLAG](selflag.md) spécifiées avec l’appel définissent l’opération à effectuer.

Si [**IAccessible :: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) est appelé avec l’indicateur [**SELFLAG \_ TAKEFOCUS**](selflag.md) sur un objet enfant qui a un **HWND**, l’indicateur prend effet uniquement si le parent de l’objet a le focus.

## <a name="performing-complex-selection-operations"></a>Exécution d’opérations de sélection complexes

Les éléments suivants décrivent les valeurs SELFLAG à spécifier lors de l’appel de [**IAccessible :: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) pour effectuer des opérations de sélection complexes.

**Pour simuler un clic**

-   [**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ TAKESELECTION**](selflag.md)

**Pour sélectionner un élément cible en simulant CTRL + clic**

-   [**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ ADDSELECTION**](selflag.md)

**Pour annuler la sélection d’un élément cible en simulant CTRL + clic**

-   [**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ REMOVESELECTION**](selflag.md)

**Pour simuler MAJ + clic**

-   [**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ EXTENDSELECTION**](selflag.md)

**Pour sélectionner une plage d’objets et placer le focus sur le dernier objet**

1.  Spécifiez [**SELFLAG \_ TAKEFOCUS**](selflag.md) sur l’objet de départ pour définir l’ancre de sélection.
2.  Appelez à nouveau [**IAccessible :: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) et spécifiez [**SELFLAG \_ EXTENDSELECTION**](selflag.md) \| [**SELFLAG \_ TAKEFOCUS**](selflag.md) sur le dernier objet.

**Pour désélectionner tous les objets**

1.  Spécifiez [**SELFLAG \_ TAKESELECTION**](selflag.md) sur n’importe quel objet. Cet indicateur Désélectionne tous les objets sélectionnés, à l’exception de ceux que vous venez de sélectionner.
2.  Appelez à nouveau [**IAccessible :: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) et spécifiez [**SELFLAG \_ REMOVESELECTION**](selflag.md) sur l’objet restant.

 

 




