---
description: Modifie les paramètres de sécurité actuels d’un ordinateur virtuel.
ms.assetid: b3eedab6-fd69-4c54-a8bf-4e3b77207687
title: Méthode ModifySecuritySettings de la classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.ModifySecuritySettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 47562ac8aac79a8aa4401abd17c667df1917ee38dd2874a4208d46d8de438b05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147238"
---
# <a name="modifysecuritysettings-method-of-the-msvm_securityservice-class"></a>Méthode ModifySecuritySettings de la \_ classe securityservice MSVM

Modifie les paramètres de sécurité actuels d’un ordinateur virtuel.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ModifySecuritySettings(
  [in]  string              SecuritySettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SecuritySettingData* \[ dans\]
</dt> <dd>

Nouvelles données de paramètre de sécurité.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Paramètre facultatif permettant de surveiller la progression de l’opération, qui est utilisé si la méthode n’a pas pu être exécutée de façon synchrone. Si l’opération s’exécute de façon asynchrone, la valeur de retour est 4096.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, retourne 0 ; Sinon, retourne une erreur.

<dl> <dt>

**Terminé sans erreur** (0)
</dt> <dt>

**Non pris en charge** (1)
</dt> <dt>

**Échec** (2)
</dt> <dt>

**Délai d’expiration** (3)
</dt> <dt>

**Paramètre non valide** (4)
</dt> <dt>

**État non valide** (5)
</dt> <dt>

**Paramètres incompatibles** (6)
</dt> <dt>

**DMTF réservé** (..)
</dt> <dt>

**Paramètres de méthode activés-tâche démarrée** (4096)
</dt> <dt>

**Méthode réservée** (4097.. 32767)
</dt> <dt>

**Spécifique au fournisseur** (32768.. 65535)
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

 

 




