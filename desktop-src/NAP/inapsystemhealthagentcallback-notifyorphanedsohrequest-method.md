---
title: Méthode INapSystemHealthAgentCallback NotifyOrphanedSoHRequest (NapSystemHealthAgent. h)
description: Est appelé si un SoHRequest a été interrogé à partir de l’algorithme SHA, mais que la réponse n’a jamais été renvoyée.
ms.assetid: 9e6fac6c-fb23-4725-ae0f-28ef8a6c4ea6
keywords:
- Méthode NotifyOrphanedSoHRequest NAP
- Méthode NotifyOrphanedSoHRequest NAP, interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP, méthode NotifyOrphanedSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.NotifyOrphanedSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 676b67b61a9375f4fd44ecc41f9e56e92a97b693
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011639"
---
# <a name="inapsystemhealthagentcallbacknotifyorphanedsohrequest-method"></a>INapSystemHealthAgentCallback :: NotifyOrphanedSoHRequest, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSystemHealthAgentCallback :: NotifyOrphanedSoHRequest** est appelée si un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) a été interrogé à partir de l’algorithme SHA, mais que la réponse n’a jamais été renvoyée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT NotifyOrphanedSoHRequest(
  [in] const CorrelationId *correlationId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CorrelationId* \[ dans\]
</dt> <dd>

Pointeur vers la structure d’ID de [**corrélation**](/windows/win32/api/naptypes/ns-naptypes-correlationid) unique qui identifie le [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)orphelin.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                          | Description                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Indique la réussite de l’opération.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode de rappel est déclarée par le système NAP et doit être implémentée par l’enregistreur SHA.

Cette méthode peut être appelée par le système dans les cas suivants :

-   Un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) n’a pas pu être envoyé sur le réseau.
-   Un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) a été envoyé sur le réseau, mais aucun **SoHResponse** n’a été renvoyé, c.-à-d. que l’application a dépassé le délai d’attente ou qu’il n’y avait pas de validateur de validateur correspondant côté serveur.
-   La connexion s’est arrêtée ou un enforceur est passé hors connexion.

Comme il ne s’agit que d’une notification de meilleur effort, il ne doit pas compter sur ces informations pour nettoyer l’État. Il existe plusieurs situations dans lesquelles un SHA ne sera pas notifié :

-   En cas de dysfonctionnement d’un application, autrement dit, il n’avertit pas l’SHA lorsque l’état de la connexion est inactif.
-   Si une application se bloque.
-   Dans les conditions d’erreur, par exemple, la mémoire NapAgent est insuffisante.

Les agents d’intégrité du service peuvent obtenir des notifications erronées lorsqu’ils se lient pour la première fois au NapAgent, par exemple, si un échange SoH est en cours d’exécution lorsque la liaison SHA est terminée, puis expire.

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

 

 





