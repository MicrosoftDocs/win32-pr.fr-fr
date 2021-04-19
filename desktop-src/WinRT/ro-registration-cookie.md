---
description: Représente les fabriques d’activation inscrites en appelant la fonction RoRegisterActivationFactories.
ms.assetid: D74E5886-45DB-40DE-9740-D14341E78713
title: RO_REGISTRATION_COOKIE (Roapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe9b5242901c1beff4152bc16108976d6f7de275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514613"
---
# <a name="ro_registration_cookie"></a>déborder le \_ cookie d’inscription \_

Représente les fabriques d’activation inscrites en appelant la fonction [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) .


```C++
typedef struct {}* RO_REGISTRATION_COOKIE;
```



## <a name="remarks"></a>Notes

La fonction [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) retourne un **\_ \_ cookie d’inscription Roll** quand les fabriques de classes activables sont inscrites auprès du Windows Runtime. La fonction [**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) utilise le cookie pour supprimer les fabriques de classes.

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

 

 
