---
title: Méthode IWMDRMLicenseManagement StoreLicense (wmdrmsdk. h)
description: La méthode StoreLicense comprend une licence générée en dehors du sous-système local DRM dans le magasin de licences local.
ms.assetid: 2190ff8c-8969-4f03-9f90-331bff8f4da2
keywords:
- Méthode StoreLicense format Windows Media
- Méthode StoreLicense format Windows Media, interface IWMDRMLicenseManagement
- Interface IWMDRMLicenseManagement Windows Media format, méthode StoreLicense
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.StoreLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcfde6347e099ceb9fc168e1183cbd62c90f9b9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543591"
---
# <a name="iwmdrmlicensemanagementstorelicense-method"></a>IWMDRMLicenseManagement :: StoreLicense, méthode

La méthode **StoreLicense** comprend une licence générée en dehors du sous-système local DRM dans le magasin de licences local.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT StoreLicense(
  [in] BSTR bstrLicenseResponse
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrLicenseResponse* \[ dans\]
</dt> <dd>

Chaîne de réponse de licence à décoder et à ajouter au magasin de licences local.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Vous pouvez utiliser cette méthode pour ajouter des licences XMR que vous avez créées dans le magasin de licences local.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





