---
title: Méthode IWMDRMSecurity SetRevocationData (wmdrmsdk. h)
description: La méthode SetRevocationData définit une liste de révocation de certificats dans le magasin local.
ms.assetid: 7e1c6d50-7a22-41b7-b29f-b1e5809a2097
keywords:
- Méthode SetRevocationData format Windows Media
- Méthode SetRevocationData format Windows Media, interface IWMDRMSecurity
- Interface IWMDRMSecurity Windows Media format, méthode SetRevocationData
topic_type:
- apiref
api_name:
- IWMDRMSecurity.SetRevocationData
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e3ece5a9285420261add123a61d0b7123896e2d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127225881"
---
# <a name="iwmdrmsecuritysetrevocationdata-method"></a>IWMDRMSecurity :: SetRevocationData, méthode

La méthode **SetRevocationData** définit une liste de révocation de certificats dans le magasin local.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetRevocationData(
  [in] REFGUID f_guidRevocationType,
  [in] BYTE    *f_pbCRL,
  [in] DWORD   f_cbCRL
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
| \_REVOCATIONTYPE WMDRM \_ CARDEA | spécifie la Windows Media DRM pour les périphériques réseau liste de révocation de certificats. |



 

</dd> <dt>

*f \_ pbCRL* \[ dans\]
</dt> <dd>

Mémoire tampon contenant la liste de révocation de certificats.

</dd> <dt>

*f \_ cbCRL* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetRevocationData**](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[**GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[**Interface IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 





