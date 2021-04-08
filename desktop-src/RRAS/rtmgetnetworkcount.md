---
title: Fonction RtmGetNetworkCount (RTM. h)
description: La fonction RtmGetNetworkCount récupère le nombre de réseaux sur lesquels le gestionnaire de tables de routage a des itinéraires.
ms.assetid: d0c04b8d-a6c4-44bf-a3f2-de822d635131
keywords:
- RtmGetNetworkCount fonction RAS
topic_type:
- apiref
api_name:
- RtmGetNetworkCount
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eab4babd1e9d98071b2fbe6ab30c9b92d4a23f0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741412"
---
# <a name="rtmgetnetworkcount-function"></a>RtmGetNetworkCount fonction)

\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003. Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]

La fonction **RtmGetNetworkCount** récupère le nombre de réseaux sur lesquels le gestionnaire de tables de routage a des itinéraires.

## <a name="syntax"></a>Syntaxe


```C++
ULONG RtmGetNetworkCount(
  _In_ DWORD ProtocolFamily
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ProtocolFamily* \[ dans\]
</dt> <dd>

Spécifie le type de réseau pour obtenir des informations sur l’itinéraire, par exemple, IP ou IPX.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction s’exécute correctement, la valeur de retour est le nombre de réseaux, le nombre de réseaux connus des protocoles de routage de la famille de protocoles spécifiée.

Si la valeur de retour est égale à zéro, aucun itinéraire n’est disponible ou l’opération a échoué. Appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir plus d’informations.



| Valeur                                                                                                    | Description                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**AUCUNE \_ erreur**</dt> </dl>                 | L’opération a réussi, mais aucun itinéraire n’est disponible.<br/>                                             |
| <dl> <dt>**paramètre d’erreur \_ non valide \_**</dt> </dl> | La valeur du paramètre *ProtocolFamily* ne correspond à aucune famille de protocoles installée.<br/> |



 

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

[Identificateurs de famille de protocole RTMv1](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

