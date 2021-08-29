---
description: Tente d’envoyer un code de contrôle défini par l’utilisateur à un service géré par un pilote système.
ms.assetid: 62e66c35-f264-43d0-9e94-fb5e85f936e0
ms.tgt_platform: multiple
title: Méthode UserControlService de la classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e64d4493e43e23b6826c81ac61ae90d64a236d7ffcace32bb29f53b5c0c039fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105059"
---
# <a name="usercontrolservice-method-of-the-win32_systemdriver-class"></a>Méthode UserControlService de la \_ classe Win32 SystemDriver

La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UserControlService** tente d’envoyer un code de contrôle défini par l’utilisateur à un service géré par un pilote système.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ControlCode* \[ dans\]
</dt> <dd>

Spécifie des valeurs définies (de 128 à 255) qui fournissent des commandes de contrôle spécifiques à un utilisateur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur 0 (zéro) si la demande **UserControlService** a été acceptée, 1 (un) si la demande n’est pas prise en charge, et tout autre nombre pour indiquer une erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_SystemDriver Win32**](win32-systemdriver.md)
</dt> </dl>

 

