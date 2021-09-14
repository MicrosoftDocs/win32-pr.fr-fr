---
description: Cette classe est la classe de type d’événement pour l’événement d’informations de fichier. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 41ae1f8a-a90f-43d0-a848-a2c095f046d4
title: Classe FileIo_Info
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Info
- FileIo_Info.IrpPtr
- FileIo_Info.TTID
- FileIo_Info.FileObject
- FileIo_Info.FileKey
- FileIo_Info.ExtraInfo
- FileIo_Info.InfoClass
api_type:
- NA
api_location: ''
ms.openlocfilehash: 985986132abe432e1adefb51939b8ace1aa48c8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416920"
---
# <a name="fileio_info-class"></a>FileIo \_ info (classe)

Cette classe est la classe de type d’événement pour l’événement d’informations de fichier.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{69, 70, 71, 74, 75}, EventTypeName{"SetInfo", "Delete", "Rename", "QueryInfo", "FSControl"}]
class FileIo_Info : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 ExtraInfo;
  uint32 InfoClass;
};
```

## <a name="members"></a>Membres

La classe d' **\_ informations FileIo** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe d' **\_ informations FileIo** possède ces propriétés.

<dl> <dt>

**Argument**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (5), pointeur
</dt> </dl>

Pour les demandes FileDispositionInformation, ce champ contient la disposition demandée. Pour les demandes FileEndOfFileInformation et FileAllocationInformation, ce champ contient la taille de fichier spécifiée.

</dd> <dt>

**FileKey**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (4), pointeur
</dt> </dl>

Pour déterminer le nom de fichier, faites correspondre la valeur de cette propriété à la propriété **FileObject** d’un événement de [**\_ nom FileIo**](fileio-name.md) .

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

Qualificateurs : WmiDataId (6)
</dt> </dl>

Classe d’informations de fichier demandée.

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

Définir des informations et des événements d’informations de requête indique que les attributs de fichier ont été définis ou interrogés. Un événement de contrôle de système de fichiers (FSControl) est enregistré lors de l’émission d’une commande FSCTL.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




