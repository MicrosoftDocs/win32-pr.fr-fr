---
title: IWMDRMEncrypt, méthode de chiffrement (wmdrmsdk. h)
description: La méthode Encrypt chiffre une mémoire tampon de données en place.
ms.assetid: 9626f53e-3602-4369-99ed-fbcd8d5f4d9e
keywords:
- Méthode Encrypt Windows Media format
- Méthode Encrypt Windows Media format, interface IWMDRMEncrypt
- Interface IWMDRMEncrypt Windows Media format, méthode Encrypt
topic_type:
- apiref
api_name:
- IWMDRMEncrypt.Encrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13380b321b540cbb5edce3c03e422b49c7b90e54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528371"
---
# <a name="iwmdrmencryptencrypt-method"></a>IWMDRMEncrypt :: Encrypt, méthode

La méthode **Encrypt** chiffre une mémoire tampon de données en place.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Encrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbData* \[ in, out\]
</dt> <dd>

Données à chiffrer. Si la méthode est réussie, les données sont chiffrées lors du retour.

</dd> <dt>

*cbData* \[ dans\]
</dt> <dd>

Taille des données en octets.

</dd> <dt>

*pWMCryptoData* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**WMDRMCryptoData**](wmdrmcryptodata.md) contenant des paramètres supplémentaires. Affectez la valeur **null** pour utiliser les valeurs de chiffrement par défaut.

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

[**Interface IWMDRMEncrypt**](iwmdrmencrypt.md)
</dt> <dt>

[**WMDRMCryptoData**](wmdrmcryptodata.md)
</dt> </dl>

 

 





