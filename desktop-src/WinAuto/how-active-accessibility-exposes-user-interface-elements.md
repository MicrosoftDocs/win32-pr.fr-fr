---
title: Comment Active Accessibility expose les éléments d’interface utilisateur
description: Microsoft Active Accessibility crée un objet proxy pour chaque élément de l’interface utilisateur qu’il expose.
ms.assetid: 64aa8fac-cea7-4466-ae34-2760956c296b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b450ebe79aa467100fe9b6fb3bc4cdfb5540b60c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196761"
---
# <a name="how-active-accessibility-exposes-user-interface-elements"></a>Comment Active Accessibility expose les éléments d’interface utilisateur

Microsoft Active Accessibility crée un objet *proxy* pour chaque élément de l’interface utilisateur qu’il expose. Un objet proxy joue le rôle d’intermédiaire entre l’utilitaire client et l’élément d’interface utilisateur. L’objectif de l’objet proxy est de surveiller l’étendue de la durée de vie de l’élément d’interface utilisateur et d’implémenter les propriétés et les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour le compte de l’élément d’interface utilisateur. Les développeurs de serveurs qui créent des contrôles personnalisés ou d’autres éléments d’interface utilisateur personnalisés doivent également créer des objets proxy. Pour plus d’informations, consultez [création d’objets proxy](creating-proxy-objects.md).

Lorsque Microsoft Active Accessibility crée un objet pour exposer un contrôle prédéfini ou commun, il crée en fait au moins deux objets : un pour le contrôle et un pour la fenêtre qui entoure le contrôle. Dans la plupart des cas, ces fenêtres parentes possèdent la [propriété Role](role-property.md) de la [**\_ \_ fenêtre système Role**](object-roles.md) et ont les mêmes [propriété Name](name-property.md) et Name Class Name que le contrôle. Les informations sur le contrôle que les clients transmettent aux utilisateurs finaux sont contenues dans l’objet que Microsoft Active Accessibility crée pour exposer le contrôle, et non l’objet parent qui expose la fenêtre qui entoure le contrôle.

Pour plus d'informations, consultez les rubriques ci-dessous.

-   [Filtrage des objets inutiles](screening-out-unnecessary-objects.md)
-   [Fourniture de la propriété Name](providing-the-name-property.md)
-   [S’assurer que les éléments d’interface utilisateur sont correctement nommés](ensure-that-ui-elements-are-named-correctly.md)
-   [Éléments d’interface utilisateur non pris en charge](unsupported-user-interface-elements.md)

 

 




