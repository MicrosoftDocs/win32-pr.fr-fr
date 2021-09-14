---
title: Méthode IWMDRMNetTransmitter GetLeafLicenseResponse (wmdrmsdk. h)
description: La méthode GetLeafLicenseResponse génère un message de réponse de licence feuille.
ms.assetid: b2893d22-b6f3-44d2-b6db-e2b07fbe098d
keywords:
- Méthode GetLeafLicenseResponse format Windows Media
- Méthode GetLeafLicenseResponse format Windows Media, interface IWMDRMNetTransmitter
- Interface IWMDRMNetTransmitter Windows Media format, méthode GetLeafLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetLeafLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf2374966abfae4353a72755313c1cbbdfb7287
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195963"
---
# <a name="iwmdrmnettransmittergetleaflicenseresponse-method"></a>IWMDRMNetTransmitter :: GetLeafLicenseResponse, méthode

La méthode **GetLeafLicenseResponse** génère un message de réponse de licence feuille.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetLeafLicenseResponse(
  [in]  BSTR            bstrKID,
  [in]  WMDRMNET_POLICY *pPolicy,
  [out] IWMDRMEncrypt   **ppIWMDRMEncrypt,
  [out] BYTE            **ppbLicenseResponse,
  [out] DWORD           *pcbLicenseResponse
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrKID* \[ dans\]
</dt> <dd>

Identificateur de clé encodé en base64 à utiliser pour la nouvelle licence feuille. L’identificateur de clé doit être une valeur GUID générée de façon aléatoire.

</dd> <dt>

*pPolicy* \[ dans\]
</dt> <dd>

Pointeur vers la structure de [**\_ stratégie WMDRMNET**](wmdrmnet-policy.md) qui définit la stratégie à utiliser pour la licence feuille.

</dd> <dt>

*ppIWMDRMEncrypt* \[ à\]
</dt> <dd>

Adresse d’une variable qui reçoit un pointeur vers l’interface [**IWMDRMEncrypt**](iwmdrmencrypt.md) qui peut être utilisée pour chiffrer les données de la nouvelle licence feuille.

</dd> <dt>

*ppbLicenseResponse* \[ à\]
</dt> <dd>

Adresse d’une variable qui reçoit l’adresse de la réponse de licence générée. Lorsque vous avez terminé ces données, vous devez libérer la mémoire en appelant **CoTaskMemFree**.

</dd> <dt>

*pcbLicenseResponse* \[ à\]
</dt> <dd>

Adresse d’une variable qui reçoit la taille de la réponse de licence, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                                | Description                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**le \_ RIV de la messagerie DRM E est \_ \_ \_ trop \_ petit**</dt> </dl> | Une liste de révocation de contenu mise à jour est nécessaire.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>                       | S_OK<br/>                         |



 

## <a name="remarks"></a>Notes

Aucun.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





