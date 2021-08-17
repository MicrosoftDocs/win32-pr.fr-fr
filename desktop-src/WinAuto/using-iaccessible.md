---
title: Utilisation de l’interface IAccessible
description: L’interface IAccessible est une collection de méthodes qui exposent les attributs et les comportements les plus courants d’un large éventail d’éléments d’interface utilisateur.
ms.assetid: 82f6e934-58ea-47f2-98a3-2ab1c20f24c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c683e83928db53894c7c2c22976a5cf58c402c241e698dca5248230b1b24177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744894"
---
# <a name="using-the-iaccessible-interface"></a>Utilisation de l’interface IAccessible

L’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) est une collection de méthodes qui exposent les attributs et les comportements les plus courants d’un large éventail d’éléments d’interface utilisateur. Un élément d’interface utilisateur est un contrôle, tel qu’un menu ou un bouton de commande, qui fait partie de l’interface utilisateur. Un objet accessible est un élément d’interface utilisateur qui a une interface **IAccessible** significative.

Certaines propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ne sont pas applicables à chaque type d’élément d’interface utilisateur. En outre, l’implémentation de **IAccessible** varie d’une application à l’autres.

Bien que les paramètres et les valeurs de retour pour les propriétés et les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) soient entièrement spécifiés, la manière dont un client doit utiliser une propriété ou la manière dont un serveur doit implémenter une propriété est parfois sujette à l’interprétation.

Cette section fournit des suggestions, des instructions et des exemples pour aider les applications clientes à obtenir des informations sur les éléments d’interface utilisateur et à aider les applications serveur à fournir les informations appropriées.

## <a name="in-this-section"></a>Dans cette section

-   [Contenu des propriétés descriptives](content-of-descriptive-properties.md)
-   [Propriétés et méthodes de sélection et de focus](selection-and-focus-properties-and-methods.md)
-   [Propriétés et méthodes de navigation entre les objets](object-navigation-properties-and-methods.md)

 

 




