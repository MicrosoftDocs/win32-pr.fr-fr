---
title: '\_Classe InstalledStoreProgram Win32'
description: la \_ classe InstalledStoreProgram Win32 représente une application Windows store installée.
ms.assetid: 154c19c7-f2e5-48bd-b05b-3022e45f2aa4
keywords:
- Application de la classe Win32_InstalledStoreProgram et fournisseur d’inventaire des appareils
- Application de la classe Win32_InstalledStoreProgram et fournisseur d’inventaire des appareils, Description
topic_type:
- apiref
api_name:
- Win32_InstalledStoreProgram
- Win32_InstalledStoreProgram.ProgramId
- Win32_InstalledStoreProgram.Name
- Win32_InstalledStoreProgram.Vendor
- Win32_InstalledStoreProgram.Version
- Win32_InstalledStoreProgram.Language
- Win32_InstalledStoreProgram.Architecture
api_location:
- Root\CIMv2
api_type:
- Schema
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 613baba9990da8403417aa4f8639ed7e9b5a7a5f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122917908"
---
# <a name="win32_installedstoreprogram-class"></a>\_Classe InstalledStoreProgram Win32

la **classe \_ InstalledStoreProgram Win32** représente une application Windows store installée.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
class Win32_InstalledStoreProgram
{
  string ProgramId;
  string Name;
  string Vendor;
  string Version;
  string Language;
  string Architecture;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ InstalledStoreProgram** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ InstalledStoreProgram** a ces propriétés.

<dl> <dt>

**Architecture**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

architectures de processeur prises en charge pour l’application Windows store.

</dd> <dt>

**Langage**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

langues prises en charge pour l’application Windows store.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

nom de l’application Windows store.

</dd> <dt>

**ProgramId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

identificateur unique de l’application Windows store.

</dd> <dt>

**Fournisseur**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

éditeur de l’application Windows store.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

version de l’application Windows store.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| Espace de noms<br/>                | Racine\\CIMv2<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Aeinv. mof</dt> </dl> |



 

 





