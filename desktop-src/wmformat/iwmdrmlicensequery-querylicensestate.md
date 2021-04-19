---
title: Méthode IWMDRMLicenseQuery QueryLicenseState (wmdrmsdk. h)
description: La méthode QueryLicenseState interroge le magasin de licences local pour obtenir les informations de licence qui s’appliquent à un ID de clé pour un ou plusieurs droits spécifiques.
ms.assetid: 17f40c56-2266-4c94-9e95-a33a92ddef74
keywords:
- Méthode QueryLicenseState format Windows Media
- Méthode QueryLicenseState format Windows Media, interface IWMDRMLicenseQuery
- Interface IWMDRMLicenseQuery Windows Media format, méthode QueryLicenseState
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryLicenseState
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e101d4ad9b5405906d05ba5e5f230326a1a3f13a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541023"
---
# <a name="iwmdrmlicensequeryquerylicensestate-method"></a>IWMDRMLicenseQuery :: QueryLicenseState, méthode

La méthode **QueryLicenseState** interroge le magasin de licences local pour obtenir les informations de licence qui s’appliquent à un ID de clé pour un ou plusieurs droits spécifiques.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT QueryLicenseState(
  [in]  BSTR                   bstrKID,
  [in]  DWORD                  cActionsToQuery,
  [in]  BSTR                   rgbstrActionsToQuery[],
  [out] DRM_LICENSE_STATE_DATA rgResultStateData[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrKID* \[ dans\]
</dt> <dd>

ID de clé à interroger. Seules les licences qui s’appliquent à cet ID de clé sont évaluées.

</dd> <dt>

*cActionsToQuery* \[ dans\]
</dt> <dd>

Nombre d’actions à interroger. Cette valeur doit être définie sur le nombre d’éléments dans les tableaux passés pour les paramètres *rgbstrActionsToQuery* et *rgResultStateData* .

</dd> <dt>

*\[ rgbstrActionsToQuery \]* \[dans\]
</dt> <dd>

Tableau d’un ou de plusieurs droits à interroger. Ce tableau doit contenir autant d’éléments que ce qui est spécifié par *cActionsToQuery*. Chaque élément doit être défini sur l’une des constantes suivantes.



| Constante                                        | Description                                                                                                                                        |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| c \_ wszWMDRM \_ LicenseState \_ sauvegarde               | Incluez pour demander les détails sur le droit de sauvegarder et de restaurer la licence.                                                               |
| g \_ wszWMDRM \_ LicenseState \_ CollaborativePlay    | Incluez pour demander les détails sur le droit de partager le contenu avec un groupe d’utilisateurs dans le cadre d’un scénario de lecture collaborative.          |
| \_wszWMDRM g \_ LicenseState \_ copie                 | Include pour rechercher les détails sur le droit de copier le contenu vers des périphériques ou des médias externes.                                                 |
| g \_ wszWMDRM \_ LicenseState \_ CopyToCD             | Incluez pour demander les détails sur le droit de copier le contenu sur CD.                                                                        |
| g \_ wszWMDRM \_ LicenseState \_ CopyToNonSDMIDevice  | Incluez pour demander les détails sur le droit de copier le contenu sur un appareil qui ne prend pas en charge l’initiative de support numérique sécurisé (SDMI). |
| g \_ wszWMDRM \_ LicenseState \_ CopyToSDMIDevice     | Inclure pour demander les détails sur le droit de copier le contenu sur un appareil qui prend en charge le périphérique SDMI.                                           |
| g \_ wszWMDRM \_ LicenseState \_ CreateThumbnailImage | Include pour rechercher les détails sur le droit de créer une image miniature à partir du contenu.                                                     |
| \_lecture wszWMDRM \_ LicenseState \_ g             | Include pour rechercher les détails sur le droit de lire le contenu.                                                                              |
| g \_ wszWMDRM \_ LicenseState \_ PlaylistBurn         | Inclure pour demander les détails sur le droit de copier le contenu sur CD dans le cadre d’une sélection.                                                  |



 

</dd> <dt>

*\[ rgResultStateData \]* en \[ sortie\]
</dt> <dd>

Tableau d’une ou de plusieurs structures de [**données d' \_ État de licence \_ \_ DRM**](drmdrm-license-state-data.md) qui reçoivent les informations d’état de licence qui s’appliquent à droite dans l’élément correspondant du paramètre *rgbstrActionsToQuery* .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Toutes les licences qui s’appliquent à l’ID de clé spécifié seront recherchées et évaluées. Les résultats sont agrégés, de sorte que chaque structure de **\_ données d' \_ état \_ de licence DRM** peut contenir des informations provenant de plusieurs licences.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMLicenseQuery**](iwmdrmlicensequery.md)
</dt> </dl>

 

 





