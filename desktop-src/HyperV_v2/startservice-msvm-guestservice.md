---
description: Met le service invité dans un état Démarré.
ms.assetid: 1DC6A5B3-0F91-4AC1-99D5-0E8CF5ED35A2
title: 'Msvm_GuestService :: StartService, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 52f3f05eef622940e0fb1a9645a66097a8930fac9a236f432d5471c4ee20c208
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050399"
---
# <a name="msvm_guestservicestartservice-method"></a>MSVM \_ GuestService :: StartService, méthode

Met le service invité dans un état Démarré.

## <a name="syntax"></a>Syntaxe


```C++
uint32 StartService();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne l’une des valeurs suivantes.



| Code/valeur de retour                                                                                                                                             | Description         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**Terminé sans erreur**</dt> <dt>0</dt> </dl> | Réussite.<br/> |
| <dl> <dt>**Non pris en charge**</dt> <dt>1</dt> </dl>           |                     |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                                 |
| Espace de noms<br/>                | \\\\\\Virtualisation racine \\ v2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ GuestService**](msvm-guestservice.md)
</dt> </dl>

 

 




