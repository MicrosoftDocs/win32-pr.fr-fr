---
title: Faders
description: Faders
ms.assetid: 2ca6be9f-9825-44d9-99c1-abcf6f0b42f7
keywords:
- mixages audio, contrôles
- mixages audio, faders
- mélangeurs, contrôles
- mélangeurs, faders
- faders
- Structure MIXERCONTROLDETAILS_UNSIGNED
- contrôle de l’atténuation du volume
- contrôle de fondu du volume de basses
- contrôle de fondu du volume des aigus
- contrôle d’égaliseur graphique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2b560b61a694089b947b0cfda7a54b486f1e3a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195356"
---
# <a name="faders"></a>Faders

Les contrôles d’atténuation sont généralement des contrôles verticaux qui peuvent être ajustés ou réduits. Ces contrôles ont une échelle linéaire et utilisent la [**structure \_ non signée MIXERCONTROLDETAILS**](/previous-versions//dd757298(v=vs.85)) pour récupérer et définir les détails du contrôle. Le tableau suivant décrit les types de faders.



| Control   | Description                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Émission     | Contrôle d’atténuation général. La plage de valeurs acceptables est comprise entre 0 et 65 535.                                                                                                                                                                                                                                                                                                                                       |
| Volume    | Contrôle général de l’atténuation du volume. La plage de valeurs acceptables est comprise entre 0 et 65 535. Pour plus d’informations sur la modification de cette plage, consultez la documentation de votre appareil de mixage.                                                                                                                                                                                                                                        |
| Graves      | Contrôle de fondu du volume de basses. La plage de valeurs acceptables est comprise entre 0 et 65 535. Les limites de la bande de fréquence des basses sont spécifiques au matériel. Pour plus d’informations sur les limites de bande, consultez la documentation de votre appareil de mixage.                                                                                                                                                                                      |
| Les aigus    | Contrôle de fondu des volumes aigus. La plage de valeurs acceptables est comprise entre 0 et 65 535. Les limites de la bande de fréquence des aigus sont spécifiques au matériel. Pour plus d’informations sur les limites de bande, consultez la documentation de votre appareil de mixage.                                                                                                                                                                              |
| Equalizer | Contrôle d’égaliseur graphique. La plage de valeurs acceptables pour une bande de l’égaliseur est comprise entre 0 et 65 535. Le nombre de bandes d’égaliseur et leurs limites sont spécifiques au matériel. Pour plus d’informations sur l’égaliseur, consultez la documentation de votre appareil de mixage. Vous pouvez utiliser la structure [**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85)) pour récupérer des étiquettes de texte pour l’égaliseur. |



 

 

 