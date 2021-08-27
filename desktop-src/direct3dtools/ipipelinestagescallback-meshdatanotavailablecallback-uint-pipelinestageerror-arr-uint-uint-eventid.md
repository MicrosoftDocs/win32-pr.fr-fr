---
description: Rappel qui avertit l’hôte des étapes de pipeline qui ne sont pas en mesure de retourner des données de maillage pour l’événement spécifié dans la demande associée.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataNotAvailableCallback\_UINT\_PipeLineStageError\_arr\_UINT\_UINT\_EventID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesCallback :: MeshDataNotAvailableCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A51E7C45-C1F0-4576-8638-9C3B185385BA
api_name:
- IPipeLineStagesCallback.MeshDataNotAvailableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9c95f661c5a18f2573fe477f3aa1ef4d0035ee1e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622135"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventidspanipipelinestagescallbackmeshdatanotavailablecallback-method"></a><span id="vspixengine.ipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventid"></span>IPipeLineStagesCallback :: MeshDataNotAvailableCallback, méthode

Rappel qui avertit l’hôte des étapes de pipeline qui ne sont pas en mesure de retourner des données de maillage pour l’événement spécifié dans la demande associée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT MeshDataNotAvailableCallback(
   UINT                  numberStages,
   PipeLineStageError [] count0_errors,
   UINT                  width,
   UINT                  height,
   EventID               eid
);
```

## <a name="parameters"></a>Paramètres

*numberStages*   
Nombre d’erreurs d’étape retournées.

*\_Erreurs count0*   
Erreurs d’étape de pipeline.

*Largeur*   
Largeur de la chaîne de permutation dans avec l’appel de dessin. Utilisé lors de la demande d’images d’aperçu de pipeline.

*celle*   
Hauteur de la chaîne de permutation dans avec l’appel de dessin. Utilisé lors de la demande d’images d’aperçu de pipeline.

*Numéro*   
Événement représenté dans les résultats.

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IPipeLineStagesCallback**](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
