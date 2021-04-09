---
description: Cet attribut ajoute l’icône d’élévation du contrôle de compte d’utilisateur (icône bouclier) au contrôle PushButton.
ms.assetid: ec52d660-eb83-4f27-b640-ea89156260aa
title: Attribut ElevationShield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c580beefd1d2c0a80b0ee63b7a44e58a2a2fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115674"
---
# <a name="elevationshield-attribute"></a>Attribut ElevationShield

Cet attribut ajoute l’icône d’élévation du [*contrôle de compte d’utilisateur*](u-gly.md) (icône bouclier) au [contrôle PUSHBUTTON](pushbutton-control.md).

Si ce bit est défini et que l’installation n’est pas encore en cours d’exécution avec des privilèges [*élevés*](e-gly.md) , le contrôle PUSHBUTTON est créé à l’aide de l’icône d’élévation du [*contrôle de compte d’utilisateur*](u-gly.md) (icône bouclier).

Si ce bit est défini et que l’installation est déjà en cours d’exécution avec des privilèges [*élevés*](e-gly.md) , le contrôle PUSHBUTTON est créé à l’aide des autres attributs d’icône.

Si ce bit n’est pas défini, le contrôle PUSHBUTTON est créé à l’aide des autres attributs d’icône.

## <a name="valid-controls"></a>Contrôles valides

[Boutons](pushbutton-control.md)

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                                  |
|---------|-------------|-------------------------------------------|
| 8388608 | 0x00800000  | **msidbControlAttributesElevationShield** |



 

 

 



