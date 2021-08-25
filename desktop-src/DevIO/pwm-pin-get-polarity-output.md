---
description: Contient une valeur de polarité à retourner.
ms.assetid: 432C10EF-AC08-4781-9BCA-A31E0DF12704
title: Structure de PWM_PIN_GET_POLARITY_OUTPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_GET_POLARITY_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 7d4c3103663ceac65deff7744b0cf45a21a787959cc6e866bde5ac8673f7f64a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984429"
---
# <a name="pwm_pin_get_polarity_output-structure"></a>Structure de sortie de la polarité du \_ code confidentiel PWM \_ \_ \_

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

Contient une valeur de polarité à retourner.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PWM_PIN_GET_POLARITY_OUTPUT {
  PWM_POLARITY Polarity;
} PWM_PIN_GET_POLARITY_OUTPUT;
```



## <a name="members"></a>Membres

<dl> <dt>

**Polarité**
</dt> <dd>

Polarité de la broche ou du canal en tant que valeur de [**\_ polarité PWM**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) . La polarité est soit active élevée, soit faible.

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

[**\_polarité du \_ code confidentiel PWM \_ d’IOCTL \_**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_POLARITY**)
</dt> <dt>

[**\_polarité PWM**](/windows/win32/api/pwm/ne-pwm-pwm_polarity)
</dt> </dl>

 

