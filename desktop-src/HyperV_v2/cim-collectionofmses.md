---
description: Classe abstraite pour les sous-classes qui représentent une collection d' \_ objets MANAGEDSYSTEMELEMENT CIM. Ces collections permettent de regrouper les éléments système gérés à des fins d’identification et de simplifier l’Association des paramètres et des configurations.
ms.assetid: f47bf1d6-6d89-4d9f-82d1-99a7343481bc
title: Classe CIM_CollectionOfMSEs (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.CollectionID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8598b8208b9291ec9dabc405f1b1c8d18513ff111e22ec8caa6c8bf32fb946f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813322"
---
# <a name="cim_collectionofmses-class-hyper-v-management"></a>Classe CIM_CollectionOfMSEs (gestion Hyper-V)

Classe abstraite pour les sous-classes qui représentent une collection d’objets [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) . Ces collections permettent de regrouper les éléments système gérés à des fins d’identification et de simplifier l’Association des paramètres et des configurations.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_CollectionOfMSEs : CIM_Collection
{
  string CollectionID;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ CollectionOfMSEs** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ CollectionOfMSEs** possède les propriétés suivantes.

<dl> <dt>

**CollectionID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identification de l’objet de collection. Lorsqu’elle est sous-classée **, la propriété** de l’un peut être substituée en tant que propriété de clé.

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

[**\_Collection CIM**](cim-collection.md)
</dt> </dl>

 

