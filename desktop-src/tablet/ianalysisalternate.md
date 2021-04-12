---
description: Représente les correspondances possibles pour les mots de reconnaissance de l’écriture manuscrite pour les objets IContextNode.
ms.assetid: a497c140-6166-4309-af0f-851af09015c6
title: Interface IAnalysisAlternate (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8f65b97ca3811212b73c6bdb12e9b889636dd6ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201521"
---
# <a name="ianalysisalternate-interface"></a>Interface IAnalysisAlternate

Représente les correspondances possibles pour les mots de reconnaissance de l’écriture manuscrite pour les objets [**IContextNode**](icontextnode.md) .

## <a name="members"></a>Membres

L’interface **IAnalysisAlternate** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IAnalysisAlternate** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IAnalysisAlternate** possède ces méthodes.



| Méthode                                                                          | Description                                                                                                                                                          |
|:--------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAlternateNodes**](ianalysisalternate-getalternatenodes.md)               | Récupère les objets [**IContextNode**](icontextnode.md) associés à cet autre.<br/>                                                       |
| [**GetRecognitionConfidence**](ianalysisalternate-getrecognitionconfidence.md) | Récupère une valeur qui indique le niveau de confiance de l' [**IInkAnalyzer**](iinkanalyzer.md) dans la précision du **IAnalysisAlternate**.<br/> |
| [**GetRecognizedString**](ianalysisalternate-getrecognizedstring.md)           | Récupère la valeur de chaîne reconnue de l’objet **IAnalysisAlternate** .<br/>                                                                               |
| [**GetStrokeIds**](ianalysisalternate-getstrokeids.md)                         | Récupère les identificateurs de trait associés à ce **IAnalysisAlternate**.<br/>                                                                    |



 

## <a name="remarks"></a>Notes

Il existe de nombreuses variantes dans l’écriture manuscrite des utilisateurs. Pour cette raison, les reconnaissance de l’écriture manuscrite peuvent parfois convertir l’écriture manuscrite en texte qui diffère de celui prévu par l’utilisateur. Lorsqu’un [**IInkAnalyzer**](iinkanalyzer.md) effectue une analyse sur une collection de traits, le **IInkAnalyzer** recherche l’ensemble de mots le plus probable représenté par l’écriture manuscrite. En outre, le **IInkAnalyzer** trouve également des ensembles d’autres correspondances de reconnaissance, qui sont stockées dans une collection [**IAnalysisAlternates**](ianalysisalternates.md) . Pour qu’un utilisateur puisse tirer parti des alternatives de reconnaissance, vous devez créer une interface utilisateur qui permet à l’utilisateur de sélectionner le **IAnalysisAlternate** approprié.

Les objets **IAnalysisAlternate** sont généralement obtenus par le biais de la [**méthode IInkAnalyzer :: GetAlternates**](iinkanalyzer-getalternates.md). Le premier objet **IAnalysisAlternate** de la collection est ce que le [**IInkAnalyzer**](iinkanalyzer.md) considère comme étant le plus probable.

Cette interface est équivalente à [System. Windows. Ink. AnalysisCore. AnalysisAlternateBase](/previous-versions/ms610092(v=vs.100)) dans le .NET Framework.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[**IInkAnalyzer :: GetAlternatesForContextNodes, méthode**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**IInkAnalyzer :: GetAlternatesForStrokes, méthode**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[**IInkAnalyzer :: GetAlternates, méthode**](iinkanalyzer-getalternates.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

