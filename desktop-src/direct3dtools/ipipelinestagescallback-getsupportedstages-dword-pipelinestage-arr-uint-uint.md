---
description: Rappel qui avertit l’hôte des étapes de pipeline utilisées par l’appel de dessin de la demande dans.
MS-HAID: vspixengine.IPipeLineStagesCallback\_GetSupportedStages\_DWORD\_PipeLineStage\_arr\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesCallback :: GetSupportedStages, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F7046A41-5C9C-42FE-B1E2-879A47CE08E3
api_name:
- IPipeLineStagesCallback.GetSupportedStages
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 91e2d80813d8d87c92819aab29dbc368b397d074
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623305"
---
# <a name="span-idvspixengineipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uintspanipipelinestagescallbackgetsupportedstages-method"></a><span id="vspixengine.ipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uint"></span>IPipeLineStagesCallback :: GetSupportedStages, méthode

Rappel qui avertit l’hôte des étapes de pipeline utilisées par l’appel de dessin de la demande dans.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSupportedStages(
   DWORD            numColumns,
   PipeLineStage [] count0_pStages,
   UINT             swapChainWidth,
   UINT             swapChainHeight
);
```

## <a name="parameters"></a>Paramètres

*numColumns*   
Nombre d’étapes retournées.

*count0 \_ pStages*   
Étapes du pipeline.

*swapChainWidth*   
Largeur de la chaîne de permutation dans avec l’appel de dessin. Utilisé lors de la demande d’images d’aperçu de pipeline.

*swapChainHeight*   
Hauteur de la chaîne de permutation dans avec l’appel de dessin. Utilisé lors de la demande d’images d’aperçu de pipeline.

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IPipeLineStagesCallback**](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
