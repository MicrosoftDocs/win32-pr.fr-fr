---
description: Le type de données Language est une chaîne de texte contenant un ou plusieurs ID de langue numériques valides. S’il existe deux ou plusieurs ID de langue, ceux-ci doivent être séparés par des virgules.
ms.assetid: 547fc662-f055-421e-a621-eecdfa0b13f6
title: Langage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b98e24ec0ad4d4b42dfcba02374792e10ea117db474a973eae06336a55834538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013127"
---
# <a name="language"></a>Langage

Le type de données Language est une chaîne de texte contenant un ou plusieurs ID de langue numériques valides. S’il existe deux ou plusieurs ID de langue, ceux-ci doivent être séparés par des virgules.

Le type de données Language est une valeur 16 bits qui est la combinaison d’ID numériques primaires et de sous-langage. Le LANGID principal comprend les bits de 0 à 9, tandis que l’ID de sous-langue est bits 10 à 15. Pour obtenir la liste des identificateurs numériques primaires et secondaires, consultez la rubrique relative aux [constantes et aux chaînes](../intl/language-identifier-constants-and-strings.md) de l’identificateur de langue.

Pour les ID de langue principaux, la plage 0x200 à 0x3FF est définissable par l’utilisateur. La plage 0x000 à 0x1ff est réservée à l’utilisation du système. Pour les ID de sous-langue, la plage 0x20 à 0x3F est définissable par l’utilisateur. La plage 0x00 à 0x1F est réservée à l’utilisation du système.

 

 
