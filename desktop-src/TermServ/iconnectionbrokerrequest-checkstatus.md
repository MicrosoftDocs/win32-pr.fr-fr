---
title: Méthode IConnectionBrokerRequest CheckStatus (Cbclient. h)
description: Appelé pour déterminer l’état d’une requête asynchrone.
ms.assetid: 6B0DDDB2-9905-4B48-8CCB-D6A6591B7723
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode CheckStatus
- Méthode CheckStatus Services Bureau à distance, interface IConnectionBrokerRequest
- Services Bureau à distance de l’interface IConnectionBrokerRequest, méthode CheckStatus
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest.CheckStatus
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d2409c739e0d65315e512a4e9dd7027e4cc63f5b7ac36883ed766f215a7ec91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059177"
---
# <a name="iconnectionbrokerrequestcheckstatus-method"></a>IConnectionBrokerRequest :: CheckStatus, méthode

Appelé pour déterminer l’état d’une requête asynchrone.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CheckStatus(
  [out] CB_REQUEST_STATUS *pReqStatus
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pReqStatus* \[ à\]
</dt> <dd>

Adresse d’une variable qui reçoit une valeur de l’énumération de l' [**\_ \_ État de la demande CB**](cb-request-status.md) qui indique l’état de la demande.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Cbclient. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Cbclient. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IConnectionBrokerRequest**](iconnectionbrokerrequest.md)
</dt> </dl>

 

 





