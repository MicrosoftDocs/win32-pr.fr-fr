---
description: Retourne les identificateurs de trait associés à ce IAnalysisAlternate.
ms.assetid: 495d485f-0d16-4085-9213-cc55f3f259f0
title: 'IAnalysisAlternate :: GetStrokeIds, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 80882a83e9a0fa9bf973990a689e2abf1a52a870
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862730"
---
# <a name="ianalysisalternategetstrokeids-method"></a>IAnalysisAlternate :: GetStrokeIds, méthode

Retourne les identificateurs de trait associés à ce [**IAnalysisAlternate**](ianalysisalternate.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokeIds
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pulStrokeIdsCount* \[ in, out\]
</dt> <dd>

Pointeur vers un **ULong** qui a pour valeur le nombre d’identificateurs de trait associés à ce [**IAnalysisAlternate**](ianalysisalternate.md).

</dd> <dt>

*pplStrokeIds* \[ à\]
</dt> <dd>

\[out, size \_ is ( \* *PULSTROKEIDSCOUNT* \* sizeof (long))\]

Tableau de *pulStrokeIdsCount* de longueur **long** qui a pour valeur les identificateurs de trait associés à ce [**IAnalysisAlternate**](ianalysisalternate.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

> [!Caution]  
> Pour éviter une fuite de mémoire, utilisez [CoTaskMemFree](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire à partir de \* *pplStrokeIds* lorsque vous n’avez plus besoin des informations.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

