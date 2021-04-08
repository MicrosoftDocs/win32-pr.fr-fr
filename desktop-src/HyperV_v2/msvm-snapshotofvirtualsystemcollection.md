---
description: Associe le \_ SnapshotCollection MSVM aux objets MSVM \_ VirtualSystemCollection correspondants.
ms.assetid: 4dbfe21f-e700-4266-aedb-236c57c424f6
title: Classe Msvm_SnapshotOfVirtualSystemCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotOfVirtualSystemCollection
- Msvm_SnapshotOfVirtualSystemCollection.Antecedent
- Msvm_SnapshotOfVirtualSystemCollection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae3c9c146cea8a8af98f4d3071ee7339d53eb6b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863561"
---
# <a name="msvm_snapshotofvirtualsystemcollection-class"></a>MSVM \_ SnapshotOfVirtualSystemCollection, classe

Associe [**le \_ SnapshotCollection MSVM**](msvm-snapshotcollection.md) aux objets [**MSVM \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) correspondants.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotOfVirtualSystemCollection : CIM_Dependency
{
  CIM_CollectionOfMSEs REF Antecedent;
  CIM_Collection       REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ SnapshotOfVirtualSystemCollection** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ SnapshotOfVirtualSystemCollection** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ CollectionOfMSEs**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

[**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) qui représente l’objet indépendant dans cette association.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données **: \_ collecte CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »)
</dt> </dl>

[**\_ Collection CIM**](cim-collection.md) qui représente l’objet qui dépend de l' **antécédent.**

</dd> </dl>

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

[**\_Dépendance CIM**](cim-dependency.md)
</dt> </dl>

 

