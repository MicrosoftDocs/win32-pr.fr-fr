---
description: Demande de données d’analyse hors connexion.
MS-HAID: vspixengine.IOfflineAnalysisRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IOfflineAnalysisRequest
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1E438545-D4C4-45A7-918E-D3D9DC06BA08
api_name:
- IOfflineAnalysisRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0a5171972c407848193239fb2b356e9451a57d2f
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627135"
---
# <a name="span-idvspixengineiofflineanalysisrequestspaniofflineanalysisrequest-interface"></a><span id="vspixengine.iofflineanalysisrequest"></span>Interface IOfflineAnalysisRequest

Demande de données d’analyse hors connexion.

## <a name="members"></a>Membres

L’interface **IOfflineAnalysisRequest** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IOfflineAnalysisRequest** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Méthodes

L’interface **IOfflineAnalysisRequest** possède ces méthodes.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th style="text-align: left;">Méthode</th><th style="text-align: left;">Description</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/iofflineanalysisrequest-cancelofflineanalysisasync-dword"><strong>CancelOfflineAnalysisAsync</strong></a></td><td style="text-align: left;"><p>Demandes d’annulation de l’analyse hors connexion dans une demande d’analyse hors connexion.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/iofflineanalysisrequest-requestofflineanalysisasync-enumofflineanalysissource-bstr-bstr-dword-bstr-dword-bstr-iofflineanalysiscallback-ptr"><strong>RequestOfflineAnalysisAsync</strong></a></td><td style="text-align: left;"><p>Demandes d’exécution de l’analyse hors connexion avec la source, le manifeste, les paramètres et le frame spécifiés.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
