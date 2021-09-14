---
title: IWMDRMLicense CreateDecryptor, méthode (wmdrmsdk. h)
description: La méthode CreateDecryptor crée un objet déchiffreur à l’aide des paramètres de la licence actuelle.
ms.assetid: 69b7f96b-a0d6-455e-8ef9-0faf9690cef1
keywords:
- Méthode CreateDecryptor format Windows Media
- Méthode CreateDecryptor format Windows Media, interface IWMDRMLicense
- Interface IWMDRMLicense Windows Media format, méthode CreateDecryptor
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e987e7ffa3390462889b128f390934f05e64cdff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219500"
---
# <a name="iwmdrmlicensecreatedecryptor-method"></a>IWMDRMLicense :: CreateDecryptor, méthode

La méthode **CreateDecryptor** crée un objet déchiffreur à l’aide des paramètres de la licence actuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateDecryptor(
  [out] IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppDecryptor* \[ à\]
</dt> <dd>

Reçoit un pointeur vers l’interface [**IWMDRMDecrypt**](iwmdrmdecrypt.md) de l’objet nouvellement créé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                                | Description                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**le \_ RIV de la messagerie DRM E est \_ \_ \_ trop \_ petit**</dt> </dl> | Une liste de révocation de contenu mise à jour est nécessaire.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>                       | S_OK<br/>                         |



 

## <a name="remarks"></a>Notes

Aucun.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CreateEncryptor**](iwmdrmlicense-createencryptor.md)
</dt> <dt>

[**Interface IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





