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
ms.openlocfilehash: 87590013ef905ffbdd13dd3b767435a907b08783
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543263"
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
| En-tête<br/> | <dl> <dt>Winutil. h (include streams. h)</dt> </dl> |



 

 




