---
title: Sélection des objets enfants
description: Les clients appellent la méthode IAccessible accSelect pour modifier la sélection ou le focus clavier parmi les enfants d’un objet. Les constantes SELFLAG spécifiées avec l’appel définissent l’opération à effectuer.
ms.assetid: 5e7ad1e9-b1b2-4e76-93e8-b58251930621
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc15ab48a42be44c62c8c7bc2b9151158875509a2e43010c5da70830b2f2973
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133682"
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

 

 




