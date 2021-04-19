---
description: Représente une entrée de contrôle d’accès (ACE) qui détermine l’accès à la session interactive d’un ordinateur virtuel.
ms.assetid: dfec83d6-8033-47b5-aa6f-fc7447a29f43
title: Classe Msvm_InteractiveSessionACE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InteractiveSessionACE
- Msvm_InteractiveSessionACE.Trustee
- Msvm_InteractiveSessionACE.AccessType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6c4b63e769b04092323cd2da7362ef6b156886b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515883"
---
# <a name="msvm_interactivesessionace-class"></a>MSVM \_ InteractiveSessionACE, classe

Représente une *entrée de contrôle d’accès* (ACE) qui détermine l’accès à la session interactive d’un ordinateur virtuel.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InteractiveSessionACE
{
  string Trustee;
  uint16 AccessType;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ InteractiveSessionACE** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ InteractiveSessionACE** possède les propriétés suivantes.

<dl> <dt>

**AccessType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si l’entrée du contrôle d’accès accorde ou refuse l’accès au tiers de confiance.

<dt>

<span id="Access_Allowed"></span><span id="access_allowed"></span><span id="ACCESS_ALLOWED"></span>

**Accès autorisé** (0)


</dt> <dd></dd> <dt>

<span id="Access_Denied"></span><span id="access_denied"></span><span id="ACCESS_DENIED"></span>

**Accès refusé** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**Tiers**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identifie le principal de sécurité auquel l’entrée de contrôle d’accès accorde ou refuse l’accès. Les formats valides pour cette propriété sont le format de nom d’utilisateur compatible avec SAM Windows et le format de chaîne SID Windows.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetInteractiveSessionACL**](getinteractivesessionacl-msvm-terminalservice.md)
</dt> </dl>

 

 




