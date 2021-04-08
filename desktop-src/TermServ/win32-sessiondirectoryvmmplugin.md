---
title: Classe Win32_SessionDirectoryVMMPlugin
description: Représente un plug-in Virtual Machine Manager (VMM) inscrit auprès d’un service session Broker.
ms.assetid: b5c5deb1-6c1b-4547-a24a-db3ce6654144
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryVMMPlugin de la classe Services Bureau à distance
- Win32_SessionDirectoryVMMPlugin de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin.sName
- Win32_SessionDirectoryVMMPlugin.sProvider
- Win32_SessionDirectoryVMMPlugin.sClassID
- Win32_SessionDirectoryVMMPlugin.sServiceLocation
- Win32_SessionDirectoryVMMPlugin.Priority
- Win32_SessionDirectoryVMMPlugin.Enabled
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c5fc6b899eaa264357527eb107e11ad5a40ad67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941809"
---
# <a name="win32_sessiondirectoryvmmplugin-class"></a>\_Classe SessionDirectoryVMMPlugin Win32

Représente un plug-in Virtual Machine Manager (VMM) inscrit auprès d’un service session Broker.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYVMMPLUGIN_Prov"), AMENDMENT]
class Win32_SessionDirectoryVMMPlugin
{
  string  sName;
  string  sProvider;
  string  sClassID;
  string  sServiceLocation;
  sint32  Priority = 0;
  boolean Enabled = FALSE;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ SessionDirectoryVMMPlugin** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ SessionDirectoryVMMPlugin** possède ces méthodes.



| Méthode                                                                             | Description                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------|
| [**GetCurrentVMMPlugin**](getcurrentvmmplugin-win32-sessiondirectoryvmmplugin.md) | Obtient le plug-in avec la priorité la plus élevée qui est activé.<br/> |
| [**RegisterVMMPlugin**](registervmmplugin-win32-sessiondirectoryvmmplugin.md)     | Inscrit un nouveau plug-in VMM.<br/>                       |
| [**SetEnabled**](setenabled-win32-sessiondirectoryvmmplugin.md)                   | Active ou désactive le plug-in.<br/>                   |
| [**SetName**](setname-win32-sessiondirectoryvmmplugin.md)                         | Définit le nom du plug-in.<br/>                      |
| [**SetPriority**](setpriority-win32-sessiondirectoryvmmplugin.md)                 | Définit la priorité du plug-in.<br/>                  |
| [**SetProvider**](setprovider-win32-sessiondirectoryvmmplugin.md)                 | Définit le nom du fournisseur du plug-in.<br/>             |
| [**SetServiceLocation**](setservicelocation-win32-sessiondirectoryvmmplugin.md)   | Définit l’emplacement du service du plug-in.<br/>          |
| [**UnregisterVMMPlugin**](unregistervmmplugin-win32-sessiondirectoryvmmplugin.md) | Annule l’inscription du plug-in.<br/>                           |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ SessionDirectoryVMMPlugin** a ces propriétés.

<dl> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le plug-in est activé ou désactivé. **True** si le plug-in est activé ou **false** dans le cas contraire. Le plug-in est désactivé par défaut.

</dd> <dt>

**Priorité**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Priorité du plug-in. Plus la valeur est élevée, plus la priorité du plug-in est élevée. La priorité est égale à zéro par défaut.

</dd> <dt>

**sClassID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur de classe du plug-in.

</dd> <dt>

**sName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom du plug-in.

</dd> <dt>

**sProvider**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom du fournisseur de plug-ins.

</dd> <dt>

**sServiceLocation**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Emplacement du service que le plug-in doit contacter.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                      |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

