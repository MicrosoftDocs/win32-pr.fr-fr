---
title: Fonction RtmAddRoute (RTM. h)
description: La fonction RtmAddRoute ajoute une entrée de routage ou met à jour une entrée d’itinéraire existante.
ms.assetid: 09a9b57d-f10b-40b7-a3c1-2e0613f29431
keywords:
- RtmAddRoute fonction RAS
topic_type:
- apiref
api_name:
- RtmAddRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c3ee68c9b026fc37457819777e69d2be7984e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510982"
---
# <a name="rtmaddroute-function"></a>RtmAddRoute fonction)

\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003. Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]

La fonction **RtmAddRoute** ajoute une entrée de routage ou met à jour une entrée d’itinéraire existante.

## <a name="syntax"></a>Syntaxe


```C++
DWORD RtmAddRoute(
  _In_  HANDLE ClientHandle,
  _In_  PVOID  Route,
  _In_  DWORD  TimeToLive,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute,
  _Out_ PVOID  PrevBestRoute
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ClientHandle* \[ dans\]
</dt> <dd>

Handle qui identifie le client et, par conséquent, le protocole de routage, qui a ajouté ou mis à jour l’itinéraire. Obtenez ce handle en appelant [**RtmRegisterClient**](rtmregisterclient.md).

</dd> <dt>

*Itinéraire* \[ dans\]
</dt> <dd>

Pointeur vers une structure spécifique à la famille de protocoles qui spécifie l’itinéraire nouveau ou mis à jour. Les champs suivants sont utilisés par le gestionnaire de tables de routage pour mettre à jour la table de routage :



| Valeur                                                                                                                                                                                                                                 | Signification                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <dt>**Réseau de RR \_**</dt> </dl>                                                     | Spécifie le numéro de réseau de destination.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <dt>**RR \_ InterfaceId**</dt> </dl>                                     | Spécifie l’index de l’interface par le biais duquel l’itinéraire a été reçu.<br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <dt>**\_NEXTHOPADDRESS RR**</dt> </dl>                         | Spécifie l’adresse du routeur de tronçon suivant.<br/>                                                                                                                                                                                                                                                                                                                                                  |
| <span id="RR_FamilySpecificData"></span><span id="rr_familyspecificdata"></span><span id="RR_FAMILYSPECIFICDATA"></span><dl> <dt>**\_FAMILYSPECIFICDATA RR**</dt> </dl>         | Spécifie les données qui sont spécifiques à la famille de protocoles. Bien que les données soient transparentes pour le gestionnaire de tables de routage, elles sont prises en compte lors de la comparaison des itinéraires pour déterminer si les informations de routage ont changé. Les données sont également utilisées pour définir des valeurs de métrique qui sont indépendantes du protocole de routage. Par conséquent, ces données sont utilisées pour déterminer le meilleur itinéraire pour le réseau de destination.<br/> |
| <span id="RR_ProtocolSpecificData"></span><span id="rr_protocolspecificdata"></span><span id="RR_PROTOCOLSPECIFICDATA"></span><dl> <dt>**\_PROTOCOLSPECIFICDATA RR**</dt> </dl> | Spécifie des données qui sont spécifiques au protocole de routage qui a fourni l’itinéraire.<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="RR_TimeStamp"></span><span id="rr_timestamp"></span><span id="RR_TIMESTAMP"></span><dl> <dt>**Horodateur du RR \_**</dt> </dl>                                             | Spécifie l’heure système actuelle. Ce champ est défini par le gestionnaire de tables de routage.<br/>                                                                                                                                                                                                                                                                                                             |



 

</dd> <dt>

*TimeToLive* \[ dans\]
</dt> <dd>

Spécifie le nombre de secondes pendant lesquelles l’itinéraire spécifié doit être conservé dans la table de routage. Si ce paramètre est défini sur Infinite, l’itinéraire est conservé jusqu’à ce qu’il soit explicitement supprimé. La limite actuelle pour *TimeToLive* est 2147483 s (24 + jours).

</dd> <dt>

*Indicateurs* \[ à\]
</dt> <dd>

Pointeur vers une variable **DWORD** . La valeur de cette variable est définie par le gestionnaire de tables de routage. La valeur indique le type de la modification et les informations qui ont été retournées dans les mémoires tampons fournies. Ce paramètre est l’un des éléments suivants.



| Indicateurs                                                                                                                                                                      | Signification                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <dt>**RTM- \_ aucune \_ modification**</dt> </dl>             | L’ajout ou la mise à jour n’a modifié aucun des paramètres d’itinéraire significatifs, ou l’entrée de route affectée n’est pas la meilleure route parmi les entrées pour le réseau de destination.<br/>                                                                                                          |
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <dt>**\_itinéraire RTM \_ ajouté**</dt> </dl>       | L’itinéraire a été ajouté pour le réseau de destination. Le paramètre *CurBestRoute* pointe vers les informations de l’itinéraire ajouté.<br/>                                                                                                                                                                    |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**\_itinéraire RTM \_ modifié**</dt> </dl> | Au moins un des paramètres significatifs a été modifié pour le meilleur itinéraire vers le réseau de destination. Les paramètres significatifs sont les suivants : <br/> Identificateur de protocole<br/> Index d’interface<br/> Adresse du tronçon suivant<br/> Données spécifiques à la famille de protocoles (y compris les métriques d’itinéraires)<br/> |



 

Le paramètre *PrevBestRoute* pointe vers les informations d’itinéraire telles qu’elles étaient avant la modification. Le paramètre *CurBestRoute* pointe vers les informations d’itinéraire actuelles (c’est-à-dire après modification).

</dd> <dt>

*CurBestRoute* \[ à\]
</dt> <dd>

Pointeur vers une structure qui reçoit les informations de meilleure route actuelles, le cas échéant. Le type de la structure est spécifique à la famille de protocoles, par exemple, IP ou IPX.

Ce paramètre est facultatif. Si l’appelant spécifie la **valeur null** pour ce paramètre, les informations de meilleure route actuelles ne sont pas retournées.

</dd> <dt>

*PrevBestRoute* \[ à\]
</dt> <dd>

Pointeur vers une structure qui reçoit les informations de meilleur itinéraire précédentes, le cas échéant. Le type de la structure est spécifique à la famille de protocoles, par exemple, IP ou IPX.

Ce paramètre est facultatif. Si l’appelant spécifie **null** pour ce paramètre, les informations sur le meilleur itinéraire précédent ne sont pas retournées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est l’un des codes suivants.



| Valeur                                                                                                       | Description                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**AUCUNE \_ erreur**</dt> </dl>                    | L’itinéraire a été ajouté ou mis à jour avec succès.<br/>                 |
| <dl> <dt>**HANDLE d’erreur \_ non valide \_**</dt> </dl>       | Le paramètre de handle du client n’est pas un handle valide.<br/>           |
| <dl> <dt>**paramètre d’erreur \_ non valide \_**</dt> </dl>    | La structure de l’itinéraire contient un paramètre non valide.<br/>           |
| <dl> <dt>**ERREUR \_ aucune \_ \_ ressource système**</dt> </dl> | Les ressources sont insuffisantes pour effectuer l’opération.<br/> |
| <dl> <dt>**ERREUR \_ de \_ mémoire insuffisante \_**</dt> </dl>   | La mémoire est insuffisante pour allouer l’entrée d’itinéraire.<br/>    |



 

## <a name="remarks"></a>Notes

La fonction génère un message de modification de l’itinéraire si le meilleur itinéraire vers un réseau de destination a été modifié à la suite de cette opération. Toutefois, le message de modification d’itinéraire n’est pas envoyé au client qui effectue cet appel. Au lieu de cela, les informations pertinentes sont retournées par cette fonction directement à ce client via les paramètres *Flags*, *CurBestRoute* et *PrevBestRoute* .

## <a name="requirements"></a>Configuration requise



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

[**RtmDeleteRoute**](rtmdeleteroute.md)
</dt> <dt>

[**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





