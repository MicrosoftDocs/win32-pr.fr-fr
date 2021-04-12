---
description: Enregistre les résultats d’analyse pour les traits spécifiés associés à un IInkAnalyzer.
ms.assetid: 6ff29b95-6c76-4e3d-b4c0-5e7cb6a9ddf9
title: 'IInkAnalyzer :: SaveResultsForStrokes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1371b056cf01beba75fdcbd427c526ed29d20c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318446"
---
# <a name="iinkanalyzersaveresultsforstrokes-method"></a>IInkAnalyzer :: SaveResultsForStrokes, méthode

Enregistre les résultats d’analyse pour les traits spécifiés associés à un [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SaveResultsForStrokes(
  [in]          ULONG ulStrokeIdsCount,
  [in]          LONG  *plStrokeIds,
  [in, out]     ULONG *pulSerializedDataSize,
  [out, retval] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ulStrokeIdsCount* \[ dans\]
</dt> <dd>

Nombre d’identificateurs de trait dans **plStrokeIds**.

</dd> <dt>

*plStrokeIds* \[ dans\]
</dt> <dd>

Tableau d’identificateurs de trait.

</dd> <dt>

*pulSerializedDataSize* \[ in, out\]
</dt> <dd>

Nombre d’octets dans *ppbSerializedData*.

</dd> <dt>

*ppbSerializedData* \[ out, retval\]
</dt> <dd>

Pointeur vers les données d’analyse sérialisées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) sur \* *ppbSerializedData* lorsque vous n’avez plus besoin des informations.

 

Cette méthode enregistre les résultats de l’analyse actuelle pour les traits spécifiés. Cette méthode enregistre les objets [**IContextNode**](icontextnode.md) feuille manuscrits contenant les traits et tous les ancêtres de ces nœuds de contexte. Cette méthode n’enregistre aucune donnée de trait ni aucun nœud d’indicateur d’analyse. Il incombe à votre application de synchroniser les résultats de l’analyse et les données de trait correspondantes, si elle persiste.

Cette méthode retourne un code d’erreur lorsqu’un objet [**IContextNode**](icontextnode.md) à enregistrer est partiellement rempli (consultez [**IContextNode :: GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
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

[**IInkAnalyzer :: SaveResultsForNodes, méthode**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

