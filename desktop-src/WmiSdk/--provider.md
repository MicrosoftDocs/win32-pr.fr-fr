---
description: Sert de classe parente pour la \_ \_ classe système Win32Provider.
ms.assetid: e4cad7c6-4650-4334-b8c4-ac65381bced7
ms.tgt_platform: multiple
title: Classe __Provider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Provider
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 733323c106a5d682e7eddbe3a41bf9c156520c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518306"
---
# <a name="__provider-class"></a>\_\_Classe de fournisseur

La classe de système **\_ \_ fournisseur** est une classe de base abstraite qui sert de classe parente pour la classe système [**\_ \_ Win32Provider**](--win32provider.md) .

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[abstract]
class __Provider : __SystemClass
{
  string Name;
};
```

## <a name="members"></a>Membres

La classe de **\_ \_ fournisseur** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe de **\_ \_ fournisseur** a ces propriétés.

<dl> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [ **clé**](standard-qualifiers.md)
</dt> </dl>

Chaîne indépendante du langage qui identifie le fournisseur de manière unique. Le format suivant est suggéré pour empêcher les conflits de noms :

\|version du fournisseur fournisseur \|

Par exemple, le nom de ce fournisseur représente la version 1,0 de Microsoft TestProvider :

« Microsoft \| TestProvider \| v 1.0 »

</dd> </dl>

## <a name="remarks"></a>Notes

La classe de **\_ \_ fournisseur** est dérivée de [**\_ \_ SystemClass**](--systemclass.md), qui n’a pas de propriétés.

Les fournisseurs créent des instances [**\_ \_ Win32Provider**](--win32provider.md) pour spécifier des informations sur leur implémentation physique.

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
</dt> <dt>

[**\_\_Win32Provider**](--win32provider.md)
</dt> </dl>

 

