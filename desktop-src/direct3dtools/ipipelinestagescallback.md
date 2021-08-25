---
description: <span id="vspixengine.ipipelinestagescallback"></span>Interface IPipeLineStagesCallback-non utilisée. Anciennement un rappel pour les données d’étapes de pipeline.
MS-HAID: vspixengine.IPipeLineStagesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPipeLineStagesCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2F5B84DB-3D06-4D82-BF1D-E5853CC4B835
api_name:
- IPipeLineStagesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7c37fa4d282c8c17237a5e0149debb481c6325c9
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622755"
---
# <a name="span-idvspixengineipipelinestagescallbackspanipipelinestagescallback-interface"></a><span id="vspixengine.ipipelinestagescallback"></span>Interface IPipeLineStagesCallback

Non utilisé. Anciennement un rappel pour les données d’étapes de pipeline.

## <a name="members"></a>Membres

L’interface **IPipeLineStagesCallback** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPipeLineStagesCallback** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Méthodes

L’interface **IPipeLineStagesCallback** possède ces méthodes.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th style="text-align: left;">Méthode</th><th style="text-align: left;">Description</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-getsupportedstages-dword-pipelinestage-arr-uint-uint"><strong>GetSupportedStages</strong></a></td><td style="text-align: left;"><p>Rappel qui avertit l’hôte des étapes de pipeline utilisées par l’appel de dessin de la demande dans.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatanotavailablecallback-uint-pipelinestageerror-arr-uint-uint-eventid"><strong>MeshDataNotAvailableCallback</strong></a></td><td style="text-align: left;"><p>Rappel qui avertit l’hôte des étapes de pipeline qui ne sont pas en mesure de retourner des données de maillage pour l’événement spécifié dans la demande associée.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatavertcallback-uint-uint-meshdatabufferlayoutentry-arr-uint-uint-byte-arr-uint-byte-arr-uint-uint-uint-uint-bool-uint-uint"><strong>MeshDataVertCallback</strong></a></td><td style="text-align: left;"><p>Rappel qui avertit l’hôte des informations de maillage des étapes de pipeline retournées par la requête dans.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-resultcallback-pipelinestagesid-eventid-dword-dword-dword-dword-byte-arr"><strong>ResultCallback</strong></a></td><td style="text-align: left;"><p>Rappel qui avertit l’hôte des informations d’image des étapes de pipeline retournées par la requête dans.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
