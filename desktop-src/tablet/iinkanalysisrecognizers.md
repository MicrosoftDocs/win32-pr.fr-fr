---
description: Contient une collection d’objets qui implémentent l’interface IInkAnalysisRecognizer et qui représentent la capacité de reconnaître l’écriture manuscrite, les objets ou les gestes.
ms.assetid: d9264c9f-bf75-493e-8e41-57ea69955e6b
title: Interface IInkAnalysisRecognizers (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ba9bbcd029803e613fb27d351de554c013c02616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318462"
---
# <a name="iinkanalysisrecognizers-interface"></a>Interface IInkAnalysisRecognizers

Contient une collection d’objets qui implémentent l’interface [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) et qui représentent la capacité de reconnaître l’écriture manuscrite, les objets ou les gestes.

## <a name="members"></a>Membres

L’interface **IInkAnalysisRecognizers** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IInkAnalysisRecognizers** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IInkAnalysisRecognizers** possède ces méthodes.



| Méthode                                                                               | Description                                                                                                             |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**GetCount**](iinkanalysisrecognizers-getcount.md)                                 | Récupère le nombre d’objets [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) dans cette collection.<br/> |
| [**GetInkAnalysisRecognizer**](iinkanalysisrecognizers-getinkanalysisrecognizer.md) | Récupère le [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) à l’index spécifié.<br/>               |



 

## <a name="remarks"></a>Notes

La méthode [**IInkAnalyzer :: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) méthode de [**IInkAnalyzer**](iinkanalyzer.md) retourne une collection **IInkAnalysisRecognizers** contenant les détecteurs d’encre disponibles sur le Tablet PC actuel.

Pour un module de reconnaissance de langage, la méthode [**IInkAnalysisRecognizer :: GetLanguages**](iinkanalysisrecognizer-getlanguages.md) retourne un tableau non vide. Pour les modules de reconnaissance de mouvement et d’objet, la méthode **IInkAnalysisRecognizer :: GetLanguages** retourne un tableau vide.

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

[**IInkAnalyzer :: GetInkAnalysisRecognizersByPriority, méthode**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

