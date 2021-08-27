---
description: Demande d’intersections et de primitives de l’historique des pixels séparément.
MS-HAID: vspixengine.IPixelHistoryRequest2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPixelHistoryRequest2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B62A9EBA-4497-4825-A2F1-285A4AD45012
api_name:
- IPixelHistoryRequest2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e4fc6c450a2ac31dc364ed20f4eb466ca0ae4d99
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622545"
---
# <a name="span-idvspixengineipixelhistoryrequest2spanipixelhistoryrequest2-interface"></a><span id="vspixengine.ipixelhistoryrequest2"></span>Interface IPixelHistoryRequest2

Demande d’intersections et de primitives de l’historique des pixels séparément.

## <a name="members"></a>Membres

L’interface **IPixelHistoryRequest2** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPixelHistoryRequest2** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Méthodes

L’interface **IPixelHistoryRequest2** possède ces méthodes.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th style="text-align: left;">Méthode</th><th style="text-align: left;">Description</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixelhistoryrequest2-requestintersections-dword-point2d-dword-ipixelhistorycallback2-ptr-dword-dword"><strong>RequestIntersections</strong></a></td><td style="text-align: left;"><p>Demande une liste d’événements qui provoquent une modification dans le pixel spécifié, le rendu cible/UAV et le frame.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixelhistoryrequest2-requestprimitives-pixelhistoryintersection-ptr-ipixelhistorycallback2-ptr-dword-dword"><strong>RequestPrimitives</strong></a></td><td style="text-align: left;"><p>Demande une liste de primitives à partir d’une intersection particulière. Pour plus d’informations, consultez la fonction membre RequestIntersections.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
