---
title: Classe Win32_RDMSPublishedApplication
description: Gère une application publiée.
ms.assetid: 7a529f1d-1aaf-42fb-8469-92d38a7b0ffc
ms.tgt_platform: multiple
keywords:
- Win32_RDMSPublishedApplication de la classe Services Bureau à distance
- Win32_RDMSPublishedApplication de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDMSPublishedApplication
- Win32_RDMSPublishedApplication.AppAlias
- Win32_RDMSPublishedApplication.PoolName
- Win32_RDMSPublishedApplication.DisplayName
- Win32_RDMSPublishedApplication.ShowInPortal
- Win32_RDMSPublishedApplication.SecurityDescriptor
- Win32_RDMSPublishedApplication.AppPath
- Win32_RDMSPublishedApplication.VirtualPath
- Win32_RDMSPublishedApplication.CommandLineSetting
- Win32_RDMSPublishedApplication.RequiredCommandLine
- Win32_RDMSPublishedApplication.Folder
- Win32_RDMSPublishedApplication.IconPath
- Win32_RDMSPublishedApplication.IconIndex
- Win32_RDMSPublishedApplication.IconContents
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb003faf5e51c9da1f46f23c5f8d6b5ae977987c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317426"
---
# <a name="win32_rdmspublishedapplication-class"></a>\_Classe RDMSPublishedApplication Win32

Gère une application publiée.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSPublishedApplication
{
  string  AppAlias;
  string  PoolName;
  string  DisplayName;
  boolean ShowInPortal;
  string  SecurityDescriptor;
  string  AppPath;
  string  VirtualPath;
  uint32  CommandLineSetting;
  string  RequiredCommandLine;
  string  Folder;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ RDMSPublishedApplication** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ RDMSPublishedApplication** a ces propriétés.

<dl> <dt>

**AppAlias**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtient et définit l’alias de l’application.

</dd> <dt>

**AppPath**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit le chemin d’accès à l’application.

</dd> <dt>

**CommandLineSetting**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit le paramètre de ligne de commande pour l’application.

Cette propriété peut prendre les valeurs suivantes :

<dt>

<span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>

<span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0)


</dt> <dd>

N’autorisez pas les arguments de ligne de commande.

</dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Autoriser** (1)


</dt> <dd>

Autorisez les arguments de ligne de commande.

</dd> <dt>

<span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>

<span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Exiger** (2)


</dt> <dd>

Exiger des arguments de ligne de commande.

</dd> </dl>

</dd> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit le nom complet de l’application.

</dd> <dt>

**Folder**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit le chemin d’accès à l’application.

</dd> <dt>

**IconContents**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit un tableau qui contient l’icône de l’application.

</dd> <dt>

**IndexIcône**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit l’index de l’icône de l’application.

</dd> <dt>

**IconPath**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit le chemin d’accès à l’icône pour cette application.

</dd> <dt>

**PoolName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtient et définit le nom du pool d’applications de l’application.

</dd> <dt>

**RequiredCommandLine**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit les arguments de ligne de commande requis pour l’application.

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtient et définit le descripteur de sécurité qui contrôle l’accès à l’application, au format SDDL (Security Descriptor Definition Language).

</dd> <dt>

**ShowInPortal**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique s’il faut afficher l’application dans les Accès web Terminal Services (TS Accès web). **True** pour afficher l’application dans les accès Web TS ; Sinon, **false**.

</dd> <dt>

**VirtualPath**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit le chemin d’accès virtuel à l’application.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                              |
| Espace de noms<br/>                | Racine \\ cimv2 cimv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fournisseur de services de gestion Bureau à distance](rdms-api-reference.md)
</dt> </dl>

 

