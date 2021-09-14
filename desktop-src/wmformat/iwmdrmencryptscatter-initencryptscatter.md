---
title: Méthode IWMDRMEncryptScatter InitEncryptScatter (wmdrmsdk. h)
description: La méthode InitEncryptScatter Initialise l’interface IWMDRMEncryptScatter à utiliser.
ms.assetid: c5f2fa14-9465-4c53-bc42-ffcec34af083
keywords:
- Méthode InitEncryptScatter format Windows Media
- Méthode InitEncryptScatter format Windows Media, interface IWMDRMEncryptScatter
- Interface IWMDRMEncryptScatter Windows Media format, méthode InitEncryptScatter
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.InitEncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef788ecbe85defc7d3593f0c12c035e516f095eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219508"
---
# <a name="iwmdrmencryptscatterinitencryptscatter-method"></a>IWMDRMEncryptScatter :: InitEncryptScatter, méthode

La méthode **InitEncryptScatter** Initialise l’interface **IWMDRMEncryptScatter** à utiliser.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT InitEncryptScatter(
  [in] DWORD                      cStreams,
  [in] WMDRM_ENCRYPT_SCATTER_INFO *rgInfos
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cStreams* \[ dans\]
</dt> <dd>

Nombre d’éléments dans le tableau *rgInfos* . Il s’agit également du nombre de flux inclus dans les données à chiffrer.

</dd> <dt>

*rgInfos* \[ dans\]
</dt> <dd>

Tableau d’une ou de plusieurs structures d' [**\_ informations de \_ diffusion \_ de chiffrement WMDRM**](wmdrm-encrypt-scatter-info.md) . Chaque élément contient des informations de chiffrement pour un flux. Le nombre d’éléments de ce tableau doit être égal à la valeur de *cStreams*.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Aucun.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md)
</dt> <dt>

[**Interface IWMDRMEncryptScatter**](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





