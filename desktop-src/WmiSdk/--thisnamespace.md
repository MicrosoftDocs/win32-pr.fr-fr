---
description: Contient les droits de sécurité de l’espace de noms sous la forme d’un descripteur de sécurité.
ms.assetid: 84e514f5-b114-4bfc-ab0b-9745f249168b
ms.tgt_platform: multiple
title: classe __thisNAMESPACE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __thisNAMESPACE
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 440ccdf0eda794b5d648cae756f9a9c808eb2db6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524392"
---
# <a name="__thisnamespace-class"></a>\_\_thisNAMESPACE, classe

La classe système **\_ \_ thisNAMESPACE** contient les droits de sécurité pour l’espace de noms sous la forme d’un descripteur de sécurité. Cette classe et une instance unique se trouvent dans tous les espaces de noms.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[singleton]
class __thisNAMESPACE : __SystemClass
{
  uint8 SECURITY_DESCRIPTOR[];
};
```

## <a name="members"></a>Membres

La classe **\_ \_ thisNAMESPACE** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ thisNAMESPACE** possède les propriétés suivantes.

<dl> <dt>

**descripteur de sécurité \_**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Descripteur de sécurité décrivant qui peut accéder à l’espace de noms et qui peut lire ou écrire dans l’espace de noms. Cette propriété est héritée de l' [**\_ \_ événement**](--event.md). Pour plus d’informations sur le format des descripteurs de sécurité, voir [descripteurs de sécurité](/windows/desktop/SecAuthZ/security-descriptors) dans la section sécurité de la SDK Windows.

</dd> </dl>

## <a name="remarks"></a>Notes

L’instance singleton de **\_ \_ thisNAMESPACE** est en lecture seule. Pour modifier les paramètres de la propriété descripteur de sécurité, utilisez les méthodes de la classe [**\_ \_ SystemSecurity**](--systemsecurity.md) . La classe **\_ \_ thisNAMESPACE** dérive de [**\_ \_ SystemClass**](--systemclass.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_SystemClass**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> </dl>

 

