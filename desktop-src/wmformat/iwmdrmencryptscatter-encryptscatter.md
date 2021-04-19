---
title: Méthode IWMDRMEncryptScatter EncryptScatter (wmdrmsdk. h)
description: La méthode EncryptScatter déchiffre et chiffre les données.
ms.assetid: e7f87aac-387b-4483-956e-bfbca0cec0f2
keywords:
- Méthode EncryptScatter format Windows Media
- Méthode EncryptScatter format Windows Media, interface IWMDRMEncryptScatter
- Interface IWMDRMEncryptScatter Windows Media format, méthode EncryptScatter
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.EncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58b2d1d6182aed55b60aa1cedfbce5dd870691bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542428"
---
# <a name="iwmdrmencryptscatterencryptscatter-method"></a>IWMDRMEncryptScatter :: EncryptScatter, méthode

La méthode **EncryptScatter** déchiffre et chiffre les données.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EncryptScatter(
  [in]  DWORD                       cBlocks,
  [in]  WMDRM_ENCRYPT_SCATTER_BLOCK *rgBlocks,
  [in]  WMDRMCryptoData             *pWMCryptoData,
  [in]  DWORD                       cbOutput,
  [out] BYTE                        *pbOutput
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cBlocks* \[ dans\]
</dt> <dd>

Nombre d’éléments dans le tableau *rgBlocks* .

</dd> <dt>

*rgBlocks* \[ dans\]
</dt> <dd>

Tableau d’une ou de plusieurs structures de [**\_ blocs de \_ diffusion \_ de chiffrement WMDRM**](wmdrm-encrypt-scatter-block.md) . Chaque élément décrit un bloc de données à déchiffrer et à chiffrer.

</dd> <dt>

*pWMCryptoData* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**WMDRMCryptoData**](wmdrmcryptodata.md) qui contient des paramètres de chiffrement. Affectez la valeur **null** pour utiliser les paramètres par défaut.

</dd> <dt>

*cbOutput* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon de données de sortie passée en tant que *pbOutput*.

</dd> <dt>

*pbOutput* \[ à\]
</dt> <dd>

Mémoire tampon de sortie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Aucun.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**InitEncryptScatter**](iwmdrmencryptscatter-initencryptscatter.md)
</dt> <dt>

[**Interface IWMDRMEncryptScatter**](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





