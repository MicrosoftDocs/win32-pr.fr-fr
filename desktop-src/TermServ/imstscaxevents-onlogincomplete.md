---
title: Méthode IMsTscAxEvents OnLoginComplete
description: Appelé lorsque le contrôle client s’est correctement connecté à un serveur d’hôte de session Bureau à distance (hôte de session Bureau à distance), en suivant l’affichage de la boîte de dialogue ouverture de session Windows.
ms.assetid: acb345a6-3153-4b8f-ac51-fe0c19fa750a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnLoginComplete
- Méthode OnLoginComplete Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnLoginComplete
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLoginComplete
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74d6b63f74ed99c8af939bafdc8a55a41e33b404
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508761"
---
# <a name="imstscaxeventsonlogincomplete-method"></a>IMsTscAxEvents :: OnLoginComplete, méthode

Appelé lorsque le contrôle client s’est correctement connecté à un serveur d’hôte de session Bureau à distance (hôte de session Bureau à distance), en suivant l’affichage de la boîte de dialogue ouverture de session Windows.

## <a name="syntax"></a>Syntaxe


```C++
void OnLoginComplete();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Implémentez cette méthode dans votre récepteur d’événements pour recevoir une notification indiquant que le contrôle a terminé l’ouverture de session.

## <a name="examples"></a>Exemples

L’exemple suivant montre comment gérer cet événement à l’aide de Visual Basic Code de script. Dans cet exemple, l’hypothèse est que votre objet de contrôle est nommé « MsRdpClient ».

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).


```VB
Sub MsRdpClient.OnLoginComplete()
    Msgbox("Login has completed")
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

 

 





