---
title: Méthode INapSystemHealthAgentCallback GetSoHRequest (NapSystemHealthAgent. h)
description: Est appelé par le NapAgent pour interroger la demande de déclaration d’intégrité de l’agent d’intégrité système.
ms.assetid: 4161a3e7-2f7a-40d1-b973-47f991bba5d0
keywords:
- Méthode GetSoHRequest NAP
- Méthode GetSoHRequest NAP, interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP, méthode GetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0fd95ce79587b5e7e259323286cfce138dd2df2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384836"
---
# <a name="inapsystemhealthagentcallbackgetsohrequest-method"></a>INapSystemHealthAgentCallback :: GetSoHRequest, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSystemHealthAgentCallback :: GetSoHRequest** est appelée par le NapAgent pour interroger la requête soh de l’agent d’intégrité système.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSoHRequest(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*demande* \[ dans\]
</dt> <dd>

Pointeur COM vers un objet [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) qui identifie l’objet de requête.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée



| Code de retour                                                                                                                      | Description                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                             | Indique la réussite de l’opération.<br/>                                                                                                                      |
| <dl> <dt>**HRESULT \_ à partir de \_ Win32 (RPC \_ S \_ Server \_ non disponible)**</dt> </dl> | Si ce code est retourné par votre implémentation, NapAgent supprime l’algorithme SHA de la liste des transactions de hachage et vide son entrée de cache.<br/> |



 

Quand une valeur de retour (à l’exception **\_ de HRESULT de \_ Win32 (RPC \_ S \_ Server \_ non disponible)**) est retournée par votre implémentation, le système NAP construit et retourne un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) à la SHV correspondante avec les types et valeurs d’attribut suivants :

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = <> de code d’erreur

## <a name="remarks"></a>Notes

Cette méthode de rappel est déclarée par le système NAP et doit être implémentée par l’enregistreur SHA.

Cette méthode doit traiter la demande et retourner immédiatement. Le retardement du retour de cette méthode a un impact négatif sur les performances du système et la réactivité, et peut entraîner l’expiration du délai d’autres parties du système d’exploitation.

L’analyse de l’état d’intégrité ne doit pas être effectuée dans le cadre de cet appel, en particulier s’il s’agit d’un calcul intensif et prend beaucoup de temps. L’analyse de l’état d’intégrité et le calcul de l’SoH doivent être effectués dans un service ou un thread distinct. La seule fonction de cette méthode consiste à définir la SoH de l’algorithme SHA et à retourner.

Si l’algorithme SHA prend beaucoup de temps pour générer une SoH, la SoH mise en cache doit être retournée au NapAgent. S’il n’y a aucune déclaration SoH mise en cache à retourner, le SHA doit immédiatement retourner une SoH avec les valeurs et types d’attributs suivants :

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientCommunication**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  E/r [ **NAP \_ \_ non \_ mis en cache \_**](nap-error-constants.md)

Une fois la SoH générée, l’agent SHA doit appeler [**INapSystemHealthAgentBinding :: NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) pour notifier le NapAgent de la modification d’intégrité du système.

Le NapAgent appelle cette méthode pour interroger le SoHRequest de l’agent d’intégrité système. L’agent SHA peut interroger l’objet [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) passé pour les paramètres dont il a besoin pour calculer le SoHRequest. L’algorithme SHA doit définir le SoHRequest calculé sur l’objet de requête. L’algorithme SHA ne doit pas contenir de références à l’objet de requête une fois cet appel terminé.

Lorsque cette méthode est appelée, s’il existe une SoH dans le cache de NapAgent, elle est définie sur l’objet de requête. L’agent SHA peut l’interroger à l’aide de **GetSoHRequest**. Si l’algorithme SHA ne définit pas une nouvelle SoH, l’algorithme mis en cache est utilisé.

Pour les Sha non liés qui sont inscrits auprès du système, le système NAP construit et envoie un SoHRequest au VALIDateur correspondant avec les types et valeurs d’attribut suivants :

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **NAP \_ E \_ non \_ initialisé**](nap-error-constants.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





