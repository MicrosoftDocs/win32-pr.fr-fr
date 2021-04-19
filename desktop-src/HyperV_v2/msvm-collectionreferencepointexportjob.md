---
description: Cette classe représente un travail d’exportation de point de référence de collection.
ms.assetid: c752ff1d-163c-4aa9-b29e-76478a18a08c
title: Classe Msvm_CollectionReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob
- Msvm_CollectionReferencePointExportJob.Cancellable
- Msvm_CollectionReferencePointExportJob.ErrorSummaryDescription
- Msvm_CollectionReferencePointExportJob.CollectionId
- Msvm_CollectionReferencePointExportJob.ReferencePointGroupId
- Msvm_CollectionReferencePointExportJob.BaseReferencePointGroupId
- Msvm_CollectionReferencePointExportJob.VirtualMachineId
- Msvm_CollectionReferencePointExportJob.ExportDirectory
- Msvm_CollectionReferencePointExportJob.ExportedDisks
- Msvm_CollectionReferencePointExportJob.ExportedLogFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedConfigFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedRuntimeFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedGuestStateFilePaths
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d21fab1519664471bdc2bb5d7102d94cbe3dde1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535696"
---
# <a name="msvm_collectionreferencepointexportjob-class"></a>MSVM \_ CollectionReferencePointExportJob, classe

Cette classe représente un travail d’exportation de point de référence de collection.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionReferencePointExportJob : CIM_ConcreteJob
{
  boolean Cancellable;
  string  ErrorSummaryDescription;
  string  CollectionId;
  string  ReferencePointGroupId;
  string  BaseReferencePointGroupId;
  string  VirtualMachineId[];
  string  ExportDirectory;
  string  ExportedDisks[];
  string  ExportedLogFilePaths[];
  string  ExportedConfigFilePaths[];
  string  ExportedRuntimeFilePaths[];
  string  ExportedGuestStateFilePaths[];
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ CollectionReferencePointExportJob** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MSVM \_ CollectionReferencePointExportJob** possède ces méthodes.



| Méthode                                                                                  | Description                                        |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------|
| [**GetError**](msvm-collectionreferencepointexportjob-geterror.md)                     | Récupère une erreur.<br/>                     |
| [**GetErrorEx**](msvm-collectionreferencepointexportjob-geterrorex.md)                 | Récupère des informations supplémentaires sur l’erreur.<br/> |
| [**RequestStateChange**](msvm-collectionreferencepointexportjob-requeststatechange.md) | Demande un changement d’État.<br/>                |



 

### <a name="properties"></a>Propriétés

La classe **MSVM \_ CollectionReferencePointExportJob** possède les propriétés suivantes.

<dl> <dt>

**BaseReferencePointGroupId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

GUID du point de référence de collection utilisé comme base dans le exportoperation.

</dd> <dt>

**Annulable**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le travail peut être annulé. La valeur de cette propriété ne garantit pas qu’une demande d’annulation du travail échoue.

</dd> <dt>

**CollectionId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

GUID du groupe de machines virtuelles pour lequel les fichiers journaux wereexported.

</dd> <dt>

**ErrorSummaryDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («[**\_ tâche CIM**](cim-job.md).**ErrorCode**»)
</dt> </dl>

Contient une description résumée des erreurs.

</dd> <dt>

**ExportDirectory**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Emplacement d’exportation.

</dd> <dt>

**ExportedConfigFilePaths**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès du fichier de configuration de l’ordinateur virtuel exporté.

</dd> <dt>

**ExportedDisks**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

ID d’instance des disques virtuels pour lesquels les fichiers journaux ont été exportés.

</dd> <dt>

**ExportedGuestStateFilePaths**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès du fichier d’État invité de l’ordinateur virtuel exporté.

> [!Note]  
> Ajouté dans Windows 10, version 1709.

 

</dd> <dt>

**ExportedLogFilePaths**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemins des fichiers journaux qui ont été exportés.

</dd> <dt>

**ExportedRuntimeFilePaths**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès du fichier d’état d’exécution de l’ordinateur virtuel exporté.

</dd> <dt>

**ReferencePointGroupId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

GUID du point de référence de collection qui est exporté.

</dd> <dt>

**VirtualMachineId**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

GUID des machines virtuelles pour lesquelles l’opération d’exportation a été effectuée.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1703 \[ uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_CONCRETEJOB CIM**](cim-concretejob.md)
</dt> </dl>

 

