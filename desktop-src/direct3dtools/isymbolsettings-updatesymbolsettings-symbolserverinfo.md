---
description: Demande d’envoi de chemins d’accès aux symboles de débogage au moteur local (non distant).
MS-HAID: vspixengine.ISymbolSettings\_UpdateSymbolSettings\_SymbolServerInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ISymbolSettings :: UpdateSymbolSettings, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E48E509F-8C33-49D6-B799-B16F70C1AA64
api_name:
- ISymbolSettings.UpdateSymbolSettings
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2bcf8cf82eb50b7731a84b00a20716e1545742ff
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629974"
---
# <a name="span-idvspixengineisymbolsettings_updatesymbolsettings_symbolserverinfospanisymbolsettingsupdatesymbolsettings-method"></a><span id="vspixengine.isymbolsettings_updatesymbolsettings_symbolserverinfo"></span>ISymbolSettings :: UpdateSymbolSettings, méthode

Demande d’envoi de chemins d’accès aux symboles de débogage au moteur local (non distant).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UpdateSymbolSettings(
   SymbolServerInfo symbolServerInfo
);
```

## <a name="parameters"></a>Paramètres

*symbolServerInfo*   
Déboguer les informations de chemin d’accès du serveur de symboles.

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**ISymbolSettings**](/windows/desktop/direct3dtools/isymbolsettings)

 

 
