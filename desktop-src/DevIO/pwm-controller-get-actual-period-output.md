---
description: Contient la période de signal de sortie effective pour un contrôleur de modulation d’impulsions (PWM).
ms.assetid: 280F564F-FF7F-4121-B726-9F9AF9E98EB7
title: Structure de PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: f63057299a8ef37ed1b38151958d2e0061ad2727
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748341"
---
# <a name="pwm_controller_get_actual_period_output-structure"></a>Structure de sortie de la récupération de la \_ \_ \_ \_ période réelle \_ du contrôleur PWM

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

Contient la période de signal de sortie effective pour un contrôleur de modulation d’impulsions (PWM).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT {
  PWM_PERIOD ActualPeriod;
} PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT;
```



## <a name="members"></a>Membres

<dl> <dt>

**ActualPeriod**
</dt> <dd>

La période de signal de sortie effective telle qu’elle sera mesurée sur les canaux de sortie du contrôleur.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ uniquement\]<br/>                                             |
| Version KMDF minimale<br/>     | 1,19<br/>                                                                                  |
| Version UMDF minimale<br/>     | 2.19<br/>                                                                                  |
| En-tête<br/>                   | <dl> <dt>PWM. h (include PWM. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_récupération de \_ la \_ \_ période réelle \_ par le contrôleur PWM IOCTL**](https://www.bing.com/search?q=**IOCTL\_PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD**)
</dt> </dl>

 

 




