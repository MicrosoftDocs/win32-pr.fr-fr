---
title: Fonction RtmGetNextRoute (RTM. h)
description: La fonction RtmGetNextRoute retourne l’itinéraire suivant à partir du sous-ensemble spécifié d’itinéraires dans la table.
ms.assetid: 0f413276-2ace-4216-a1a0-1b3061bacc4a
keywords:
- RtmGetNextRoute fonction RAS
topic_type:
- apiref
api_name:
- RtmGetNextRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da8592855e0c30cef2ed43b7818badd336bc2ab6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508782"
---
# <a name="rtmgetnextroute-function"></a>RtmGetNextRoute fonction)

\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003. Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]

La fonction **RtmGetNextRoute** retourne l’itinéraire suivant à partir du sous-ensemble spécifié d’itinéraires dans la table.

## <a name="syntax"></a>Syntaxe


```C++
DWORD RtmGetNextRoute(
  _In_    DWORD ProtocolFamily,
  _In_    DWORD EnumerationFlags,
  _Inout_ PVOID Route
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ProtocolFamily* \[ dans\]
</dt> <dd>

Spécifie la famille de protocoles d’itinéraires à récupérer, par exemple, IP ou IPX.

</dd> <dt>

*EnumerationFlags* \[ dans\]
</dt> <dd>

Spécifie les itinéraires qui doivent être énumérés. Ce paramètre limite l’ensemble des itinéraires supprimés à un sous-ensemble défini par les indicateurs suivants et les valeurs des membres correspondants de la structure vers laquelle pointe le paramètre *CriteriaRoute* . Les indicateurs sont les mêmes que ceux utilisés dans [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).

</dd> <dt>

*Itinéraire* \[ in, out\]
</dt> <dd>

En entrée, l' *itinéraire* pointe vers une structure spécifique à la famille de protocoles ( [**\_ \_ itinéraire IP RTM**](rtm-ip-route.md) ou [**\_ \_ itinéraire IPX RTM**](rtm-ipx-route.md)).

La fonction appelante fournit des valeurs de membre pour cette structure. Ces valeurs, conjointement avec le paramètre *EnumerationFlags* , spécifient le jeu à partir duquel les itinéraires doivent être retournés.

Lors de la sortie, l' *itinéraire* pointe vers une structure qui reçoit le premier itinéraire correspondant aux critères spécifiés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour n’est **pas une \_ erreur**.

Si la fonction échoue, la valeur de retour est l’un des codes d’erreur suivants.



| Valeur                                                                                                       | Description                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**paramètre d’erreur \_ non valide \_**</dt> </dl>    | L’un des paramètres n’est pas valide.<br/>                            |
| <dl> <dt>**ERREUR \_ aucun \_ itinéraire**</dt> </dl>            | Aucun itinéraire ne correspond aux critères spécifiés.<br/>       |
| <dl> <dt>**ERREUR \_ aucune \_ \_ ressource système**</dt> </dl> | Les ressources sont insuffisantes pour effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Notes

Les itinéraires sont retournés dans l’ordre suivant :

1.  Numéro de réseau
2.  Protocole de routage
3.  Identificateur d’interface
4.  Adresse du tronçon suivant

Cette fonction est moins efficace que les fonctions de handle d’énumération correspondantes.

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

[**RtmCloseEnumerationHandle**](rtmcloseenumerationhandle.md)
</dt> <dt>

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> <dt>

[**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md)
</dt> <dt>

[**RtmGetFirstRoute**](rtmgetfirstroute.md)
</dt> </dl>

 

 





