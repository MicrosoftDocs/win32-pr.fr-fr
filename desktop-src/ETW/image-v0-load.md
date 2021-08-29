---
description: Classe Image_V0_Load-cette classe est la classe de type d’événement pour les événements de chargement d’image. La syntaxe suivante est simplifiée à partir du code MOF.
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
ms.openlocfilehash: 006dc57aefdec374a85167580280b171d852172bf45bf979b76948a5014f1c24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070179"
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Image \_ v0**](image-v0.md)
</dt> </dl>

 

 




