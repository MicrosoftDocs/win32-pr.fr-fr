---
description: Demande de retour de la liste des événements dans un frame.
MS-HAID: vspixengine.IFrameEventsRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IFrameEventsRequest
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E171A94C-012F-4296-B1EC-2E814F977565
api_name:
- IFrameEventsRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 52f60bd5ad14e68a0ed1935ade404d99a378e9a0
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629073"
---
# <a name="span-idvspixengineiframeeventsrequestspaniframeeventsrequest-interface"></a><span id="vspixengine.iframeeventsrequest"></span>Interface IFrameEventsRequest

Demande de retour de la liste des événements dans un frame.

## <a name="members"></a>Membres

L’interface **IFrameEventsRequest** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IFrameEventsRequest** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Méthodes

L’interface **IFrameEventsRequest** possède ces méthodes.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th style="text-align: left;">Méthode</th><th style="text-align: left;">Description</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/iframeeventsrequest-requestasync-dword-dword-dword-arr-iframeeventscallback-ptr-dword-dword"><strong>RequestAsync</strong></a></td><td style="text-align: left;"><p>Demande asynchrone pour obtenir des informations spécifiées sur un frame spécifié unique.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/iframeeventsrequest-requestsupportedcolumnsasync-iframeeventscallback-ptr-dword"><strong>RequestSupportedColumnsAsync</strong></a></td><td style="text-align: left;"><p>Demande asynchrone pour obtenir des informations sur les colonnes (champs) prises en charge par ce type de demande d’événements de frame.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
