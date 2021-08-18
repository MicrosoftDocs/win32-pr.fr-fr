---
title: INapServerCallback OnComplete, méthode (NapSystemHealthValidator. h)
description: Utilisé par les validateurs d’intégrité du système pour signaler la fin de la requête asynchrone.
ms.assetid: 959ee4ac-7c29-4013-a174-24abc6a580c7
keywords:
- OnComplete, méthode NAP
- OnComplete méthode NAP, interface INapServerCallback
- Interface INapServerCallback NAP, méthode OnComplete
topic_type:
- apiref
api_name:
- INapServerCallback.OnComplete
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16b0eb14663894eb1aac6911659eb452a1d50af59219b9c978215dc96de8a12f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012587"
---
# <a name="inapservercallbackoncomplete-method"></a>INapServerCallback :: OnComplete, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapServerCallback :: OnComplete** est utilisée par les validateurs de validation pour signaler la fin de la requête asynchrone.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OnComplete(
  [in] INapSystemHealthValidationRequest *request,
  [in] HRESULT                           errorCode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*demande* \[ dans\]
</dt> <dd>

Pointeur vers un objet [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) qui représente une demande de validation.

</dd> <dt>

*ErrorCode* \[ dans\]
</dt> <dd>

[**Code d’erreur NAP**](nap-error-constants.md) qui indique la raison pour laquelle la validation n’a pas pu être effectuée.

> [!Note]  
> En règle générale, la valeur de retour de la méthode [**INapSystemHealthValidationRequest :: SetSoHResponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md) est passée à ce paramètre. Toutefois, si **SetSoHResponse** n’a pas pu être appelé en raison d’un échec de retraitement, la valeur retournée par la commande ayant échoué est passée.

 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Opération réussie.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Remarques

Les validateurs doivent retourner la \_ valeur OK si la validation [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) peut être effectuée, que le **SoHRequest** ait réussi ou non le contrôle d’intégrité.

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


</dt> <dt>

[**INapServerCallback**](inapservercallback.md)
</dt> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





