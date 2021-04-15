---
title: Fonction RtmDeregisterClient (RTM. h)
description: La fonction RtmDeregisterClient annule l’inscription du client et libère les ressources associées au client.
ms.assetid: 5d04f276-86a7-4e63-8266-e93f0d6e5241
keywords:
- RtmDeregisterClient fonction RAS
topic_type:
- apiref
api_name:
- RtmDeregisterClient
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab1f56d3d65e13c083d8952f500cfba4638ab83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384636"
---
# <a name="rtmderegisterclient-function"></a>RtmDeregisterClient fonction)

\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003. Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]

La fonction **RtmDeregisterClient** annule l’inscription du client et libère les ressources associées au client.

## <a name="syntax"></a>Syntaxe


```C++
DWORD RtmDeregisterClient(
  _In_ HANDLE ClientHandle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ClientHandle* \[ dans\]
</dt> <dd>

Handle qui identifie le client dont l’inscription doit être annulée. Obtenez ce handle en appelant [**RtmRegisterClient**](rtmregisterclient.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour n’est pas une \_ erreur.

Si la fonction échoue, la valeur de retour est l’un des codes d’erreur suivants.



| Valeur                                                                                                       | Description                                                    |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**HANDLE d’erreur \_ non valide \_**</dt> </dl>       | Le paramètre *ClientHandle* n’est pas un handle valide.<br/> |
| <dl> <dt>**ERREUR \_ aucune \_ \_ ressource système**</dt> </dl> | Ressources insuffisantes pour effectuer l’opération.<br/>  |



 

## <a name="remarks"></a>Notes

Cette fonction supprime tous les itinéraires qui ont été ajoutés par le client.

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

[**RtmRegisterClient**](rtmregisterclient.md)
</dt> </dl>

 

 





