---
title: Mètres
description: Mètres
ms.assetid: 11a98d2a-7cdd-4249-bba9-7edc51d7f8b0
keywords:
- mixages audio, contrôles
- mixages audio, mètres
- mélangeurs, contrôles
- mélangeurs, mètres
- contrôles de compteur
- Structure MIXERCONTROLDETAILS_BOOLEAN
- Structure MIXERCONTROLDETAILS_SIGNED
- Structure MIXERCONTROLDETAILS_UNSIGNED
- Contrôle booléen
- contrôle de pointe
- contrôle signé
- contrôle non signé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36f1bebfca22b963e5c1eb6fede3f2786b35199
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368844"
---
# <a name="meters"></a>Mètres

Le compteur contrôle les données de mesure en passant par une ligne audio. Ces contrôles utilisent les structures [**MIXERCONTROLDETAILS \_ Boolean**](/previous-versions//dd757295(v=vs.85)), [**MIXERCONTROLDETAILS \_ signed**](/previous-versions//dd757297(v=vs.85))et [**MIXERCONTROLDETAILS \_ non signées**](/previous-versions//dd757298(v=vs.85)) pour récupérer et définir des propriétés de contrôle. Le tableau suivant décrit les types de compteurs.



| Control  | Description                                                                                                                                            |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Boolean  | Mesure si une valeur entière est FALSe/OFF (zéro) ou TRUE/ON (valeur différente de zéro).                                                                            |
| Peak     | Mesure la déviation de 0 dans les directions positive et négative. La plage de valeurs entières pour le compteur de pic est comprise entre – 32 768 et 32 767. |
| Signé   | Mesure les valeurs entières dans la plage comprise entre – 231 et (231 – 1). Le pilote de mixage définit les limites de ce compteur.                                     |
| Non signé | Mesure les valeurs entières dans la plage comprise entre 0 et (232 – 1). Le pilote de mixage définit les limites de ce compteur.                                        |



 

 

 