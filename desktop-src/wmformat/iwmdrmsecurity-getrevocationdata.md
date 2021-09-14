---
title: Méthode IWMDRMSecurity GetRevocationData (wmdrmsdk. h)
description: La méthode GetRevocationData récupère une liste de révocation de certificats à partir du magasin local.
ms.assetid: 218f4f3a-02bc-4b1d-9320-e35ed8cc3b11
keywords:
- Méthode GetRevocationData format Windows Media
- Méthode GetRevocationData format Windows Media, interface IWMDRMSecurity
- Interface IWMDRMSecurity Windows Media format, méthode GetRevocationData
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetRevocationData
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38e9e0b428a3922f84141ef855d8468b79b3bb2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127225905"
---
# <a name="iwmdrmsecuritygetrevocationdata-method"></a>IWMDRMSecurity :: GetRevocationData, méthode

La méthode **GetRevocationData** récupère une liste de révocation de certificats à partir du magasin local.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetRevocationData(
  [in]      REFGUID f_guidRevocationType,
  [out]     BYTE    *f_pbCRL,
  [in, out] DWORD   *f_pcbCRL
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*f \_ guidRevocationType* \[ dans\]
</dt> <dd>

GUID identifiant le type de liste de révocation à récupérer. Utilisez l’une des constantes dans le tableau suivant.



| GUID, constante                 | Description                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| \_application REVOCATIONTYPE \_ WMDRM    | Spécifie la liste de révocation des certificats d’application.                           |
| \_appareil REVOCATIONTYPE \_ WMDRM | Spécifie la liste de révocation de certificats de l’appareil.                                |
| \_REVOCATIONTYPE WMDRM \_ CARDEA | spécifie la Windows Media DRM pour les périphériques réseau liste de révocation de certificats. |



 

</dd> <dt>

*f \_ pbCRL* \[\]
</dt> <dd>

Mémoire tampon qui reçoit la liste de révocation. Affectez la valeur **null** pour connaître la taille de mémoire tampon requise.

</dd> <dt>

*f \_ pcbCRL* \[ dans, out\]
</dt> <dd>

Taille, en octets, de la mémoire tampon. Si *f \_ pbCRL* a la valeur **null**, cette valeur est définie sur la taille de mémoire tampon requise sur la sortie.

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

[**Révocation et renouvellement de composants automatisés**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[**Interface IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> <dt>

[**SetRevocationData**](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





