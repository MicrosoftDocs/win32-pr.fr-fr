---
description: Obtient un handle vers la boîte de dialogue qui affiche les messages d’erreur et fournit un ou plusieurs boutons pour continuer, annuler ou abandonner l’application.
ms.assetid: 54deac2e-a395-45dc-b9f9-ecf8140fd9d7
title: 'IWiaAppErrorHandler :: GetWindow, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler.GetWindow
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 1bac7ba2f2f9d394218d851f9bbe7939168c2abbc7df5fb8c57a52f29fa6e2b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965758"
---
# <a name="iwiaapperrorhandlergetwindow-method"></a>IWiaAppErrorHandler :: GetWindow, méthode

Obtient un handle vers la boîte de dialogue qui affiche les messages d’erreur et fournit un ou plusieurs boutons pour continuer, annuler ou abandonner l’application.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetWindow(
  [out] HWND *phwnd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*phwnd* \[ à\]
</dt> <dd>

Type : **HWND\***

HWND utilisé par le gestionnaire d’erreurs d’application, le gestionnaire d’erreurs de pilote et le gestionnaire d’erreurs par défaut pour les boîtes de dialogue de message de l’appareil (à la fois erreur et information). La valeur de sortie peut être **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

*phwnd* pointe vers la fenêtre transmise dans [**ReportStatus**](-wia-iwiaerrorhandler-reportstatus.md) par le Proxy de l’Acquisition d’images Windows (WIA) 2,0. Cette fenêtre doit rester valide pendant toute la durée du transfert de données.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 




