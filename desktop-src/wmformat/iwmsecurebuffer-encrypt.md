---
title: IWMSecureBuffer, méthode de chiffrement (wmdrmsdk. h)
description: La méthode Encrypt chiffre un pointeur de données.
ms.assetid: da391dcb-3ef8-4c09-bca6-507f67a24ee6
keywords:
- Méthode Encrypt Windows Media format
- Méthode Encrypt Windows Media format, interface IWMSecureBuffer
- Interface IWMSecureBuffer Windows Media format, méthode Encrypt
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Encrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e5badce8249e5d6b9d2460fec0e72ef4ca4b81f5b8ffa0d3edd83729f98bd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808309"
---
# <a name="iwmsecurebufferencrypt-method"></a>IWMSecureBuffer :: Encrypt, méthode

La méthode **Encrypt** chiffre un pointeur de données.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Encrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSecureChannel* \[ dans\]
</dt> <dd>

Pointeur vers une interface de canal sécurisé contenant le pointeur de données à chiffrer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Remarques

Utilisez cette méthode pour chiffrer les pointeurs de données afin qu’ils puissent être envoyés à travers les limites des DLL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Crypté**](iwmsecurebuffer-decrypt.md)
</dt> <dt>

[**Interface IWMSecureBuffer**](iwmsecurebuffer.md)
</dt> </dl>

 

 





