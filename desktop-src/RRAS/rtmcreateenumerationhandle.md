---
title: Fonction RtmCreateEnumerationHandle (RTM. h)
description: La fonction RtmCreateEnumerationHandle retourne un handle à utiliser avec RtmEnumerateGetNextRoute pour analyser tous les itinéraires, ou un sous-ensemble d’itinéraires, connus du gestionnaire de tables de routage.
ms.assetid: 73e3ac7d-498a-4d89-a6b5-17aaf4b17ec2
keywords:
- RtmCreateEnumerationHandle fonction RAS
topic_type:
- apiref
api_name:
- RtmCreateEnumerationHandle
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14086639db299038139e0e7d02eb12bb892042bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127239490"
---
# <a name="rtmcreateenumerationhandle-function"></a>RtmCreateEnumerationHandle fonction)

\[cette api a été remplacée par l’api du [gestionnaire de Table de routage Version 2](about-routing-table-manager-version-2.md) et ne sera pas disponible au-delà de Windows Server 2003. Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]

La fonction **RtmCreateEnumerationHandle** retourne un handle à utiliser avec [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md) pour analyser tous les itinéraires, ou un sous-ensemble d’itinéraires, connus du gestionnaire de tables de routage.

## <a name="syntax"></a>Syntaxe


```C++
HANDLE RtmCreateEnumerationHandle(
  _In_ DWORD ProtocolFamily,
  _In_ DWORD EnumerationFlags,
  _In_ PVOID CriteriaRoute
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ProtocolFamily* \[ dans\]
</dt> <dd>

Spécifie la famille de protocoles des itinéraires à énumérer.

</dd> <dt>

*EnumerationFlags* \[ dans\]
</dt> <dd>

Spécifie les itinéraires qui doivent être énumérés. Ce paramètre limite l’ensemble des itinéraires retournés par l’API d’énumération à un sous-ensemble défini par les indicateurs suivants et les valeurs des membres correspondants de la structure vers laquelle pointe le paramètre *CriteriaRoute* . Ce paramètre peut prendre les valeurs suivantes.



| EnumerationFlags                                                                                                                                                                              | Signification                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ONLY_THIS_NETWORK"></span><span id="rtm_only_this_network"></span><dl> <dt>**RTM \_ uniquement \_ ce \_ réseau**</dt> </dl>       | Énumérer uniquement les itinéraires qui ont le même numéro de réseau que le \_ membre de réseau RR de la structure vers laquelle pointe CriteriaRoute.<br/>                        |
| <span id="RTM_ONLY_THIS_INTERFACE"></span><span id="rtm_only_this_interface"></span><dl> <dt>**RTM \_ uniquement \_ cette \_ interface**</dt> </dl> | Énumère uniquement les itinéraires obtenus par le biais de l’interface spécifiée par le \_ champ de RR InterfaceId de la structure vers laquelle pointe CriteriaRoute.<br/>    |
| <span id="RTM_ONLY_THIS_PROTOCOL"></span><span id="rtm_only_this_protocol"></span><dl> <dt>**RTM \_ uniquement \_ ce \_ protocole**</dt> </dl>    | Énumère uniquement les itinéraires qui ont été ajoutés par le protocole de routage spécifié par le \_ champ ROUTINGPROTOCOL RR de la structure vers laquelle pointe CriteriaRoute.<br/> |
| <span id="RTM_ONLY_BEST_ROUTES"></span><span id="rtm_only_best_routes"></span><dl> <dt>**les \_ \_ meilleurs \_ itinéraires RTM**</dt> </dl>          | Énumérer uniquement les meilleurs itinéraires à chacun des réseaux de l’ensemble.<br/>                                                                                           |



 

</dd> <dt>

*CriteriaRoute* \[ dans\]
</dt> <dd>

Pointeur vers une structure de route spécifique à la famille de protocoles ([**\_ \_ itinéraire IP RTM**](rtm-ip-route.md) ou [**\_ \_ itinéraire IPX RTM**](rtm-ipx-route.md)). Les valeurs de membre de cette structure correspondent aux indicateurs spécifiés par le paramètre *EnumerationFlags* .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction est réussie, la valeur de retour est un **handle** à utiliser avec les appels d’énumération suivants.

Si la fonction échoue ou qu’il n’existe aucun itinéraire avec les critères spécifiés, la valeur de retour est **null**. Appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir plus d’informations.



| Valeur                                                                                                       | Description                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERREUR \_ aucun \_ itinéraire**</dt> </dl>            | Aucun itinéraire n’a les critères spécifiés.<br/>                                                             |
| <dl> <dt>**paramètre d’erreur \_ non valide \_**</dt> </dl>    | Un ou plusieurs des paramètres d’entrée ne sont pas valides (par exemple, famille de protocole inconnue, indicateurs d’énumération non valides).<br/> |
| <dl> <dt>**ERREUR \_ aucune \_ \_ ressource système**</dt> </dl> | Les ressources sont insuffisantes pour effectuer l’opération.<br/>                                                      |
| <dl> <dt>**ERREUR \_ de \_ mémoire insuffisante \_**</dt> </dl>   | La mémoire est insuffisante pour allouer le descripteur.<br/>                                                              |



 

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

[**\_itinéraire IP \_ RTM**](rtm-ip-route.md)
</dt> <dt>

[**\_itinéraire IPX \_ RTM**](rtm-ipx-route.md)
</dt> <dt>

[**RtmCloseEnumerationHandle**](rtmcloseenumerationhandle.md)
</dt> <dt>

[**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md)
</dt> </dl>

 

