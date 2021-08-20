---
description: Méthode StartService de la classe Msvm_SecurityService-démarre le service.
ms.assetid: 59918c15-7216-4cf7-9215-b27532febc72
title: Méthode StartService de la classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e6f21f50600bfa7c666cc722c001b4ea32a6f51f5a63d1982b49d56f1cc0b91e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118146988"
---
# <a name="startservice-method-of-the-msvm_securityservice-class"></a>Méthode StartService de la \_ classe MSVM securityservice

démarre le service.

## <a name="syntax"></a>Syntaxe


```mof
uint32 StartService();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

En cas de réussite, retourne 0 ; Sinon, retourne une erreur.

<dl> <dt>

**Terminé sans erreur** (0)
</dt> <dt>

**Non pris en charge** (1)
</dt> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1703 \[ uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ securityservice**](msvm-securityservice.md)
</dt> </dl>

 

 




