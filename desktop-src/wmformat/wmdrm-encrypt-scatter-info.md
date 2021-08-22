---
title: Structure WMDRM_ENCRYPT_SCATTER_INFO (wmdrmsdk. h)
description: La structure d’informations sur le \_ nuage de points de chiffrement WMDRM \_ contient les \_ informations nécessaires à la configuration de l’interface IWMDRMEncryptScatter à utiliser.
ms.assetid: 25e19511-56ac-441b-b521-5097dd792ead
keywords:
- Structure WMDRM_ENCRYPT_SCATTER_INFO format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_INFO
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef766f40742713b01648348bedb4c1a35494fdc02d02843f8f2a41f133938a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083813"
---
# <a name="wmdrm_encrypt_scatter_info-structure"></a>\_Structure des \_ informations de diffusion de CHIFFREment WMDRM \_

La structure d’informations sur le nuage de points de **\_ chiffrement \_ \_ WMDRM** contient les informations nécessaires à la configuration de l’interface [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md) à utiliser.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_INFO {
  DWORD dwStreamID;
  DWORD dwSampleProtectionVersion;
  DWORD cbProtectionInfo;
  BYTE  *pbProtectionInfo;
} ;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwStreamID**
</dt> <dd>

Identificateur du flux à chiffrer.

</dd> <dt>

**dwSampleProtectionVersion**
</dt> <dd>

Exemple de version de protection à utiliser pour encoder les données du flux spécifié.

</dd> <dt>

**cbProtectionInfo**
</dt> <dd>

Taille de la mémoire tampon **pbProtectionInfo** en octets.

</dd> <dt>

**pbProtectionInfo**
</dt> <dd>

Mémoire tampon contenant des informations de protection supplémentaires.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure est utilisée par la méthode [**IWMDRMEncryptScatter :: InitEncryptScatter**](iwmdrmencryptscatter-initencryptscatter.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures**](drm-structures.md)
</dt> </dl>

 

 





