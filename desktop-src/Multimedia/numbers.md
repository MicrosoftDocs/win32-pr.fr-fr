---
title: Nombres (Windows Multimedia)
description: Nombres
ms.assetid: d416c4c2-a3e1-45a2-9ae1-82050a5e471b
keywords:
- mixages audio, contrôles
- mixages audio, chiffres
- mélangeurs, contrôles
- mélangeurs, nombres
- contrôles Number
- Structure MIXERCONTROLDETAILS_SIGNED
- Structure MIXERCONTROLDETAILS_UNSIGNED
- contrôle décibel
- contrôle de pourcentage
- contrôle signé
- contrôle non signé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02c4ffd40f1058fae51af3798135840394be918
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102672"
---
# <a name="numbers-windows-multimedia"></a>Nombres (Windows Multimedia)

Les contrôles Number permettent à l’utilisateur d’entrer des données numériques associées à une ligne. Les données numériques sont exprimées en tant qu’entiers signés, entiers non signés ou valeurs de décibels entières. Ces contrôles utilisent les structures [**\_ non signées**](/previous-versions//dd757298(v=vs.85)) [**MIXERCONTROLDETAILS \_ signées**](/previous-versions//dd757297(v=vs.85)) et MIXERCONTROLDETAILS pour récupérer et définir des propriétés de contrôle. Le tableau suivant décrit les types de contrôles Number.



| Contrôler  | Description                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| Signé   | Autorise les valeurs entières entrées dans la plage comprise entre – 231 et (231 – 1).                                                               |
| Non signé | Autorise les valeurs entières entrées dans la plage comprise entre 0 et (232 – 1).                                                                   |
| Décibel  | Permet d’entrer des valeurs entières de décibels, en dixièmes de décibels. La plage de valeurs pour ce contrôle est comprise entre – 32 768 et 32 767. |
| Pourcentage  | Permet d’entrer des valeurs sous forme de pourcentages.                                                                                         |



 

 

 
