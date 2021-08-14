---
title: Méthode INapSystemHealthValidationRequest GetSoHRequest (NapSystemHealthValidator. h)
description: Permet aux programmes de validation d’intégrité système (SHV) de récupérer et de valider les informations de SoHRequest envoyées par leurs homologues de l’agent d’intégrité système (SHA) sur le client.
ms.assetid: e06e07c6-7305-4171-b94e-19c360e94c67
keywords:
- Méthode GetSoHRequest NAP
- Méthode GetSoHRequest NAP, interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, méthode GetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetSoHRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9d9dc3b28aec92b7125dc2cad6bf8b843975945ca89687957d56be0ff562d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367727"
---
# <a name="inapsystemhealthvalidationrequestgetsohrequest-method"></a>INapSystemHealthValidationRequest :: GetSoHRequest, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSystemHealthValidationRequest :: GetSoHRequest** permet aux programmes de validation d’intégrité système (SHV) de récupérer et de valider les informations de [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) envoyées par leurs homologues de l’agent d’intégrité système (SHA) sur le client.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest,
  [out] BOOL       *napSystemGenerated
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sohRequest* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers une structure [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) .

</dd> <dt>

*napSystemGenerated* \[ à\]
</dt> <dd>

Valeur **booléenne** qui est **true** si la SoH a été créée par le NapAgent pour le compte de l’algorithme SHA et **false** dans le cas contraire. Il est principalement utilisé pour indiquer un échec SHA pour l’intégrité du service.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Opération réussie.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Remarques

Le paramètre *sohRequest* peut retourner la **valeur null** si le client n’a pas envoyé de [**sohRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) à l’SHV. Dans ce scénario, le SHV peut remplir un **SoHResponse** avec le code d’erreur de l' [**\_ \_ \_ SOH NAP manquant**](nap-error-constants.md).

Si le paramètre *napSystemGenerated* a la **valeur true**, le format de *SoHRequest* est le suivant :

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **<SHA-Failure-erreur-code>**](nap-error-constants.md)

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

 

 





