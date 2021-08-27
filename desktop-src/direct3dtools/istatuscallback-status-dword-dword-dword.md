---
description: Fonction de rappel utilisée pour informer l’hôte de la progression des moteurs. Cela permet également à l’hôte de déterminer que le moteur est toujours en cours d’exécution.
title: 'IStatusCallback :: Status, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4DC2A05F-506C-4AB4-98E1-58827056700D
api_name:
- IStatusCallback.Status
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: edf48e62389224a01af7e52aa7e87f3db63b3740
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622305"
---
# <a name="span-idvspixengineistatuscallback_status_dword_dword_dwordspanistatuscallbackstatus-method"></a><span id="vspixengine.istatuscallback_status_dword_dword_dword"></span>IStatusCallback :: Status, méthode

Fonction de rappel utilisée pour informer l’hôte de la progression du moteur. Cela permet également à l’hôte de déterminer que le moteur est toujours en cours d’exécution.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Status(
   DWORD dwMillisecondsElapsed,
   DWORD dwFramesCaptured,
   DWORD dwFramesElapsed
);
```

## <a name="parameters"></a>Paramètres

*dwMillisecondsElapsed*   
Temps écoulé depuis le dernier appel de l’État, en millisecondes.

*dwFramesCaptured*   
Nombre de frames capturés depuis le dernier appel de l’État.

*dwFramesElapsed*   
Nombre de frames écoulés depuis le dernier appel à l’État.

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne **S_OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IStatusCallback**](/windows/desktop/direct3dtools/istatuscallback)

 

 
