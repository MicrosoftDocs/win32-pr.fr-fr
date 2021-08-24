---
description: Configure les paramètres IP des cartes réseau à appliquer à un ordinateur virtuel après un basculement.
ms.assetid: a49d089e-f5dc-4bfb-9f66-2593304b9795
title: Méthode SetFailoverNetworkAdapterSettings de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.SetFailoverNetworkAdapterSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 744c1b2e56fb50e5a0c16db7d03d7558b1ed69360de98f69a4aac795f9f7db63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147762"
---
# <a name="setfailovernetworkadaptersettings-method-of-the-msvm_replicationservice-class"></a>Méthode SetFailoverNetworkAdapterSettings de la \_ classe ReplicationService MSVM

Configure les paramètres IP de la carte réseau à appliquer à un ordinateur virtuel après un basculement. ces paramètres de configuration sont appliqués après une opération de basculement, immédiatement après l’établissement de la communication avec le composant d’intégration KVP Exchange s’exécutant dans le système d’exploitation invité.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetFailoverNetworkAdapterSettings(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 NetworkSettings[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ComputerSystem* \[ dans\]
</dt> <dd>

Référence à une instance [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel dont les cartes réseau doivent être configurées.

</dd> <dt>

*NetworkSettings* \[ dans\]
</dt> <dd>

Tableau d’instances incorporées d’objets [**MSVM \_ FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md) . Chaque instance décrit les paramètres de configuration de l’une des cartes réseau de l’ordinateur virtuel. Les propriétés **adressesIP** et **DHCPEnabled** doivent être spécifiées sur chaque instance.

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

**Paramètres de méthode activés-tâche démarrée** (4096)
</dt> <dt>

**Échec** (32768)
</dt> <dt>

**Accès refusé** (32769)
</dt> <dt>

**Non pris en charge** (32770)
</dt> <dt>

**État inconnu** (32771)
</dt> <dt>

**Délai d’expiration** (32772)
</dt> <dt>

**Paramètre non valide** (32773)
</dt> <dt>

Le **système est en cours d’utilisation** (32774)
</dt> <dt>

**État non valide pour cette opération** (32775)
</dt> <dt>

**Type de données incorrect** (32776)
</dt> <dt>

Le **système n’est pas disponible** (32777)
</dt> <dt>

**Mémoire insuffisante** (32778)
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

[**InitiateFailover**](initiatefailover-msvm-replicationservice.md)
</dt> <dt>

[**MSVM \_ ReplicationService**](msvm-replicationservice.md)
</dt> <dt>

[**RevertFailover**](revertfailover-msvm-replicationservice.md)
</dt> </dl>

 

