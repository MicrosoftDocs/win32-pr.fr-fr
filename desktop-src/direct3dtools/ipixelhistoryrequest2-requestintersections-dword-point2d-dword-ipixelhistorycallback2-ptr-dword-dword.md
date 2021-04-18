---
description: Demande une liste d’événements qui provoquent une modification dans le pixel spécifié, le rendu cible/UAV et le frame.
MS-HAID: vspixengine.IPixelHistoryRequest2\_RequestIntersections\_DWORD\_Point2D\_DWORD\_IPixelHistoryCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixelHistoryRequest2 :: RequestIntersections, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C8E47935-DFA1-4A76-9D0A-3DF5833A1249
api_name:
- IPixelHistoryRequest2.RequestIntersections
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 56f8da17ca492ca15ca51676ae4f1e1654c6f41f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521556"
---
# <a name="span-idvspixengineipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dwordspanipixelhistoryrequest2requestintersections-method"></a><span id="vspixengine.ipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dword"></span>IPixelHistoryRequest2 :: RequestIntersections, méthode

Demande une liste d’événements qui provoquent une modification dans le pixel spécifié, le rendu cible/UAV et le frame.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RequestIntersections(
   DWORD                    frameNumber,
   Point2D                  pixel,
   DWORD                    renderTargetPtr,
   IPixelHistoryCallback2 * requestCallback,
   DWORD                    requestCookie,
   DWORD                    progressIntervalMsecs
);
```

## <a name="parameters"></a>Paramètres

*frameNumber*   
Frame spécifié.

*pixellisé*   
Pixel spécifié.

*renderTargetPtr*   
Adresse de la cible de rendu spécifiée

*requestCallback*   
Adresse du rappel utilisée pour notifier l’hôte de résultats.

*requestCookie*   
Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.

*progressIntervalMsecs*   
Non utilisé.

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IPixelHistoryRequest2**](/windows/desktop/direct3dtools/ipixelhistoryrequest2)

 

 
