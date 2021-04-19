---
description: Associe un ordinateur virtuel à une connexion de terminal.
ms.assetid: 31979FB8-3870-44D9-9720-AD99237C5268
title: Classe Msvm_SystemTerminalConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemTerminalConnection
- Msvm_SystemTerminalConnection.Antecedent
- Msvm_SystemTerminalConnection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 368c25b8505ec7ddd29da3b95d95fc842602119e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544214"
---
# <a name="msvm_systemterminalconnection-class"></a>MSVM \_ SystemTerminalConnection, classe

Associe un ordinateur virtuel à une connexion de terminal.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemTerminalConnection : CIM_HostedDependency
{
  Msvm_ComputerSystem     REF Antecedent;
  Msvm_TerminalConnection REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ SystemTerminalConnection** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ SystemTerminalConnection** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ordinateur virtuel auquel la connexion est attachée.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ TerminalConnection**](msvm-terminalconnection.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

Connexion à la machine virtuelle.

</dd> </dl>

## <a name="remarks"></a>Notes

L’accès à la classe **MSVM \_ SystemTerminalConnection** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_HOSTEDDEPENDENCY CIM**](cim-hosteddependency.md)
</dt> <dt>

[**\_HOSTEDDEPENDENCY CIM**](/previous-versions//cc136861(v=vs.85))
</dt> <dt>

[Classes vidéo](video-classes.md)
</dt> </dl>

 

