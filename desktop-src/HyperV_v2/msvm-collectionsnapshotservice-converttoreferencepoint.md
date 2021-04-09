---
description: Convertit une capture instantanée de collection existante en collection de points de référence. La collection d’instantanés est supprimée en tant qu’effet secondaire. Seuls les instantanés de récupération peuvent être convertis en points de référence.
ms.assetid: 6b304782-9e5e-43b1-af7d-08617d65850c
title: Méthode ConvertToReferencePoint de la classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ConvertToReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 810761b67303ad33ced6fdaef857c96f65365091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869085"
---
# <a name="converttoreferencepoint-method-of-the-msvm_collectionsnapshotservice-class"></a>Méthode ConvertToReferencePoint de la \_ classe CollectionSnapshotService MSVM

Convertit une capture instantanée de collection existante en collection de points de référence. La collection d’instantanés est supprimée en tant qu’effet secondaire. Seuls les instantanés de récupération peuvent être convertis en points de référence.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ConvertToReferencePoint(
  [in]      Msvm_SnapshotCollection       REF AffectedSnapshotCollection,
  [in, out] Msvm_ReferencePointCollection REF ResultingReferencePointCollection,
  [out]     CIM_ConcreteJob               REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*AffectedSnapshotCollection* \[ dans\]
</dt> <dd>

Référence à un [**\_ SnapshotCollection MSVM**](msvm-snapshotcollection.md) contenant la collection d’instantanés du système virtuel affectée.

</dd> <dt>

*ResultingReferencePointCollection* \[ in, out\]
</dt> <dd>

Référence à un [**\_ ReferencePointCollection MSVM**](msvm-referencepointcollection.md) contenant la collection de points de référence du système virtuel résultant

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est exécutée à long terme, vous pouvez éventuellement retourner un travail.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, retourne 0 (terminé) ou 4096 (travail démarré); Sinon, retourne une erreur.

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

**Méthode réservée** (4097.. 32767)
</dt> <dt>

**Spécifique au fournisseur** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




