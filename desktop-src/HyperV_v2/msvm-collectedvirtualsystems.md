---
description: Associe le \_ VirtualSystemCollection MSVM aux objets MSVM \_ ComputerSystem contenus.
ms.assetid: ad783188-b60a-4271-aa2d-8050c36e70eb
title: Classe Msvm_CollectedVirtualSystems
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedVirtualSystems
- Msvm_CollectedVirtualSystems.Collection
- Msvm_CollectedVirtualSystems.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0803eda14ffbaf21ee2bf4491bd835123b7191e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526238"
---
# <a name="msvm_collectedvirtualsystems-class"></a>MSVM \_ CollectedVirtualSystems, classe

Associe [**le \_ VirtualSystemCollection MSVM**](msvm-virtualsystemcollection.md) aux objets [**MSVM \_ ComputerSystem**](msvm-computersystem.md) contenus.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedVirtualSystems : CIM_CollectedMSEs
{
  Msvm_VirtualSystemCollection REF Collection;
  Msvm_ComputerSystem          REF Member;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ CollectedVirtualSystems** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ CollectedVirtualSystems** possède les propriétés suivantes.

<dl> <dt>

**Collection**
</dt> <dd> <dl> <dt>

Type de données : **MSVM \_ VirtualSystemCollection**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("collection")
</dt> </dl>

Un regroupement [**MSVM \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) ou un objet « Bag » qui représente la collection.

</dd> <dt>

**Membre**
</dt> <dd> <dl> <dt>

Type de données : **MSVM \_ ComputerSystem**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")
</dt> </dl>

Objet [**MSVM \_ ComputerSystem**](msvm-computersystem.md) contenant les membres de la collection.

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

[**\_COLLECTEDMSES CIM**](cim-collectedmses.md)
</dt> </dl>

 

