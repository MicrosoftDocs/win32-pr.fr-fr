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
ms.openlocfilehash: e7758903de5f4a68cddffee982ad457d03ae6094
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295891"
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

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Utilisez cette méthode pour chiffrer les pointeurs de données afin qu’ils puissent être envoyés à travers les limites des DLL.

## <a name="requirements"></a>Spécifications



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

 

 





