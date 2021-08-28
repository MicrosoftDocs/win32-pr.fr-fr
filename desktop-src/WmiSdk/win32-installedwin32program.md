---
title: '\_Classe InstalledWin32Program Win32'
description: La \_ classe Win32 InstalledWin32Program représente une application Win32 installée.
ms.assetid: 2eef00da-8597-4852-b4fb-4276d05fd724
keywords:
- Application de la classe Win32_InstalledWin32Program et fournisseur d’inventaire des appareils
- Application de la classe Win32_InstalledWin32Program et fournisseur d’inventaire des appareils, Description
topic_type:
- apiref
api_name:
- Win32_InstalledWin32Program
- Win32_InstalledWin32Program.ProgramId
- Win32_InstalledWin32Program.Name
- Win32_InstalledWin32Program.Vendor
- Win32_InstalledWin32Program.Version
- Win32_InstalledWin32Program.Language
- Win32_InstalledWin32Program.MsiPackageCode
- Win32_InstalledWin32Program.MsiProductCode
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
ms.openlocfilehash: 51cfbf56591bca71f8364d97a9a4adb0d995c4c3
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122917902"
---
# <a name="win32_installedwin32program-class"></a>\_Classe InstalledWin32Program Win32

La classe **Win32 \_ InstalledWin32Program** représente une application Win32 installée.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
class Win32_InstalledWin32Program
{
  string ProgramId;
  string Name;
  string Vendor;
  string Version;
  string Language;
  string MsiPackageCode;
  string MsiProductCode;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ InstalledWin32Program** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ InstalledWin32Program** a ces propriétés.

<dl> <dt>

**Langage**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Langues prises en charge pour l’application Win32 installée.

</dd> <dt>

**MsiPackageCode**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Code du package MSI, si l’application Win32 a été installée à l’aide d’un MSI.

</dd> <dt>

**MsiProductCode**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Code du produit MSI, si l’application Win32 a été installée à l’aide d’un MSI.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de l’application Win32 installée.

</dd> <dt>

**ProgramId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Identificateur unique de l’application Win32 installée. Cette valeur aide à mettre en corrélation les **\_ InstalledWin32Program Win32** avec [**Win32 \_ InstalledProgramFramework**](win32-installedprogramframework.md).

</dd> <dt>

**Fournisseur**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Serveur de publication de l’application Win32 installée.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Version de l’application Win32 installée.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| Espace de noms<br/>                | Racine\\CIMv2<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Aeinv. mof</dt> </dl> |



 

 





