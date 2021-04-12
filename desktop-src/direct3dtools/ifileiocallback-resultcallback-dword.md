---
description: Fonction de rappel utilisée pour informer l’hôte des erreurs lors de la capture ou de la lecture.
MS-HAID: vspixengine.IFileIOCallback\_ResultCallback\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IFileIOCallback :: ResultCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E4418A63-47C6-4F12-94FA-0F1B5465FE84
api_name:
- IFileIOCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 751c4d0b57165e148002218ae2151aaba69e48f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109247"
---
# <a name="span-idvspixengineifileiocallback_resultcallback_dwordspanifileiocallbackresultcallback-method"></a><span id="vspixengine.ifileiocallback_resultcallback_dword"></span>IFileIOCallback :: ResultCallback, méthode

Fonction de rappel utilisée pour informer l’hôte des erreurs lors de la capture ou de la lecture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ResultCallback(
   DWORD resultState
);
```

## <a name="parameters"></a>Paramètres

*resultState*   
Indique le type d’erreur rencontrée.

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IFileIOCallback**](/windows/desktop/direct3dtools/ifileiocallback)

 

 
