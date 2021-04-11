---
title: Notes annexes D pour les développeurs Visual Basic
description: Cette section fournit des informations sur Microsoft Active Accessibility pour les développeurs Microsoft Visual Basic.
ms.assetid: 82a016a2-872d-4ba6-ac93-78b59f7ec639
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc09c23a81b2f987a6f651a923dd10b0d16a2a27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939908"
---
# <a name="appendix-d-notes-for-visual-basic-developers"></a>Annexe D : notes pour les développeurs Visual Basic

Cette section fournit des informations sur Microsoft Active Accessibility pour les développeurs Microsoft Visual Basic.

Les applications écrites en Visual Basic sont des clients Microsoft Active Accessibility. Ils ne fournissent pas d’informations sur leurs éléments d’interface utilisateur personnalisés, car ils n’implémentent pas [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ou une autre interface com (Component Object Model).

Cette documentation utilise les noms C/C++ pour les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Toutefois, les noms de Visual Basic sont similaires. Par exemple, la propriété [**IAccessible :: obtenir \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) serait appelée **accName** dans une application Visual Basic.

## <a name="in-this-section"></a>Dans cette section

-   [Remarques sur la méthode Visual Basic : accName](visual-basic-method-notes--accname.md)
-   [Remarques sur la méthode Visual Basic : accValue](visual-basic-method-notes--accvalue.md)
-   [Exemples de programmes Visual Basic](visual-basic-sample-programs.md)

 

 




