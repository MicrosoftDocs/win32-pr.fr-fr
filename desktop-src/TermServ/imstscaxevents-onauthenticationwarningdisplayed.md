---
title: Méthode IMsTscAxEvents OnAuthenticationWarningDisplayed
description: appelé avant qu’un contrôle ActiveX affiche une boîte de dialogue d’authentification (par exemple, la boîte de dialogue erreur de certificat).
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
ms.openlocfilehash: df2de56a612c748db720e485d9f1e6e5750c9fc3281500dfddd751f41aed1641
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118854007"
---
# <a name="imstscaxeventsonauthenticationwarningdisplayed-method"></a>IMsTscAxEvents :: OnAuthenticationWarningDisplayed, méthode

appelé avant qu’un contrôle ActiveX affiche une boîte de dialogue d’authentification (par exemple, la boîte de dialogue erreur de certificat).

## <a name="syntax"></a>Syntaxe


```C++
void OnAuthenticationWarningDisplayed();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Si nécessaire, la propriété [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) de l’interface [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) peut être utilisée pour s’assurer que la boîte de dialogue d’authentification modale à afficher est apparentée par une fenêtre spécifiée (cela peut être nécessaire pour empêcher les utilisateurs d’utiliser d’autres boîtes de dialogue pendant que la boîte de dialogue d’authentification est affichée). par défaut, le parent est la fenêtre de contrôle ActiveX.

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows serveur 2008, Windows server 2008 avec SP1<br/>                           |
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

 

 





