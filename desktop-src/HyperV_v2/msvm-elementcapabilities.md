---
description: Représente l’association entre les éléments managés et leurs fonctionnalités.
ms.assetid: F083E6D2-CC74-4DAD-8FF7-3FE3CA4EEFFF
title: Classe Msvm_ElementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementCapabilities
- Msvm_ElementCapabilities.ManagedElement
- Msvm_ElementCapabilities.Capabilities
- Msvm_ElementCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 56b0180e7f6fe4b7bb80129006e9290c23b38f2c5c10beaaa6377096b243b275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148443"
---
# <a name="msvm_elementcapabilities-class"></a>MSVM \_ ElementCapabilities, classe

Représente l’association entre les éléments managés et leurs fonctionnalités.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementCapabilities : CIM_ElementCapabilities
{
  CIM_ManagedElement REF ManagedElement;
  CIM_Capabilities   REF Capabilities;
  uint16                 Characteristics[];
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ ElementCapabilities** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ ElementCapabilities** possède les propriétés suivantes.

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Type de données : **[ **\_ fonctionnalités CIM**](/previous-versions//cc136806(v=vs.85))**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Objet de fonctionnalités associé à l’élément. Cette propriété est héritée de la [**\_ ElementCapabilities CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).

</dd> <dt>

**Caractéristiques**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Fournit des informations descriptives sur les fonctionnalités de. Cette propriété est héritée de la [**\_ ElementCapabilities CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).



| Valeur                                                                                                                                                                                                                       | Signification                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <dt>**Par défaut**</dt> <dt>2</dt> </dl> | Les fonctionnalités associées représentent les fonctionnalités par défaut de l’élément géré.<br/> |
| <span id="Current"></span><span id="current"></span><span id="CURRENT"></span><dl> <dt>**Actuel**</dt> <dt>3</dt> </dl> | Les fonctionnalités associées représentent les fonctionnalités actuelles de l’élément managé.<br/> |



 

</dd> <dt>

**Propriété ManagedElement**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**, **min** (1)
</dt> </dl>

Élément managé. Cette propriété est héritée de la [**\_ ElementCapabilities CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).

</dd> </dl>

## <a name="remarks"></a>Remarques

L’accès à la classe **MSVM \_ ElementCapabilities** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_ELEMENTCAPABILITIES CIM**](cim-elementcapabilities.md)
</dt> <dt>

[**\_ELEMENTCAPABILITIES CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)
</dt> <dt>

[**MSVM \_ ElementCapabilities (v1)**](/previous-versions/windows/desktop/virtual/msvm-elementcapabilities)
</dt> </dl>

 

