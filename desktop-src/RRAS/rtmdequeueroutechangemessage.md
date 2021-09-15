---
title: Fonction RtmDequeueRouteChangeMessage (RTM. h)
description: La fonction RtmDequeueRouteChangeMessage retourne le prochain message de modification de l’itinéraire dans la file d’attente associée au client spécifié.
ms.assetid: 44f2116a-3c8d-4ac6-896e-b12930b218a5
keywords:
- RtmDequeueRouteChangeMessage fonction RAS
topic_type:
- apiref
api_name:
- RtmDequeueRouteChangeMessage
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 448df230742b03f82294de102bf14b50fefa035c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238271"
---
# <a name="rtmdequeueroutechangemessage-function"></a>RtmDequeueRouteChangeMessage fonction)

\[cette api a été remplacée par l’api du [gestionnaire de Table de routage Version 2](about-routing-table-manager-version-2.md) et ne sera pas disponible au-delà de Windows Server 2003. Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]

La fonction **RtmDequeueRouteChangeMessage** retourne le prochain message de modification de l’itinéraire dans la file d’attente associée au client spécifié.

## <a name="syntax"></a>Syntaxe


```C++
DWORD RtmDequeueRouteChangeMessage(
  _In_  HANDLE ClientHandle,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute,
  _Out_ PVOID  PrevBestRoute
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ClientHandle* \[ dans\]
</dt> <dd>

Handle qui identifie le client pour lequel l’opération est effectuée. Obtenez ce handle en appelant [**RtmRegisterClient**](rtmregisterclient.md).

</dd> <dt>

*Indicateurs* \[ à\]
</dt> <dd>

Pointeur vers une variable **DWORD** . La valeur de cette variable est définie par le gestionnaire de tables de routage. La valeur spécifie le type du message de modification et les informations qui ont été retournées dans les mémoires tampons fournies. Ce paramètre est l’un des éléments suivants.



| Indicateurs                                                                                                                                                                      | Signification                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <dt>**\_itinéraire RTM \_ ajouté**</dt> </dl>       | Le premier itinéraire a été ajouté pour un réseau de destination particulier. Le paramètre *CurBestRoute* pointe vers les informations de l’itinéraire ajouté.<br/>                                                                                                                                                            |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <dt>**\_itinéraire RTM \_ supprimé**</dt> </dl> | Le seul itinéraire disponible pour un réseau de destination particulier a été supprimé. Le paramètre *PrevBestRoute* pointe vers les informations de l’itinéraire supprimé.<br/>                                                                                                                                              |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**\_itinéraire RTM \_ modifié**</dt> </dl> | Au moins un des paramètres significatifs a été modifié pour un itinéraire optimal vers un réseau de destination particulier. Les paramètres significatifs sont les suivants : <br/> Identificateur de protocole<br/> Index d’interface<br/> Adresse du tronçon suivant<br/> Données spécifiques à la famille de protocoles (y compris les métriques d’itinéraires)<br/> |



 

Le paramètre *PrevBestRoute* pointe vers les informations d’itinéraire telles qu’elles étaient avant la modification. Le paramètre *CurBestRoute* pointe vers les informations d’itinéraire actuelles (autrement dit, après modification).

</dd> <dt>

*CurBestRoute* \[ à\]
</dt> <dd>

Pointeur vers une structure qui reçoit les informations de meilleure route actuelles (le cas échéant). Le type de la structure est spécifique à la famille de protocoles, par exemple, IP ou IPX.

Ce paramètre est facultatif. Si l’appelant spécifie la **valeur null** pour ce paramètre, les informations de meilleure route actuelles ne sont pas retournées.

</dd> <dt>

*PrevBestRoute* \[ à\]
</dt> <dd>

Pointeur vers une structure qui reçoit les informations de meilleur itinéraire précédentes, le cas échéant. Le type de la structure est spécifique à la famille de protocoles, par exemple, IP ou IPX.

Ce paramètre est facultatif. Si l’appelant spécifie **null** pour ce paramètre, les informations sur le meilleur itinéraire précédent ne sont pas retournées.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est l’un des codes suivants.



| Valeur                                                                                                       | Description                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**AUCUNE \_ erreur**</dt> </dl>                    | Ce message était le dernier message de la file d’attente du client. L’objet d’événement est réinitialisé.<br/>                                                                                                                                               |
| <dl> <dt>**HANDLE d’erreur \_ non valide \_**</dt> </dl>       | Le paramètre *ClientHandle* n’est pas un handle valide, ou à l’inscription, le client n’a pas fourni d’objet d’événement pour la notification de modification de message (voir [**RtmRegisterClient**](rtmregisterclient.md)).<br/>                           |
| <dl> <dt>**MESSAGES d’erreur \_ supplémentaires \_**</dt> </dl>        | La file d’attente du client contient des messages supplémentaires. Le client doit appeler **RtmDequeueRouteChangeMessage** à nouveau dès que possible pour permettre au gestionnaire de tables de routage de libérer les ressources associées aux messages en attente.<br/> |
| <dl> <dt>**ERREUR \_ aucun \_ message**</dt> </dl>          | La file d’attente du client ne contient aucun message. l’appel n’a pas été sollicité. L’événement est réinitialisé.<br/>                                                                                                                                            |
| <dl> <dt>**ERREUR \_ aucune \_ \_ ressource système**</dt> </dl> | Les ressources sont insuffisantes pour effectuer l’opération.<br/>                                                                                                                                                                      |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>RTM. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>RTM. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Rtm.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence de la version 1 du gestionnaire de tables de routage](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Fonctions de la version 1 du gestionnaire de table de routage](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**RtmRegisterClient**](rtmregisterclient.md)
</dt> </dl>

 

 





