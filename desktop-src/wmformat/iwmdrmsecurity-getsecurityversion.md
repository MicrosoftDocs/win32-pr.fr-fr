---
title: Méthode IWMDRMSecurity GetSecurityVersion (wmdrmsdk. h)
description: La méthode GetSecurityVersion récupère la version du sous-système DRM sur l’ordinateur client.
ms.assetid: ec97dec8-61ba-4424-b5eb-2e6885cc1f48
keywords:
- Méthode GetSecurityVersion format Windows Media
- Méthode GetSecurityVersion format Windows Media, interface IWMDRMSecurity
- Interface IWMDRMSecurity Windows Media format, méthode GetSecurityVersion
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetSecurityVersion
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33be994383a7e16d136aac340a77deef8256d62f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127225900"
---
# <a name="iwmdrmsecuritygetsecurityversion-method"></a>IWMDRMSecurity :: GetSecurityVersion, méthode

La méthode **GetSecurityVersion** récupère la version du sous-système DRM sur l’ordinateur client.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSecurityVersion(
  [out] BSTR *pbstrVersion
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbstrVersion* \[ à\]
</dt> <dd>

Adresse d’une variable qui reçoit le numéro de version du sous-système DRM.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Le numéro de version est exprimé sous la forme d’une chaîne composée de quatre nombres séparés par des points. Le premier numéro est le numéro de version principale, qui est généralement défini sur 2. Le deuxième nombre est le numéro de version secondaire, compris entre 2 et 10. Le troisième nombre a toujours la valeur 0. Le quatrième nombre a la valeur 0 ou 1, et est une valeur booléenne indiquant si le sous-système a été individualisé. Par exemple, le numéro de version « 2.4.0.1 » indique la quatrième version mineure de la deuxième version principale.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 





