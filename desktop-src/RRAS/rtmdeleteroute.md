---
title: Fonction RtmDeleteRoute (RTM. h)
description: La fonction RtmDeleteRoute supprime une entrée d’itinéraire.
ms.assetid: a98026e9-40f5-42e9-943c-dfc561feef6d
keywords:
- RtmDeleteRoute fonction RAS
topic_type:
- apiref
api_name:
- RtmDeleteRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0efe2e34345cc335b8214b781da4dce608dddcc4c2f77e80d8c86f76007c2855
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073849"
---
# <a name="rtmdeleteroute-function"></a>RtmDeleteRoute fonction)

\[cette api a été remplacée par l’api du [gestionnaire de Table de routage Version 2](about-routing-table-manager-version-2.md) et ne sera pas disponible au-delà de Windows Server 2003. Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]

La fonction **RtmDeleteRoute** supprime une entrée d’itinéraire.

## <a name="syntax"></a>Syntaxe


```C++
DWORD RtmDeleteRoute(
  _In_  HANDLE ClientHandle,
  _In_  PVOID  Route,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ClientHandle* \[ dans\]
</dt> <dd>

Handle qui identifie le client et, par conséquent, le protocole de routage de l’itinéraire ajouté ou mis à jour. Obtenez ce handle en appelant [**RtmRegisterClient**](rtmregisterclient.md).

</dd> <dt>

*Itinéraire* \[ dans\]
</dt> <dd>

Pointeur vers une structure spécifique à la famille de protocoles qui spécifie l’itinéraire nouveau ou mis à jour. Les champs suivants sont utilisés par le gestionnaire de tables de routage pour mettre à jour la table de routage :



| Valeur                                                                                                                                                                                                         | Signification                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <dt>**Réseau de RR \_**</dt> </dl>                             | Spécifie le numéro de réseau de destination. <br/>                                 |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <dt>**RR \_ InterfaceId**</dt> </dl>             | Spécifie l’index de l’interface par le biais duquel l’itinéraire a été reçu.<br/> |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <dt>**\_NEXTHOPADDRESS RR**</dt> </dl> | Spécifie l’adresse réseau du routeur de tronçon suivant.<br/>                      |



 

</dd> <dt>

*Indicateurs* \[ à\]
</dt> <dd>

Pointeur vers un jeu d’indicateurs qui indiquent le type du message de modification et les informations qui ont été placées dans les mémoires tampons fournies. Ce paramètre est l’une des valeurs suivantes.



| Indicateurs                                                                                                                                                                      | Signification                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <dt>**RTM- \_ aucune \_ modification**</dt> </dl>             | La suppression de l’itinéraire n’a pas affecté le meilleur itinéraire vers un réseau de destination. En d’autres termes, une autre entrée représente un itinéraire vers le même réseau de destination et a une métrique inférieure.<br/> |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <dt>**\_itinéraire RTM \_ supprimé**</dt> </dl> | L’itinéraire supprimé était le seul itinéraire disponible pour un réseau de destination particulier.<br/>                                                                                                  |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**\_itinéraire RTM \_ modifié**</dt> </dl> | Après la suppression de cet itinéraire, un autre itinéraire est devenu le meilleur itinéraire vers un réseau de destination particulier. *CurBestRoute* pointe vers les informations pour le nouveau meilleur itinéraire.<br/>               |



 

</dd> <dt>

*CurBestRoute* \[ à\]
</dt> <dd>

Pointeur vers une structure qui reçoit les informations de meilleure route actuelles, le cas échéant. Le type de la structure est spécifique à la famille de protocoles, par exemple, IP ou IPX.

Ce paramètre est facultatif. Si l’appelant spécifie la **valeur null** pour ce paramètre, les informations de meilleure route actuelles ne sont pas retournées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour n’est **pas une \_ erreur**.

Si la fonction échoue, la valeur de retour est l’un des codes d’erreur suivants.



| Valeur                                                                                                       | Description                                                                                            |
|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**HANDLE d’erreur \_ non valide \_**</dt> </dl>       | Le paramètre de handle du client n’est pas un handle valide.<br/>                                          |
| <dl> <dt>**paramètre d’erreur \_ non valide \_**</dt> </dl>    | La structure d’itinéraire vers laquelle pointe le paramètre d' *itinéraire* contient une valeur de membre.<br/>            |
| <dl> <dt>**ERREUR \_ aucun \_ itinéraire de ce type \_**</dt> </dl>       | Il n’existe aucune entrée dans la table de routage qui correspond aux paramètres de l’itinéraire spécifié.<br/> |
| <dl> <dt>**ERREUR \_ aucune \_ \_ ressource système**</dt> </dl> | Les ressources sont insuffisantes pour effectuer l’opération. <br/>                                 |



 

## <a name="remarks"></a>Remarques

La fonction génère un message de modification d’itinéraire si le meilleur itinéraire vers un réseau de destination a été modifié à la suite de la suppression. Toutefois, le message de modification d’itinéraire n’est pas envoyé au client qui effectue cet appel. Au lieu de cela, les informations pertinentes sont retournées par cette fonction directement à ce client.

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

[**RtmAddRoute**](rtmaddroute.md)
</dt> <dt>

[**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





