---
description: Récupère le IInkAnalysisRecognizer à l’index spécifié.
ms.assetid: e4db56c6-7c15-4336-bc0a-f50222c3520e
title: 'IInkAnalysisRecognizers :: GetInkAnalysisRecognizer, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers.GetInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1008ae0b26d30233c3b00167391523d321cd381e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485089"
---
# <a name="iinkanalysisrecognizersgetinkanalysisrecognizer-method"></a>IInkAnalysisRecognizers :: GetInkAnalysisRecognizer, méthode

Récupère le [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) à l’index spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetInkAnalysisRecognizer(
  [in]  ULONG                  ulIndex,
  [out] IInkAnalysisRecognizer **ppInkAnalysisRecognizer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ulIndex* \[ dans\]
</dt> <dd>

Index de base zéro de l’objet [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) à récupérer.

</dd> <dt>

*ppInkAnalysisRecognizer* \[ à\]
</dt> <dd>

Pointeur vers le [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) à l’index spécifié.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppInkAnalysisRecognizer* lorsque vous n’avez plus besoin d’utiliser le module de reconnaissance de l’analyse de l’encre.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**InkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

