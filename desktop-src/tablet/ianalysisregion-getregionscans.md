---
description: Récupère un tableau de rectangles qui définit la zone du IAnalysisRegion.
ms.assetid: 40de4c27-4b3b-4db3-af08-cb53e638db6b
title: 'IAnalysisRegion :: GetRegionScans, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetRegionScans
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6cb8db60b5818f5bc2bc38892912e9ec40af1eb9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235103"
---
# <a name="ianalysisregiongetregionscans-method"></a>IAnalysisRegion :: GetRegionScans, méthode

Récupère un tableau de rectangles qui définit la zone du [**IAnalysisRegion**](ianalysisregion.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetRegionScans(
  [out] ULONG *pulCount,
  [out] RECT  **pRegionScans
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pulCount* \[ à\]
</dt> <dd>

Nombre de rectangles retournés dans *pRegionScans*.

</dd> <dt>

*pRegionScans* \[ à\]
</dt> <dd>

Pointeur vers un tableau de rectangles qui définit la zone du [**IAnalysisRegion**](ianalysisregion.md).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

Si *pRegionScans* est passé comme **null**, la méthode **GetRegionScans** retourne **S \_ OK** et le nombre de rectangles est retourné dans *pulCount*.

> [!Caution]  
> Pour éviter une fuite de mémoire, utilisez [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire à partir de \* *pRegionScans* lorsque vous n’avez plus besoin des informations.

 

Les limites des rectangles sont exprimées en coordonnées d’espace manuscrit.

L’Union des rectangles retournés représente la zone du [**IAnalysisRegion**](ianalysisregion.md).

## <a name="examples"></a>Exemples

L’exemple suivant montre comment récupérer les rectangles qui définissent la zone du [**IAnalysisRegion**](ianalysisregion.md) `region` et comment récupérer uniquement le nombre de rectangles.


```C++
// Get the count and the rectangles.
ULONG count = 0;
RECT* rects = 0;
region->GetRegionScans(&count, &rects);

// Use rects

::CoTaskMemFree(rects);

// GetRegionScans just gets the count and returns S_OK
ULONG number = 0;
region->GetRegionScans(&number, NULL); 
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

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**IAnalysisRegion :: GetBounds, méthode**](ianalysisregion-getbounds.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

