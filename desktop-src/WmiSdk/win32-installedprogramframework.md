---
title: '\_Classe InstalledProgramFramework Win32'
description: La \_ classe InstalledProgramFramework Win32 représente un Framework technologique sur lequel une \_ instance InstalledWin32Program Win32 est compilée ou utilisée au moment de l’exécution.
ms.assetid: bb5c18c7-ec71-4579-8190-942de4fccd9e
keywords:
- Application de la classe Win32_InstalledProgramFramework et fournisseur d’inventaire des appareils
- Application de la classe Win32_InstalledProgramFramework et fournisseur d’inventaire des appareils, Description
topic_type:
- apiref
api_name:
- Win32_InstalledProgramFramework
- Win32_InstalledProgramFramework.FrameworkName
- Win32_InstalledProgramFramework.FrameworkPublisher
- Win32_InstalledProgramFramework.FrameworkVersion
- Win32_InstalledProgramFramework.FrameworkVersionActual
- Win32_InstalledProgramFramework.ProgramId
- Win32_InstalledProgramFramework.IsPrivate
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
ms.openlocfilehash: 3e447544dbfdebd6e4f4dd12752171089b8da041
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122917894"
---
# <a name="win32_installedprogramframework-class"></a>\_Classe InstalledProgramFramework Win32

La **classe \_ InstalledProgramFramework Win32** représente un Framework technologique sur lequel une instance [**\_ InstalledWin32Program Win32**](win32-installedwin32program.md) est compilée ou utilisée au moment de l’exécution. les infrastructures que cette classe peut actuellement signaler sont OpenSSL, Visual Basic, Visual C++ .net, Visual C++, java (détecte uniquement les fichiers binaires du runtime Java) et CLR.

> [!Note]  
> L’ensemble des frameworks que cette classe peut détecter peut être mis à jour au fil du temps.

 

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
class Win32_InstalledProgramFramework
{
  string  FrameworkName;
  string  FrameworkPublisher;
  string  FrameworkVersion;
  string  FrameworkVersionActual;
  string  ProgramId;
  boolean IsPrivate;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ InstalledProgramFramework** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ InstalledProgramFramework** a ces propriétés.

<dl> <dt>

**FrameworkName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Nom de l’infrastructure dont dépend l’application identifiée par **ProgramId** .

</dd> <dt>

**FrameworkPublisher**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Éditeur de l’infrastructure.

</dd> <dt>

**FrameworkVersion**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Version de l’infrastructure sur laquelle l’application a une dépendance.

</dd> <dt>

**FrameworkVersionActual**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Version de l’infrastructure que l’application utilise réellement lors de l’exécution, si l’infrastructure peut être détectée.

</dd> <dt>

**IsPrivate**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

TRUE si l’application regroupe une copie privée de l’infrastructure.

</dd> <dt>

**ProgramId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Identificateur unique de l’instance de [**\_ InstalledWin32Program Win32**](win32-installedwin32program.md) , à laquelle les données de l’infrastructure sont associées.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| Espace de noms<br/>                | Racine\\CIMv2<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Aeinv. mof</dt> </dl> |



 

 





