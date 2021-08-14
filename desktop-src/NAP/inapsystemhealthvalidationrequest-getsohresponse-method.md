---
title: Méthode INapSystemHealthValidationRequest GetSoHResponse (NapSystemHealthValidator. h)
description: Récupère le SoHResponse.
ms.assetid: 7db9d134-5cd4-4a6c-8576-843b9a920864
keywords:
- Méthode GetSoHResponse NAP
- Méthode GetSoHResponse NAP, interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, méthode GetSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetSoHResponse
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da93f53f3dcc9f4e566703d4d2f63415bb7feb9b0c00d5086fe598ab442e1d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799056"
---
# <a name="inapsystemhealthvalidationrequestgetsohresponse-method"></a>INapSystemHealthValidationRequest :: GetSoHResponse, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSystemHealthValidationRequest :: GetSoHResponse** récupère le [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sohResponse* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers le [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh)reçu.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Opération réussie.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                    |
| En-tête<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





