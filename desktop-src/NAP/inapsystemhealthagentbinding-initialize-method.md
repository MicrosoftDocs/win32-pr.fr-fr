---
title: INapSystemHealthAgentBinding Initialize, méthode (NapSystemHealthAgent. h)
description: Initialise l’agent d’intégrité système (SHA) et lie l’algorithme SHA au service NapAgent.
ms.assetid: abbc942b-0217-4b07-bf43-fab55ca9c411
keywords:
- Initialiser la méthode NAP
- Méthode Initialize NAP, interface INapSystemHealthAgentBinding
- INapSystemHealthAgentBinding interface NAP, Initialize, méthode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ee4d4f602303ca1943e47c04ba30ab8f6e75e72
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317133"
---
# <a name="inapsystemhealthagentbindinginitialize-method"></a>INapSystemHealthAgentBinding :: Initialize, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSystemHealthAgentBinding :: Initialize** Initialise l’agent d’intégrité système (SHA) et lie l’algorithme SHA au service NapAgent. Cette méthode doit être appelée avant d’appeler toute autre méthode sur l’interface [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId          id,
  [in] INapSystemHealthAgentCallback *callback
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ID* \[ dans\]
</dt> <dd>

[SystemHealthEntityId](nap-datatypes.md) unique qui contient l’ID de l’agent SHA lié au service NapAgent.

</dd> <dt>

*rappel* \[ dans\]
</dt> <dd>

Pointeur COM vers une interface [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md) utilisée par le NapAgent pour rappeler l’agent d’intégrité avec une notification/un processus. Le NapAgent contient une référence à l’objet associé à cette interface jusqu’à ce que [**Uninitialize**](inapsystemhealthagentbinding-uninitialize-method.md) soit appelé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                                | Description                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                      | Opération réussie.<br/>                                                                                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>            | Erreur d’autorisation, accès refusé.<br/>                                                                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>             | Limite du système, impossible d’effectuer l’opération.<br/>                                                             |
| <dl> <dt>**ERREUR \_ déjà \_ initialisée**</dt> </dl> | Si l’agent SHA a été initialisé précédemment, cette erreur est retournée.<br/>                                                      |
| <dl> <dt>**NAP \_ E \_ non \_ inscrit**</dt> </dl>     | Si l’agent SHA n’a pas été inscrit précédemment, cette erreur est retournée.<br/>                                                      |
| <dl> <dt>**RPC \_ E \_ déconnecté**</dt> </dl>        | Le NapAgent a été arrêté. Cet objet est automatiquement récupéré et est de nouveau lié au NapAgent, une fois qu’il a redémarré.<br/> |



 

## <a name="remarks"></a>Notes

NapAgent ne déclenche pas d’échange SoH en raison de l’initialisation. Un agent d’intégrité système doit appeler [**NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) pour demander un échange de paquets SOH après l’initialisation avec NapAgent.

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

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





