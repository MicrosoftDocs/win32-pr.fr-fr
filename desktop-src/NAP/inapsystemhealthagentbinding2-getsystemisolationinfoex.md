---
title: Méthode INapSystemHealthAgentBinding2 GetSystemIsolationInfoEx (NapSystemHealthAgent. h)
description: Est appelé par l’SHA pour déterminer l’état d’isolement du système et l’état d’isolement étendu.
ms.assetid: 237e5539-889c-457d-8db0-bf3379f28b85
keywords:
- Méthode GetSystemIsolationInfoEx NAP
- Méthode GetSystemIsolationInfoEx NAP, interface INapSystemHealthAgentBinding2
- INapSystemHealthAgentBinding2 interface NAP, méthode GetSystemIsolationInfoEx
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2643d62afba1a35ebd96b8b39ea2fcf90397576
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508678"
---
# <a name="inapsystemhealthagentbinding2getsystemisolationinfoex-method"></a>INapSystemHealthAgentBinding2 :: GetSystemIsolationInfoEx, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSystemHealthAgentBinding2 :: GetSystemIsolationInfoEx** est appelée par l’SHA pour déterminer l’état d’isolement système et l’état d’isolement étendu.

> [!Note]  
> Utilisez [**INapSystemHealthAgentBinding :: GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) pour déterminer uniquement l’état d’isolement du système.

 

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*isolationInfo* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers une structure [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) qui contient l’état d’isolement étendu du système pour les connexions connues. *isolationInfo* indique si le système est dans un état d’accès restreint, de stage ou d’accès non restreint, ainsi que des informations [**ExtendedIsolationState**](/windows/win32/api/naptypes/ne-naptypes-extendedisolationstate) .

</dd> <dt>

*unknownConnections* \[ à\]
</dt> <dd>

Pointeur vers un **booléen** qui a la **valeur true** si toutes les connexions sont dans un état inconnu et **false** dans le cas contraire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                             | Description                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Opération réussie.<br/>                                                                                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Erreur d’autorisation, accès refusé.<br/>                                                                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Limite du système, impossible d’effectuer l’opération.<br/>                                                             |
| <dl> <dt>**NAP \_ E \_ non \_ initialisé**</dt> </dl> | L’algorithme SHA n’a pas été précédemment initialisé.<br/>                                                                        |
| <dl> <dt>**RPC \_ E \_ déconnecté**</dt> </dl>     | Le NapAgent a été arrêté. Cet objet est automatiquement récupéré et est de nouveau lié au NapAgent, une fois qu’il a redémarré.<br/> |



 

## <a name="remarks"></a>Notes

L’algorithme SHA doit libérer la structure [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) en appelant [**FreeIsolationInfoEx**](freeisolationinfoex.md).

L’algorithme SHA doit appeler [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) avant d’appeler cette méthode ou toute autre méthode de l’interface [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)
</dt> </dl>

 

 





