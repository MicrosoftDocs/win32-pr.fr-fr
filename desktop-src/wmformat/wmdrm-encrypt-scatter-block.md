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
ms.openlocfilehash: 8911ba1822b146de4a99ff1fe144afcfd8e212e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528394"
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

## <a name="remarks"></a>Notes

Cette structure est utilisée par la méthode [**IWMDRMEncryptScatter :: EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md) pour identifier les blocs de données à chiffrer.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures**](drm-structures.md)
</dt> </dl>

 

 





