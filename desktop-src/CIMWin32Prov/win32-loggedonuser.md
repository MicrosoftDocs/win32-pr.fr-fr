---
description: La \_ classe WMI de l’Association LoggedOnUser Win32 lie une session et un compte d’utilisateur.
ms.assetid: b1233f90-4898-4ced-84d2-0858027e935a
ms.tgt_platform: multiple
title: Classe Win32_LoggedOnUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoggedOnUser
- Win32_LoggedOnUser.Dependent
- Win32_LoggedOnUser.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73cb34246f7b31393527aef053c0cb8cbd12702217dd7113d5714ac022bc3716
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973444"
---
# <a name="win32_loggedonuser-class"></a>\_Classe LoggedOnUser Win32

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ LoggedOnUser Win32** lie une session et un compte d’utilisateur.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8BB5B3EC-E1F7-4b39-942A-605D5F55789A}"), AMENDMENT]
class Win32_LoggedOnUser : CIM_Dependency
{
  Win32_LogonSession REF Dependent;
  Win32_Account      REF Antecedent;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ LoggedOnUser** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ LoggedOnUser** a ces propriétés.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données **: \_ compte Win32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent), [**Key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

[**\_ Compte Win32**](win32-account.md) qui décrit le compte utilisé lors de l’initiation de cette session. Le compte peut être un compte d’utilisateur ou un compte système.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ LogonSession**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (dépendant), [**clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

[**\_ LogonSession Win32**](win32-logonsessionmappeddisk.md) qui décrit la session actuellement utilisée par le compte.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **Win32 \_ LoggedOnUser** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).

## <a name="examples"></a>Exemples

L’exemple PowerShell de [fonction loggedonuser](https://Gallery.TechNet.Microsoft.Com/scriptcenter/0e43993a-895a-4afe-a2b2-045a5146048a) obtient les utilisateurs connectés sur un ordinateur local ou distant, avec les informations de session.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Dépendance CIM**](cim-dependency.md)
</dt> <dt>

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

