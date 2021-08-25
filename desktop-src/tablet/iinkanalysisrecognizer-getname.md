---
description: Récupère le nom du module de reconnaissance.
ms.assetid: bd97fead-1e80-49dc-ada0-38eb5dc015ae
title: 'IInkAnalysisRecognizer :: GetName, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: df86f5526a6b28f8a7f383ddfb49ca999875b8aa08c66e07a9ac95c41acd13cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773619"
---
# <a name="iinkanalysisrecognizergetname-method"></a>IInkAnalysisRecognizer :: GetName, méthode

Récupère le nom du module de reconnaissance.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetName(
  [out] BSTR *pbstrName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbstrName* \[ à\]
</dt> <dd>

Nom du module de reconnaissance.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) sur \* *pbstrName* lorsque vous n’avez plus besoin d’utiliser la chaîne.

 

Le nom est localisé pour la langue indépendante de la région que le module de reconnaissance prend en charge.

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

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

