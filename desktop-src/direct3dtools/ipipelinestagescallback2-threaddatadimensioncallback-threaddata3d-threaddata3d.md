---
description: Rappel qui avertit l’hôte du nombre de threads et de groupes du nuanceur de calcul dans la requête associée.
MS-HAID: vspixengine.IPipeLineStagesCallback2\_ThreadDataDimensionCallback\_ThreadData3D\_ThreadData3D
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesCallback2 :: ThreadDataDimensionCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E8765C14-0A55-468D-BCA8-3E28E5476DFB
api_name:
- IPipeLineStagesCallback2.ThreadDataDimensionCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0d56989325aa59f4bc1681e3d799420453945e7363736410ba5e46efbc69c3f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023039"
---
# <a name="span-idvspixengineipipelinestagescallback2_threaddatadimensioncallback_threaddata3d_threaddata3dspanipipelinestagescallback2threaddatadimensioncallback-method"></a><span id="vspixengine.ipipelinestagescallback2_threaddatadimensioncallback_threaddata3d_threaddata3d"></span>IPipeLineStagesCallback2 :: ThreadDataDimensionCallback, méthode

Rappel qui avertit l’hôte du nombre de threads et de groupes du nuanceur de calcul dans la requête associée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ThreadDataDimensionCallback(
   ThreadData3D threadGroupCount,
   ThreadData3D threadGroupSize
);
```

## <a name="parameters"></a>Paramètres

*threadGroupCount*   
Nombre multidimensionnel de groupes de threads.

*threadGroupSize*   
Taille multidimensionnelle de chaque groupe de threads.

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IPipeLineStagesCallback2**](/windows/desktop/direct3dtools/ipipelinestagescallback2)

 

 
