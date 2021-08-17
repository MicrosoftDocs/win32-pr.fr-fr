---
description: Représente un descripteur de sécurité.
ms.assetid: 1ade1751-52a2-4ada-8255-323321111663
ms.tgt_platform: multiple
title: Classe __SecurityDescriptor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SecurityDescriptor
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
ms.openlocfilehash: c248a437651396811f71c04e72dd8b209c5d10823f49d03abbe7e9d9ee6b6867
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110196"
---
# <a name="__securitydescriptor-class"></a>\_\_SecurityDescriptor (classe)

La **\_ \_ classe de système** abstrait abstrait représente un [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly).

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __SecurityDescriptor
{
  uint32 ControlFlags;
  __ACE  DACL[];
  __ACE  Group;
  __ACE  Owner;
  __ACE  SACL;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ SecurityDescriptor** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ SecurityDescriptor** possède ces propriétés.

<dl> <dt>

**ControlFlags**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indicateurs binaires qui fournissent des informations sur le contenu et le format du descripteur. Pour obtenir une description des indicateurs, consultez la propriété **ControlFlags** dans la classe [**\_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .

</dd> <dt>

**DACL**
</dt> <dd> <dl> <dt>

Type de données : tableau **[**\_ \_ ACE**](--ace.md)**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Tableau d’entrées [**\_ \_ ACE**](--ace.md) qui spécifient l’accès à l’objet.

</dd> <dt>

**Groupe**
</dt> <dd> <dl> <dt>

Type de données : **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

ACE qui identifie le tiers de confiance représentant le groupe de l’objet.

</dd> <dt>

**Propriétaire**
</dt> <dd> <dl> <dt>

Type de données : **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

ACE qui identifie le tiers de confiance représentant le propriétaire de l’objet.

</dd> <dt>

**SACL**
</dt> <dd> <dl> <dt>

Type de données : **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau d’entrées [**\_ \_ ACE**](--ace.md) qui identifie les utilisateurs et les groupes pour lesquels des informations d’audit sont collectées.

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

Cette classe fournit les propriétés héritées par le [**\_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor). Pour plus d’informations, consultez [objets descripteur de sécurité WMI](wmi-security-descriptor-objects.md) et [modification de la sécurité d’accès sur des objets sécurisables](changing-access-security-on-securable-objects.md). Pour plus d’informations sur les ACE, consultez [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).

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

[**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Maintenance de la sécurité WMI](maintaining-wmi-security.md)
</dt> </dl>

 

