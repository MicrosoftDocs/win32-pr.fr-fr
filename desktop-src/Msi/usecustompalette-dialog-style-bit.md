---
description: Si ce bit est défini, les images de la boîte de dialogue sont créées avec la palette personnalisée (une par boîte de dialogue reçue à partir du premier contrôle créé). Si le bit n’est pas défini, les images sont rendues à l’aide d’une palette par défaut.
ms.assetid: 9cfc7fd9-27a3-4208-b42c-48369890a74b
title: UseCustomPalette bit de style de boîte de dialogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9863f9b20ad85caf3712c3cfa00fd88de72f82b947a329d367d06f02ba06163
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809479"
---
# <a name="usecustompalette-dialog-style-bit"></a>UseCustomPalette bit de style de boîte de dialogue

Si ce bit est défini, les images de la boîte de dialogue sont créées avec la palette personnalisée (une par boîte de dialogue reçue à partir du premier contrôle créé). Si le bit n’est pas défini, les images sont rendues à l’aide d’une palette par défaut.

En général, vous définissez ce bit si la boîte de dialogue contient une image avec une palette spéciale, ou plusieurs images partageant une palette personnalisée. Le bit ne doit pas être défini si la boîte de dialogue contient plusieurs images avec différentes palettes. Dans ce cas, la palette par défaut est susceptible d’obtenir un résultat satisfaisant pour toutes les images.

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                                  |
|---------|-------------|-------------------------------------------|
| 64      | 0x00000040  | **msidbDialogAttributesUseCustomPalette** |



 

 

 



