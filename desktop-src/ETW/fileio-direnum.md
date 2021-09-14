---
description: Cette classe est la classe de type d’événement pour les événements d’énumération de notifications de répertoires et de répertoires. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 08458385-6066-4523-a053-aceb5e5d6f10
title: Classe FileIo_DirEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_DirEnum
- FileIo_DirEnum.IrpPtr
- FileIo_DirEnum.TTID
- FileIo_DirEnum.FileObject
- FileIo_DirEnum.FileKey
- FileIo_DirEnum.Length
- FileIo_DirEnum.InfoClass
- FileIo_DirEnum.FileIndex
- FileIo_DirEnum.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 12f8fd8b4629ac11e7316caae0690982c210e4bc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416921"
---
# <a name="fileio_direnum-class"></a>FileIo \_ DirEnum, classe

Cette classe est la classe de type d’événement pour les événements d’énumération de notifications de répertoires et de répertoires.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{72, 77}, EventTypeName{"DirEnum", "DirNotify"}]
class FileIo_DirEnum : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 Length;
  uint32 InfoClass;
  uint32 FileIndex;
  string FileName;
};
```

## <a name="members"></a>Membres

La classe **FileIo \_ DirEnum** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **FileIo \_ DirEnum** possède les propriétés suivantes.

<dl> <dt>

**FileIndex**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (7)
</dt> </dl>

Index de fichier à partir duquel continuer l’énumération de répertoires.

</dd> <dt>

**FileKey**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (4), pointeur
</dt> </dl>

Pour déterminer le nom du répertoire, faites correspondre la valeur de cette propriété à la propriété **FileObject** d’un événement de [**\_ nom FileIo**](fileio-name.md) .

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (8), StringTermination ("NullTerminated"), format ("w")
</dt> </dl>

Modèle spécifié pour l’énumération de répertoires.

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (3), pointeur
</dt> </dl>

Identificateur qui peut être utilisé pour mettre en corrélation des opérations avec la même instance d’objet de fichier ouverte entre les événements de création et de fermeture de fichier.

</dd> <dt>

**InfoClass**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (6), pointeur
</dt> </dl>

Classe d’informations d’énumération de répertoire demandée.

</dd> <dt>

**IrpPtr**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1), pointeur
</dt> </dl>

Paquet de demande d’e/s. Cette propriété identifie l’activité d’e/s.

</dd> <dt>

**Durée**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (5)
</dt> </dl>

Taille de la mémoire tampon de requête, en octets.

</dd> <dt>

**TTID**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2), pointeur
</dt> </dl>

Identificateur du thread qui effectue l’opération.

</dd> </dl>

## <a name="remarks"></a>Notes

L’énumération de répertoires et les événements de notification d’annuaire sont enregistrés lorsqu’un répertoire est énuméré ou lorsqu’une notification de modification de répertoire est envoyée aux écouteurs inscrits, respectivement.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




