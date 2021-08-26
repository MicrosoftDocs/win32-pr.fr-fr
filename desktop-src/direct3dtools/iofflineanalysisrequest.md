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
ms.openlocfilehash: de8a4b73c2808347ec7cb15d9e2b3f9c213bc1d0
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786555"
---
# <a name="span-idvspixengineiofflineanalysisrequestspaniofflineanalysisrequest-interface"></a><span id="vspixengine.iofflineanalysisrequest"></span>Interface IOfflineAnalysisRequest

Demande de données d’analyse hors connexion.

## <a name="members"></a>Membres

L’interface **IOfflineAnalysisRequest** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IOfflineAnalysisRequest** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Méthodes

L’interface **IOfflineAnalysisRequest** possède ces méthodes.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Méthode</th><th >Description</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/iofflineanalysisrequest-cancelofflineanalysisasync-dword"><strong>CancelOfflineAnalysisAsync</strong></a></td><td ><p>Demandes d’annulation de l’analyse hors connexion dans une demande d’analyse hors connexion.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/iofflineanalysisrequest-requestofflineanalysisasync-enumofflineanalysissource-bstr-bstr-dword-bstr-dword-bstr-iofflineanalysiscallback-ptr"><strong>RequestOfflineAnalysisAsync</strong></a></td><td ><p>Demandes d’exécution de l’analyse hors connexion avec la source, le manifeste, les paramètres et le frame spécifiés.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
