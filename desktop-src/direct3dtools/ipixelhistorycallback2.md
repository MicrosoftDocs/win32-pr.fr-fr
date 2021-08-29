---
description: Rappel pour retourner les intersections de l’historique des pixels (dessiner le niveau d’appel) et les primitives (niveau de triangle) dans deux résultats différents.
MS-HAID: vspixengine.IPixelHistoryCallback2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPixelHistoryCallback2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0111482E-B66A-4763-8890-85B1711F38B2
api_name:
- IPixelHistoryCallback2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dab9359d117043ee0902df8869a3cf9bb8f30b27
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/24/2021
ms.locfileid: "122787175"
---
# <a name="span-idvspixengineipixelhistorycallback2spanipixelhistorycallback2-interface"></a><span id="vspixengine.ipixelhistorycallback2"></span>Interface IPixelHistoryCallback2

Rappel pour retourner les intersections de l’historique des pixels (dessiner le niveau d’appel) et les primitives (niveau de triangle) dans deux résultats différents.

## <a name="members"></a>Membres

L’interface **IPixelHistoryCallback2** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPixelHistoryCallback2** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Méthodes

L’interface **IPixelHistoryCallback2** possède ces méthodes.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Méthode</th><th >Description</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-intersectionscallback-dword-pixelhistoryintersection-arr"><strong>IntersectionsCallback</strong></a></td><td ><p>Rappel qui avertit l’hôte des informations d’intersection de l’historique des pixels retournées par la requête dans.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-primitivescallback-dword-pixelhistoryoperation-arr"><strong>PrimitivesCallback</strong></a></td><td ><p>Rappel qui avertit l’hôte des informations d’opération primitives de l’historique des pixels retournées par la requête associée.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
