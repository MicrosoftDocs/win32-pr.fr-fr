---
description: Représente une entrée du contrôle d'accès.
ms.assetid: 47daffd0-b9db-4367-b0b8-654a2da30fed
ms.tgt_platform: multiple
title: Classe __ACE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ACE
- All
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
ms.openlocfilehash: ea2a765225145ce3d44e0aff89aeaca0a7563e0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485753"
---
# <a name="__ace-class"></a>\_\_Classe ACE

La classe système abstraite **\_ \_ ACE** représente une entrée de contrôle d’accès ([*ACE*](/windows/desktop/SecGloss/a-gly)).

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class  __ACE : __SecurityRelatedClass
{
            AceFlags;
            AccessMask;
            AceType;
            GuidInheritedObjectType;
            GuidObjectType;
  uint64    TIME_CREATED;
  __Trustee Trustee;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ ACE** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ ACE** possède ces propriétés.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Type de données : 
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indicateurs de bits représentant les droits accordés ou refusés au tiers de confiance. Pour plus d’informations et pour obtenir une description des indicateurs, consultez propriété **AccessMask** dans la classe [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .

</dd> <dt>

**AceFlags**
</dt> <dd> <dl> <dt>

Type de données : 
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indicateurs binaires spécifiant l’héritage de l’entrée du contrôle d’accès. Pour plus d’informations et pour obtenir une description des indicateurs, consultez la propriété **AceFlags** dans la classe [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .

</dd> <dt>

**AceType**
</dt> <dd> <dl> <dt>

Type de données : 
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Type d’entrée d’entrée du contrôle d’accès que cette instance représente.

</dd> <dt>

**GuidInheritedObjectType**
</dt> <dd> <dl> <dt>

Type de données : 
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

GUID du parent de l’objet auquel s’appliquent les droits d’accès de la propriété **AccessMask** .

</dd> <dt>

**GuidObjectType**
</dt> <dd> <dl> <dt>

Type de données : 
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

GUID qui indique le type d’objet auquel s’appliquent les droits de la propriété **AccessMask** .

</dd> <dt>

**HEURE de \_ création**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Heure, au format [ \_ DateTime CIM](cim-datetime.md) , de la création du descripteur de sécurité.

</dd> <dt>

**Tiers**
</dt> <dd> <dl> <dt>

Type de données : **[ **\_ \_ tiers de confiance**](--trustee.md)**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Le tiers de confiance de l’entrée ACE représentée par cette instance de la classe **\_ \_ ACE** .

</dd> </dl>

## <a name="remarks"></a>Notes

Cette classe fournit les propriétés héritées par la classe [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) , qui est un membre de la classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) . Pour plus d’informations, consultez [objets descripteur de sécurité WMI](wmi-security-descriptor-objects.md) et [modification de la sécurité d’accès sur des objets sécurisables](changing-access-security-on-securable-objects.md). Pour plus d’informations sur les ACE, consultez [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_SecurityRelatedClass**](--securityrelatedclass.md)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> <dt>

[**\_ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[Maintenance de la sécurité WMI](maintaining-wmi-security.md)
</dt> </dl>

 

