---
title: Méthode INapSystemHealthValidationRequest GetMachineName (NapSystemHealthValidator. h)
description: Est utilisé par les programmes de validation d’intégrité système (SHV) pour récupérer le nom de l’ordinateur du client NAP. Le VALIDateur de la journalisation des informations.
ms.assetid: 2ea6a65d-1579-4a05-b5bc-aebf6421e46a
keywords:
- Méthode GetMachineName NAP
- Méthode GetMachineName NAP, interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, méthode GetMachineName
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetMachineName
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be1c3e264d7d2d6e4d93e3ad71d7f3adc92ff8d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106507"
---
# <a name="inapsystemhealthvalidationrequestgetmachinename-method"></a>INapSystemHealthValidationRequest :: GetMachineName, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSystemHealthValidationRequest :: GetMachineName** est utilisée par les programmes de validation d’intégrité système (SHV) pour récupérer le nom de l’ordinateur du client NAP. Le VALIDateur de la journalisation des informations.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetMachineName(
  [out] CountedString **machineName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nomordinateur* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers une structure [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) qui contient le nom de l’ordinateur du client NAP.

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
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                    |
| En-tête<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





