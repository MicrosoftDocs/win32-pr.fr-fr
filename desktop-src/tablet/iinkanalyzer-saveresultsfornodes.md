---
description: Enregistre les résultats d’analyse pour une collection de nœuds de contexte spécifique associée à un IInkAnalyzer.
ms.assetid: 671bdb11-6e30-4254-b320-208face1f593
title: 'IInkAnalyzer :: SaveResultsForNodes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4386f9b051bf1cfcda6ee55d7b83728b096dc6f69de4d87745ce564f19249565
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091568"
---
# <a name="iinkanalyzersaveresultsfornodes-method"></a>IInkAnalyzer :: SaveResultsForNodes, méthode

Enregistre les résultats d’analyse pour une collection de nœuds de contexte spécifique associée à un [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SaveResultsForNodes(
  [in]      IContextNodes *pContextNodes,
  [in, out] ULONG         *pulSerializedDataSize,
  [out]     BYTE          **ppbSerializedData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pContextNodes* \[ dans\]
</dt> <dd>

Collection [**IContextNode**](icontextnode.md) pour laquelle enregistrer les résultats de l’analyse.

</dd> <dt>

*pulSerializedDataSize* \[ in, out\]
</dt> <dd>

Nombre d’octets dans *ppbSerializedData*.

</dd> <dt>

*ppbSerializedData* \[ à\]
</dt> <dd>

Pointeur vers les données d’analyse sérialisées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) sur \* *ppbSerializedData* lorsque vous n’avez plus besoin des informations.

 

Cette méthode enregistre les résultats de l’analyse actuelle pour les objets [**IContextNode**](icontextnode.md) dans *pContextNodes* et tous leurs nœuds de contexte ancêtres et descendants. Cette méthode n’enregistre aucune donnée de trait. Il incombe à votre application de synchroniser les résultats de l’analyse et les données de trait correspondantes, si elle persiste.

Si l’objet [**IContextNode**](icontextnode.md) à enregistrer n’est rempli que partiellement, cette méthode retourne un code d’erreur (consultez [**IContextNode :: GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer :: LoadResults, méthode**](iinkanalyzer-loadresults.md)
</dt> <dt>

[**IInkAnalyzer :: SaveResults, méthode**](iinkanalyzer-saveresults.md)
</dt> <dt>

[**IInkAnalyzer :: SaveResultsForStrokes, méthode**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

