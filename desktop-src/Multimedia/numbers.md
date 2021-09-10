---
title: nombres (Windows multimédia)
description: À l’aide de nombres
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368852"
---
# <a name="numbers-windows-multimedia"></a>nombres (Windows multimédia)

Les contrôles Number permettent à l’utilisateur d’entrer des données numériques associées à une ligne. Les données numériques sont exprimées en tant qu’entiers signés, entiers non signés ou valeurs de décibels entières. Ces contrôles utilisent les structures [**\_ non signées**](/previous-versions//dd757298(v=vs.85)) [**MIXERCONTROLDETAILS \_ signées**](/previous-versions//dd757297(v=vs.85)) et MIXERCONTROLDETAILS pour récupérer et définir des propriétés de contrôle. Le tableau suivant décrit les types de contrôles Number.



| Control  | Description                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| Signé   | Autorise les valeurs entières entrées dans la plage comprise entre – 231 et (231 – 1).                                                               |
| Non signé | Autorise les valeurs entières entrées dans la plage comprise entre 0 et (232 – 1).                                                                   |
| Décibel  | Permet d’entrer des valeurs entières de décibels, en dixièmes de décibels. La plage de valeurs pour ce contrôle est comprise entre – 32 768 et 32 767. |
| Pourcentage  | Permet d’entrer des valeurs sous forme de pourcentages.                                                                                         |



 

 

 
