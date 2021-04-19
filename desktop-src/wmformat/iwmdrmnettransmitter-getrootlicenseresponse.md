---
title: Méthode IWMDRMNetTransmitter GetRootLicenseResponse (wmdrmsdk. h)
description: La méthode GetRootLicenseResponse génère un message de réponse de licence racine.
ms.assetid: c735ee52-f0e0-4404-881b-18ee9a7fa9f9
keywords:
- Méthode GetRootLicenseResponse format Windows Media
- Méthode GetRootLicenseResponse format Windows Media, interface IWMDRMNetTransmitter
- Interface IWMDRMNetTransmitter Windows Media format, méthode GetRootLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetRootLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3497a3eaedb872b7d2c9eb5d7782d01f8b35462
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542549"
---
# <a name="iwmdrmnettransmittergetrootlicenseresponse-method"></a>IWMDRMNetTransmitter :: GetRootLicenseResponse, méthode

La méthode **GetRootLicenseResponse** génère un message de réponse de licence racine.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetRootLicenseResponse(
  [in]  BSTR  bstrKID,
  [out] BYTE  **ppbLicenseResponse,
  [out] DWORD *pcbLicenseResponse
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrKID* \[ dans\]
</dt> <dd>

Identificateur de clé encodé en base64 à utiliser pour la nouvelle licence racine. L’identificateur de clé doit être une valeur GUID générée de façon aléatoire.

</dd> <dt>

*ppbLicenseResponse* \[ à\]
</dt> <dd>

Adresse d’une variable qui reçoit l’adresse de la réponse de licence générée. Lorsque vous avez terminé ces données, vous devez libérer la mémoire en appelant **CoTaskMemFree**.

</dd> <dt>

*pcbLicenseResponse* \[ à\]
</dt> <dd>

Adresse d’une variable qui reçoit la taille de la réponse de licence, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                                | Description                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**le \_ RIV de la messagerie DRM E est \_ \_ \_ trop \_ petit**</dt> </dl> | Une liste de révocation de contenu mise à jour est nécessaire.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>                       | S_OK<br/>                         |



 

## <a name="remarks"></a>Notes

La licence racine générée est créée à l’aide des informations des données de demande de licence, qui sont traitées pour l’interface en appelant [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md).

La licence racine est utilisée dans la génération de licences feuille, ce qui est accompli en appelant la méthode [**GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) . L’interface **IWMDRMNetTransmitter** conserve une copie de la licence racine pour cette utilisation.

La licence racine créée par l’appel de cette méthode n’a aucune stratégie et est configurée de sorte qu’elle ne puisse pas être rendue persistante sur l’appareil de réception.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





