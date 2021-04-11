---
title: Classe Win32_SessionDirectoryVirtualDesktopServer
description: Représente un serveur de serveur hôte de virtualisation des services Bureau à distance (hôte de virtualisation des services Bureau à distance) joint à un service session Broker.
ms.assetid: a09221bd-d1b1-465b-91bb-9ca400a796b1
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryVirtualDesktopServer de la classe Services Bureau à distance
- Win32_SessionDirectoryVirtualDesktopServer de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVirtualDesktopServer
- Win32_SessionDirectoryVirtualDesktopServer.Name
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2940679c13c5bd86f7d6b02340698f529e8149e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032578"
---
# <a name="win32_sessiondirectoryvirtualdesktopserver-class"></a>\_Classe SessionDirectoryVirtualDesktopServer Win32

Représente un serveur de serveur hôte de virtualisation des services Bureau à distance (hôte de virtualisation des services Bureau à distance) joint à un service session Broker.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_SDVirtualDesktopServer_Prov"), AMENDMENT]
class Win32_SessionDirectoryVirtualDesktopServer
{
  string Name;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ SessionDirectoryVirtualDesktopServer** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ SessionDirectoryVirtualDesktopServer** a ces propriétés.

<dl> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nom DNS du serveur hôte de virtualisation des services Bureau à distance. Ce nom se présente sous la forme «*MachineName*. *Domain*. com».

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                      |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

