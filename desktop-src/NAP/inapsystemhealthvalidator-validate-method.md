---
title: INapSystemHealthValidator Validate, méthode (NapSystemHealthValidator. h)
description: Le système NAP pour valider les SoHRequest reçus d’un client.
ms.assetid: d67dc2c8-f18c-4e06-a51e-a538ca75c3f1
keywords:
- Valider la méthode NAP
- Valider la méthode NAP, interface INapSystemHealthValidator
- INapSystemHealthValidator interface NAP, Validate, méthode
topic_type:
- apiref
api_name:
- INapSystemHealthValidator.Validate
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f7589a67b9a3b1454e3c65b17ad6f584ce0e655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512793"
---
# <a name="inapsystemhealthvalidatorvalidate-method"></a>INapSystemHealthValidator :: Validate, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSystemHealthValidator :: Validate** est définie par le développeur SHV et appelée par le système NAP pour valider les [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) reçues d’un client.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Validate(
  [in] INapSystemHealthValidationRequest *request,
  [in] UINT32                            hintTimeOutInMsec,
  [in] INapServerCallback                *callback
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*demande* \[ dans\]
</dt> <dd>

Pointeur COM vers un objet [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) qui identifie l’objet de demande de validation.

</dd> <dt>

*hintTimeOutInMsec* \[ dans\]
</dt> <dd>

Durée, en millisecondes, du délai d’attente de communication. Le programme de validation d’intégrité système (SHV) doit répondre dans ce laps de temps. dans le cas contraire, la réponse est supprimée.

> [!Note]  
> Le délai d’expiration par défaut pour tous les validateurs d’intégrité est de 2000 millisecondes. L’utilisation d’une valeur autre que la valeur par défaut modifie le délai d’expiration pour tous les validateurs d’intégrité inscrits.

 

</dd> <dt>

*rappel* \[ dans\]
</dt> <dd>

Pointeur vers l’objet de rappel [**INapServerCallback**](inapservercallback.md). Ce pointeur de rappel est utilisé par les validateurs d’intégrité du système lorsqu’ils retournent **E \_ en attente** à partir de l’appel à **INapSystemHealthValidator :: Validate**. Utilisé pour la validation asynchrone. Les validateurs d’intégrité du système sont censés répondre dans le temps *hintTimeOutInMsec* , sinon la réponse sera supprimée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si un autre code d’erreur est retourné, le système suppose que l’échec de serverComponent s’est produit et que le mappage approprié est effectué pour réussir ou échouer.



| Code de retour                                                                                                | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                       | Indique que le validateur a défini un SoHResponse sur l’objet « Request ».<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**E \_ en attente**</dt> </dl>                  | Indique que OnComplete () sera appelé sur un thread séparé.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>**\_serveur RPC \_ S \_ non disponible**</dt> </dl> | Indique que le processus du programme de validation d’intégrité système (SHV) s’est terminé sans que le NapServer libère réellement une référence à ce dernier. Le NapServer essaiera de recréer une nouvelle référence au VALIDateur de validation et de réexécuter l’appel Validate une seule fois. Si la création de l’objet ou de la validation réexécutée échoue, le SHV est supprimé de la liste des validateurs chargés. Le seul moyen de rechargement de ce VALIDateur consiste à annuler l’inscription et à réinscrire le SHV, ou lors du redémarrage de NapServer<br/> |



 

## <a name="remarks"></a>Notes

Pour permettre la prise en charge de la détection d’intrusion, les validateurs d’intégrité système seront invités à valider l’ordinateur client, que le client ait envoyé un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) destiné à l’intégrité du système.

Le SHV doit effectuer les opérations suivantes :

-   Récupérez le [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) à partir de la *demande* en appelant la [**demande. GetSoHRequest ()**](inapsystemhealthvalidationrequest-getsohrequest-method.md).
-   Si le paquet [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) est NULL :
    -   Si le SHV est un système de détection d’intrusion, renseignez un paquet [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) avec le [**code d’erreur NAP**](nap-error-constants.md) approprié en fonction de la raison pour laquelle l’ordinateur client est malveillant.
    -   Tous les autres programmes de validation d’intégrité système doivent remplir un paquet [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) avec un code d’erreur de [**déclaration d' \_ \_ \_ intégrité réseau manquante NAP**](nap-error-constants.md).
-   Si *napSystemGenerated* a la **valeur true** à partir de l’appel à la [**requête. GetSoHRequest ()**](inapsystemhealthvalidationrequest-getsohrequest-method.md), le SHV doit s’attendre à un paquet [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) avec les 3 TLVs suivants : [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md), **sohAttributeTypeFailureCategory**, **sohAttributeTypeErrorCodes**. Ce **SoHRequest** est généré par le NapAgent pour le compte de l’agent d’intégrité système (SHA), car une erreur s’est produite lors de la récupération d’un paquet de demande à partir de l’agent Sha.
-   Validez le paquet [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) .
    -   Si le [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) est incorrect, construisez un paquet **SoHResponse** avec le code d’erreur [**NAP \_ E \_ \_ Packet non valide**](nap-error-constants.md).
    -   Si le programme de validation d’intégrité du service utilise uniquement des informations mises en cache pour valider le paquet [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) (c’est-à-dire qu’aucune e/s n’est effectuée), il peut alors construire le **SoHResponse**, le définir sur l’objet dans la *demande* et retourner la valeur **\_ OK**.
    -   Si le programme de validation d’intégrité du service effectue des e/s afin de communiquer avec ses serveurs principaux pour valider l’intégrité du client, il doit mettre en file d’attente les e/s et retourner cette fonction avec **E \_ en attente**. Dans ce cas, le validateur d’intégrité des appels doit appeler le [**rappel. OnComplete ()**](inapservercallback-oncomplete-method.md) sur un thread distinct dans le délai d’attente, *hintTimeOutInMsec*. Dans le cas contraire, la réponse du SHV sera supprimée.
-   Ne retournez aucune autre erreur que celles indiquées ci-dessus. Si un autre code d’erreur est retourné par le SHV (par exemple, une erreur système), le paquet est ignoré.

Un SHV doit retourner un **sohAttributeTypeComplianceResultCodes** ou un **sohAttributeTypeFailureCategory** TLV dans son [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).

-   [**SOHATTRIBUTETYPECOMPLIANCERESULTCODES TLV**](sohattributetype-enum.md): si le SHV peut valider l’intégrité du client (par exemple sain ou défectueux), cette TLV est retournée.
-   [**SOHATTRIBUTETYPEFAILURECATEGORY TLV**](sohattributetype-enum.md): en cas d’échec de composant ou de communication sur le client ou le serveur, celui-ci doit être indiqué par ce TLV. Ce TLV sera davantage mappé à sain ou défectueux, en fonction de la configuration du SHV. Pour plus d’informations, consultez l’interface [**INapServerManagement**](inapservermanagement.md) et la structure [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) .

Le SHV ne doit pas contenir de références à la *demande* ou au *rappel* une fois l’appel asynchrone terminé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                    |
| En-tête<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapSystemHealthValidator**](inapsystemhealthvalidator.md)
</dt> </dl>

 

 





