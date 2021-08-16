---
title: Fonction RtmBlockDeleteRoutes (RTM. h)
description: La fonction RtmBlockDeleteRoutes supprime tous les itinéraires dans le sous-ensemble spécifié d’itinéraires dans la table.
ms.assetid: d191883d-da3d-4a91-92e6-4979db96f4a4
keywords:
- RtmBlockDeleteRoutes fonction RAS
topic_type:
- apiref
api_name:
- RtmBlockDeleteRoutes
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f830603bba4bcdf07bd7bc8c631ac17028301a795fc14ebbce6483ef72f81361
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073879"
---
# <a name="rtmblockdeleteroutes-function"></a>RtmBlockDeleteRoutes fonction)

\[cette api a été remplacée par l’api du [gestionnaire de Table de routage Version 2](about-routing-table-manager-version-2.md) et ne sera pas disponible au-delà de Windows Server 2003. Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]

La fonction **RtmBlockDeleteRoutes** supprime tous les itinéraires dans le sous-ensemble spécifié d’itinéraires dans la table.

## <a name="syntax"></a>Syntaxe


```C++
HANDLE RtmBlockDeleteRoutes(
  _In_ HANDLE ClientHandle,
  _In_ DWORD  EnumerationFlags,
  _In_ PVOID  CriteriaRoute
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ClientHandle* \[ dans\]
</dt> <dd>

Handle qui identifie le client et, par conséquent, le protocole de routage des itinéraires à supprimer.

</dd> <dt>

*EnumerationFlags* \[ dans\]
</dt> <dd>

Spécifie les itinéraires qui doivent être énumérés. Ce paramètre limite l’ensemble des itinéraires supprimés à un sous-ensemble défini par les indicateurs suivants et les valeurs des membres correspondants de la structure vers laquelle pointe le paramètre *CriteriaRoute* . Les indicateurs sont les mêmes que ceux utilisés dans [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md) , à ceci près que la version RTM \_ \_ \_ des meilleurs itinéraires est redondante pour **RtmBlockDeleteRoutes**. La meilleure désignation de route est ajustée en fonction de la suppression des itinéraires. par conséquent, la fonction supprime tous les itinéraires dans le sous-ensemble.

</dd> <dt>

*CriteriaRoute* \[ dans\]
</dt> <dd>

Pointeur vers une structure de route spécifique à la famille de protocoles ( [**\_ \_ itinéraire IP RTM**](rtm-ip-route.md) ou [**\_ \_ itinéraire IPX RTM**](rtm-ipx-route.md)). Les valeurs de membre de cette structure correspondent aux indicateurs spécifiés par le paramètre *EnumerationFlags* .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour n’est pas une \_ erreur.

Si la fonction échoue, la valeur de retour est l’un des codes d’erreur suivants.



| Valeur                                                                                                       | Description                                                                                                |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERREUR \_ aucun \_ itinéraire**</dt> </dl>            | Aucun itinéraire n’a les critères spécifiés.<br/>                                           |
| <dl> <dt>**HANDLE d’erreur \_ non valide \_**</dt> </dl>       | Le paramètre *ClientHandle* n’est pas valide.<br/>                                                      |
| <dl> <dt>**paramètre d’erreur \_ non valide \_**</dt> </dl>    | Un ou plusieurs des paramètres d’entrée ne sont pas valides, par exemple, les indicateurs d’énumération ne sont pas valides.<br/> |
| <dl> <dt>**ERREUR \_ aucune \_ \_ ressource système**</dt> </dl> | Les ressources sont insuffisantes pour effectuer l’opération.<br/>                                    |
| <dl> <dt>**ERREUR \_ de \_ mémoire insuffisante \_**</dt> </dl>   | La mémoire est insuffisante pour effectuer l’opération.<br/>                                        |



 

## <a name="remarks"></a>Remarques

La fonction génère des messages de notification appropriés à tous les clients inscrits, y compris l’appelant.

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

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> <dt>

[**RtmRegisterClient**](rtmregisterclient.md)
</dt> </dl>

 

 





