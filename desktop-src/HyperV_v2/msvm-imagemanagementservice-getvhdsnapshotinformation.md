---
description: Récupère des informations sur une capture instantanée de disque dur virtuel dans un fichier de définition de VHD.
ms.assetid: 43745935-9bc3-4a87-8762-54693b2cdef6
title: Méthode GetVHDSnapshotInformation de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVHDSnapshotInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 85ea18e2be5329345ba49f4956307c4b29134ed6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514210"
---
# <a name="getvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a>Méthode GetVHDSnapshotInformation de la \_ classe ImageManagementService MSVM

Récupère des informations sur une capture instantanée de disque dur virtuel dans un fichier de définition de VHD.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetVHDSnapshotInformation(
  [in]  string              VHDSetPath,
  [in]  string              SnapshotIds[],
  [in]  uint32              AdditionalInformation[],
  [out] string              SnapshotInformation[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*VHDSetPath* \[ dans\]
</dt> <dd>

Chemin d’accès qualifié complet qui spécifie l’emplacement du fichier de définition de disque dur virtuel.

</dd> <dt>

*SnapshotIds* \[ dans\]
</dt> <dd>

Liste de GUID représentant les ID d’instantané de chaque capture instantanée pour laquelle les informations sont demandées. Si ce paramètre a la valeur NULL, les informations de tous les instantanés sont récupérées.

</dd> <dt>

*AdditionalInformation* \[ dans\]
</dt> <dd>

Tableau spécifiant les informations supplémentaires à collecter sur chaque instantané de disque dur virtuel. Chaque entrée du tableau est un type d’informations supplémentaires. Si ce paramètre a la valeur NULL, aucune information supplémentaire n’est récupérée.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Parent_Paths"></span><span id="parent_paths"></span><span id="PARENT_PATHS"></span>

**Chemins d’accès parents** (2)


</dt> <dd></dd> </dl> </dd> <dt>

*SnapshotInformation* \[ à\]
</dt> <dd>

En cas de réussite, un tableau d’informations sur chaque capture instantanée demandée. Chaque élément est une instance incorporée de [**MSVM \_ VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Référence au travail (peut avoir la valeur null si la tâche est terminée).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l'une des valeurs suivantes :

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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




