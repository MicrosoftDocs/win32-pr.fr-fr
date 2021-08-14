---
title: Méthode IWMDRMNetReceiver ProcessLicenseResponse (wmdrmsdk. h)
description: La méthode ProcessLicenseResponse traite la réponse de licence envoyée par l’émetteur en réponse à une demande de licence.
ms.assetid: b6d04651-746b-474e-8a02-6b7cbee9db46
keywords:
- Méthode ProcessLicenseResponse format Windows Media
- Méthode ProcessLicenseResponse format Windows Media, interface IWMDRMNetReceiver
- Interface IWMDRMNetReceiver Windows Media format, méthode ProcessLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7ba84c7bf58091bb17500b0d35390062710a79a9a32b939ac8b9517cbcfaba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118700823"
---
# <a name="iwmdrmnetreceiverprocesslicenseresponse-method"></a>IWMDRMNetReceiver ::P méthode rocessLicenseResponse

La méthode **ProcessLicenseResponse** traite la réponse de licence envoyée par l’émetteur en réponse à une demande de licence.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ProcessLicenseResponse(
  [in]  BYTE  *pbLicenseResponse,
  [in]  DWORD cbLicenseResponse,
  [out] BYTE  **ppbWMDRMNetLicenseRepresentation,
  [out] DWORD *pcbWMDRMNetLicenseRepresentation
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbLicenseResponse* \[ dans\]
</dt> <dd>

Réponse de la licence reçue de l’émetteur.

</dd> <dt>

*cbLicenseResponse* \[ dans\]
</dt> <dd>

Taille de la réponse en octets.

</dd> <dt>

*ppbWMDRMNetLicenseRepresentation* \[ à\]
</dt> <dd>

Adresse d’une variable qui reçoit l’adresse de la représentation de licence interne pour la licence contenue dans le message de réponse de licence. Lorsque vous avez terminé ces données, vous devez libérer la mémoire en appelant **CoTaskMemFree**. Ce paramètre peut avoir la valeur **null** si la représentation de la licence n’est pas nécessaire.

</dd> <dt>

*pcbWMDRMNetLicenseRepresentation* \[ à\]
</dt> <dd>

Adresse d’une variable qui reçoit la taille de la représentation de licence. Doit avoir la valeur **null** si *PpbWMDRMNetLicenseRepresentation* a la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                                | Description                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**le \_ RIV de la messagerie DRM E est \_ \_ \_ trop \_ petit**</dt> </dl> | Une liste de révocation de contenu mise à jour est nécessaire.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>                       | S_OK<br/>                         |



 

## <a name="remarks"></a>Remarques

La réponse de licence traitée à l’aide de cette méthode doit correspondre à la dernière demande de licence générée sur l’ordinateur client.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> <dt>

[**IWMDRMNetReceiver::GetLicenseChallenge**](iwmdrmnetreceiver-getlicensechallenge.md)
</dt> </dl>

 

 





