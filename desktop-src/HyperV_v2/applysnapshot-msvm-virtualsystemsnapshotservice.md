---
description: Applique un instantané d’ordinateur virtuel à la machine virtuelle à partir de laquelle il a été créé.
ms.assetid: 45f1ec8f-aa96-4060-8f8c-0471d0ad4a21
title: Méthode ApplySnapshot de la classe Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 735e827935689a0f0ede7fbac1d582ea40772ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865222"
---
# <a name="applysnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a>Méthode ApplySnapshot de la \_ classe VirtualSystemSnapshotService MSVM

Applique un instantané d’ordinateur virtuel à la machine virtuelle à partir de laquelle il a été créé.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ApplySnapshot(
  [in]  CIM_VirtualSystemSettingData REF Snapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Instantané* \[ dans\]
</dt> <dd>

Référence à une classe dérivée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) qui représente la capture instantanée d’ordinateur virtuel à appliquer.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Cette opération est toujours exécutée de façon asynchrone. Cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

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

**Type non valide** (6)
</dt> <dt>

**DMTF réservé** (..)
</dt> <dt>

**Paramètres de méthode activés-tâche démarrée** (4096)
</dt> <dt>

**Accès refusé** (32769)
</dt> <dt>

**Paramètre non valide** (32773)
</dt> <dt>

**État non valide** (32775)
</dt> <dt>

**Méthode réservée** (4097.. 32767)
</dt> <dt>

**Spécifique au fournisseur** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ VirtualSystemSnapshotService**](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[**ApplyVirtualSystemSnapshot (v1)**](/previous-versions/windows/desktop/virtual/applyvirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> <dt>

[**ApplyVirtualSystemSnapshotEx (v1)**](/previous-versions/windows/desktop/virtual/msvm-virtualsystemmanagementservice-applyvirtualsystemsnapshotex)
</dt> </dl>

 

