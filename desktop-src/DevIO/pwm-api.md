---
description: La modulation d’impulsions en largeur (PWM) est la technique de la génération d’une onde d’impulsion rectangulaire qui a une largeur d’impulsion modulée pour produire la variation de la valeur moyenne de la forme d’onde.
ms.assetid: 16B1E46F-2C42-4D94-949E-BE8F53EB1E1E
title: API PWM
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 10b1951d9d96f49a9df9a51604767dbce360f9e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114285"
---
# <a name="pwm-api"></a>API PWM

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

La modulation d’impulsions en largeur (PWM) est la technique de la génération d’une onde d’impulsion rectangulaire qui a une largeur d’impulsion modulée pour produire la variation de la valeur moyenne de la forme d’onde. Les utilisations les plus courantes incluent les moteurs d’asservissement, les voyants de gradation ou d’autres fonctions associées. Le PWM est destiné à être principalement utilisé pour les scénarios de Internet des objets.

## <a name="about-pulse-width-modulation"></a>À propos de la modulation par impulsions de largeur

Une forme d’onde PWM peut être catégorisée par deux paramètres :

-   Une période de forme d’onde (T)

-   Le cycle de l’utilisation, où la fréquence de la forme d’onde (f) est la réciproque de la période f = 1/T

Le cycle de responsabilité décrit la proportion de **la durée d'** / **activité** par rapport à l’intervalle régulier ou à la **période** de temps. Un cycle d’utilisation faible correspond à une puissance moyenne de sortie basse, car l’alimentation est désactivée pour la plupart du temps. Le cycle de l’utilisation est exprimé sous la forme d’un pourcentage. Entièrement sur 100%. La valeur OFF est égale à 0%. La moitié **active** est de 50%.

Les développeurs qui cherchent à implémenter le PWM dans leurs applications IoT doivent examiner la [documentation du PWM WinRT.](/uwp/api/windows.devices.pwm)

## <a name="pulse-width-modulation-types"></a>Types de modulation d’impulsions en largeur

PWM utilise ces codes, [structures](pwm-structures.md)et [énumérations](pwm-enumeration-types.md) de [contrôle d’e/s](pwm-control-codes.md).

Le PWM utilise également la fonction suivante : [**PwmParsePinPath**](/windows-hardware/drivers/ddi/content/pwmutil/nf-pwmutil-pwmparsepinpath).

 

 
