---
title: IWMDRMLicense CreateEncryptor, méthode (wmdrmsdk. h)
description: La méthode CreateEncryptor crée un objet chiffreur à l’aide des paramètres de la licence actuelle.
ms.assetid: 570ba898-e846-4981-8ea8-ce16f2dad68a
keywords:
- Méthode CreateEncryptor format Windows Media
- Méthode CreateEncryptor format Windows Media, interface IWMDRMLicense
- Interface IWMDRMLicense Windows Media format, CreateEncryptor, méthode
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateEncryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481e33b6a3d4ffff3805ccc14f45b06a12ad2296fdaaedf13608f3a519c6ed10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433658"
---
# <a name="iwmdrmlicensecreateencryptor-method"></a>IWMDRMLicense :: CreateEncryptor, méthode

La méthode **CreateEncryptor** crée un objet chiffreur à l’aide des paramètres de la licence actuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateEncryptor(
  [out] IWMDRMEncrypt **ppEncryptor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppEncryptor* \[ à\]
</dt> <dd>

Reçoit un pointeur vers l’interface [**IWMDRMEncrypt**](iwmdrmencrypt.md) de l’objet nouvellement créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                                | Description                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**le \_ RIV de la messagerie DRM E est \_ \_ \_ trop \_ petit**</dt> </dl> | Une liste de révocation de contenu mise à jour est nécessaire.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>                       | S_OK<br/>                         |



 

## <a name="remarks"></a>Notes

Aucun.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CreateDecryptor**](iwmdrmlicense-createdecryptor.md)
</dt> <dt>

[**Interface IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





