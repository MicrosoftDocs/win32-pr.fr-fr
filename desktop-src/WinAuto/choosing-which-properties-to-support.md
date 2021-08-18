---
title: Choix des propriétés à prendre en charge
description: Les propriétés IAccessible permettent aux développeurs de serveurs de décrire un large éventail d’éléments d’interface utilisateur.
ms.assetid: c51fd8a1-dc23-4d64-8921-e0a795c3ffb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76a3c9ef5d56c6d963a05ac84b5e2cacafde488c377ebcc73fa1e2c4be1adab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133962"
---
# <a name="choosing-which-properties-to-support"></a>Choix des propriétés à prendre en charge

Les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) permettent aux développeurs de serveurs de décrire un large éventail d’éléments d’interface utilisateur. Toutefois, les propriétés ne sont pas toutes applicables pour chaque type d’élément d’interface utilisateur. En outre, certaines propriétés fournissent des informations descriptives qui sont utiles, mais pas essentielles.

Les serveurs doivent prendre en charge les propriétés et méthodes suivantes pour chaque objet :

-   [**Nom**](name-property.md)
-   [**Rôle**](role-property.md)
-   [**Département**](state-property.md)
-   [**Emplacement**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) et [ **IAccessible :: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**Parent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) et [ **IAccessible :: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

Les propriétés et la méthode suivantes doivent être prises en charge si elles s’appliquent à l’objet :

-   [**KeyboardShortcut**](keyboardshortcut-property.md)
-   [**Valeur**](value-property.md)

Les propriétés et la méthode suivantes doivent être prises en charge si l’objet a des enfants :

-   [**Enfant**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) et [ **ChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [**Focus, sélection**](selection-and-focus-properties-and-methods.md)et [ **IAccessible :: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

Les propriétés suivantes sont facultatives, mais fournissent des informations descriptives utiles sur l’objet. La propriété [**Description**](description-property.md) est implémentée pour décrire des bitmaps et d’autres images.

-   [**Description**](description-property.md)
-   [**Nœuds DefaultAction**](defaultaction-property.md) et [ **IAccessible :: accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)
-   [**Aide**](help-property.md)
-   [**HelpTopic**](helptopic-property.md)

 

 




