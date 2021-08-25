---
title: Contenu des propriétés descriptives
description: L’interface IAccessible fournit des propriétés descriptives, qui décrivent les différents aspects d’un objet.
ms.assetid: e6c1d1a3-417d-4aea-abac-f84a55f666b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7073d44478d3e7236a56828898346499922ab5e16e401489e54a41b61d7637e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860639"
---
# <a name="content-of-descriptive-properties"></a>Contenu des propriétés descriptives

L’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) fournit des propriétés descriptives, qui décrivent les différents aspects d’un objet. Certaines de ces propriétés sont spécifiques au contenu. le contenu des autres propriétés est constitué d’un texte descriptif fourni par le serveur. Le type d’informations pour chaque propriété varie en fonction de l’objet.

Les rubriques suivantes décrivent les informations que les clients obtiennent à partir de ces propriétés. Ils fournissent également aux serveurs des suggestions pour le choix du contenu.

-   [Propriété Name](name-property.md)
-   [Role, propriété](role-property.md)
-   [Propriété State](state-property.md)
-   [Propriété Value](value-property.md)
-   [Description, propriété](description-property.md)
-   [Help, propriété](help-property.md)
-   [Propriété HelpTopic](helptopic-property.md)
-   [Propriété KeyboardShortcut](keyboardshortcut-property.md)
-   [DefaultAction, propriété](defaultaction-property.md)

Lors de la conception d’objets accessibles, les développeurs de serveurs doivent également consulter les rubriques suivantes :

-   [Choix des propriétés à prendre en charge](choosing-which-properties-to-support.md)
-   [Choix du contenu pour les propriétés descriptives](choosing-the-content-for-descriptive-properties.md)

Pour plus d’informations sur les paramètres et les valeurs de retour de ces propriétés, consultez la section [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de la référence Microsoft Active Accessibility [C/C++](c-c---reference.md).

 

 




