---
description: Applique une collection d’instantanés à la collection de systèmes d’ordinateurs virtuels.
ms.assetid: c76c552a-ae07-4dab-a938-740d77447a53
title: Méthode ApplySnapshot de la classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f4dd36db457099aaa9c134593fa385f21480e036e15629d10c32e716e604a462
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119426929"
---
# <a name="applysnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Méthode ApplySnapshot de la \_ classe CollectionSnapshotService MSVM

Applique une collection d’instantanés à la collection de systèmes d’ordinateurs virtuels.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ApplySnapshot(
  [in]  CIM_Collection  REF SnapshotCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SnapshotCollection* \[ dans\]
</dt> <dd>

Référence à une [**\_ collection CIM**](cim-collection.md) qui représente la collection d’instantanés à appliquer.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Référence facultative qui est retournée si l’opération est exécutée de façon asynchrone. Si elle est présente, la référence retournée à une instance de [**\_ ConcreteJob CIM**](cim-concretejob.md) peut être utilisée pour surveiller la progression et pour obtenir le résultat de la méthode.

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
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1703 \[ uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




