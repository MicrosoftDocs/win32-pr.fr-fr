---
description: Le type de données Language est une chaîne de texte contenant un ou plusieurs ID de langue numériques valides. S’il existe deux ou plusieurs ID de langue, ceux-ci doivent être séparés par des virgules.
ms.assetid: 547fc662-f055-421e-a621-eecdfa0b13f6
title: Language
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc87cb8b88dc3a693eee6890276adb67ad359e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201468"
---
# <a name="language"></a>Language

Le type de données Language est une chaîne de texte contenant un ou plusieurs ID de langue numériques valides. S’il existe deux ou plusieurs ID de langue, ceux-ci doivent être séparés par des virgules.

Le type de données Language est une valeur 16 bits qui est la combinaison d’ID numériques primaires et de sous-langage. Le LANGID principal comprend les bits de 0 à 9, tandis que l’ID de sous-langue est bits 10 à 15. Pour obtenir la liste des identificateurs numériques primaires et secondaires, consultez la rubrique relative aux [constantes et aux chaînes](../intl/language-identifier-constants-and-strings.md) de l’identificateur de langue.

Pour les ID de langue principaux, la plage 0x200 à 0x3FF est définissable par l’utilisateur. La plage 0x000 à 0x1ff est réservée à l’utilisation du système. Pour les ID de sous-langue, la plage 0x20 à 0x3F est définissable par l’utilisateur. La plage 0x00 à 0x1F est réservée à l’utilisation du système.

 

 
