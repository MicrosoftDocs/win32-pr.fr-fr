---
description: Demande à déboguer un nuanceur sur le GPU (débogage dynamique) vs CPU (débogage basé sur trace).
MS-HAID: vspixengine.IDebugLiveShaderRequest\_BeginDebugLiveShader\_DebugShaderRequestInfo\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IDebugLiveShaderRequest :: BeginDebugLiveShader, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 805B2B68-C251-4192-85A3-F857B3F204C7
api_name:
- IDebugLiveShaderRequest.BeginDebugLiveShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2b09bff6a414df620e06263e13d94c2f39e36903
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746749"
---
# <a name="span-idvspixengineidebugliveshaderrequest_begindebugliveshader_debugshaderrequestinfo_ptrspanidebugliveshaderrequestbegindebugliveshader-method"></a><span id="vspixengine.idebugliveshaderrequest_begindebugliveshader_debugshaderrequestinfo_ptr"></span>IDebugLiveShaderRequest :: BeginDebugLiveShader, méthode

Demande à déboguer un nuanceur sur le GPU (débogage dynamique) vs CPU (débogage basé sur trace).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT BeginDebugLiveShader(
   DebugShaderRequestInfo * requestInfo
);
```

## <a name="parameters"></a>Paramètres

*requestInfo*   
Adresse d’une structure DebugShaderRequestInfo qui décrit l’événement/vertex/pixel demandé.

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IDebugLiveShaderRequest**](/windows/desktop/direct3dtools/idebugliveshaderrequest)

 

 
