---
title: Méthode IMsTscAxEvents OnRequestLeaveFullScreen
description: Appelée lorsque le client demande à conserver le mode plein écran et que la propriété IMsTscAdvancedSettings put \_ ContainerHandledFullScreen a été définie sur une valeur différente de zéro.
ms.assetid: db6ee012-8288-4360-98b2-12858ea65baa
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnRequestLeaveFullScreen
- Méthode OnRequestLeaveFullScreen Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnRequestLeaveFullScreen
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestLeaveFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e814d6153e32fdf4fa498a6630fc9ca2908510e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742093"
---
# <a name="imstscaxeventsonrequestleavefullscreen-method"></a>IMsTscAxEvents :: OnRequestLeaveFullScreen, méthode

Appelée lorsque le client demande à conserver le mode plein écran et que la propriété [**IMsTscAdvancedSettings ::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) a été définie sur une valeur différente de zéro.

## <a name="syntax"></a>Syntaxe


```C++
void OnRequestLeaveFullScreen();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

En mode plein écran géré par un conteneur, le conteneur doit conserver le mode plein écran standard en réponse à cet événement.

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

 

 





