---
description: Interface d’origine pour la communication des données relatives à un vsglog.
MS-HAID: vspixengine.IPixEngine
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPixEngine
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 87AB1D07-8E90-49F0-B44D-F6185923B8D4
api_name:
- IPixEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e370cb3f9f586cc1814c6fcd6f2adc2545bd197c
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786515"
---
# <a name="span-idvspixengineipixenginespanipixengine-interface"></a><span id="vspixengine.ipixengine"></span>Interface IPixEngine

Interface d’origine pour la communication des données relatives à un vsglog.

## <a name="members"></a>Membres

L’interface **IPixEngine** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPixEngine** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Méthodes

L’interface **IPixEngine** possède ces méthodes.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Méthode</th><th >Description</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipixengine-openfile-bstr-bstr-inewframescallback-ptr-ifileiocallback-ptr-lcid"><strong>OpenFile</strong></a></td><td ><p>Ouvre un journal de graphisme.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipixengine-runexperiment-experiment-irunexperimentcallback-ptr-inewframescallback-ptr-ifileiocallback-ptr-dword-experimenttrigger-arr"><strong>RunExperiment</strong></a></td><td ><p>Exécute une expérience.</p></td></tr><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipixengine-savefile-bstr-ifileiocallback-ptr"><strong>SaveFile</strong></a></td><td ><p>Enregistre le journal de graphisme à l’emplacement spécifié.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipixengine-setparentprocess-dword"><strong>SetParentProcess</strong></a></td><td ><p>Non utilisé.</p></td></tr><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipixengine-shutdown"><strong>Correct</strong></a></td><td ><p>Arrête le moteur.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
