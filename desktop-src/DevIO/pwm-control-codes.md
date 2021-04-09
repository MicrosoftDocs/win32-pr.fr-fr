---
description: Cette rubrique répertorie les IOCTL pour la modulation d’impulsions en largeur.
ms.assetid: 2ED7A06A-A7EC-4C44-AB22-4A52CF2DF2C5
title: Codes de contrôle PWM
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: de7de81b26a1970bbecde76729be2f1c84e6c067
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950440"
---
# <a name="pwm-control-codes"></a>Codes de contrôle PWM

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

Cette rubrique répertorie les IOCTL pour la modulation d’impulsions en largeur.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                                      | Description                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_récupération de \_ la \_ \_ période réelle \_ par le contrôleur PWM IOCTL**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_get_actual_period)<br/>                   | Récupère la période de signal de sortie effective du contrôleur de modulation d’impulsions (PWM) telle qu’elle est mesurée sur ses canaux de sortie.<br/>                                                                                                                                                                                  |
| [**\_informations d' \_ extraction du contrôleur PWM \_ IOCTL \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_get_info)<br/>                                      | Récupère des informations sur un contrôleur de modulation d’impulsions en largeur (PWM). Ces informations ne changent pas après l’initialisation du contrôleur. <br/>                                                                                                                                                                                |
| [**\_période souhaitée de l' \_ \_ ensemble de CONTRÔLEurs PWM IOCTL \_ \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_set_desired_period)<br/>                 | Définit la période de signal de sortie d’un contrôleur de modulation d’impulsions (PWM) sur une valeur suggérée. <br/>                                                                                                                                                                                                                            |
| [**\_pourcentage du \_ \_ cycle d' \_ \_ utilisation \_ \_ du code confidentiel PWM d’IOCTL**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_get_active_duty_cycle_percentage)<br/> | Récupère le pourcentage de cycle de responsabilité actuel pour un pin ou un canal. Le code de contrôle retourne le pourcentage sous la forme d’une structure de [**\_ \_ \_ \_ \_ \_ \_ sortie de pourcentage d’utilisation d’un code confidentiel**](pwm-pin-get-active-duty-cycle-percentage-output.md) .<br/>                                                                                  |
| [**\_pourcentage du \_ cycle \_ de \_ \_ \_ vie \_ du pin PWM d’IOCTL activé**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_set_active_duty_cycle_percentage)<br/> | Définissez la valeur de pourcentage du cycle de responsabilité souhaité pour le code PIN ou le canal du contrôleur. Le code de contrôle spécifie le pourcentage en tant que structure [**\_ \_ \_ \_ \_ \_ \_ d’entrée de pourcentage du cycle de vie actif d’un code confidentiel**](pwm-pin-set-active-duty-cycle-percentage-input.md) . <br/>                                                                      |
| [**\_polarité du \_ code confidentiel PWM \_ d’IOCTL \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_get_polarity)<br/>                                            | Récupère la polarité de signal actuelle du code confidentiel ou du canal. Le code de contrôle obtient la polarité de signal comme une structure de sortie de polarité d’un [**\_ code confidentiel \_ \_ \_**](pwm-pin-get-polarity-output.md) . La polarité de signal est soit active haute, soit faible, comme défini dans l’énumération de [**\_ polarité PWM**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) . <br/> |
| [**\_polarité du \_ jeu de codes confidentiels PWM IOCTL \_ \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_set_polarity)<br/>                                            | Définit la polarité du signal du code PIN ou du canal. Le code de contrôle définit la polarité de signal basée sur une structure [**\_ \_ \_ \_ d’entrée de polarité d’ensemble de codes confidentiels**](/windows/desktop/api/Pwm/ns-pwm-pwm_pin_set_polarity_input) . La polarité de signal est soit active haute, soit faible, comme défini dans l’énumération de [**\_ polarité PWM**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) .<br/>           |
| [**\_démarrage du \_ code confidentiel PWM IOCTL \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_start)<br/>                                                           | Démarre la génération d’un signal de modulation d’impulsions en largeur (PWM) sur un pin ou un canal. Pour vérifier si un code PIN est démarré, utilisez le [**\_ \_ code confidentiel PWM IOCTL \_ \_ démarré**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**).<br/>                                                                                                                                |
| [**\_arrêt du \_ pin \_ PWM IOCTL**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_stop)<br/>                                                             | Arrête la génération du signal de modulation d’impulsions en largeur (PWM) sur un pin ou un canal. Pour vérifier si un code PIN est démarré, utilisez le [**\_ \_ code confidentiel PWM IOCTL \_ \_ démarré**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**).<br/>                                                                                                                                 |
| [**le \_ pin PWM IOCTL \_ \_ est \_ démarré**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_is_started)<br/>                                                | Récupère l’état de génération de signal pour un code confidentiel ou un canal. Chaque code confidentiel a un état Démarré ou arrêté, car la structure de [**\_ sortie du code confidentiel \_ est \_ démarrée \_**](pwm-pin-is-started-output.md) .<br/>                                                                                                                                 |



 

 

 




