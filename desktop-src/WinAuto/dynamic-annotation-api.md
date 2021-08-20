---
title: API d’annotation dynamique
description: L’API d’annotation dynamique est une extension de Microsoft Active Accessibility qui permet aux développeurs de personnaliser la prise en charge des IAccessible existants sans avoir à utiliser des techniques de sous-classe ou d’encapsulage sujettes aux erreurs.
ms.assetid: 2daf0e76-b300-47e7-994b-d1d00d0dca4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca8b95d1175d4a6bd894e79c55f6798a73165fab2d6e6da40e3b952e68824d50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115319"
---
# <a name="dynamic-annotation-api"></a>API d’annotation dynamique

L’API d’annotation dynamique est une extension de Microsoft Active Accessibility qui permet aux développeurs de personnaliser la prise en charge des [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) existants sans avoir à utiliser des techniques de sous-classe ou d’encapsulage sujettes aux erreurs. Ce mécanisme permet également aux développeurs de transmettre des indications ou d’autres informations utiles aux proxies Oleacc.dll.

L’annotation dynamique est généralement utilisée pour corriger ou modifier une instance inexacte d’un objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) exposé par un proxy Oleacc.dll existant. Par exemple, vous pouvez l’utiliser pour remplacer le [**nom**](name-property.md) et les propriétés de [**rôle**](role-property.md) fournis par le proxy par défaut, et pour fournir la [**Description**](description-property.md) et les propriétés [**d’aide**](help-property.md) (qui peuvent ne pas être fournies par le proxy par défaut).

avec Windows 7, les développeurs peuvent utiliser l’API d’Annotation dynamique pour annoter les propriétés de microsoft UI Automation, ainsi que les propriétés de microsoft Active Accessibility des objets proxy créés par Oleacc.dll pour les contrôles de Windows standard. Les objets proxy Oleacc.dll servent à la fois à des clients Microsoft Active Accessibility et UI Automation.

## <a name="in-this-section"></a>Dans cette section

-   [Informations générales](background-information.md)
-   [Alternatives à l’annotation dynamique](alternatives-to-dynamic-annotation.md)
-   [Types d’annotation dynamique](types-of-dynamic-annotation.md)
-   [Annotation directe](direct-annotation.md)
-   [Annotation de la carte des valeurs](value-map-annotation.md)
-   [Annotation de serveur](server-annotation.md)
-   [Problèmes et limitations](issues-and-limitations.md)

 

 




