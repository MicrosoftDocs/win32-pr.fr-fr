---
title: Méthode IMsTscAxEvents OnConnecting
description: Appelé lorsque le contrôle client commence à se connecter à un serveur en réponse à un appel à IMsTscAx Connect.
ms.assetid: c5e367a8-126a-48bb-bc94-1063f77e8239
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnConnecting
- Méthode OnConnecting Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnConnecting
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2004fde83b79aff7b7c5082562de94f943eacb25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383875"
---
# <a name="imstscaxeventsonconnecting-method"></a>IMsTscAxEvents :: OnConnecting, méthode

Appelé lorsque le contrôle client commence à se connecter à un serveur en réponse à un appel à [**IMsTscAx :: Connect**](imstscax-connect.md).

## <a name="syntax"></a>Syntaxe


```C++
void OnConnecting();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Implémentez cette méthode dans votre récepteur d’événements pour recevoir une notification indiquant que le contrôle a commencé à se connecter.

## <a name="examples"></a>Exemples

L’exemple suivant montre comment gérer cet événement avec Visual Basic Code de script. Dans cet exemple, l’hypothèse est que votre objet de contrôle est nommé « MsRdpClient ».

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).


```VB
Sub MsRdpClient.OnConnecting()
    Msgbox("Connecting")
End sub
```



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

 

 





