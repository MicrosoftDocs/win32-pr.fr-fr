---
title: Fonction RtmRegisterClient (RTM. h)
description: La fonction RtmRegisterClient inscrit un client en tant que gestionnaire du protocole spécifié. Il établit un mécanisme de notification de changement d’itinéraire pour le client et définit des options de protocole.
ms.assetid: 70426601-695d-47ed-b71a-1df3fb8ddf10
keywords:
- RtmRegisterClient fonction RAS
topic_type:
- apiref
api_name:
- RtmRegisterClient
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 564f47e68fd6cdce3d5437fe184bac1ed74d8322
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743109"
---
# <a name="rtmregisterclient-function"></a>RtmRegisterClient fonction)

\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003. Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]

La fonction **RtmRegisterClient** inscrit un client en tant que gestionnaire du protocole spécifié. Il établit un mécanisme de notification de changement d’itinéraire pour le client et définit des options de protocole.

## <a name="syntax"></a>Syntaxe


```C++
HANDLE RtmRegisterClient(
  _In_ DWORD  ProtocolFamily,
  _In_ DWORD  RoutingProtocol,
  _In_ HANDLE ChangeEvent,
  _In_ DWORD  Flags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ProtocolFamily* \[ dans\]
</dt> <dd>

Spécifie la famille de protocoles du protocole de routage à inscrire.

</dd> <dt>

*RoutingProtocol* \[ dans\]
</dt> <dd>

Spécifie l’identificateur de protocole de routage, identique à celui utilisé lors de l’inscription auprès du gestionnaire de routage. Consultez [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol).

</dd> <dt>

*ChangeEvent* \[ dans\]
</dt> <dd>

Spécifie qu’un itinéraire optimal vers un réseau de la table a changé. Le gestionnaire de table de routage signale cet événement après une modification du meilleur itinéraire vers un réseau de la table. Pour plus d’informations sur la notification de modification de route, consultez [**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md) .

Ce paramètre est facultatif. Si l’appelant spécifie la **valeur null** pour ce paramètre, le gestionnaire de tables de routage ne notifie pas le client des modifications dans le meilleur état d’itinéraire.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Spécifie diverses options pour le traitement spécial du protocole de routage. La valeur suivante est actuellement prise en charge.



| Indicateurs                                                                                                                                                                                               | Signification                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_PROTOCOL_SINGLE_ROUTE"></span><span id="rtm_protocol_single_route"></span><dl> <dt>**\_ \_ itinéraire unique du protocole RTM \_**</dt> </dl> | Le gestionnaire de tables de routage conserve un seul itinéraire par réseau de destination pour le protocole de routage. En d’autres termes, le gestionnaire de tables de routage remplace les entrées d’itinéraire qui ont les mêmes numéros de réseau de destination au lieu d’en ajouter de nouveaux.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de retour réussi, valeur de **handle** qui identifie le client lors des appels suivants au gestionnaire de tables de routage.

Un descripteur **null** indique que le gestionnaire de table de routage n’a pas pu inscrire le client. Appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir la raison de l’échec.



| Valeur                                                                                                         | Description                                                                                     |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**le \_ client d’erreur \_ \_ existe déjà**</dt> </dl> | Un autre client s’est déjà inscrit pour gérer le protocole spécifié.<br/>              |
| <dl> <dt>**paramètre d’erreur \_ non valide \_**</dt> </dl>      | La famille de protocoles spécifiée n’est pas prise en charge ou le paramètre *Flags* n’est pas valide.<br/> |
| <dl> <dt>**ERREUR \_ aucune \_ \_ ressource système**</dt> </dl>   | Ressources insuffisantes pour effectuer l’opération.<br/>                                   |
| <dl> <dt>**ERREUR \_ de \_ mémoire insuffisante \_**</dt> </dl>     | Mémoire insuffisante pour allouer des structures de données pour le client.<br/>                      |



 

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

[**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol)
</dt> <dt>

[Identificateurs de famille de protocole RTMv1](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> <dt>

[**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md)
</dt> <dt>

[**RtmDeregisterClient**](rtmderegisterclient.md)
</dt> </dl>

 

