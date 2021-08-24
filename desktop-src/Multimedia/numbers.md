---
title: nombres (Windows multimédia)
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
ms.openlocfilehash: 21c9e1bacdea3f52129d78eea2f0bc7134df08b7077c83510bd8de824777e524
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806619"
---
# <a name="numbers-windows-multimedia"></a>nombres (Windows multimédia)

Les contrôles Number permettent à l’utilisateur d’entrer des données numériques associées à une ligne. Les données numériques sont exprimées en tant qu’entiers signés, entiers non signés ou valeurs de décibels entières. Ces contrôles utilisent les structures [**\_ non signées**](/previous-versions//dd757298(v=vs.85)) [**MIXERCONTROLDETAILS \_ signées**](/previous-versions//dd757297(v=vs.85)) et MIXERCONTROLDETAILS pour récupérer et définir des propriétés de contrôle. Le tableau suivant décrit les types de contrôles Number.



| Contrôler  | Description                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| Signé   | Autorise les valeurs entières entrées dans la plage comprise entre – 231 et (231 – 1).                                                               |
| Non signé | Autorise les valeurs entières entrées dans la plage comprise entre 0 et (232 – 1).                                                                   |
| Décibel  | Permet d’entrer des valeurs entières de décibels, en dixièmes de décibels. La plage de valeurs pour ce contrôle est comprise entre – 32 768 et 32 767. |
| Pourcentage  | Permet d’entrer des valeurs sous forme de pourcentages.                                                                                         |



 

 

 
