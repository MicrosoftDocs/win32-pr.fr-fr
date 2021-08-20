---
description: Représente une association entre un système et un pool de ressources qui est un composant du système.
ms.assetid: 0ac60dbd-0498-4978-b2d6-f4c9926a83a8
title: Classe CIM_HostedResourcePool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedResourcePool
- CIM_HostedResourcePool.GroupComponent
- CIM_HostedResourcePool.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7029e3eaebc879d5b635ffe70cd8f6d7888ff580247d992f6794f20c35db7045
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014577"
---
# <a name="cim_hostedresourcepool-class"></a>\_Classe CIM HostedResourcePool

Représente une association entre un système et un pool de ressources qui est un composant du système.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Aggregation, Composition, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_HostedResourcePool : CIM_SystemComponent
{
  CIM_System       REF GroupComponent;
  CIM_ResourcePool REF PartComponent;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ HostedResourcePool** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ HostedResourcePool** possède les propriétés suivantes.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données **: \_ système CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Système parent dans l’Association.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ ResourcePool**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Pool de ressources qui est un composant du système.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SYSTEMCOMPONENT CIM**](cim-systemcomponent.md)
</dt> </dl>

 

