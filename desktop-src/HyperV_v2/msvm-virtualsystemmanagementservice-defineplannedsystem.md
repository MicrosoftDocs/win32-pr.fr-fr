---
description: Définit un système virtuel planifié.
ms.assetid: f129554b-e43e-4c3a-8418-d5d810f4c4b5
title: Méthode DefinePlannedSystem de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DefinePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 398f0c11f748cb9dc4865cb1ccb94f24409bda104bbcb55ec00ffde62a17188b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117810484"
---
# <a name="defineplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Méthode DefinePlannedSystem de la \_ classe VirtualSystemManagementService MSVM

Définit un système virtuel planifié.

L’entrée qui n’est pas complètement spécifiée peut être remplie avec des valeurs par défaut.

## <a name="syntax"></a>Syntaxe


```mof
uint32 DefinePlannedSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SystemSettings* \[ dans\]
</dt> <dd>

Paramètres système du système virtuel.

</dd> <dt>

*ResourceSettings* \[ dans\]
</dt> <dd>

Paramètres de ressource pour le système virtuel.

</dd> <dt>

*ReferenceConfiguration* \[ dans\]
</dt> <dd>

[**\_ VirtualSystemSettingData CIM**](cim-virtualsystemsettingdata.md) contenant la configuration de référence.

</dd> <dt>

*ResultingSystem* \[ à\]
</dt> <dd>

Un [**\_ ComputerSystem CIM**](cim-computersystem.md) contenant le système résultant.

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

 

