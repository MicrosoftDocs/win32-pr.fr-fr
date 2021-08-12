---
description: La structure DIBDATA contient des informations sur une image bitmap indépendante du périphérique (DIB) GDI.
ms.assetid: abbfa5b4-8789-4a44-a467-5812d3cc8238
title: DIBDATA, structure (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIBDATA
api_type:
- HeaderDef
api_location:
- Winutil.h
ms.openlocfilehash: b4449f45afac56b202e9b23516dc849c6364e8781be7cfbe7cfb2b630bd16921
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118653816"
---
# <a name="dibdata-structure"></a>DIBDATA, structure

La `DIBDATA` structure contient des informations sur une image bitmap indépendante du périphérique (DIB) GDI.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagDIBDATA {
  LONG       PaletteVersion;
  DIBSECTION DibSection;
  HBITMAP    hBitmap;
  HANDLE     hMapping;
  BYTE       *pBase;
} DIBDATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**PaletteVersion**
</dt> <dd>

Ce membre doit être incrémenté à chaque modification de la palette.

</dd> <dt>

**DibSection**
</dt> <dd>

Structure **DIBSECTION** qui contient des informations sur le dib. Pour plus d’informations, consultez la documentation GDI.

</dd> <dt>

**hBitmap**
</dt> <dd>

Handle de l’image bitmap.

</dd> <dt>

**hMapping**
</dt> <dd>

Handle vers un objet de mappage de fichiers utilisé pour partager la mémoire entre GDI et un objet [**CImageSample**](cimagesample.md) .

</dd> <dt>

**pBase**
</dt> <dd>

Adresse de l’image bitmap.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl> |



 

 




