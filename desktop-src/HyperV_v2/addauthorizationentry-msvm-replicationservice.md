---
description: Ajoute une entrée d’autorisation à un serveur de récupération.
ms.assetid: edc11c5b-b1a1-45e0-a920-2f1f1b0b8779
title: Méthode AddAuthorizationEntry de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.AddAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 51df804e2d65733904889e2214b8d6702d30f5e14c1885ac989e70642cb9a4f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822959"
---
# <a name="addauthorizationentry-method-of-the-msvm_replicationservice-class"></a>Méthode AddAuthorizationEntry de la \_ classe ReplicationService MSVM

Ajoute une entrée d’autorisation à un serveur de récupération. Ces entrées sont utilisées pour autoriser les connexions au serveur de récupération.

## <a name="syntax"></a>Syntaxe


```mof
uint32 AddAuthorizationEntry(
  [in]  string              AuthorizationEntry,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*AuthorizationEntry* \[ dans\]
</dt> <dd>

Représentation sous forme de chaîne d’une instance de la classe [**MSVM \_ ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) qui définit l’entrée d’autorisation à ajouter.

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
</dt> <dt>

**Fichier introuvable** (32779)
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

[**ModifyAuthorizationEntry**](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[**RemoveAuthorizationEntry**](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[**SetAuthorizationEntry**](setauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[**MSVM \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

