---
description: Si ce bit est défini, les images de la boîte de dialogue sont créées avec la palette personnalisée (une par boîte de dialogue reçue à partir du premier contrôle créé). Si le bit n’est pas défini, les images sont rendues à l’aide d’une palette par défaut.
ms.assetid: 9cfc7fd9-27a3-4208-b42c-48369890a74b
title: UseCustomPalette bit de style de boîte de dialogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 507ed1c900c564e3e791f4d0bbc5f8658798fdb4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009605"
---
# <a name="usecustompalette-dialog-style-bit"></a>UseCustomPalette bit de style de boîte de dialogue

Si ce bit est défini, les images de la boîte de dialogue sont créées avec la palette personnalisée (une par boîte de dialogue reçue à partir du premier contrôle créé). Si le bit n’est pas défini, les images sont rendues à l’aide d’une palette par défaut.

En général, vous définissez ce bit si la boîte de dialogue contient une image avec une palette spéciale, ou plusieurs images partageant une palette personnalisée. Le bit ne doit pas être défini si la boîte de dialogue contient plusieurs images avec différentes palettes. Dans ce cas, la palette par défaut est susceptible d’obtenir un résultat satisfaisant pour toutes les images.

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                                  |
|---------|-------------|-------------------------------------------|
| 64      | 0x00000040  | **msidbDialogAttributesUseCustomPalette** |



 

 

 



