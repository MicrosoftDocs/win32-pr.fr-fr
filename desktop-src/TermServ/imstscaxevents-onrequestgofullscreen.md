---
title: Méthode IMsTscAxEvents OnRequestGoFullScreen
description: Appelée lorsque le client demande à basculer en mode plein écran et que la méthode IMsTscAdvancedSettings put \_ ContainerHandledFullScreen est appelée pour définir la propriété ContainerHandledFullScreen sur une valeur différente de zéro.
ms.assetid: f61520dc-a72a-4205-8761-92aaf08b5f90
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnRequestGoFullScreen
- Méthode OnRequestGoFullScreen Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnRequestGoFullScreen
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestGoFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6d689469f635694357890c620866fff5783680f8e9e8d11a1a05c78f6e1e322
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770679"
---
# <a name="imstscaxeventsonrequestgofullscreen-method"></a>IMsTscAxEvents :: OnRequestGoFullScreen, méthode

Appelée lorsque le client demande à basculer en mode plein écran et que la méthode [**IMsTscAdvancedSettings ::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) est appelée pour définir la propriété **ContainerHandledFullScreen** sur une valeur différente de zéro.

## <a name="syntax"></a>Syntaxe


```C++
void OnRequestGoFullScreen();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

En mode plein écran géré par un conteneur, le conteneur doit passer en mode plein écran standard en réponse à cet événement.

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

 

 





