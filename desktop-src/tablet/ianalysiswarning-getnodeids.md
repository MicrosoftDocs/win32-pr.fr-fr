---
description: Retourne les identificateurs de tous les nœuds de contexte appropriés associés à cet avertissement.
ms.assetid: 8c418f48-3903-47c1-82e2-085de39574d4
title: 'IAnalysisWarning :: GetNodeIds, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetNodeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a38abd054e457ef9dbaf5dd93c38954b1ce6dcb3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523292"
---
# <a name="ianalysiswarninggetnodeids-method"></a>IAnalysisWarning :: GetNodeIds, méthode

Retourne les identificateurs de tous les nœuds de contexte appropriés associés à cet avertissement.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetNodeIds(
  [in, out] ULONG *pulCount,
  [out]     GUID  **ppNodeIds
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pulCount* \[ in, out\]
</dt> <dd>

Nombre d’identificateurs globaux uniques (GUID) dans *ppNodeIds*.

</dd> <dt>

*ppNodeIds* \[ à\]
</dt> <dd>

Pointeur vers un tableau de GUID qui identifie les nœuds de contexte associés à cet avertissement d’analyse, ou **null** si aucun nœud de contexte n’est associé à l’avertissement.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

Si *ppNodeIds* est passé comme **null**, la méthode **GetNodeIds** retourne **S \_ OK** et le nombre de rectangles est retourné dans *pulCount*.

> [!Caution]  
> Pour éviter une fuite de mémoire, utilisez [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire à partir de \* *ppNodeIds* lorsque vous n’avez plus besoin des informations.

 

## <a name="examples"></a>Exemples

L’exemple suivant montre comment récupérer les objets [**IContextNode**](icontextnode.md) qui se trouvent dans le [**IAnalysisWarning**](ianalysiswarning.md), `warning` et comment récupérer uniquement le nombre d’objets **IContextNode**


```C++
// Get the count of the context nodes and their identifiers.
ULONG count = 0;
GUID* nodeIds = 0;
warning->GetNodeIds(&count, &nodeIds);

// Use nodeIds

::CoTaskMemFree(nodeIds);

// GetNodeIds just gets the count and returns S_OK
ULONG number = 0;
warning->GetNodeIds(&number, NULL); 
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer :: FindNode, méthode**](iinkanalyzer-findnode.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

