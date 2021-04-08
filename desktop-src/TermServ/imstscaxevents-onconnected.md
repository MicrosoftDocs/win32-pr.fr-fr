---
title: Méthode IMsTscAxEvents OnConnected
description: Appelé lorsque le contrôle client est en train d’établir une connexion avec un serveur d’hôte de session Bureau à distance (hôte de session Bureau à distance).
ms.assetid: 9c26d112-c070-4870-93d5-2fcc84a1331f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnConnected
- Méthode OnConnected Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnConnected
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d83a6a14f58a0704f0a3110532ad8cf8c0d7dc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741324"
---
# <a name="imstscaxeventsonconnected-method"></a>IMsTscAxEvents :: OnConnected, méthode

Appelé lorsque le contrôle client est en train d’établir une connexion avec un serveur d’hôte de session Bureau à distance (hôte de session Bureau à distance).

## <a name="syntax"></a>Syntaxe


```C++
void OnConnected();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Implémentez cette méthode dans votre récepteur d’événements pour recevoir une notification indiquant que le contrôle a établi une connexion avec un serveur hôte de session Bureau à distance.

Pour plus d’informations sur l’appel de cette méthode, reportez-vous à l’événement [**IMsTscAxEvents :: OnLoginComplete**](imstscaxevents-onlogincomplete.md) .

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





