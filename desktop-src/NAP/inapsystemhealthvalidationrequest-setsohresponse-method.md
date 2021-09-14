---
title: Méthode INapSystemHealthValidationRequest SetSoHResponse (NapSystemHealthValidator. h)
description: Permet aux programmes de validation d’intégrité système de définir le SoHResponse à envoyer à son homologue de l’agent d’intégrité système (SHA) côté client.
ms.assetid: 250b90ac-ce8f-4771-9d20-84c491adfb2c
keywords:
- Méthode SetSoHResponse NAP
- Méthode SetSoHResponse NAP, interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, méthode SetSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.SetSoHResponse
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b818218ef4f8601ecf4927f5e8b90f93e5386b56
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110630"
---
# <a name="inapsystemhealthvalidationrequestsetsohresponse-method"></a>INapSystemHealthValidationRequest :: SetSoHResponse, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSystemHealthValidationRequest :: SetSoHResponse** permet aux programmes de validation d’intégrité système (SHV) de définir le [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) à envoyer à son homologue de l’agent d’intégrité système (SHA) côté client.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetSoHResponse(
  [in] const SoHResponse *sohResponse
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sohResponse* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Opération réussie.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="requirements"></a>Spécifications



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

 

 





