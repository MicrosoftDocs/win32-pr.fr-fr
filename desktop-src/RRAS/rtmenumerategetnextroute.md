---
title: Fonction RtmEnumerateGetNextRoute (RTM. h)
description: La fonction RtmEnumerateGetNextRoute retourne l’entrée Next-route dans l’énumération démarrée par un appel à RtmCreateEnumerationHandle.
ms.assetid: fff6fb58-8a37-49f0-abc5-354b5bc340f8
keywords:
- RtmEnumerateGetNextRoute fonction RAS
topic_type:
- apiref
api_name:
- RtmEnumerateGetNextRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6105340003c6240b49acec4699fa7b229d11963116367ab0fa0c069211b6fd1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035869"
---
# <a name="rtmenumerategetnextroute-function"></a>RtmEnumerateGetNextRoute fonction)

\[cette api a été remplacée par l’api du [gestionnaire de Table de routage Version 2](about-routing-table-manager-version-2.md) et ne sera pas disponible au-delà de Windows Server 2003. Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]

La fonction **RtmEnumerateGetNextRoute** retourne l’entrée Next-route dans l’énumération démarrée par un appel à [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).

## <a name="syntax"></a>Syntaxe


```C++
DWORD RtmEnumerateGetNextRoute(
  _In_  HANDLE EnumerationHandle,
  _Out_ PVOID  Route
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*EnumerationHandle* \[ dans\]
</dt> <dd>

Handle qui identifie l’énumération et spécifie sa portée. Obtenez ce handle en appelant [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).

</dd> <dt>

*Itinéraire* \[ à\]
</dt> <dd>

Pointeur vers une structure de route spécifique à la famille de protocoles ( [**\_ \_ itinéraire IP RTM**](rtm-ip-route.md) ou [**\_ \_ itinéraire IPX RTM**](rtm-ipx-route.md)). Cette structure recevra l’itinéraire suivant dans l’énumération.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour n’est pas une \_ erreur.

Si la fonction échoue, la valeur de retour est l’un des codes d’erreur suivants.



| Valeur                                                                                                       | Description                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**HANDLE d’erreur \_ non valide \_**</dt> </dl>       | Le paramètre *EnumerationHandle* n’est pas valide.<br/>              |
| <dl> <dt>**ERREUR \_ \_ plus aucun \_ itinéraire**</dt> </dl>      | Il n’y a plus d’itinéraires dans l’énumération.<br/>                 |
| <dl> <dt>**ERREUR \_ aucune \_ \_ ressource système**</dt> </dl> | Les ressources sont insuffisantes pour effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Remarques

Bien que les itinéraires ne soient pas retournés dans un ordre particulier, chaque itinéraire de l’énumération n’est retourné qu’une seule fois.

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

[**\_itinéraire IP \_ RTM**](rtm-ip-route.md)
</dt> <dt>

[**\_itinéraire IPX \_ RTM**](rtm-ipx-route.md)
</dt> <dt>

[**RtmCloseEnumerationHandle**](rtmcloseenumerationhandle.md)
</dt> <dt>

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> </dl>

 

 





