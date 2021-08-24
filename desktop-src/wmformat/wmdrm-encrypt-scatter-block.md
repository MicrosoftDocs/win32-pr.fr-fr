---
title: Structure WMDRM_ENCRYPT_SCATTER_BLOCK (wmdrmsdk. h)
description: La \_ \_ structure de bloc de diffusion de chiffrement WMDRM \_ contient un bloc de données à chiffrer.
ms.assetid: 73c871f0-3d0d-480f-856c-0f7d5dde5895
keywords:
- Structure WMDRM_ENCRYPT_SCATTER_BLOCK format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_BLOCK
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 258cb7e0d8d2cac8da40197aaa45028a56af0ff3a313d65c1a98c50d45b8d3b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658159"
---
# <a name="wmdrm_encrypt_scatter_block-structure"></a>\_Structure de \_ bloc de diffusion de CHIFFREment WMDRM \_

La structure de **\_ bloc de \_ diffusion \_ de chiffrement WMDRM** contient un bloc de données à chiffrer.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_BLOCK {
  DWORD dwStreamID;
  DWORD cbBlock;
  BYTE  *pbBlock;
} ;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwStreamID**
</dt> <dd>

Identificateur du flux auquel le bloc de données appartient.

</dd> <dt>

**cbBlock**
</dt> <dd>

Taille du bloc en octets.

</dd> <dt>

**pbBlock**
</dt> <dd>

Pointeur vers une mémoire tampon contenant le bloc de données.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure est utilisée par la méthode [**IWMDRMEncryptScatter :: EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md) pour identifier les blocs de données à chiffrer.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures**](drm-structures.md)
</dt> </dl>

 

 





