---
title: Interface INapSystemHealthValidationRequest (NapSystemHealthValidator. h)
description: Sont utilisés pour prendre en charge les validateurs d’intégrité du système qui sont définis par le développeur de l’application.
ms.assetid: faa91ff5-49f5-4aec-81d7-02ec59274f23
keywords:
- NAP de l’interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, Description
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e7b6b2fdc0da8757ddd29b963445c0b984c45d19955c093270cf397fcac14b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133474"
---
# <a name="inapsystemhealthvalidationrequest-interface"></a>Interface INapSystemHealthValidationRequest

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

L’interface **INapSystemHealthValidationRequest** fournit des méthodes qui sont utilisées pour prendre en charge les validateurs d’intégrité du système qui sont définis par le développeur de l’application.

> [!Note]  
> [**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) hérite de toutes les méthodes de cette interface et doit être utilisé à la place.

 

## <a name="members"></a>Membres

L’interface **INapSystemHealthValidationRequest** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapSystemHealthValidationRequest** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **INapSystemHealthValidationRequest** possède ces méthodes.



| Méthode                                                                                                                               | Description                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**INapSystemHealthValidationRequest::GetCorrelationId**](inapsystemhealthvalidationrequest-getcorrelationid-method.md)             | Utilisé par les validateurs pour récupérer l’ID de corrélation. Le validateur doit ensuite enregistrer ces informations.<br/>           |
| [**INapSystemHealthValidationRequest::GetMachineName**](inapsystemhealthvalidationrequest-getmachinename-method.md)                 | Utilisé par les validateurs pour récupérer le nom de l’ordinateur. Le validateur doit ensuite enregistrer ces informations.<br/>             |
| [**INapSystemHealthValidationRequest::GetPrivateData**](inapsystemhealthvalidationrequest-getprivatedata-method.md)                 | Autorise le NapServer à récupérer des informations d’État.<br/>                                                        |
| [**INapSystemHealthValidationRequest::GetSoHRequest**](inapsystemhealthvalidationrequest-getsohrequest-method.md)                   | Autorise les validateurs à récupérer et valider les informations SoHRequest.<br/>                                     |
| [**INapSystemHealthValidationRequest::GetSoHResponse**](inapsystemhealthvalidationrequest-getsohresponse-method.md)                 | Obtient l’objet SoHResponse.<br/>                                                                               |
| [**INapSystemHealthValidationRequest::GetStringCorrelationId**](inapsystemhealthvalidationrequest-getstringcorrelationid-method.md) | Utilisé par les validateurs pour récupérer un identificateur Exchange unique. Le validateur doit ensuite enregistrer ces informations.<br/> |
| [**INapSystemHealthValidationRequest::SetPrivateData**](inapsystemhealthvalidationrequest-setprivatedata-method.md)                 | Permet au NapServer de stocker des informations d’État.<br/>                                                           |
| [**INapSystemHealthValidationRequest::SetSoHResponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md)                 | Autorise les validateurs à définir le SoHResponse.<br/>                                                                  |



 

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

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Référence NAP](nap-reference.md)
</dt> </dl>

 

