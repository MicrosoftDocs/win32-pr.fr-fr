---
description: Classe FileIo_Name-cette classe est la classe de type d’événement pour les événements d’e/s de fichier. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: ed72daa3-06c0-46f1-bb9d-c0b343228f28
title: Classe FileIo_Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Name
- FileIo_Name.FileObject
- FileIo_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 147e7fd2cb28f7245d8366dc66d7b3859f37586f1bd7c9c0b96d2d7ef57e35d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829711"
---
# <a name="fileio_name-class"></a>\_Classe de nom FileIo

Cette classe est la classe de type d’événement pour les événements d’e/s de fichier.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{0, 32, 35, 36}, EventTypeName{"Name", "FileCreate", "FileDelete", "FileRundown"}]
class FileIo_Name : FileIo
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a>Membres

La classe de **\_ nom FileIo** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe de **\_ nom FileIo** possède les propriétés suivantes.

<dl> <dt>

FileName
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2), StringTermination ("NullTerminated"), format ("w")
</dt> </dl>

Chemin d’accès complet au fichier, à l’exclusion de la lettre de lecteur.

</dd> <dt>

FileObject
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1), pointeur
</dt> </dl>

Faire correspondre la valeur de ce pointeur à la valeur de pointeur **FileObject** dans un événement [**\_ TypeGroup1 e**](diskio-typegroup1.md) pour déterminer le type d’opération d’e/s.

</dd> </dl>

## <a name="remarks"></a>Remarques

**Windows Server 2003 :** Pour récupérer la lettre de lecteur pour le chemin d’accès au nom de fichier, utilisez la valeur de propriété **FileObject** pour effectuer un mappage à l’événement [ \_ TypeGroup1 e](diskio-typegroup1.md) correspondant. À partir de l' \_ événement e TypeGroup1, utilisez les valeurs de propriété **DiskNumber** et **ByteOffset** pour mapper à l’événement SystemConfig [ \_ LogDisk](systemconfig-logdisk.md) correspondant (**ByteOffset** est mappé à **StartOffset**). La propriété **DriveLetterString** contient la lettre de lecteur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Value |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




