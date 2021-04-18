---
title: Méthode de déchiffrement IWMDRMDecrypt (wmdrmsdk. h)
description: La méthode Decrypt déchiffre une mémoire tampon de données sur place.
ms.assetid: ca0a5b2f-d25f-423e-8956-fca264399083
keywords:
- Méthode de déchiffrement Windows Media format
- Méthode Decrypt Windows Media format, interface IWMDRMDecrypt
- Interface IWMDRMDecrypt Windows Media format, méthode Decrypt
topic_type:
- apiref
api_name:
- IWMDRMDecrypt.Decrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb3c1437bc4b4d2f442c61e54f238f176adf66b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532900"
---
# <a name="iwmdrmdecryptdecrypt-method"></a>IWMDRMDecrypt ::D méthode ecrypt

La méthode **Decrypt** déchiffre une mémoire tampon de données sur place.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Decrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbData* \[ in, out\]
</dt> <dd>

Données à déchiffrer. Si la méthode est réussie, ces données sont déchiffrées lors du retour.

</dd> <dt>

*cbData* \[ dans\]
</dt> <dd>

Taille des données en octets.

</dd> <dt>

*pWMCryptoData* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**WMDRMCryptoData**](wmdrmcryptodata.md) contenant des paramètres supplémentaires. Peut avoir la **valeur null** si le contenu a été chiffré à l’aide des paramètres par défaut.

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

[**Interface IWMDRMDecrypt**](iwmdrmdecrypt.md)
</dt> <dt>

[**WMDRMCryptoData**](wmdrmcryptodata.md)
</dt> </dl>

 

 





