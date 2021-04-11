---
description: Exporte une collection d’instantanés de systèmes d’ordinateurs virtuels dans un fichier. La collection d’instantanés, ses paramètres de configuration associés et les paramètres de ressources qui lui sont associés sont conservés dans le fichier résultant.
ms.assetid: 61fbc81c-c3e8-4058-b11a-4ed69481207c
title: Méthode temps de la classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ExportSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f4dd29e001c8335477451e86151d950c25edb9b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202215"
---
# <a name="exportsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Méthode temps de la \_ classe CollectionSnapshotService MSVM

Exporte une collection d’instantanés de systèmes d’ordinateurs virtuels dans un fichier. La collection d’instantanés, ses paramètres de configuration associés et les paramètres de ressources qui lui sont associés sont conservés dans le fichier résultant.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ExportSnapshot(
  [in]  CIM_Collection  REF SnapshotCollection,
  [in]  string              ExportDirectory,
  [in]  string              ExportSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SnapshotCollection* \[ dans\]
</dt> <dd>

Référence à une [**\_ collection CIM**](cim-collection.md) qui représente la collection d’instantanés à exporter.

</dd> <dt>

*ExportDirectory* \[ dans\]
</dt> <dd>

Chemin d’accès complet du répertoire dans lequel la collection de systèmes virtuels doit être exportée. Si la propriété **CreateVmExportSubdirectory** dans le paramètre *ExportSettingData* est définie sur **true** , ce répertoire peut être réutilisé pour l’exportation de plusieurs collections de systèmes virtuels et cette méthode place chaque définition de collection de système virtuel dans un sous-répertoire distinct sous ce chemin d’accès.

</dd> <dt>

*ExportSettingData* \[ dans\]
</dt> <dd>

Instance de [**MSVM \_ CollectionSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md) qui représente les paramètres de l’opération d’exportation.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Référence facultative qui est retournée si l’opération est exécutée de façon asynchrone. Si elle est présente, la référence retournée à une instance de [**\_ ConcreteJob CIM**](cim-concretejob.md) peut être utilisée pour surveiller la progression et pour obtenir le résultat de la méthode.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est exécutée de façon synchrone, elle retourne 0 si elle réussit. Si cette méthode est exécutée de façon asynchrone, elle retourne 4096 et le paramètre de sortie de la tâche peut être utilisé pour suivre la progression de l’opération asynchrone. Toute autre valeur de retour indique une erreur.

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

 

 




