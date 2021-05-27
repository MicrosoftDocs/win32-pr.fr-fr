---
UID: NS:dwrite_3.DWRITE_BITMAP_DATA_BGRA32
title: DWRITE_BITMAP_DATA_BGRA32 (dwrite_3.h)
description: Représente des données bitmap au format BGRA32.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite_3.h
req.include-header: dwrite_core.h
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWRITE_BITMAP_DATA_BGRA32
- dwrite_3/DWRITE_BITMAP_DATA_BGRA32
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite_3.h
api_name:
- DWRITE_BITMAP_DATA_BGRA32
ms.openlocfilehash: 813f3601cac03dcf477fa40f6db5105e075029ab
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548924"
---
# <a name="dwrite_bitmap_data_bgra32-structure-dwrite_3h"></a>DWRITE_BITMAP_DATA_BGRA32 structure (dwrite_3. h)

Représente des données bitmap au format BGRA32.

> [!IMPORTANT]
> Cette API est disponible dans le cadre de l’implémentation DWriteCore de [DirectWrite](../direct-write-portal.md). DWriteCore est une forme de DirectWrite qui s’exécute sur les versions de Windows jusqu’à Windows 8, et qui vous permet de l’utiliser sur plusieurs plateformes. Pour plus d’informations et pour obtenir des exemples de code, consultez [vue d’ensemble de DWriteCore](../dwritecore-overview.md).

## <a name="syntax"></a>Syntaxe

```cpp
struct DWRITE_BITMAP_DATA_BGRA32
{
  UINT32 width;
  UINT32 height;
  _Field_size_(width * height) UINT32* pixels;
};
```

## <a name="members"></a>Membres

`width`

Type : **[UInt32](../../winprog/windows-data-types.md)**

Largeur, en pixels, de la bitmap.


`height`

Type : **[UInt32](../../winprog/windows-data-types.md)**

Hauteur, en pixels, de la bitmap.


`pixels`

Type : \_ taille du champ \_ \_ (largeur * hauteur)**[UInt32](../../winprog/windows-data-types.md)\***

Pointeur vers l’emplacement des valeurs de bit de l’image bitmap.


## <a name="examples"></a>Exemples

Consultez la rubrique [vue d’ensemble de DWriteCore](../dwritecore-overview.md) et l’exemple d’application [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .

## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, réunion de projet (applications Win32) |
| **En-tête** | dwrite_3. h (inclure dwrite_core. h) |