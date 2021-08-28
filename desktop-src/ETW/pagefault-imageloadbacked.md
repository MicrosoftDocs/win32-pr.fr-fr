---
description: Cette classe est la classe de type d’événement pour le chargement d’image dans les événements de fichier d’échange. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 7d2f08e8-ec1f-4630-922a-548b55eadfda
title: Classe PageFault_ImageLoadBacked
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_ImageLoadBacked
- PageFault_ImageLoadBacked.FileObject
- PageFault_ImageLoadBacked.DeviceChar
- PageFault_ImageLoadBacked.FileChar
- PageFault_ImageLoadBacked.LoadFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 75104fcf923ed59bfcc99e214e66a235549b7059ca0e36c41b6f90d308a3efff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811769"
---
# <a name="pagefault_imageloadbacked-class"></a>PageFault \_ ImageLoadBacked, classe

Cette classe est la classe de type d’événement pour le chargement d’image dans les événements de fichier d’échange.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{105}, EventTypeName{"ImageLoadBacked"}]
class PageFault_ImageLoadBacked : PageFault_V2
{
  uint32 FileObject;
  uint32 DeviceChar;
  uint16 FileChar;
  uint16 LoadFlags;
};
```

## <a name="members"></a>Membres

La classe **PageFault \_ ImageLoadBacked** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **PageFault \_ ImageLoadBacked** possède les propriétés suivantes.

<dl> <dt>

**DeviceChar**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2), format ("x")
</dt> </dl>

Réservé.

</dd> <dt>

**FileChar**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (3), format ("x")
</dt> </dl>

Réservé.

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1), pointeur
</dt> </dl>

Faire correspondre la valeur de ce pointeur à la valeur de pointeur **FileObject** dans un événement de [**\_ nom FileIo**](fileio-name.md) pour déterminer le nom du fichier.

</dd> <dt>

**LoadFlags**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (4), format ("x")
</dt> </dl>

Réservé.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’événement est enregistré lors de la création d’une section d’image (par exemple, un chargement de DLL) lorsque le gestionnaire de mémoire détermine que l’image doit être copiée et exécutée à partir du fichier d’échange. En règle générale, les images sont exécutées à partir du fichier source, mais la sauvegarde du fichier d’échange peut se produire lorsque le gestionnaire de mémoire détermine que le fichier source peut être modifié de façon asynchrone par des Writers existants ou lorsque le fichier source se trouve sur un support amovible ou un périphérique distant.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PageFault \_ v2**](pagefault-v2.md)
</dt> </dl>

 

 




