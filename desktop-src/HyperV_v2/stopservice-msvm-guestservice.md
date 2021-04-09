---
description: Arrête le service invité.
ms.assetid: 67FFA46C-0B61-4845-A617-BA10F4D42CBC
title: 'Msvm_GuestService :: StopService, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6c396078e2bd623a768f391a645091679694f453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862362"
---
# <a name="msvm_guestservicestopservice-method"></a>MSVM \_ GuestService :: StopService, méthode

Arrête le service invité.

## <a name="syntax"></a>Syntaxe


```C++
uint32 StopService();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne l’une des valeurs suivantes.



| Code/valeur de retour                                                                                                                                             | Description         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**Terminé sans erreur**</dt> <dt>0</dt> </dl> | Opération réussie.<br/> |
| <dl> <dt>**Non pris en charge**</dt> <dt>1</dt> </dl>           |                     |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                                                 |
| Espace de noms<br/>                | \\\\\\Virtualisation racine \\ v2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ GuestService**](msvm-guestservice.md)
</dt> </dl>

 

 




