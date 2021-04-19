---
title: Méthode IWMDRMLicenseManagement CreateLicenseEnumeration (wmdrmsdk. h)
description: La méthode CreateLicenseEnumeration crée un objet énumérateur de licence avec lequel vous pouvez obtenir des informations sur les licences dans le magasin de licences local.
ms.assetid: 48da1ef4-89bc-4cba-b5c9-0e202eb2986f
keywords:
- Méthode CreateLicenseEnumeration format Windows Media
- Méthode CreateLicenseEnumeration format Windows Media, interface IWMDRMLicenseManagement
- Interface IWMDRMLicenseManagement Windows Media format, méthode CreateLicenseEnumeration
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseEnumeration
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bb75d21cc640da39c3679ac118ead629b24f719
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523897"
---
# <a name="iwmdrmlicensemanagementcreatelicenseenumeration-method"></a>IWMDRMLicenseManagement :: CreateLicenseEnumeration, méthode

La méthode **CreateLicenseEnumeration** crée un objet énumérateur de licence avec lequel vous pouvez obtenir des informations sur les licences dans le magasin de licences local.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateLicenseEnumeration(
  [in]  WMDRM_LICENSE_FILTER *pLicenseFilter,
  [out] IWMDRMLicense        **pEnumerator
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pLicenseFilter* \[ dans\]
</dt> <dd>

Pointeur vers une structure de [**\_ \_ filtre de licence WMDRM**](wmdrm-license-filter.md) contenant les paramètres de filtrage pour la liste de licences dans l’énumérateur.

</dd> <dt>

*pEnumerator* \[ à\]
</dt> <dd>

Pointeur qui reçoit l’adresse de l’interface [**IWMDRMLicense**](iwmdrmlicense.md) de l’objet énumérateur de licence nouvellement créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                                | Description                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**le \_ RIV de la messagerie DRM E est \_ \_ \_ trop \_ petit**</dt> </dl> | Une liste de révocation de contenu mise à jour est nécessaire.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>                       | S_OK<br/>                         |



 

## <a name="remarks"></a>Notes

Aucun.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Énumération des licences dans le magasin de licences local**](enumerating-licenses-in-the-local-license-store.md)
</dt> <dt>

[**Interface IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





