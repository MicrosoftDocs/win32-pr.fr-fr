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
ms.openlocfilehash: 09fba28486bd6f1c43e4b0c4fb0dfcf495e0722b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106517165"
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

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne **S_OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IStatusCallback**](/windows/desktop/direct3dtools/istatuscallback)

 

 
