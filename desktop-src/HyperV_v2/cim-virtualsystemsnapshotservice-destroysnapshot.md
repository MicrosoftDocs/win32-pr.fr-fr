---
description: Détruisez un instantané de système virtuel existant. Cette méthode peut, en tant qu’effet secondaire, détruire d’autres instantanés qui dépendent de l’instantané affecté.
ms.assetid: 69f60d0e-50ef-4a38-ad4b-88534b7fb3f8
title: Méthode DestroySnapshot de la classe CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 986ffe6a7a5bd6ac18d47bcbebe40ac038ea86cdc096173704d30515067fcccc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646368"
---
# <a name="destroysnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a>Méthode DestroySnapshot de la \_ classe CIM VirtualSystemSnapshotService

Détruisez un instantané de système virtuel existant. Cette méthode peut, en tant qu’effet secondaire, détruire d’autres instantanés qui dépendent de l’instantané affecté.

## <a name="syntax"></a>Syntaxe


```mof
uint32 DestroySnapshot(
  [in]  CIM_VirtualSystemSettingData REF AffectedSnapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*AffectedSnapshot* \[ dans\]
</dt> <dd>

Référence [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) à l’instantané du système virtuel affecté.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est exécutée à long terme, éventuellement [**un \_ ConcreteJob CIM**](cim-concretejob.md) représentant le travail peut être retourné.

> [!Note]  
> Ce paramètre a été en lecture/écriture dans Windows 8.1.

 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite ; Sinon, retourne une erreur.

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
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_VIRTUALSYSTEMSNAPSHOTSERVICE CIM**](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




