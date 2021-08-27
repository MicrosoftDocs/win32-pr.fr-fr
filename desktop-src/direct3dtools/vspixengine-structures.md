---
description: Les structures suivantes sont déclarées dans vspixengine. h.
MS-HAID: vspixengine.vspixengine\_structures
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Structures de l’interface de capture des diagnostics Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 97F142F6-FED1-4AF4-B9E3-BB1E30F3FAD2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 611a8112c1eb99c142c92f63f598e903352528f8
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622285"
---
# <a name="span-idvspixenginevspixengine_structuresspandirect3d-diagnostics-capture-interface-structures"></a><span id="vspixengine.vspixengine_structures"></span>Structures de l’interface de capture des diagnostics Direct3D

Les structures suivantes sont déclarées dans vspixengine. h.

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>Dans cette section

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th>Rubrique</th><th>Description</th></tr></thead><tbody><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/resourcepair"><strong>ResourcePair</strong></a></p></td><td><p>Représente une ressource partagée qui est encodée sous la forme d’une chaîne COM.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/descriptorheaprecord"><strong>DescriptorHeapRecord</strong></a></p></td><td><p>Représente les informations du tas du descripteur.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pipelinestageerror"><strong>PipeLineStageError</strong></a></p></td><td><p>Représente une erreur dans une étape de pipeline.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pipelinestage"><strong>PipeLineStage</strong></a></p></td><td><p>Représente une étape de pipeline, y compris les détails du nuanceur utilisé.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/experimenttrigger"><strong>ExperimentTrigger</strong></a></p></td><td><p>Représente des informations sur le déclencheur d’expérimentation.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/packedcallpkg"><strong>PackedCallPkg</strong></a></p></td><td><p>Représente un package de quatre appels.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/symbolserverinfo"><strong>SymbolServerInfo</strong></a></p></td><td><p>Représente des informations sur le serveur de symboles de débogage.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/callstackframe"><strong>CallStackFrame</strong></a></p></td><td><p>Représente des informations sur un frame sur la pile des appels.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/sourcefileinfo"><strong>SourceFileInfo</strong></a></p></td><td><p>Représente des informations sur un fichier de code source.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/summaryitem"><strong>SummaryItem</strong></a></p></td><td><p>Représente des informations de synthèse sur un événement.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/debugshader"><strong>DebugShader</strong></a></p></td><td><p>Représente des informations sur un nuanceur sous le débogueur.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/experiment"><strong>Expérience</strong></a></p></td><td><p>Représente des informations sur une expérience (capture).</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/issue"><strong>Problème</strong></a></p></td><td><p>Représente des informations sur un problème.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/point2d"><strong>Point2D</strong></a></p></td><td><p>Représente un point 2D avec des coordonnées entières non signées.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/threaddata3d"><strong>ThreadData3D</strong></a></p></td><td><p>Représente un index 3D dans des données de thread</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/inputlayoutstruct"><strong>InputLayoutStruct</strong></a></p></td><td><p>Représente les champs de disposition d’entrée d’une mémoire tampon de vertex, un par champ dans la mémoire tampon de vertex.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixelhistoryoperation"><strong>PixelHistoryOperation</strong></a></p></td><td><p>Représente des informations sur l’historique des pixels.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixelhistoryintersection"><strong>PixelHistoryIntersection</strong></a></p></td><td><p>Représente des informations sur un</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/meshdatabufferlayoutentry"><strong>MeshDataBufferLayoutEntry</strong></a></p></td><td><p>Représente des informations sur une seule entrée dans la disposition de la mémoire tampon d’un maillage.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/debugshaderrequestinfo"><strong>DebugShaderRequestInfo</strong></a></p></td><td><p>Représente des informations sur une demande de débogueur de nuanceur.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixengineint4"><strong>PixEngineInt4</strong></a></p></td><td><p>Représente un vecteur 4D avec des coordonnées entières signées.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginepoint4d"><strong>PixEnginePoint4D</strong></a></p></td><td><p>Représente un point 4D avec des coordonnées à virgule flottante 64 bits (double).</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixenginechanneldesc"><strong>PixEngineChannelDesc</strong></a></p></td><td><p>Représente une description d’un canal de couleur (exemple).</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginetextureformatdesc"><strong>PixEngineTextureFormatDesc</strong></a></p></td><td><p>Représente une description d’un format de texture.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixenginetexturedescriptor"><strong>PixEngineTextureDescriptor</strong></a></p></td><td><p>Représente une description d’une ressource de texture.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginetextureslicedescriptor"><strong>PixEngineTextureSliceDescriptor</strong></a></p></td><td><p>Représente une description d’une tranche de texture.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixenginetexturesliceindex"><strong>PixEngineTextureSliceIndex</strong></a></p></td><td><p>Représente l’index d’une tranche de texture</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginehistogram"><strong>PixEngineHistogram</strong></a></p></td><td><p>Représente un histogramme d’une texture.</p></td></tr></tbody></table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Rubriques connexes

[Informations de référence sur l’interface de capture des diagnostics Direct3D](vspixengine-reference.md)

 

 
