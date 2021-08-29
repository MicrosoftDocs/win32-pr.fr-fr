---
title: Classe Win32_RDMSFileTypeAssociation
description: Gère une association de types de fichiers pour une application publiée.
ms.assetid: 22c945cb-4c47-431a-bc9b-d33ba15c8ab3
ms.tgt_platform: multiple
keywords:
- Win32_RDMSFileTypeAssociation de la classe Services Bureau à distance
- Win32_RDMSFileTypeAssociation de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDMSFileTypeAssociation
- Win32_RDMSFileTypeAssociation.AppAlias
- Win32_RDMSFileTypeAssociation.PoolName
- Win32_RDMSFileTypeAssociation.ExtName
- Win32_RDMSFileTypeAssociation.ProgIdHint
- Win32_RDMSFileTypeAssociation.IconPath
- Win32_RDMSFileTypeAssociation.IconIndex
- Win32_RDMSFileTypeAssociation.IconContents
- Win32_RDMSFileTypeAssociation.IsPrimaryHandler
- Win32_RDMSFileTypeAssociation.IsPublished
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb76c904164bcf005ccbbb8348c60d2ba91514f420ba1d62fcbb40301c8e71a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868199"
---
# <a name="win32_rdmsfiletypeassociation-class"></a>\_Classe RDMSFileTypeAssociation Win32

Gère une association de types de fichiers pour une application publiée.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSFileTypeAssociation
{
  string  AppAlias;
  string  PoolName;
  string  ExtName;
  string  ProgIdHint;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
  boolean IsPrimaryHandler;
  boolean IsPublished;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ RDMSFileTypeAssociation** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ RDMSFileTypeAssociation** a ces propriétés.

<dl> <dt>

**AppAlias**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtient et définit l’alias de l’application associée au type de fichier.

</dd> <dt>

**ExtName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtient le nom de l’extension de fichier.

</dd> <dt>

**IconContents**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit le contenu de l’icône pour le type de fichier.

</dd> <dt>

**IndexIcône**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit l’index de l’icône pour le type de fichier.

</dd> <dt>

**IconPath**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit le chemin d’accès à l’icône pour le type de fichier.

</dd> <dt>

**IsPrimaryHandler**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit une valeur qui indique si l’Association de type de fichier est pour le gestionnaire principal. **True** si l’Association de types de fichiers est destinée au gestionnaire principal ; Sinon, **false**.

</dd> <dt>

**IsPublished**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si ce Association est publié.

Obtient et définit une valeur qui indique si l’Association de types de fichiers est publiée. **True** si l’Association de types de fichiers est publiée ; Sinon, **false**.

</dd> <dt>

**PoolName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtient et définit le nom du pool d’applications pour l’Association de types de fichiers.

</dd> <dt>

**ProgIdHint**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient un indicateur pour aider les utilisateurs à ouvrir l’extension de fichier.

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

 

