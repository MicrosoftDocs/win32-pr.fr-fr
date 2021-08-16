---
title: Méthode IWMDRMLicense GetLicenseProperty (wmdrmsdk. h)
description: La méthode GetLicenseProperty récupère une propriété de la licence actuelle.
ms.assetid: 5431f849-b37e-40b7-8bdb-ee30948aeff1
keywords:
- Méthode GetLicenseProperty format Windows Media
- Méthode GetLicenseProperty format Windows Media, interface IWMDRMLicense
- Interface IWMDRMLicense Windows Media format, méthode GetLicenseProperty
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicenseProperty
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 167fc0aa050765700805b4339e68142fa5d1eb7fc99e010c7393095dd9aa5c0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084839"
---
# <a name="iwmdrmlicensegetlicenseproperty-method"></a>IWMDRMLicense :: GetLicenseProperty, méthode

La méthode **GetLicenseProperty** récupère une propriété de la licence actuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetLicenseProperty(
  [in]  BSTR        bstrName,
  [out] PROPVARIANT *ppropVariant
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrName* \[ dans\]
</dt> <dd>

Nom de la propriété à récupérer. Définissez l’une des constantes dans le tableau suivant :



| Constante                   | Description                                                                                                          |
|----------------------------|----------------------------------------------------------------------------------------------------------------------|
| révocation de \_ wszWMDRMNet g \_ | utilisez pour obtenir le Windows Media DRM pour la liste de révocation des périphériques réseau pour la licence actuelle.                        |
| g \_ wszWMDRM \_ SAPLEVEL      | Utilisez pour obtenir le niveau de chemin d’accès audio sécurisé (SAP) requis pour lire le contenu couvert par la licence actuelle.                |
| g \_ wszWMDRM \_ SAPRequired   | Utilisez pour vérifier si la licence actuelle requiert que SAP soit utilisé pour lire le contenu.                               |
| \_wszWMDRM \_ SOURCEID      | Utilisez pour obtenir l’identificateur source de la licence actuelle.                                                            |
| \_priorité wszWMDRM \_ g      | Utilisez pour connaître la priorité de la licence actuelle. Les licences de priorité plus élevée sont appliquées avant les licences de faible priorité. |
| g \_ wszWMDRM \_      | Utilisez pour récupérer l’ID de clé de la licence racine dans la chaîne de licences à laquelle la licence actuelle appartient.                  |



 

</dd> <dt>

*ppropVariant* \[ à\]
</dt> <dd>

Reçoit la valeur de la propriété.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



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

[**GetLicense**](iwmdrmlicense-getlicense.md)
</dt> <dt>

[**Interface IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





