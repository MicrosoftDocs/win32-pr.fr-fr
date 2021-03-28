---
description: Cette classe est la classe de type d’événement pour les événements de chargement d’image. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: e2836153-8e4f-4c7f-9542-9402ed9e4356
title: Classe Image_V0_Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V0_Load
- Image_V0_Load.BaseAddress
- Image_V0_Load.ModuleSize
- Image_V0_Load.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: b2486e6918884e51a57f077dc9c569f926dc902e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971934"
---
# <a name="image_v0_load-class"></a>Classe de charge d’image \_ v0 \_

Cette classe est la classe de type d’événement pour les événements de chargement d’image.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V0_Load
{
  uint32 BaseAddress;
  uint32 ModuleSize;
  string ImageFileName;
};
```

## <a name="members"></a>Membres

La **classe \_ \_ Load de l’image v0** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe de **\_ \_ chargement image v0** possède ces propriétés.

<dl> <dt>

BaseAddress
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1), pointeur
</dt> </dl>

Adresse de base de l’application dans laquelle l’image est chargée.

</dd> <dt>

ImageFileName
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (3), StringTermination ("NullTerminated"), format ("w")
</dt> </dl>

Nom de fichier et extension de la DLL ou de l’image exécutable à charger.

</dd> <dt>

Module
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2)
</dt> </dl>

Taille de l’image.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Image \_ v0**](image-v0.md)
</dt> </dl>

 

 




