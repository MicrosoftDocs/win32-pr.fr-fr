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
ms.openlocfilehash: a83a28c4d9f3758b711c43ddd83a509c58f8ea8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532956"
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

Spécifie si le contenu sera rendu à l’aide des objets du kit de développement logiciel (SDK) Microsoft Media Foundation. **False** indique le rendu par les objets du kit de développement logiciel (SDK) de format Windows Media. Ce paramètre est facultatif.

</dd> <dt>

*dwAppSecLevel* \[ dans\]
</dt> <dd>

Niveau de sécurité de l’application de requête. Cette valeur n’est importante que si les objets du kit de développement logiciel (SDK) du format Windows Media sont utilisés, auquel cas *fIsMF* doit avoir la valeur **false**. Ce paramètre est facultatif.

</dd> <dt>

*fHasSerialNumber* \[ dans\]
</dt> <dd>

Spécifie si l’appareil cible pour une opération de copie a un numéro de série. Ce paramètre est facultatif et s’applique uniquement aux requêtes pour les opérations de copie.

</dd> <dt>

*bstrDeviceCert* \[ dans\]
</dt> <dd>

Certificat d’appareil de l’appareil cible lors de l’utilisation de Windows Media DRM pour les appareils mobiles. Ce paramètre est facultatif et s’applique uniquement aux requêtes pour les opérations de copie.

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

[**Interface IWMDRMLicenseQuery**](iwmdrmlicensequery.md)
</dt> <dt>

[**Interrogation pour obtenir des informations détaillées sur les droits**](querying-for-detailed-rights-information.md)
</dt> </dl>

 

 





