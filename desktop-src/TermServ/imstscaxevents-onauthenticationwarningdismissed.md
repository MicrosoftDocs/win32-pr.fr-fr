---
title: Méthode IMsTscAxEvents OnAuthenticationWarningDismissed
description: Appelé après qu’un contrôle ActiveX affiche une boîte de dialogue d’authentification (par exemple, la boîte de dialogue erreur de certificat).
ms.assetid: bf5dbe4a-9129-47b3-9808-ed09d9010099
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnAuthenticationWarningDismissed
- Méthode OnAuthenticationWarningDismissed Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnAuthenticationWarningDismissed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDismissed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86bdadfdbc8e0a1387a1f3aaf712188689d0f808
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384580"
---
# <a name="imstscaxeventsonauthenticationwarningdismissed-method"></a>IMsTscAxEvents :: OnAuthenticationWarningDismissed, méthode

Appelé après qu’un contrôle ActiveX affiche une boîte de dialogue d’authentification (par exemple, la boîte de dialogue erreur de certificat).

## <a name="syntax"></a>Syntaxe


```C++
void OnAuthenticationWarningDismissed();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si nécessaire, la propriété [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) de l’interface [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) peut être utilisée pour rétablir tout parent éventuellement effectué dans la méthode [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) .

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008, Windows Server 2008 avec SP1<br/>                           |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md)
</dt> <dt>

[**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





