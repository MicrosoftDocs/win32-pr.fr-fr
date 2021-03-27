---
description: Cette classe est la classe de type d’événement pour les événements de chargement d’image. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 43bf0b2b-3ab4-4561-b48c-65fbace38a79
title: Classe Image_V1_Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V1_Load
- Image_V1_Load.ImageBase
- Image_V1_Load.ImageSize
- Image_V1_Load.ProcessId
- Image_V1_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: bd0a2a61b263ce78c2cf28cdf1cd5df4b702140d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971931"
---
# <a name="image_v1_load-class"></a>\_Classe de \_ charge image v1

Cette classe est la classe de type d’événement pour les événements de chargement d’image.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V1_Load : Image_V1
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  string FileName;
};
```

## <a name="members"></a>Membres

La **classe \_ \_ Load de l’image v1** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe de **\_ \_ chargement image v1** possède ces propriétés.

<dl> <dt>

FileName
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (4), StringTermination ("NullTerminated"), format ("w")
</dt> </dl>

Nom de fichier et extension de la DLL ou de l’image exécutable à charger.

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

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Image \_ v1**](image-v1.md)
</dt> </dl>

 

 




