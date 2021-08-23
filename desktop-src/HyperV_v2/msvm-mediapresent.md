---
description: Associe un lecteur de stockage au support inséré dans le lecteur.
ms.assetid: C0B2D604-0B55-4EA0-A46E-2450D89A5B22
title: Classe Msvm_MediaPresent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MediaPresent
- Msvm_MediaPresent.Antecedent
- Msvm_MediaPresent.Dependent
- Msvm_MediaPresent.FixedMedia
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7044cfed5a4affd628ea8008c89b4aabeee3499d65f03abf815e68d73d06a773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521719"
---
# <a name="msvm_mediapresent-class"></a>MSVM \_ MediaPresent, classe

Associe un lecteur de stockage au support inséré dans le lecteur. Cette association est utilisée pour tous les objets de lecteur de stockage.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MediaPresent : CIM_MediaPresent
{
  CIM_MediaAccessDevice REF Antecedent;
  CIM_StorageExtent     REF Dependent;
  boolean                   FixedMedia;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ MediaPresent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ MediaPresent** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à l’appareil d’accès au média. Cette propriété est héritée de la [**\_ MediaPresent CIM**](/windows/desktop/CIMWin32Prov/cim-mediapresent).

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à l’extension de stockage accessible avec l’appareil d’accès au média. Cette propriété est héritée de la [**\_ MediaPresent CIM**](/windows/desktop/CIMWin32Prov/cim-mediapresent).

</dd> <dt>

**FixedMedia**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si l’extension de stockage accessible est fixe et ne peut pas être éjectée. La valeur est **true** pour les disques durs et **false** dans le cas contraire. Cette propriété est héritée de la [**\_ MediaPresent CIM**](/windows/desktop/CIMWin32Prov/cim-mediapresent).

</dd> </dl>

## <a name="remarks"></a>Remarques

L’accès à la classe **MSVM \_ MediaPresent** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_MEDIAPRESENT CIM**](cim-mediapresent.md)
</dt> <dt>

[**\_MEDIAPRESENT CIM**](/windows/desktop/CIMWin32Prov/cim-mediapresent)
</dt> <dt>

[Stockage Catégories](storage-classes.md)
</dt> </dl>

 

