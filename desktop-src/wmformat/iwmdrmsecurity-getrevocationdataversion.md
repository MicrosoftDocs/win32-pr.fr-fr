---
title: Méthode IWMDRMSecurity GetRevocationDataVersion (wmdrmsdk. h)
description: La méthode GetRevocationDataVersion récupère le numéro de version d’une liste de révocation de certificats dans le magasin local.
ms.assetid: 2fa13b38-02c2-4c81-938b-409cadca00fb
keywords:
- Méthode GetRevocationDataVersion format Windows Media
- Méthode GetRevocationDataVersion format Windows Media, interface IWMDRMSecurity
- Interface IWMDRMSecurity Windows Media format, méthode GetRevocationDataVersion
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetRevocationDataVersion
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705f02622b7298134328b513aa038804995eb1c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523911"
---
# <a name="iwmdrmsecuritygetrevocationdataversion-method"></a>IWMDRMSecurity :: GetRevocationDataVersion, méthode

La méthode **GetRevocationDataVersion** récupère le numéro de version d’une liste de révocation de certificats dans le magasin local.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetRevocationDataVersion(
  [in]  REFGUID   f_guidRevocationType,
  [out] ULONGLONG *f_pdwCRLVersion
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*f \_ guidRevocationType* \[ dans\]
</dt> <dd>

GUID spécifiant le type de liste de révocation. Définissez l’une des constantes dans le tableau suivant.



| GUID, constante                 | Description                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| \_application REVOCATIONTYPE \_ WMDRM    | Spécifie la liste de révocation des certificats d’application.                           |
| \_appareil REVOCATIONTYPE \_ WMDRM | Spécifie la liste de révocation de certificats de l’appareil.                                |
| \_REVOCATIONTYPE WMDRM \_ CARDEA | Spécifie la liste de révocation de certificats Windows Media DRM pour les périphériques réseau. |



 

</dd> <dt>

*f \_ pdwCRLVersion* \[\]
</dt> <dd>

Variable qui reçoit le numéro de version.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Révocation et renouvellement de composants automatisés**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**GetRevocationData**](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[**Interface IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> <dt>

[**SetRevocationData**](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





