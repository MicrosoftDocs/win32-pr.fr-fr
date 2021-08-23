---
description: Contient un pourcentage de cycle de responsabilité souhaité pour un pin ou un canal dans un contrôleur de modulation d’impulsions en largeur (PWM).
ms.assetid: CA699703-2D9B-4841-99AD-9C27FF428394
title: Structure de PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: ca6b2ee6aa4d4d2da3f94aa7cc471de12c1f8040b597edf568bf061c8e392aa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758849"
---
# <a name="pwm_pin_set_active_duty_cycle_percentage_input-structure"></a>\_ \_ \_ \_ \_ \_ Structure d’entrée en pourcentage du cycle de vie \_ de l’épinglage activé

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

Contient un pourcentage de cycle de responsabilité souhaité pour un pin ou un canal dans un contrôleur de modulation d’impulsions en largeur (PWM).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT {
  PWM_PERCENTAGE Percentage;
} PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT;
```



## <a name="members"></a>Membres

<dl> <dt>

**Percentage**
</dt> <dd>

Cycle de vie de signal PWM souhaité, en tant que \_ pourcentage PWM, qui est une valeur ULONGLONG.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                                             |
| Version KMDF minimale<br/>     | 1,19<br/>                                                                                  |
| Version UMDF minimale<br/>     | 2.19<br/>                                                                                  |
| En-tête<br/>                   | <dl> <dt>PWM. h (include PWM. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_pourcentage du \_ cycle \_ de \_ \_ \_ vie \_ du pin PWM d’IOCTL activé**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




