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
ms.openlocfilehash: 6e0d543fb0e57ae34f181e7ff0f40a1a1f8222b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523717"
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

## <a name="remarks"></a>Notes

La structure **D3DAES \_ CTR \_ IV** et la structure [**DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv) sont équivalentes.

Pour plus d’informations, voir [**DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                 |
| En-tête<br/>                   | <dl> <dt>D3d9types. h (inclure d3d9. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures vidéo Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




