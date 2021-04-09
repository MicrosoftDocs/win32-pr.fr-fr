---
description: Récupère les identificateurs pour les paramètres régionaux pris en charge par ce IInkAnalysisRecognizer.
ms.assetid: 14c91ad0-f49e-43e7-848c-abc96b0dffa8
title: 'IInkAnalysisRecognizer :: GetLanguages, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetLanguages
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1e2b9792957b2de02daf45f8b662cfcb1174be72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862709"
---
# <a name="iinkanalysisrecognizergetlanguages-method"></a>IInkAnalysisRecognizer :: GetLanguages, méthode

Récupère les identificateurs pour les paramètres régionaux pris en charge par ce [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetLanguages(
  [in, out] ULONG *pulLanguagesCount,
  [out]     ULONG **ppulLanguages
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pulLanguagesCount* \[ in, out\]
</dt> <dd>

Nombre d’identificateurs dans *ppulLanguages*.

</dd> <dt>

*ppulLanguages* \[ à\]
</dt> <dd>

Pointeur vers les identificateurs pour les paramètres régionaux pris en charge par ce [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

> [!Caution]  
> Pour éviter une fuite de mémoire, utilisez [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire à partir de \* *ppulLanguages* lorsque vous n’avez plus besoin des informations.

 

Cette méthode retourne un tableau vide pour les objets et les modules de reconnaissance de mouvement.

Pour plus d’informations sur les identificateurs de langue, consultez [constantes et chaînes d’identificateur de langue](/windows/desktop/Intl/language-identifier-constants-and-strings).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

