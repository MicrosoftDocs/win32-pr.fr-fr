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
ms.openlocfilehash: 2af44bc3c4801a35ad311f184f3aa2763ccc401ee01dce8a96ef65a0e2496219
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939137"
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

 

 





