---
title: Méthode IMsTscAxEvents OnAuthenticationWarningDisplayed
description: Appelé avant qu’un contrôle ActiveX affiche une boîte de dialogue d’authentification (par exemple, la boîte de dialogue erreur de certificat).
ms.assetid: ce307e5f-5e26-4041-bbd5-6871c0678da4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnAuthenticationWarningDisplayed
- Méthode OnAuthenticationWarningDisplayed Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnAuthenticationWarningDisplayed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33307adf103536cce5841effe2843a7c48fda357
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103528"
---
# <a name="imstscaxeventsonauthenticationwarningdisplayed-method"></a>IMsTscAxEvents :: OnAuthenticationWarningDisplayed, méthode

Appelé avant qu’un contrôle ActiveX affiche une boîte de dialogue d’authentification (par exemple, la boîte de dialogue erreur de certificat).

## <a name="syntax"></a>Syntaxe


```C++
void OnAuthenticationWarningDisplayed();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si nécessaire, la propriété [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) de l’interface [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) peut être utilisée pour s’assurer que la boîte de dialogue d’authentification modale à afficher est apparentée par une fenêtre spécifiée (cela peut être nécessaire pour empêcher les utilisateurs d’utiliser d’autres boîtes de dialogue pendant que la boîte de dialogue d’authentification est affichée). Par défaut, le parent est la fenêtre contrôle ActiveX.

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

[**OnAuthenticationWarningDismissed**](imstscaxevents-onauthenticationwarningdismissed.md)
</dt> <dt>

[**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





