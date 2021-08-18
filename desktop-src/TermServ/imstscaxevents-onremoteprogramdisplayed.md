---
title: Méthode IMsTscAxEvents OnRemoteProgramDisplayed
description: Appelé lorsqu’un programme RemoteApp est affiché.
ms.assetid: 24f5ea52-0c13-4024-9448-5c2c1896ca8b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnRemoteProgramDisplayed
- Méthode OnRemoteProgramDisplayed Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnRemoteProgramDisplayed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteProgramDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df50f9a536b367b203f395d9c856562b8967d8a5830704a2e9bbb4c69152f202
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058817"
---
# <a name="imstscaxeventsonremoteprogramdisplayed-method"></a>IMsTscAxEvents :: OnRemoteProgramDisplayed, méthode

Appelé lorsqu’un programme RemoteApp est affiché.

## <a name="syntax"></a>Syntaxe


```C++
VOID OnRemoteProgramDisplayed(
  [in] VARIANT_BOOL vbDisplayed,
  [in] ULONG        uDisplayInformation
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*vbDisplayed* \[ dans\]
</dt> <dd>

Indique si le programme RemoteApp est affiché ou masqué.

</dd> <dt>

*uDisplayInformation* \[ dans\]
</dt> <dd>

Informations d’affichage.

<dt>

<span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>

<span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>**RAIL \_ APPDISPLAY \_ reconnexion automatique**


</dt> <dd>

La reconnexion automatique est en cours.

</dd> <dt>

<span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>

<span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>**RAIL \_ APPDISPLAY \_ DESKTOPHOOKED**


</dt> <dd>

Le nombre de RemoteApp est passé à zéro.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Implémentez cette méthode dans votre récepteur d’événements pour recevoir une notification indiquant qu’un RemoteApp a été affiché.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



 

 





