---
title: Méthode IWMDRMLicenseQuery SetActionAllowedQueryParams (wmdrmsdk. h)
description: La méthode SetActionAllowedQueryParams définit des informations spécifiques à l’environnement pour obtenir des résultats de requête plus précis lors de l’utilisation de la méthode QueryActionAllowed.
ms.assetid: 1c8f9d4e-999d-4d7c-87fd-9d30e432350c
keywords:
- Méthode SetActionAllowedQueryParams format Windows Media
- Méthode SetActionAllowedQueryParams format Windows Media, interface IWMDRMLicenseQuery
- Interface IWMDRMLicenseQuery Windows Media format, méthode SetActionAllowedQueryParams
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.SetActionAllowedQueryParams
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54dfa59300c9d222b13067524d2e9e174e1600adff98bbaaed3973a0168942ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655036"
---
# <a name="iwmdrmlicensequerysetactionallowedqueryparams-method"></a>IWMDRMLicenseQuery :: SetActionAllowedQueryParams, méthode

La méthode **SetActionAllowedQueryParams** définit des informations spécifiques à l’environnement pour obtenir des résultats de requête plus précis lors de l’utilisation de la méthode [**QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetActionAllowedQueryParams(
  [in] BOOL  fIsMF,
  [in] DWORD dwAppSecLevel,
  [in] BOOL  fHasSerialNumber,
  [in] BSTR  bstrDeviceCert
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fIsMF* \[ dans\]
</dt> <dd>

Spécifie si le contenu sera rendu à l’aide des objets du kit de développement logiciel (SDK) Microsoft Media Foundation. **false** indique le rendu par les objets du kit de développement logiciel (SDK) de Format multimédia Windows. Ce paramètre est facultatif.

</dd> <dt>

*dwAppSecLevel* \[ dans\]
</dt> <dd>

Niveau de sécurité de l’application de requête. cette valeur n’est importante que si les objets du kit de développement logiciel (SDK) de Format multimédia Windows sont utilisés, auquel cas *fIsMF* doit avoir la valeur **false**. Ce paramètre est facultatif.

</dd> <dt>

*fHasSerialNumber* \[ dans\]
</dt> <dd>

Spécifie si l’appareil cible pour une opération de copie a un numéro de série. Ce paramètre est facultatif et s’applique uniquement aux requêtes pour les opérations de copie.

</dd> <dt>

*bstrDeviceCert* \[ dans\]
</dt> <dd>

certificat d’appareil de l’appareil cible lors de l’utilisation de Windows Media DRM pour les appareils mobiles. Ce paramètre est facultatif et s’applique uniquement aux requêtes pour les opérations de copie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Aucun.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMLicenseQuery**](iwmdrmlicensequery.md)
</dt> <dt>

[**Interrogation pour obtenir des informations détaillées sur les droits**](querying-for-detailed-rights-information.md)
</dt> </dl>

 

 





