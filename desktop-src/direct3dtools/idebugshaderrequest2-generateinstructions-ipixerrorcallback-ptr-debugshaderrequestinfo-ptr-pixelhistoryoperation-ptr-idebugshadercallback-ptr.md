---
description: Demandes de génération d’instructions de trace de nuanceur dans une demande de débogage. Le débogage basé sur la trace se produit sur le processeur (Warp) au lieu du GPU.
MS-HAID: vspixengine.IDebugShaderRequest2\_GenerateInstructions\_IPixErrorCallback\_ptr\_DebugShaderRequestInfo\_ptr\_PixelHistoryOperation\_ptr\_IDebugShaderCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IDebugShaderRequest2 :: GenerateInstructions, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 50685D38-AA85-43D7-9199-12B3776708C2
api_name:
- IDebugShaderRequest2.GenerateInstructions
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 08005bd777f8835f60615c61dfc6ae763f2a5a8345bb8309e0923941eeacf2dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094869"
---
# <a name="span-idvspixengineidebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptrspanidebugshaderrequest2generateinstructions-method"></a><span id="vspixengine.idebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptr"></span>IDebugShaderRequest2 :: GenerateInstructions, méthode

Demandes de génération d’instructions de trace de nuanceur dans une demande de débogage. Le débogage basé sur la trace se produit sur le processeur (Warp) au lieu du GPU.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GenerateInstructions(
   IPixErrorCallback *      errorCallback,
   DebugShaderRequestInfo * requestInfo,
   PixelHistoryOperation *  pPixelHistory,
   IDebugShaderCallback *   pCallback
);
```

## <a name="parameters"></a>Paramètres

*errorCallback*   
Adresse d’un rappel pour les erreurs qui peuvent se produire lors de la génération des instructions de trace du nuanceur.

*requestInfo*   
Adresse d’une structure DebugShaderRequestInfo qui décrit l’événement/vertex/pixel demandé.

*pPixelHistory*   
Adresse des résultats de l’historique des pixels utilisée pour rechercher le pixel associé à déboguer. S’applique uniquement lors du débogage d’un nuanceur de pixels.

*pCallback*   
Adresse d’un rappel utilisé pour notifier l’hôte de résultats.

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IDebugShaderRequest2**](/windows/desktop/direct3dtools/idebugshaderrequest2)

 

 
