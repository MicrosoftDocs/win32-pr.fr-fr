---
title: Méthode IWMDRMLicenseManagement DeleteLicense (wmdrmsdk. h)
description: La méthode DeleteLicense supprime une licence du magasin de licences local temporaire.
ms.assetid: 0aa7143a-845a-41a4-8b3c-a04c68ee280a
keywords:
- Méthode DeleteLicense format Windows Media
- Méthode DeleteLicense format Windows Media, interface IWMDRMLicenseManagement
- Interface IWMDRMLicenseManagement Windows Media format, méthode DeleteLicense
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.DeleteLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d5b52f6277459f147285f46fc791669e56061a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542417"
---
# <a name="iwmdrmlicensemanagementdeletelicense-method"></a>IWMDRMLicenseManagement ::D méthode eleteLicense

La méthode **DeleteLicense** supprime une licence du magasin de licences local temporaire.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DeleteLicense(
  [in] BSTR  bstrKID,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrKID* \[ dans\]
</dt> <dd>

ID de clé (KID) de la licence à supprimer.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Indicateurs d’option de suppression de licence. Définissez l’une des valeurs du tableau suivant.



| Valeur                                    | Description                                                                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Supprimer la \_ licence WMDRM \_ immédiatement      | Spécifie que la licence doit être supprimée immédiatement du magasin.                                                                                                                              |
| \_suppression \_ de la \_ marque de licence WMDRM \_ pour la \_ purge | Spécifie que la licence doit être marquée pour suppression, mais ne doit pas être supprimée du magasin tant que la méthode [**CleanLicenseStore**](iwmdrmlicensemanagement-cleanlicensestore.md) n’est pas appelée. |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                            | Description                                                                                                         |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | S_OK<br/>                                                                                    |
| <dl> <dt>**\_LICENSENOTFOUND DRM E \_**</dt> </dl> | La licence spécifiée n’existe pas dans le magasin.<br/> - OU -<br/> Le magasin est introuvable.<br/> |



 

## <a name="remarks"></a>Notes

Pour supprimer des licences du magasin de licences local permanent, vous devez utiliser la révocation de licence.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





