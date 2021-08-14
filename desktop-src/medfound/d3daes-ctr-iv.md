---
description: Contient un vecteur d’initialisation (IV) pour le chiffrement par bloc du mode de chiffrement par blocs 128 Advanced Encryption Standard bits (AES-CTR).
ms.assetid: 2ee738c2-d56c-4a50-94b8-b7180918aa8c
title: Structure D3DAES_CTR_IV (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAES_CTR_IV
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 09535b432ff1af60ad33b622810d0d8a4d190cb81650214aa71b445ba3c22f4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974788"
---
# <a name="d3daes_ctr_iv-structure"></a>Structure D3DAESs \_ \_ CS

Contient un vecteur d’initialisation (IV) pour le chiffrement par bloc du mode de chiffrement par blocs 128 Advanced Encryption Standard bits (AES-CTR).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DAES_CTR_IV {
  UINT64 IV;
  UINT64 Count;
} D3DAES_CTR_IV;
```



## <a name="members"></a>Membres

<dl> <dt>

**IV**
</dt> <dd>

IV, au format Big-endian.

</dd> <dt>

**Count**
</dt> <dd>

Nombre de blocs, au format Big-endian.

</dd> </dl>

## <a name="remarks"></a>Remarques

La structure **D3DAES \_ CTR \_ IV** et la structure [**DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv) sont équivalentes.

Pour plus d’informations, voir [**DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                 |
| En-tête<br/>                   | <dl> <dt>D3d9types. h (inclure d3d9. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures vidéo Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




