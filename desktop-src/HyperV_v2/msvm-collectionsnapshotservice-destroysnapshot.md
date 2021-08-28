---
description: Détruit un instantané existant de la collection de systèmes virtuels. Cette méthode peut, en tant qu’effet secondaire, détruire d’autres instantanés qui dépendent de l’instantané affecté.
ms.assetid: 79a529d5-35bb-4e63-a1b7-8943de9580e8
title: Méthode DestroySnapshot de la classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bacdb760580057516b6663bf53f5cd02a83f76148fa782ab875ca7385c053cb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119431492"
---
# <a name="destroysnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Méthode DestroySnapshot de la \_ classe CollectionSnapshotService MSVM

Détruit un instantané existant de la collection de systèmes virtuels. Cette méthode peut, en tant qu’effet secondaire, détruire d’autres instantanés qui dépendent de l’instantané affecté.

## <a name="syntax"></a>Syntaxe


```mof
uint32 DestroySnapshot(
  [in]  CIM_Collection  REF AffectedSnapshotCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*AffectedSnapshotCollection* \[ dans\]
</dt> <dd>

Référence à une [**\_ collection CIM**](cim-collection.md) qui décrit la collection d’instantanés de système virtuel affectée.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Référence facultative qui est retournée si l’opération est exécutée de façon asynchrone. Si elle est présente, la référence retournée à une instance de [**\_ ConcreteJob CIM**](cim-concretejob.md) peut être utilisée pour surveiller la progression et pour obtenir le résultat de la méthode.

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
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




