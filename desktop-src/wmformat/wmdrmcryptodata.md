---
title: WMDRMCryptoData, structure (wmdrmsdk. h)
description: La structure WMDRMCryptoData contient des informations sur l’algorithme de chiffrement utilisé pour chiffrer et déchiffrer le contenu.
ms.assetid: ad14c6d3-4305-47c0-8f67-7ef6d11cc326
keywords:
- Structure WMDRMCryptoData format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WMDRMCryptoData
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a732b7c1c4a4ca8d664255d39573b10ac1bdd4d004deb73d723a43b55db70ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083803"
---
# <a name="wmdrmcryptodata-structure"></a>WMDRMCryptoData, structure

La structure **WMDRMCryptoData** contient des informations sur l’algorithme de chiffrement utilisé pour chiffrer et déchiffrer le contenu.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct WMDRMCryptoData {
  DRM_CRYPTO_TYPE  cryptoType;
  unsigned __int64 qwCounterID;
  unsigned __int64 qwOffset;
} ;
```



## <a name="members"></a>Membres

<dl> <dt>

**cryptoType**
</dt> <dd>

Membre de l’énumération de [**\_ \_ type de chiffrement DRM**](drm-crypto-type.md) spécifiant le type d’algorithme de chiffrement.

</dd> <dt>

**qwCounterID**
</dt> <dd>

64 bits de poids fort du mode de compteur AES 128 bits. Ce membre est utilisé uniquement si le membre **cryptoType** est défini sur le **type de chiffrement \_ \_ MCE**.

</dd> <dt>

**qwOffset**
</dt> <dd>

64 bits de poids faible du mode de compteur AES 128 bits. Ce membre est utilisé uniquement si le membre **cryptoType** est défini sur le **type de chiffrement \_ \_ MCE**.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures**](drm-structures.md)
</dt> </dl>

 

 





