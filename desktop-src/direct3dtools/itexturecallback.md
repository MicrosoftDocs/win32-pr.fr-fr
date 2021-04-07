---
description: Rappel pour écrire une texture sous la forme d’un fichier DDS.
MS-HAID: vspixengine.ITextureCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface ITextureCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2558C90A-7235-4A36-859C-0E74BD0B712A
api_name:
- ITextureCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 831de15656960cdc72ef2db50c1f3d13b8491e38
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747372"
---
# <a name="span-idvspixengineitexturecallbackspanitexturecallback-interface"></a><span id="vspixengine.itexturecallback"></span>Interface ITextureCallback

Rappel pour écrire une texture sous la forme d’un fichier DDS.

## <a name="members"></a>Membres

L’interface **ITextureCallback** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITextureCallback** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Méthodes

L’interface **ITextureCallback** possède ces méthodes.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Méthode</th><th style="text-align: left;">Description</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/itexturecallback-resultcallback"><strong>ResultCallback</strong></a></td><td style="text-align: left;"><p>Rappel qui avertit l’hôte que le. Le fichier DDS (surface DirectDraw) contenant les résultats de la demande associée est prêt.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
