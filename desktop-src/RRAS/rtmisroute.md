---
title: Fonction RtmIsRoute (RTM. h)
description: La fonction RtmIsRoute détermine s’il existe un ou plusieurs itinéraires vers un réseau de destination spécifié. Si c’est le cas, la fonction retourne des informations pour le meilleur itinéraire vers ce réseau.
ms.assetid: f9939790-d0a6-487e-9674-a01d436dc962
keywords:
- RtmIsRoute fonction RAS
topic_type:
- apiref
api_name:
- RtmIsRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 312b43a7cf66e17cc6016fe3ad35bd21cd1e7ae19ecd7864a10de4d977a92ac9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073809"
---
# <a name="rtmisroute-function"></a>RtmIsRoute fonction)

\[cette api a été remplacée par l’api du [gestionnaire de Table de routage Version 2](about-routing-table-manager-version-2.md) et ne sera pas disponible au-delà de Windows Server 2003. Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]

La fonction **RtmIsRoute** détermine s’il existe un ou plusieurs itinéraires vers un réseau de destination spécifié. Si c’est le cas, la fonction retourne des informations pour le meilleur itinéraire vers ce réseau.

## <a name="syntax"></a>Syntaxe


```C++
BOOL RtmIsRoute(
  _In_  DWORD ProtocolFamily,
  _In_  PVOID Network,
  _Out_ PVOID BestRoute
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ProtocolFamily* \[ dans\]
</dt> <dd>

Spécifie le type de structure de données vers lequel pointe le paramètre *réseau* , par exemple, réseau [**IP \_**](ip-network.md), [**\_ réseau IPX**](ipx-network.md).

</dd> <dt>

*Réseau* \[ dans\]
</dt> <dd>

Pointeur vers une structure qui spécifie les données de numéro de réseau spécifiques à la famille de protocoles. Ces données identifient le réseau pour lequel l’appelant recherche des informations de routage.

</dd> <dt>

*BestRoute* \[ à\]
</dt> <dd>

Pointeur vers une structure spécifique à la famille de protocoles qui reçoit les meilleures informations d’itinéraire actuelles, le cas échéant.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est l’un des codes suivants.



| Valeur                                                                                                       | Description                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**:**</dt> </dl>                         | Au moins un itinéraire vers le réseau spécifié existe. Le meilleur itinéraire est retourné dans la structure vers laquelle pointe le paramètre *BestRoute* .<br/>      |
| <dl> <dt>**FAUSSES**</dt> </dl>                        | Il n’y a pas d’itinéraire vers le réseau spécifié, ou l’opération a échoué. Appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir plus d’informations :<br/> |
| <dl> <dt>**AUCUNE \_ erreur**</dt> </dl>                    | L’opération a réussi, mais il n’y a pas d’itinéraire vers le réseau spécifié.<br/>                                                                      |
| <dl> <dt>**paramètre d’erreur \_ non valide \_**</dt> </dl>    | La valeur du paramètre *ProtocolFamily* ne correspond à aucune famille de protocoles installée.<br/>                                             |
| <dl> <dt>**ERREUR \_ aucune \_ \_ ressource système**</dt> </dl> | Les ressources sont insuffisantes pour effectuer l’opération.<br/>                                                                                  |



 

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

[**\_réseau IP**](ip-network.md)
</dt> <dt>

[**\_réseau IPX**](ipx-network.md)
</dt> <dt>

[Identificateurs de famille de protocole RTMv1](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

