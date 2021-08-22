---
description: Ajoute des sources de démarrage à une configuration de système virtuel lorsqu’elle est appliquée à une &\# 0034 ; état&\# 0034 ; configuration du système virtuel.
ms.assetid: 2d091554-73d4-47c6-a0c2-97644fc9abe9
title: Méthode AddBootSourceSettings de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddBootSourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d52333f3118caa1cf437fabb536bb62f84b99dab01b3115e7f6a65c3f182a17e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148072"
---
# <a name="addbootsourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Méthode AddBootSourceSettings de la \_ classe VirtualSystemManagementService MSVM

Ajoute des sources de démarrage à une configuration de système virtuel lorsqu’elle est appliquée à une configuration de système virtuel « État ».

## <a name="syntax"></a>Syntaxe


```mof
uint32 AddBootSourceSettings(
  [in]  CIM_VirtualSystemSettingData REF AffectedConfiguration,
  [in]  string                           BootSourceSettings[],
  [out] CIM_SettingData              REF ResultingBootSourceSettings[],
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*AffectedConfiguration* \[ dans\]
</dt> <dd>

[**\_ VirtualSystemSettingData CIM**](cim-virtualsystemsettingdata.md) contenant la configuration affectée.

</dd> <dt>

*BootSourceSettings* \[ dans\]
</dt> <dd>

Tableau contenant les paramètres de la source de démarrage.

</dd> <dt>

*ResultingBootSourceSettings* \[ à\]
</dt> <dd>

En cas de réussite, retourne un [**\_ SettingData CIM**](cim-settingdata.md) avec les paramètres de source de démarrage résultants.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, retourne 0 ou 4096 ; Sinon, retourne une erreur.

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
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

