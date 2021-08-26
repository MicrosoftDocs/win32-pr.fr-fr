---
title: Méthode INapSystemHealthAgentCallback GetFixupInfo (NapSystemHealthAgent. h)
description: Est appelé par NapAgent pour déterminer l’état de l’agent d’intégrité système pendant le traitement d’un SoHResponse.
ms.assetid: cf919b56-3d40-4c49-9c91-25c20ae5ccda
keywords:
- Méthode GetFixupInfo NAP
- Méthode GetFixupInfo NAP, interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP, méthode GetFixupInfo
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetFixupInfo
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d82f84acbc759f8459c7eeb904ab4f08a108093fa30c3b27c033fbfef1dcf15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037749"
---
# <a name="inapsystemhealthagentcallbackgetfixupinfo-method"></a>INapSystemHealthAgentCallback :: GetFixupInfo, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSystemHealthAgentCallback :: GetFixupInfo** est appelée par le NapAgent pour déterminer l’état de l’agent d’intégrité système, pendant le traitement d’un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetFixupInfo(
  [out] FixupInfo **info
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*informations* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers une structure [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) qui contient l’état de correction de l’agent.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                          | Description                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Indique la réussite de l’opération.<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode de rappel est déclarée par le système NAP et doit être implémentée par l’enregistreur SHA.

L’agent d’intégrité système doit retourner **S \_ OK** immédiatement sans blocage.

## <a name="requirements"></a>Configuration requise



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

 

 





