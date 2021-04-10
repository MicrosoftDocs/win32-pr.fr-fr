---
title: API d’annotation dynamique
description: L’API d’annotation dynamique est une extension de Microsoft Active Accessibility qui permet aux développeurs de personnaliser la prise en charge des IAccessible existants sans avoir à utiliser des techniques de sous-classe ou d’encapsulage sujettes aux erreurs.
ms.assetid: 2daf0e76-b300-47e7-994b-d1d00d0dca4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7f73c1da79784fdd86652128b572fd81904023c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940338"
---
# <a name="dynamic-annotation-api"></a>API d’annotation dynamique

L’API d’annotation dynamique est une extension de Microsoft Active Accessibility qui permet aux développeurs de personnaliser la prise en charge des [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) existants sans avoir à utiliser des techniques de sous-classe ou d’encapsulage sujettes aux erreurs. Ce mécanisme permet également aux développeurs de transmettre des indications ou d’autres informations utiles aux proxies Oleacc.dll.

L’annotation dynamique est généralement utilisée pour corriger ou modifier une instance inexacte d’un objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) exposé par un proxy Oleacc.dll existant. Par exemple, vous pouvez l’utiliser pour remplacer le [**nom**](name-property.md) et les propriétés de [**rôle**](role-property.md) fournis par le proxy par défaut, et pour fournir la [**Description**](description-property.md) et les propriétés [**d’aide**](help-property.md) (qui peuvent ne pas être fournies par le proxy par défaut).

Avec Windows 7, les développeurs peuvent utiliser l’API d’annotation dynamique pour annoter les propriétés de Microsoft UI Automation, ainsi que les propriétés de Active Accessibility de Microsoft des objets proxy que Oleacc.dll crée pour les contrôles Windows standard. Les objets proxy Oleacc.dll servent à la fois à des clients Microsoft Active Accessibility et UI Automation.

## <a name="in-this-section"></a>Dans cette section

-   [Informations générales](background-information.md)
-   [Alternatives à l’annotation dynamique](alternatives-to-dynamic-annotation.md)
-   [Types d’annotation dynamique](types-of-dynamic-annotation.md)
-   [Annotation directe](direct-annotation.md)
-   [Annotation de la carte des valeurs](value-map-annotation.md)
-   [Annotation de serveur](server-annotation.md)
-   [Problèmes et limitations](issues-and-limitations.md)

 

 




