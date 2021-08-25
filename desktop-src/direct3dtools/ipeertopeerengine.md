---
description: Interface pour la communication à distance des données relatives à un vsglog.
MS-HAID: vspixengine.IPeerToPeerEngine
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPeerToPeerEngine
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C6C4783F-ED46-47C2-98BB-C618897F8FF8
api_name:
- IPeerToPeerEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 85c5ba2866412ff6e6378bbead625a14bf7f5435
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786935"
---
# <a name="span-idvspixengineipeertopeerenginespanipeertopeerengine-interface"></a><span id="vspixengine.ipeertopeerengine"></span>Interface IPeerToPeerEngine

Interface pour la communication à distance des données relatives à un vsglog.

## <a name="members"></a>Membres

L’interface **IPeerToPeerEngine** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPeerToPeerEngine** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Méthodes

L’interface **IPeerToPeerEngine** possède ces méthodes.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Méthode</th><th >Description</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipeertopeerengine-cancelsetplaybackendpoint"><strong>CancelSetPlaybackEndpoint</strong></a></td><td ><p>Annule une demande précédente pour configurer une connexion à distance.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipeertopeerengine-getplaybackendpoint-bool-bstr-ptr-bstr-ptr-remotingversion-ptr"><strong>GetPlaybackEndpoint</strong></a></td><td ><p>Obtient l’adresse de point de terminaison d’un moteur distant.</p></td></tr><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipeertopeerengine-setplaybackendpoint-bool-bstr-bstr-remotingversion"><strong>SetPlaybackEndpoint</strong></a></td><td ><p>Définit l’adresse de point de terminaison utilisée pour se connecter à un moteur distant.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
