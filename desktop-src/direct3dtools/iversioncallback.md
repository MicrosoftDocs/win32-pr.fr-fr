---
description: Rappel pour retourner les versions de toutes les interfaces prises en charge. Cela permet au consommateur d’être désynchronisé avec le moteur de capture.
MS-HAID: vspixengine.IVersionCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IVersionCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 7135E175-C537-4B0C-8F0A-CB77E3F2D945
api_name:
- IVersionCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c3ff23d325ff7b9d2783c9e35ca523253cea2880453c46f94a7d915cb47e8f8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119413"
---
# <a name="span-idvspixengineiversioncallbackspaniversioncallback-interface"></a><span id="vspixengine.iversioncallback"></span>Interface IVersionCallback

Rappel pour retourner les versions de toutes les interfaces prises en charge. Cela permet au consommateur d’être désynchronisé avec le moteur de capture.

## <a name="members"></a>Membres

L’interface **IVersionCallback** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IVersionCallback** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Méthodes

L’interface **IVersionCallback** possède ces méthodes.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Méthode</th><th style="text-align: left;">Description</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/iversioncallback-versiontableready-guid-arr-uint"><strong>VersionTableReady</strong></a></td><td style="text-align: left;"><p>Fonction de rappel utilisée pour informer l’hôte des interfaces prises en charge.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
