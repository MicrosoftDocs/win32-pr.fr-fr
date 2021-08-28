---
title: Notes annexes D pour les développeurs Visual Basic
description: cette section fournit des informations sur microsoft Active Accessibility pour les développeurs microsoft Visual Basic.
ms.assetid: 82a016a2-872d-4ba6-ac93-78b59f7ec639
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a857aeb8e04a0648d991e26913f9a9cf5c35328c62ed3f1ac3903a267e5a4e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122419"
---
# <a name="appendix-d-notes-for-visual-basic-developers"></a>annexe D : Notes pour les développeurs Visual Basic

cette section fournit des informations sur microsoft Active Accessibility pour les développeurs microsoft Visual Basic.

les Applications écrites en Visual Basic sont des clients Microsoft Active Accessibility. Ils ne fournissent pas d’informations sur leurs éléments d’interface utilisateur personnalisés, car ils n’implémentent pas [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ou une autre interface com (Component Object Model).

Cette documentation utilise les noms C/C++ pour les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . toutefois, les noms de Visual Basic sont similaires. par exemple, la propriété [**IAccessible :: obtenir \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) serait appelée **accName** dans une application Visual Basic.

## <a name="in-this-section"></a>Dans cette section

-   [Visual Basic Remarques sur la méthode : accName](visual-basic-method-notes--accname.md)
-   [Visual Basic Remarques sur la méthode : accValue](visual-basic-method-notes--accvalue.md)
-   [Visual Basic Exemples de programmes](visual-basic-sample-programs.md)

 

 




