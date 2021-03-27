---
description: Une application peut récupérer des métriques de police pour une police physique uniquement après que la police a été sélectionnée dans un contexte de périphérique.
ms.assetid: 3eaabc8b-e244-4b65-918b-a20043afa535
title: Unité et unités de conception
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb52a671727a2fa84d5514b469be5bd320f3318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863661"
---
# <a name="device-vs-design-units"></a>Unité et unités de conception

Une application peut récupérer des métriques de police pour une police physique uniquement après que la police a été sélectionnée dans un contexte de périphérique. Lorsqu’une police est sélectionnée dans un contexte de périphérique, elle est mise à l’échelle pour l’appareil. Les métriques de police spécifiques à l’appareil sont appelées unités de périphérique.

Les métriques portables dans les polices sont appelées unités de conception. Pour appliquer à un appareil spécifié, les unités de conception doivent être converties en unités de périphérique. Utilisez la formule suivante pour convertir les unités de conception en unités de périphérique.

*DeviceUnits* = (*DesignUnits* / *unitsPerEm*) \* (*pointer*/72) \* *DeviceResolution*

Les variables de cette formule ont les significations suivantes.



| Variable           | Description                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *DeviceUnits*      | Spécifie la métrique de police *DesignUnits* convertie en unités de périphérique. Cette valeur est dans les mêmes unités que la valeur spécifiée pour *DeviceResolution*.                          |
| *DesignUnits*      | Spécifie la métrique de police à convertir en unités de périphérique. Cette valeur peut être n’importe quelle mesure de police, y compris la largeur d’un caractère ou la valeur de l’ascendeur pour une police entière. |
| *unitsPerEm*       | Spécifie la taille du carré em de la police.                                                                                                                                 |
| *PointSize*        | Spécifie la taille de la police, en points. (Un point est égal à 1/72 de pouce.)                                                                                                 |
| *DeviceResolution* | Spécifie le nombre d’unités de l’appareil (en pixels) par pouce. Les valeurs standard peuvent être 300 pour une imprimante laser ou 96 pour un écran VGA.                                                |



 

Cette formule ne doit pas être utilisée pour reconvertir les unités de périphérique en unités de conception. Les unités de périphérique sont toujours arrondies au pixel le plus proche. L’erreur d’arrondi propagée peut devenir très importante, en particulier lorsqu’une application utilise des tailles d’écran.

Pour demander des unités de conception, créez une police logique dont la hauteur est spécifiée en tant que *unitsPerEm*. Les applications peuvent récupérer la valeur de *unitsPerEm* en appelant la fonction [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) et en vérifiant le membre **ntmSizeEM** de la structure [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) .

 

 



