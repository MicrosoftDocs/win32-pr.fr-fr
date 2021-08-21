---
description: Exportez les données de paramètre à transmettre à la méthode ExportReferencePoint de la \_ classe CollectionReferencePointService MSVM.
ms.assetid: 38299050-a53a-496c-8792-9199c394591d
title: Classe Msvm_CollectionReferencePointExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportSettingData
- Msvm_CollectionReferencePointExportSettingData.BaseReferencePointCollection
- Msvm_CollectionReferencePointExportSettingData.VirtualMachinesToDisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b8b160f16a71e25eca4afa445fd05fd1faba58c82c6ba6e08afd25bbc9ba41b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149242"
---
# <a name="msvm_collectionreferencepointexportsettingdata-class"></a>MSVM \_ CollectionReferencePointExportSettingData, classe

Exportez les données de paramètre à transmettre à la méthode [**ExportReferencePoint**](msvm-collectionreferencepointservice-exportreferencepoint.md) de la classe [**\_ CollectionReferencePointService MSVM**](msvm-collectionreferencepointservice.md) .

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[AMENDMENT]
class Msvm_CollectionReferencePointExportSettingData : CIM_SettingData
{
  string BaseReferencePointCollection;
  string VirtualMachinesToDisksToExport[];
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ CollectionReferencePointExportSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ CollectionReferencePointExportSettingData** possède les propriétés suivantes.

<dl> <dt>

**BaseReferencePointCollection**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Chemin d’accès à une instance [**MSVM \_ ReferencePointCollection**](msvm-referencepointcollection.md) qui représente la collection de points de référence de base à utiliser pour l’exportation différentielle.

</dd> <dt>

**VirtualMachinesToDisksToExport**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : **HyperVEmbeddedInstance** ("MSVM \_ VirtualMachineToDisks")
</dt> </dl>

Liste des informations de mappage « VirtualMachines to DisksToExport » pour lesquelles les données doivent être exportées.

</dd> </dl>

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

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

 




