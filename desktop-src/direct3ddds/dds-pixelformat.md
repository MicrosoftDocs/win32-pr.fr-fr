---
title: Structure de DDS_PIXELFORMAT (DDS. h)
description: Format de pixel de surface.
ms.assetid: 39c5e48d-cf20-4d77-80d5-a67f04de4883
keywords:
- DDS_PIXELFORMAT de la structure DDS
topic_type:
- apiref
api_name:
- DDS_PIXELFORMAT
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08e2c8d4b5e30a3a5a9a039e27f5704019a6300c
ms.sourcegitcommit: 205567a2a76ad672a493a0203ff9d61271d9df98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/18/2021
ms.locfileid: "122358905"
---
# <a name="dds_pixelformat-structure"></a>\_Structure DDS PIXELFORMAT

Format de pixel de surface.

## <a name="syntax"></a>Syntaxe


```C++
struct DDS_PIXELFORMAT {
  DWORD dwSize;
  DWORD dwFlags;
  DWORD dwFourCC;
  DWORD dwRGBBitCount;
  DWORD dwRBitMask;
  DWORD dwGBitMask;
  DWORD dwBBitMask;
  DWORD dwABitMask;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**dwSize nul**
</dt> <dd>

Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Taille de la structure ; Affectez la valeur 32 (octets).

</dd> <dt>

**dwFlags**
</dt> <dd>

Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valeurs qui indiquent le type de données dans la surface.



| Indicateur              | Description                                                                                                                                                                                                                                | Valeur   |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|
| DDPF \_ ALPHAPIXELS | La texture contient des données alpha ; **dwRGBAlphaBitMask** contient des données valides.                                                                                                                                                                    | 0x1     |
| DDPF \_ alpha       | Utilisé dans certains fichiers DDS plus anciens pour les données non compressées du canal alpha (dwRGBBitCount contient le canal alpha bitCount ; dwABitMask contient des données valides)                                                                                  | 0x2     |
| DDPF \_ FourCC      | La texture contient des données RVB compressées ; **dwFourCC** contient des données valides.                                                                                                                                                                    | 0x4     |
| DDPF \_ RGB         | La texture contient des données RVB non compressées ; **dwRGBBitCount** et les masques RGB (**dwRBitMask**, **dwGBitMask**, **dwBBitMask**) contiennent des données valides.                                                                                           | 0x40    |
| DDPF \_ YUV         | Utilisé dans certains fichiers DDS plus anciens pour les données non compressées YUV (dwRGBBitCount contient le nombre de bits YUV ; dwRBitMask contient le masque Y, dwGBitMask contient le masque U, dwBBitMask contient le masque V)                                          | 0x200   |
| \_luminance DDPF   | Utilisé dans certains fichiers DDS plus anciens pour les données non compressées de couleur de canal unique (dwRGBBitCount contient le nombre de bits de canal luminance ; dwRBitMask contient le masque de canal). Peut être combiné avec DDPF \_ ALPHAPIXELS pour un fichier DDS à deux canaux. | 0x20000 |



 

</dd> <dt>

**dwFourCC**
</dt> <dd>

Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Codes à quatre caractères pour spécifier des formats compressés ou personnalisés. Les valeurs possibles sont les suivantes : *DXT1*, *DXT2*, *DXT3*, *DXT4* ou *DXT5*. Un FourCC de facilement indique prescense de l’en [**-tête DDS \_ \_ DXT10**](dds-header-dxt10.md) en-tête étendu, et le membre dxgiFormat de cette structure indique le format réel. Lorsque vous utilisez un code à quatre caractères, dwFlags doit inclure *DDPF \_ FourCC*.

</dd> <dt>

**dwRGBBitCount**
</dt> <dd>

Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre de bits dans un format RVB (éventuellement, y compris alpha). Valide lorsque **dwFlags** comprend *DDPF \_ RGB*, *DDPF \_ luminance* ou *DDPF \_ YUV*.

</dd> <dt>

**dwRBitMask**
</dt> <dd>

Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Masque rouge (ou luminance ou Y) pour la lecture des données de couleur. Par exemple, étant donné le format A8R8G8B8, le masque rouge est 0x00FF0000.

</dd> <dt>

**dwGBitMask**
</dt> <dd>

Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Masque vert (ou U) pour la lecture des données de couleur. Par exemple, étant donné le format A8R8G8B8, le masque vert est 0x0000ff00.

</dd> <dt>

**dwBBitMask**
</dt> <dd>

Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Masque bleu (ou V) pour la lecture des données de couleur. Par exemple, étant donné le format A8R8G8B8, le masque bleu est 0x000000FF.

</dd> <dt>

**dwABitMask**
</dt> <dd>

Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Masque Alpha pour la lecture des données alpha. dwFlags doit inclure *DDPF \_ ALPHAPIXELS* ou *DDPF \_ alpha*. Par exemple, étant donné le format A8R8G8B8, le masque Alpha est 0xFF000000.

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour stocker des formats DXGI tels que des données à virgule flottante, utilisez un **dwFlags** de DDPF \_ FourCC et définissez **dwFourCC** sur’d', 'X', ' 1 ', ' 0 '. Utilisez l’en-tête d’extension DXT10 de l' [**\_ en-tête \_ DDS**](dds-header-dxt10.md) pour stocker le format dxgi dans le membre **dxgiFormat** .

Notez qu’il existe des variantes de fichiers DDS non standard pour lesquelles **dwFlags** a DDPF \_ FourCC et la valeur **dwFourCC** est directement définie sur une valeur d' \_ énumération de format D3DFORMAT ou DXGI. Il n’est pas possible de lever l’ambiguïté entre les valeurs de format D3DFORMAT et DXGI \_ à l’aide de ce schéma non standard. par conséquent, l’en-tête d’extension facilement est recommandé à la place.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DDS. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence pour DDS](dx-graphics-dds-reference.md)
</dt> </dl>

 

