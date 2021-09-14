---
title: Méthode INapSystemHealthAgentCallback ProcessSoHResponse (NapSystemHealthAgent. h)
description: Est appelé lorsque le NapAgent reçoit un SoHResponse destiné à cet agent d’intégrité.
ms.assetid: 860b1012-7df8-456f-8f21-eb0e1abd2b3b
keywords:
- Méthode ProcessSoHResponse NAP
- Méthode ProcessSoHResponse NAP, interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP, méthode ProcessSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.ProcessSoHResponse
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c62c585c36680dde2c54c95c255a85f69fc5ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011636"
---
# <a name="inapsystemhealthagentcallbackprocesssohresponse-method"></a>INapSystemHealthAgentCallback ::P méthode rocessSoHResponse

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSystemHealthAgentCallback ::P rocesssohresponse** est appelée quand le NapAgent reçoit un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destiné à cet agent d’intégrité.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ProcessSoHResponse(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*demande* \[ dans\]
</dt> <dd>

Pointeur COM vers un objet [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) qui identifie l’objet de requête.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                            | Description                                                                              |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | Indique la réussite de l’opération.<br/>                                                            |
| <dl> <dt>**\_paquet NAP E \_ non valide \_**</dt> </dl> | Retourné par cette implémentation si le format de la réponse n’est pas correct.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode de rappel est déclarée par le système NAP et doit être implémentée par l’enregistreur SHA.

Quand le NapAgent reçoit un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destiné à cet agent d’intégrité, il appelle cette méthode. L’agent d’intégrité doit interroger le SoHResponse à partir de l’objet de requête. Elle ne doit pas contenir de références à l’objet de requête une fois cet appel terminé.

La méthode **INapSystemHealthAgentCallback ::P rocesssohresponse** ne doit pas être bloquée. Si un traitement de correction est requis, toute implémentation de **ProcessSoHResponse** doit démarrer un nouveau thread pour effectuer un traitement de correction. NapAgent doit appeler [**INapSystemHealthAgentCallBack :: GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) pour déterminer l’état de correction de l’algorithme SHA.

Cette méthode doit retourner **le \_ paquet NAP E \_ non valide \_** si le format de la réponse n’est pas correct.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





