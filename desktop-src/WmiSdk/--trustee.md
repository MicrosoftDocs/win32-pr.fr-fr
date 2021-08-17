---
description: La \_ \_ classe système abstraite Trusted représente un tiers de confiance. Un nom ou un SID (tableau d’octets) peut être utilisé.
ms.assetid: 92d17c7c-ebca-4dd0-80d8-6edd999ca394
ms.tgt_platform: multiple
title: Classe __Trustee
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Trustee
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: ac1e80bceb3dc584a22e342780bbf32660276868e473ff33ff01d6c2ad65d504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131952"
---
# <a name="__trustee-class"></a>\_\_Classe fiduciaire

La classe système abstraite [**\_ \_ Trusted**](--securitydescriptor.md) représente un [*tiers de confiance*](/windows/desktop/SecGloss/t-gly). Un nom ou un SID (tableau d’octets) peut être utilisé.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __Trustee
{
  string Domain;
  string Name;
  uint8  SID[];
  uint32 SidLength;
  string SidString;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Membres

La classe de **\_ \_ tiers de confiance** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe de **\_ \_ tiers de confiance** possède ces propriétés.

<dl> <dt>

**Domaine**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Partie domaine du compte.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Partie nom du compte.

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

SID du tiers de confiance dans la forme de tableau d’octets binaire.

</dd> <dt>

**SidLength**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Longueur du SID en octets.

</dd> <dt>

**SidString**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

SID du tiers de confiance dans le format de chaîne, par exemple, « S-1-1-0 ».

</dd> <dt>

**HEURE de \_ création**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Heure au format [ \_ DateTime CIM](cim-datetime.md) lorsque le descripteur de sécurité a été créé.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette classe fournit des propriétés qui sont héritées par la classe [**Win32 \_ Trusted**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) , qui est un membre de la classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) . Pour plus d’informations, consultez [objets descripteur de sécurité WMI](wmi-security-descriptor-objects.md) et [modification de la sécurité d’accès sur des objets sécurisables](changing-access-security-on-securable-objects.md). Pour plus d’informations sur les ACE, consultez [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> <dt>

[**\_Confiance Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
</dt> <dt>

[Maintenance de la sécurité WMI](maintaining-wmi-security.md)
</dt> </dl>

 

