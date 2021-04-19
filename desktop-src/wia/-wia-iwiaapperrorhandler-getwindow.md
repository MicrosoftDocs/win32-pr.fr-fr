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
ms.openlocfilehash: 89a3b2bf87d99c767ab3bea46a27c8a53fab7825
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517093"
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

Type : **HWND \** _

HWND utilisé par le gestionnaire d’erreurs d’application, le gestionnaire d’erreurs de pilote et le gestionnaire d’erreurs par défaut pour les boîtes de dialogue de message de l’appareil (à la fois erreur et information). La valeur de sortie peut être _ * NULL * *.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

*phwnd* pointe vers la fenêtre transmise dans [**ReportStatus**](-wia-iwiaerrorhandler-reportstatus.md) par le proxy 2,0 d’acquisition d’images Windows (WIA). Cette fenêtre doit rester valide pendant toute la durée du transfert de données.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 




