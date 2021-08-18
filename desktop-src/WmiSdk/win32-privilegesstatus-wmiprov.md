---
description: Le \_ PrivilegesStatus Win32 &\# 8194 ; La classe WMI fournit des informations sur les privilèges requis pour effectuer une opération. Elle peut être retournée en cas d’échec d’une opération ou lorsqu’une instance partiellement remplie a été retournée.
ms.assetid: 85bda855-1488-4d7a-99ed-798e9859fef7
ms.tgt_platform: multiple
title: Classe Win32_PrivilegesStatus (WMI)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrivilegesStatus
- Win32_PrivilegesStatus.Description
- Win32_PrivilegesStatus.Operation
- Win32_PrivilegesStatus.ParameterInfo
- Win32_PrivilegesStatus.ProviderName
- Win32_PrivilegesStatus.StatusCode
- Win32_PrivilegesStatus.PrivilegesNotHeld
- Win32_PrivilegesStatus.PrivilegesRequired
api_type:
- Schema
api_location:
- Root\WMI
ms.openlocfilehash: 97276023325dc4e2a460daefd35ee01104b5c0adf5c855f145e0f11c954eba1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757629"
---
# <a name="win32_privilegesstatus-class-wmi"></a>Classe Win32_PrivilegesStatus (WMI)

La [classe WMI](retrieving-a-class.md) **Win32 \_ PrivilegesStatus** fournit des informations sur les privilèges requis pour effectuer une opération.    Elle peut être retournée en cas d’échec d’une opération ou lorsqu’une instance partiellement remplie a été retournée.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[UUID("{BE46D060-7A7C-11d2-BC85-00104B2CF71C}")]
class Win32_PrivilegesStatus : __ExtendedStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
  string PrivilegesNotHeld[];
  string PrivilegesRequired[];
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ PrivilegesStatus** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ PrivilegesStatus** a ces propriétés.

<dl> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Toute chaîne définie par l’utilisateur qui décrit une erreur ou un état opérationnel.

Cette propriété est héritée de [**\_ \_ ExtendedStatus**](--extendedstatus.md).

</dd> <dt>

**opération**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Opération qui se produit au moment d’une défaillance ou d’une anomalie. en règle générale, Windows Management Instrumentation (WMI) définit cette propriété sur le nom d’une API COM pour la méthode WMI, telle que la suivante : [**IWbemServices :: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).

Cette propriété est héritée de [**\_ \_ ExtendedStatus**](--extendedstatus.md).

</dd> <dt>

**ParameterInfo**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Paramètres impliqués dans une modification d’erreur ou d’État. Par exemple, si une application tente de récupérer une classe qui n’existe pas, cette propriété est définie sur le nom de la classe incriminée.

Cette propriété est héritée de [**\_ \_ ExtendedStatus**](--extendedstatus.md).

</dd> <dt>

**PrivilegesNotHeld**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Liste des privilèges d’accès requis manquants pour terminer une opération. les types de privilèges d’accès se trouvent sous les privilèges Windows.

exemple : « SE \_ SHUTDOWN \_ NAME »

</dd> <dt>

**PrivilegesRequired**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Liste de tous les privilèges requis pour effectuer une opération. Cela comprend les valeurs de la propriété **PrivilegesNotHeld** .

exemple : « SE \_ SHUTDOWN \_ NAME »

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identifie le fournisseur qui provoque ou signale une modification d’erreur ou d’État. si aucun fournisseur n’est impliqué, cette chaîne est définie sur « gestion de la Windows ».

Cette propriété est héritée de [**\_ \_ ExtendedStatus**](--extendedstatus.md).

</dd> <dt>

**StatusCode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Contient une erreur ou un code d’information pour une opération. Il peut s’agir de n’importe quelle valeur définie par le fournisseur, mais la valeur 0 (zéro) est généralement réservée pour indiquer la réussite. Cette propriété est héritée de [**\_ \_ NotifyStatus**](--notifystatus.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **Win32 \_ PrivilegesStatus** est dérivée de [**\_ \_ ExtendedStatus**](--extendedstatus.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                     |
| Espace de noms<br/>                | \\WMI racine<br/>                                                               |
| MOF<br/>                      | <dl> <dt>WMI. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_ExtendedStatus**](--extendedstatus.md)
</dt> </dl>

 

 




