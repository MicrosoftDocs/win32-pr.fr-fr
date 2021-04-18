---
description: Représente les paramètres de copie d’un fichier à partir de l’hôte dans l’invité.
ms.assetid: 255F4132-C212-4A3B-A9B8-3F531E7D1CF9
title: Classe Msvm_CopyFileToGuestSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestSettingData
- Msvm_CopyFileToGuestSettingData.Description
- Msvm_CopyFileToGuestSettingData.Caption
- Msvm_CopyFileToGuestSettingData.InstanceID
- Msvm_CopyFileToGuestSettingData.ElementName
- Msvm_CopyFileToGuestSettingData.OverwriteExisting
- Msvm_CopyFileToGuestSettingData.CreateFullPath
- Msvm_CopyFileToGuestSettingData.SourcePath
- Msvm_CopyFileToGuestSettingData.DestinationPath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 05e27340acc9dd341bec7857c164f50344abc36f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520132"
---
# <a name="msvm_copyfiletoguestsettingdata-class"></a>MSVM \_ CopyFileToGuestSettingData, classe

Représente les paramètres de copie d’un fichier à partir de l’hôte dans l’invité. Cette classe dérive de [**la \_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[AMENDMENT]
class Msvm_CopyFileToGuestSettingData : CIM_SettingData
{
  string  Description;
  string  Caption;
  string  InstanceID;
  string  ElementName;
  boolean OverwriteExisting;
  boolean CreateFullPath;
  string  SourcePath;
  string  DestinationPath;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ CopyFileToGuestSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ CopyFileToGuestSettingData** possède les propriétés suivantes.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **MaxLen** (64)
</dt> </dl>

Brève description textuelle de l’objet.

</dd> <dt>

**CreateFullPath**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si des répertoires absents dans le chemin d’accès du fichier de destination doivent être créés avant de copier le fichier.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description textuelle de l’objet.

</dd> <dt>

**DestinationPath**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès complet du fichier de destination à copier. Ce fichier de destination doit être accessible à l’invité et peut contenir des variables d’environnement qui sont développées par l’invité. Si le chemin d’accès spécifié est un répertoire existant dans l’invité, le fichier de destination est créé dans ce répertoire. Dans ce cas, le nom de fichier de **SourcePath** est utilisé comme nom de fichier de destination.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de cette instance de SettingData. En outre, le nom complet peut être utilisé comme propriété d’index pour une recherche ou une requête. (Remarque : il n’est pas nécessaire que le nom soit unique au sein d’un espace de noms.)

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Dans l’étendue de l’espace de noms d’instanciation, InstanceID identifie de façon opaque et unique une instance de cette classe. Pour garantir l’unicité dans l’espace de noms, la valeur d’InstanceID doit être construite à l’aide de l’algorithme « préféré » suivant : *identifiant OrgID*:*LocalID* où *identifiant OrgID* et *LocalID* sont séparés par un signe deux-points ( :), et où *identifiant OrgID* doit inclure un nom de droits d’auteur, de marque déposée ou autre que celui qui est détenu par l’entité commerciale qui crée ou définit l’InstanceId ou qui est un ID inscrit affecté à l’entité métier (Cette spécification est semblable à celle de *SchemaName* \_ Structure *className* des noms de classes de schéma.) En outre, pour garantir l’unicité, *identifiant OrgID* ne doit pas contenir de deux-points ( :). Lors de l’utilisation de cet algorithme, le premier signe deux-points devant apparaître dans InstanceID doit apparaître entre *identifiant OrgID* et *LocalID*. *LocalID* est choisi par l’entité métier et ne doit pas être réutilisé pour identifier les différents éléments sous-jacents (réels). Si l’algorithme par défaut ci-dessus n’est pas utilisé, l’entité de définition doit s’assurer que l’InstanceID qui en résulte n’est pas réutilisé dans les InstanceIDs produits par ce ou d’autres fournisseurs pour l’espace de noms de cette instance. Pour les instances définies par DMTF, l’algorithme « préféré » doit être utilisé avec le *identifiant OrgID* défini sur CIM.

</dd> <dt>

**OverwriteExisting**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si un fichier de destination existant doit être remplacé.

</dd> <dt>

**SourcePath**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès complet du fichier source à copier. Ce fichier source doit être accessible à l’hôte Hyper-V et peut contenir des variables d’environnement qui sont développées par l’hôte Hyper-V.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                                                 |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> <dt>

[**\_SETTINGDATA CIM**](/previous-versions//cc136911(v=vs.85))
</dt> </dl>

 

