---
description: Contient une collection d’objets qui implémentent l’interface IAnalysisAlternate et qui sont le résultat de l’analyse de l’encre.
ms.assetid: 53802a62-4425-40fd-bf48-0da55ea8ffbe
title: Interface IAnalysisAlternates (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e2643ef8ea90d029aee6bd0673931d27e9987b0af0a898e854cb87d74a89c0af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058089"
---
# <a name="ianalysisalternates-interface"></a>Interface IAnalysisAlternates

Contient une collection d’objets qui implémentent l’interface [**IAnalysisAlternate**](ianalysisalternate.md) et qui sont le résultat de l’analyse de l’encre.

## <a name="members"></a>Membres

L’interface **IAnalysisAlternates** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IAnalysisAlternates** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IAnalysisAlternates** possède ces méthodes.



| Méthode                                                                   | Description                                                                                                                                      |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAnalysisAlternate**](ianalysisalternates-getanalysisalternate.md) | Récupère l’objet [**IAnalysisAlternate**](ianalysisalternate.md) à l’index spécifié dans la collection.<br/>                   |
| [**GetCount**](ianalysisalternates-getcount.md)                         | Récupère le nombre d’objets [**IAnalysisAlternate**](ianalysisalternate.md) contenus dans la collection **IAnalysisAlternates** .<br/> |



 

## <a name="remarks"></a>Remarques

Cette interface est équivalente à [**System. Windows. Classe Ink. AnalysisCore. AnalysisAlternateBaseCollection**](/previous-versions/ms610094(v=vs.100)) dans la .NET Framework.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IInkAnalyzer :: GetAlternates, méthode**](iinkanalyzer-getalternates.md)
</dt> <dt>

[**IInkAnalyzer :: GetAlternatesForContextNodes, méthode**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**IInkAnalyzer :: GetAlternatesForStrokes, méthode**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

