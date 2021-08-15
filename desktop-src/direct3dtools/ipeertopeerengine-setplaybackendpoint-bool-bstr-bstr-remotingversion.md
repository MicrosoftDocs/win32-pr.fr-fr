---
description: Définit l’adresse de point de terminaison utilisée pour se connecter à un moteur distant.
MS-HAID: vspixengine.IPeerToPeerEngine\_SetPlaybackEndpoint\_BOOL\_BSTR\_BSTR\_RemotingVersion
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPeerToPeerEngine :: SetPlaybackEndpoint, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D261D2EA-C930-406E-A5E1-CE5E98162399
api_name:
- IPeerToPeerEngine.SetPlaybackEndpoint
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 81f3743c9f1cca5a763df23087d7703b79d198a9cd780f9a398017c53afaabfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721796"
---
# <a name="span-idvspixengineipeertopeerengine_setplaybackendpoint_bool_bstr_bstr_remotingversionspanipeertopeerenginesetplaybackendpoint-method"></a><span id="vspixengine.ipeertopeerengine_setplaybackendpoint_bool_bstr_bstr_remotingversion"></span>IPeerToPeerEngine :: SetPlaybackEndpoint, méthode

Définit l’adresse de point de terminaison utilisée pour se connecter à un moteur distant.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetPlaybackEndpoint(
   BOOL            bUseAuthentication,
   BSTR            endpoint,
   BSTR            sessionKey,
   RemotingVersion remoteVersion
);
```

## <a name="parameters"></a>Paramètres

*bUseAuthentication*   
true pour utiliser l’authentification ; Sinon, false.

*poste*   
Chaîne COM contenant l’adresse du point de terminaison.

*sessionKey*   
Chaîne COM contenant la clé de session utilisée pour le chiffrement.

*remoteVersion*   
Spécifie la version du moteur distant à utiliser.

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IPeerToPeerEngine**](/windows/desktop/direct3dtools/ipeertopeerengine)

 

 
