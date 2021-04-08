---
description: Définition des données à transmettre en tant que tableau à la \_ classe MSVM CollectionReferencePointExportSettingData.
ms.assetid: f127880f-f917-4069-a283-a6f9427c5e07
title: Classe Msvm_VirtualMachineToDisks
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualMachineToDisks
- Msvm_VirtualMachineToDisks.VirtualMachineId
- Msvm_VirtualMachineToDisks.DisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cad5de9389b9cb1d5e7db0573f3a4e3fc271ba31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862066"
---
# <a name="msvm_virtualmachinetodisks-class"></a>MSVM \_ VirtualMachineToDisks, classe

Définition des données à transmettre en tant que tableau à la classe [**MSVM \_ CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) .

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualMachineToDisks
{
  string VirtualMachineId;
  string DisksToExport[];
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ VirtualMachineToDisks** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ VirtualMachineToDisks** possède les propriétés suivantes.

<dl> <dt>

**DisksToExport**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

ID d’instance WMI des disques auxquels appartiennent l’ID d’ordinateur virtuel pour lequel les données doivent être exportées.

</dd> <dt>

**VirtualMachineId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

ID de machine virtuelle auquel les disques virtuels sont associés.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




