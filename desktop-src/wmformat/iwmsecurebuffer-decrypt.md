---
title: Méthode de déchiffrement IWMSecureBuffer (wmdrmsdk. h)
description: La méthode Decrypt déchiffre un pointeur de données qui a été chiffré en appelant la méthode Encrypt.
ms.assetid: 15cedb56-686a-4a3c-81a5-b1797cfe0838
keywords:
- Méthode de déchiffrement Windows Media format
- Méthode Decrypt Windows Media format, interface IWMSecureBuffer
- Interface IWMSecureBuffer Windows Media format, méthode Decrypt
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Decrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6f48ae389090840e085c90b0bc5444e7cd6784e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534917"
---
# <a name="iwmsecurebufferdecrypt-method"></a>IWMSecureBuffer ::D méthode ecrypt

La méthode **Decrypt** déchiffre un pointeur de données qui a été chiffré en appelant la méthode [**Encrypt**](iwmsecurebuffer-encrypt.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Decrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSecureChannel* \[ dans\]
</dt> <dd>

Pointeur vers une interface de canal sécurisé contenant le pointeur de données chiffrées.

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
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Encrypt (Chiffrer)**](iwmsecurebuffer-encrypt.md)
</dt> <dt>

[**Interface IWMSecureBuffer**](iwmsecurebuffer.md)
</dt> </dl>

 

 





