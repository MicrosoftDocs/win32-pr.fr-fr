---
description: Contient des informations sur une unité de traitement graphique (GPU) physique RemoteFX.
ms.assetid: 86B47AAE-DBFF-43EF-88C6-44836D6C3AFA
title: Classe Msvm_PhysicalGPUInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PhysicalGPUInfo
- Msvm_PhysicalGPUInfo.InstanceID
- Msvm_PhysicalGPUInfo.Caption
- Msvm_PhysicalGPUInfo.Description
- Msvm_PhysicalGPUInfo.ElementName
- Msvm_PhysicalGPUInfo.Name
- Msvm_PhysicalGPUInfo.ID
- Msvm_PhysicalGPUInfo.TotalVideoMemory
- Msvm_PhysicalGPUInfo.AvailableVideoMemory
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cd4ccf65b364620e84063ea6398c59dd0e467f67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524686"
---
# <a name="msvm_physicalgpuinfo-class"></a>MSVM \_ PhysicalGPUInfo, classe

Contient des informations sur une unité de traitement graphique (GPU) physique RemoteFX.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PhysicalGPUInfo : CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string Name;
  string ID;
  uint64 TotalVideoMemory;
  uint64 AvailableVideoMemory;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ PhysicalGPUInfo** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ PhysicalGPUInfo** possède les propriétés suivantes.

<dl> <dt>

**AvailableVideoMemory**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Quantité de mémoire vidéo inutilisée, en octets, sur le GPU physique qui peut être utilisé par RemoteFX.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Identifiant**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)
</dt> </dl>

Identificateur unique du GPU physique.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Chaîne qui identifie de façon unique une instance de cette classe. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)
</dt> </dl>

Nom complet du GPU physique.

</dd> <dt>

**TotalVideoMemory**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Quantité totale de mémoire vidéo, en octets, sur le GPU physique qui peut être utilisé par RemoteFX.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Propriété MANAGEDELEMENT CIM**](cim-managedelement.md)
</dt> </dl>

 

