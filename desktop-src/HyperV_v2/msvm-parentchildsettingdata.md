---
description: Association entre une instance de MSVM \_ VirtualSystemSettingData et l' \_ instance VirtualSystemSettingData MSVM qui représente l’instantané le plus récent sur lequel cet objet est basé.
ms.assetid: F779775B-9AB3-4495-B6FF-9985FCDF63E4
title: Classe Msvm_ParentChildSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ParentChildSettingData
- Msvm_ParentChildSettingData.Antecedent
- Msvm_ParentChildSettingData.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e11f8646988a8cb1d963bd4cc45901f42ffef7525cfa9d228cc8de5c0dfa3c12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147390"
---
# <a name="msvm_parentchildsettingdata-class"></a>MSVM \_ ParentChildSettingData, classe

Association entre une instance de [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) et l’instance **\_ VirtualSystemSettingData MSVM** qui représente l’instantané le plus récent sur lequel cet objet est basé.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ParentChildSettingData : CIM_Dependency
{
  Msvm_VirtualSystemSettingData REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ ParentChildSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ ParentChildSettingData** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ dependency. Antecedent")
</dt> </dl>

Données de paramètre d’instantané sur lesquelles les données de paramètres enfants sont basées.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dépendance CIM \_ . dependent")
</dt> </dl>

Données de paramètre de l’ordinateur virtuel qui représente l’enfant du parent.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’accès à la classe **MSVM \_ ParentChildSettingData** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Dépendance CIM**](cim-dependency.md)
</dt> <dt>

[**\_Dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> <dt>

[Classes du système virtuel](virtual-system-classes.md)
</dt> </dl>

 

