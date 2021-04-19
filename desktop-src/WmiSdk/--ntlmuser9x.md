---
description: Contrôle l’accès à distance aux versions non prises en charge de Windows.
ms.assetid: eb326bba-a011-4b9c-b4ee-fc08ae364f6f
ms.tgt_platform: multiple
title: Classe __NTLMUser9X
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NTLMUser9X
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 79aa5153869c7337b6849e8c465dbbf8b36a0f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523401"
---
# <a name="__ntlmuser9x-class"></a>\_\_NTLMUser9X, classe

La classe système **\_ \_ NTLMUser9X** contrôle l’accès à distance aux versions non prises en charge de Windows. La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __NTLMUser9X : __SecurityRelatedClass
{
  string Authority;
  sint32 Flags;
  sint32 Mask;
  string Name;
  sint32 Type;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ NTLMUser9X** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ NTLMUser9X** possède les propriétés suivantes.

<dl> <dt>

**Authority**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Domaine auquel s’applique un nom d’utilisateur.

</dd> <dt>

**Indicateurs**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indicateurs d’héritage.

<dt>

0
</dt> <dd>

Aucun héritage.

</dd> <dt>

2
</dt> <dd>

Appliquez aux espaces de noms enfants, en plus de l’espace de noms actuel.

</dd> </dl>

</dd> <dt>

**Filtrage**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Masque de la valeur qui spécifie les droits d’accès à l’espace de noms dans le référentiel Windows Management Instrumentation (WMI). Pour les valeurs de bit, consultez [**constantes de droits d’accès à l’espace de noms**](namespace-access-rights-constants.md).

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Nom d’utilisateur.

</dd> <dt>

**Type**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Accès autorisé.

<dt>

0
</dt> <dd>

Accès autorisé.

</dd> <dt>

2
</dt> <dd>

Accès refusé.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **\_ \_ NTLMUser9X** est utilisée comme paramètre d’entrée pour les méthodes [**\_ \_ SystemSecurity :: Get9XUserList**](--systemsecurity-get9xuserlist.md) et [**\_ \_ SystemSecurity :: Set9XUserList**](--systemsecurity-set9xuserlist.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_SecurityRelatedClass**](/windows/desktop/WmiSdk/--securityrelatedclass)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

