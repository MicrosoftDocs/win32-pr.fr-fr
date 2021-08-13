---
description: Lance la restauration automatique pour un ordinateur virtuel de récupération.
ms.assetid: F4AE1911-46B2-4412-A17F-3CA7D388276F
title: 'Msvm_ReplicationService :: InitiateFailback, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.InitiateFailback
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b573cf1a0347e8df55b239451d9b99f3d416ebd5b3d0d61e662b6023f07a5b2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118644945"
---
# <a name="msvm_replicationserviceinitiatefailback-method"></a>MSVM \_ ReplicationService :: InitiateFailback, méthode

Lance la restauration automatique pour un ordinateur virtuel de récupération.

## <a name="syntax"></a>Syntaxe


```C++
uint32 InitiateFailback(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [in]  string                 RecoveryPointIdentifier,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ComputerSystem* \[ dans\]
</dt> <dd>

Référence à une instance [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel pour lequel lancer une restauration automatique.

</dd> <dt>

*ReplicationSettingData* \[ dans\]
</dt> <dd>

Représentation sous forme de chaîne d’une instance incorporée de la classe [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) qui définit les paramètres de réplication pour la restauration automatique.

</dd> <dt>

*RecoveryPointIdentifier* \[ dans\]
</dt> <dd>

Entrée facultative qui identifie le point de récupération sur lequel la restauration automatique est demandée.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)). Cette référence peut être utilisée pour surveiller la progression et pour obtenir le résultat de la méthode.

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
</dt> <dt>

**Fichier introuvable** (32779)
</dt> </dl>

## <a name="remarks"></a>Remarques

**InitiateFailback** fonctionne sur une machine virtuelle de récupération et prend l’ordinateur virtuel à l’état *WaitingForFailback* . **InitiateFailback** transmet la requête de restauration automatique au fournisseur correspondant, qui resynchronise le point de récupération du nouveau côté principal. Une fois la restauration automatique du point de récupération demandé terminée, l’état de réplication passe à l’état *FailbackCompleted* .

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

[**MSVM \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

