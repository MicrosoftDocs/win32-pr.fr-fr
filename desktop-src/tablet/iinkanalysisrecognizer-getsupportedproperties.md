---
description: Récupère les identificateurs globaux uniques (GUID) pour les propriétés que ce IInkAnalysisRecognizer peut générer pour les résultats d’analyse.
ms.assetid: 3a36bc6c-5067-4291-9119-bc6836d32c21
title: 'IInkAnalysisRecognizer :: GetSupportedProperties, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetSupportedProperties
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fce33317a234d82d6045dbefa93ed582d31d92f6ff54abe9ef87949559a5d269
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057859"
---
# <a name="iinkanalysisrecognizergetsupportedproperties-method"></a>IInkAnalysisRecognizer :: GetSupportedProperties, méthode

Récupère les identificateurs globaux uniques (GUID) pour les propriétés que ce [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) peut générer pour les résultats d’analyse.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSupportedProperties(
  [in, out] ULONG *pulPropertiesCount,
  [out]     GUID  **ppProperties
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pulPropertiesCount* \[ in, out\]
</dt> <dd>

Nombre de GUID dans *ppProperties*.

</dd> <dt>

*ppProperties* \[ à\]
</dt> <dd>

Pointeur vers les GUID des propriétés que ce [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) peut générer pour les résultats d’analyse.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

> [!Caution]  
> Pour éviter une fuite de mémoire, utilisez [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire à partir de \* *ppProperties* lorsque vous n’avez plus besoin des informations.

 

Un module de reconnaissance peut prendre en charge les métriques de ligne, les numéros de ligne, les niveaux de confiance, etc. Pour obtenir la liste complète des propriétés qu’un module de reconnaissance peut prendre en charge, consultez [constantes RecognitionProperty](recognitionproperty-constants.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[Constantes RecognitionProperty](recognitionproperty-constants.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

