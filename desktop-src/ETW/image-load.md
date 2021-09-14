---
description: Cette classe est la classe de type d’événement pour les événements d’image. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 70ec0542-16d3-4186-a346-7f3c44dedf67
title: Classe Image_Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_Load
- Image_Load.ImageBase
- Image_Load.ImageSize
- Image_Load.ProcessId
- Image_Load.ImageCheckSum
- Image_Load.TimeDateStamp
- Image_Load.Reserved0
- Image_Load.DefaultBase
- Image_Load.Reserved1
- Image_Load.Reserved2
- Image_Load.Reserved3
- Image_Load.Reserved4
- Image_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 647879b972c7cff2c086f656f76fa8decedb49a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416894"
---
# <a name="image_load-class"></a>Classe de chargement d’image \_

Cette classe est la classe de type d’événement pour les événements d’image.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType(10, 2, 3, 4), EventTypeName("Load", "Unload", "DCStart", "DCEnd")]
class Image_Load : Image
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  uint32 ImageCheckSum;
  uint32 TimeDateStamp;
  uint32 Reserved0;
  uint32 DefaultBase;
  uint32 Reserved1;
  uint32 Reserved2;
  uint32 Reserved3;
  uint32 Reserved4;
  string FileName;
};
```

## <a name="members"></a>Membres

La classe de **\_ chargement d’image** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe de **\_ chargement d’image** possède ces propriétés.

<dl> <dt>

DefaultBase
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (7), pointeur
</dt> </dl>

Adresse de base par défaut.

</dd> <dt>

FileName
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (12), StringTermination ("NullTerminated"), format ("w")
</dt> </dl>

Nom de fichier et extension de la DLL ou de l’image exécutable.

</dd> <dt>

ImageBase
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1), pointeur
</dt> </dl>

Adresse de base de l’application dans laquelle l’image est chargée.

</dd> <dt>

ImageCheckSum
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (4)
</dt> </dl>

Somme de contrôle d’image.

</dd> <dt>

ImageSize
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2), pointeur
</dt> </dl>

Taille de l’image en cours de chargement.

Lors de l’utilisation de cette propriété, le type de données de cette propriété est taille \_ t. Le qualificateur de pointeur est utilisé pour déterminer si la taille \_ t est de 4 octets ou de 8 octets.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (3)
</dt> </dl>

Identifie le processus dans lequel l’image est chargée.

</dd> <dt>

Reserved0
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (6)
</dt> </dl>

Réservé.

</dd> <dt>

Reserved1
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (8)
</dt> </dl>

Réservé.

</dd> <dt>

Reserved2
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (9)
</dt> </dl>

Réservé.

</dd> <dt>

Reserved3
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (10)
</dt> </dl>

Réservé.

</dd> <dt>

Reserved4
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (11)
</dt> </dl>

Réservé.

</dd> <dt>

TimeDateStamp
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (5)
</dt> </dl>

Heure et date auxquelles l’image a été chargée ou déchargée.

</dd> </dl>

## <a name="remarks"></a>Notes

Les événements DCStart et DCEnd énumèrent toutes les images chargées au début et à la fin de la trace, respectivement.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Image**](image.md)
</dt> <dt>

[**Image \_ v0**](image-v0.md)
</dt> <dt>

[**Image \_ v1**](image-v1.md)
</dt> </dl>

 

 




