---
description: Demande de démarrer une session de débogage de nuanceur pour l’étape de pipeline spécifiée, le pixel/vertex, le cas échéant, l’événement et le frame.
MS-HAID: vspixengine.IDebugShaderRequest\_BeginDebugShader\_IPixErrorCallback\_ptr\_EventID\_DWORD\_DWORD\_Point2D\_PipeLineStages\_PixelHistoryOperation\_ptr\_DWORD\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IDebugShaderRequest :: BeginDebugShader, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC93D31C-8593-4B03-B974-87B886B9431D
api_name:
- IDebugShaderRequest.BeginDebugShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 20e9667ba0c0d4d36175cd9694c2e6b57d192fab
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629853"
---
# <a name="span-idvspixengineidebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptrspanidebugshaderrequestbegindebugshader-method"></a><span id="vspixengine.idebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptr"></span>IDebugShaderRequest :: BeginDebugShader, méthode

Demande de démarrer une session de débogage de nuanceur pour l’étape de pipeline spécifiée, le pixel/vertex, le cas échéant, l’événement et le frame.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT BeginDebugShader(
   IPixErrorCallback *     errorCallback,
   EventID                 eventID,
   DWORD                   frameNumber,
   DWORD                   vertex,
   Point2D                 pixel,
   PipeLineStages          stage,
   PixelHistoryOperation * pPixelHistory,
   DWORD *                 pDevice
);
```

## <a name="parameters"></a>Paramètres

*errorCallback*   
Adresse d’un rappel pour les erreurs qui peuvent se produire pendant le débogage.

*1001*   
Événement spécifié.

*frameNumber*   
Frame spécifié.

*vertex*   
Vertex spécifié. S’applique uniquement lors du débogage d’un nuanceur de sommets.

*pixellisé*   
Pixel spécifié. S’applique uniquement lors du débogage d’un nuanceur de pixels.

*mode*   
Étape de pipeline spécifiée.

*pPixelHistory*   
Adresse des résultats de l’historique des pixels utilisée pour rechercher le pixel associé à déboguer. S’applique uniquement lors du débogage d’un nuanceur de pixels.

*pDevice*   
Adresse à passer au moteur de débogage pour communiquer avec cette session de débogage (moteur de débogage ReadProcessMemory sur cette adresse).

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IDebugShaderRequest**](/windows/desktop/direct3dtools/idebugshaderrequest)

 

 
