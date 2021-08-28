---
description: Représente les fabriques d’activation inscrites en appelant la fonction RoRegisterActivationFactories.
ms.assetid: D74E5886-45DB-40DE-9740-D14341E78713
title: RO_REGISTRATION_COOKIE (Roapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8efc7d3364f02c11750e6b42ddec6d2a3dee3f83368d277bc979a22ea3a0854a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741596"
---
# <a name="ro_registration_cookie"></a>déborder le \_ cookie d’inscription \_

Représente les fabriques d’activation inscrites en appelant la fonction [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) .


```C++
typedef struct {}* RO_REGISTRATION_COOKIE;
```



## <a name="remarks"></a>Remarques

la fonction [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) retourne un **\_ \_ COOKIE d’inscription roll** quand les fabriques de classes activables sont inscrites auprès du Windows Runtime. La fonction [**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) utilise le cookie pour supprimer les fabriques de classes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Roapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories)
</dt> <dt>

[**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories)
</dt> </dl>

 

 
