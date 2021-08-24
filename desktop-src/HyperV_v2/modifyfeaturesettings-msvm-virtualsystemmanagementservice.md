---
description: Modifie les paramètres de fonctionnalité actuels d’une connexion Ethernet d’ordinateur virtuel.
ms.assetid: 3caa810f-0444-45cf-88a4-e93d04accb46
title: Méthode ModifyFeatureSettings de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: be963ee0bc57ddc0a9570c3ac9b35b1d8dadaeca48d295b45f0134b6c05f632a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694069"
---
# <a name="modifyfeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Méthode ModifyFeatureSettings de la \_ classe VirtualSystemManagementService MSVM

Modifie les paramètres de fonctionnalité actuels d’une connexion Ethernet d’ordinateur virtuel.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ModifyFeatureSettings(
  [in]  string                                        FeatureSettings[],
  [out] Msvm_EthernetSwitchPortFeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FeatureSettings* \[ dans\]
</dt> <dd>

Tableau de chaînes qui contient une instance incorporée d’une classe dérivée de la classe [**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) , qui décrit les modifications apportées aux paramètres de fonctionnalité actuels d’une connexion Ethernet existante. La propriété **InstanceID** de chacune de ces instances identifie les paramètres de fonctionnalité à modifier.

</dd> <dt>

*ResultingFeatureSettings* \[ à\]
</dt> <dd>

Tableau de références aux instances de la classe [**MSVM \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) qui représentent les paramètres de fonctionnalités modifiés.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne l’une des valeurs suivantes.

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
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

