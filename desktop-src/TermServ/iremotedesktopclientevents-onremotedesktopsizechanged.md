---
title: Méthode IRemoteDesktopClientEvents OnRemoteDesktopSizeChanged
description: Appelé lorsque la taille du Bureau à distance a changé.
ms.assetid: DA641CA7-3214-4DB6-9A7F-75903FE93DB4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnRemoteDesktopSizeChanged
- Méthode OnRemoteDesktopSizeChanged Services Bureau à distance, interface IRemoteDesktopClientEvents
- Services Bureau à distance de l’interface IRemoteDesktopClientEvents, méthode OnRemoteDesktopSizeChanged
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnRemoteDesktopSizeChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da10c37bdebcf59fc6a19581dd5bd35f0b751349d447e05524e8c806e410b9a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124859"
---
# <a name="iremotedesktopclienteventsonremotedesktopsizechanged-method"></a>IRemoteDesktopClientEvents :: OnRemoteDesktopSizeChanged, méthode

Appelé lorsque la taille du Bureau à distance a changé.

## <a name="syntax"></a>Syntaxe


```C++
void OnRemoteDesktopSizeChanged(
  [in] long width,
  [in] long height
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*largeur* \[ dans\]
</dt> <dd></dd> <dt>

*hauteur* \[ dans\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                           |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                 |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents est défini comme 079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





