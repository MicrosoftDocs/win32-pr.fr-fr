---
title: Méthode IWMDRMLicenseQuery QueryActionAllowed (wmdrmsdk. h)
description: La méthode QueryActionAllowed exécute une requête sur le magasin de licences local pour récupérer l’état de la licence pour une ou plusieurs actions DRM qui s’appliquent à un ID de clé spécifié.
ms.assetid: 814c2850-c036-4c44-a64e-861e88f16fb1
keywords:
- Méthode QueryActionAllowed format Windows Media
- Méthode QueryActionAllowed format Windows Media, interface IWMDRMLicenseQuery
- Interface IWMDRMLicenseQuery Windows Media format, méthode QueryActionAllowed
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryActionAllowed
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6564062fc9f76a840b37f6e134e960480d67a2ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533304"
---
# <a name="iwmdrmlicensequeryqueryactionallowed-method"></a>IWMDRMLicenseQuery :: QueryActionAllowed, méthode

La méthode **QueryActionAllowed** exécute une requête sur le magasin de licences local pour récupérer l’état de la licence pour une ou plusieurs actions DRM qui s’appliquent à un ID de clé spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT QueryActionAllowed(
  [in]  BSTR  bstrKID,
  [in]  BSTR  bstrMinReqIndivVersion,
  [in]  DWORD cActionsToQuery,
  [in]  BSTR  rgbstrActionsToQuery[],
  [out] DWORD rgdwQueryResult[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrKID* \[ dans\]
</dt> <dd>

ID de clé à interroger. Seules les licences qui s’appliquent à cet ID de clé sont évaluées.

</dd> <dt>

*bstrMinReqIndivVersion* \[ dans\]
</dt> <dd>

Version de sécurité minimale spécifiée dans l’en-tête du fichier ASF. Ce paramètre est facultatif. Transmettez la **valeur null** pour exécuter la requête sans ces informations.

</dd> <dt>

*cActionsToQuery* \[ dans\]
</dt> <dd>

Nombre d’actions à interroger. Cette valeur doit être définie sur le nombre d’éléments dans les tableaux passés pour les paramètres *rgbstrActionsToQuery* et *rgdwQueryResult* .

</dd> <dt>

*\[ rgbstrActionsToQuery \]* \[dans\]
</dt> <dd>

Tableau d’un ou de plusieurs droits à interroger. Ce tableau doit contenir autant d’éléments que ce qui est spécifié par *cActionsToQuery*. Chaque élément doit être défini sur l’une des constantes suivantes :



| Constante                                         | Description                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------|
| \_lecture wszWMDRM \_ ActionAllowed \_ g             | Inclure pour demander le droit de lire le contenu.                              |
| \_wszWMDRM g \_ ActionAllowed \_ copie                 | Inclure pour demander le droit de copier le contenu vers des périphériques ou des médias externes. |
| g \_ wszWMDRM \_ ActionAllowed \_ PlaylistBurn         | Inclure pour demander le droit de copier le contenu sur CD dans le cadre d’une sélection.  |
| g \_ wszWMDRM \_ ActionAllowed \_ CreateThumbnailImage | Inclure pour demander le droit de créer une image miniature à partir du contenu.     |
| g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD             | Inclure pour demander le droit de copier le contenu sur CD.                        |



 

</dd> <dt>

*\[ rgdwQueryResult \]* en \[ sortie\]
</dt> <dd>

Tableau d’une ou plusieurs variables DWORD qui reçoivent les résultats de la requête pour les droits spécifiés par *rgbstrActionsToQuery*. Si une action est autorisée, l’élément correspondant est défini à zéro. Si une action n’est pas autorisée, l’élément est défini sur une ou plusieurs valeurs de l’énumération des [**\_ \_ \_ \_ résultats de requête autorisés par l’action DRM**](drm-action-allowed-query-results.md) combinées à l’aide de l’opération or au niveau du bit. Ce tableau doit contenir autant d’éléments que ce qui est spécifié par *cActionsToQuery*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Lorsque vous interrogez des droits de lecture et de copie, vous obtiendrez des résultats plus précis en définissant les paramètres environnementaux. Utilisez la méthode [**SetActionAllowedQueryParams**](iwmdrmlicensequery-setactionallowedqueryparams.md) pour définir les paramètres d’environnement. Les résultats des requêtes pour le droit de gravure ne sont pas affectés par les paramètres environnementaux. vous pouvez utiliser les valeurs par défaut en toute sécurité.

Les résultats retournés par la méthode **QueryActionAllowed** sont agrégés à partir de zéro ou de plusieurs licences dans le magasin de licences local. La méthode peut ne pas effectuer de recherche dans toutes les licences qui s’appliquent à l’ID de clé si elle rencontre un résultat activé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMLicenseQuery**](iwmdrmlicensequery.md)
</dt> <dt>

[**Interrogation des informations de droits simples**](querying-for-simple-rights-information.md)
</dt> </dl>

 

 





