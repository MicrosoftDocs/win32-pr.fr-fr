---
title: Fonction RtmGetRouteAge (RTM. h)
description: La fonction RtmGetRouteAge retourne l’âge d’un itinéraire. L’âge est le temps, en secondes, depuis sa création ou sa dernière mise à jour.
ms.assetid: 93052412-227f-4c9e-978b-3ec4bde4a256
keywords:
- RtmGetRouteAge fonction RAS
topic_type:
- apiref
api_name:
- RtmGetRouteAge
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ee536eeb4d16cbfc2bbcfb7dc09cae8b0003bbd925945fa710e15cb1c4a96e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035659"
---
# <a name="rtmgetrouteage-function"></a>RtmGetRouteAge fonction)

\[cette api a été remplacée par l’api du [gestionnaire de Table de routage Version 2](about-routing-table-manager-version-2.md) et ne sera pas disponible au-delà de Windows Server 2003. Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]

La fonction **RtmGetRouteAge** retourne l’âge d’un itinéraire. L’âge est le temps, en secondes, depuis sa création ou sa dernière mise à jour.

## <a name="syntax"></a>Syntaxe


```C++
ULONG RtmGetRouteAge(
  _In_ PVOID Route
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Itinéraire* \[ dans\]
</dt> <dd>

Pointeur vers une structure spécifique à la famille de protocoles qui spécifie les données de routage récemment obtenues à partir du gestionnaire de tables de routage.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est l’une des valeurs suivantes.



| Valeur                                                                                   | Description                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Routage**</dt> </dl> | Durée en secondes depuis la création ou la dernière mise à jour d’un itinéraire.<br/>                                                                                    |
| <dl> <dt>**LIMITES**</dt> </dl> | Le contenu de la structure de routage n’est pas valide. Dans ce cas, un appel à [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne un \_ paramètre d’erreur non valide \_ .<br/> |



 

## <a name="remarks"></a>Remarques

L’âge de l’itinéraire est calculé à partir du \_ membre d’horodatage de RR de la structure vers laquelle pointe le paramètre d' *itinéraire* . Le gestionnaire de tables de routage définit la valeur de ce membre lorsqu’un itinéraire est ajouté ou mis à jour.

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

[Référence de la version 1 du gestionnaire de tables de routage \_](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Fonctions de la version 1 du gestionnaire de table de routage](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**\_itinéraire IP \_ RTM**](rtm-ip-route.md)
</dt> <dt>

[**\_itinéraire IPX \_ RTM**](rtm-ipx-route.md)
</dt> </dl>

 

