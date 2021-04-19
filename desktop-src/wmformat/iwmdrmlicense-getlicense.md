---
title: Méthode IWMDRMLicense GetLicense (wmdrmsdk. h)
description: La méthode GetLicense récupère la licence sous forme de données XML ou XMR.
ms.assetid: 63317841-fd13-4e83-8b99-e3cab1405050
keywords:
- Méthode GetLicense format Windows Media
- Méthode GetLicense format Windows Media, interface IWMDRMLicense
- Interface IWMDRMLicense Windows Media format, méthode GetLicense
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0692afb2ff127f9456e6da3c7546c67ae22ded
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525493"
---
# <a name="iwmdrmlicensegetlicense-method"></a>IWMDRMLicense :: GetLicense, méthode

La méthode **GetLicense** récupère la licence sous forme de données XML ou XMR.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetLicense(
  [out] BYTE  **ppbLicense,
  [out] DWORD *pcbLicense,
  [out] DWORD *pdwLicenseType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppbLicense* \[ à\]
</dt> <dd>

Reçoit la licence.

</dd> <dt>

*pcbLicense* \[ à\]
</dt> <dd>

Reçoit la taille de la licence.

</dd> <dt>

*pdwLicenseType* \[ à\]
</dt> <dd>

Reçoit le type de la licence retournée. Cette valeur est définie sur l’une des constantes dans le tableau suivant.



| Constante                  | Description                            |
|---------------------------|----------------------------------------|
| \_type de licence WMDRM \_ \_ XML | La licence Récupérée est au format XML. |
| \_type de licence WMDRM \_ \_ XMR | La licence Récupérée est au format XMR. |



 

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

[**GetLicenseProperty**](iwmdrmlicense-getlicenseproperty.md)
</dt> <dt>

[**Interface IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





