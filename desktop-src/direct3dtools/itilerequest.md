---
description: Demande d’écriture d’une texture en mosaïques sous la forme d’un fichier DDS.
MS-HAID: vspixengine.ITileRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface ITileRequest
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DBA493E7-EBB6-490D-BDC6-946265A474D6
api_name:
- ITileRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b0a5f31e68f53f316ea77f77f2ff778eb817e11c
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786165"
---
# <a name="span-idvspixengineitilerequestspanitilerequest-interface"></a><span id="vspixengine.itilerequest"></span>Interface ITileRequest

Demande d’écriture d’une texture en mosaïques sous la forme d’un fichier DDS.

## <a name="members"></a>Membres

L’interface **ITileRequest** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITileRequest** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Méthodes

L’interface **ITileRequest** possède ces méthodes.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Méthode</th><th >Description</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/itilerequest-requestbuffertileasync-eventid-dword-bstr-uint-ibufferobjectdatacallback-ptr-dword-dword"><strong>RequestBufferTileAsync</strong></a></td><td ><p>Demandes pour obtenir le contenu brut d’une vignette.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/itilerequest-requesttexturetileasync-eventid-dword-uint-uint-uint-uint-bstr-itexturecallback-ptr-dword-dword"><strong>RequestTextureTileAsync</strong></a></td><td ><p>Demande à obtenir le contenu d’une texture en mosaïque sous la forme d’un. Fichier DDS (surface DirectDraw).</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
