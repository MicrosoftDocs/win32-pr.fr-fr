---
description: Donne accès à l’analyse de la disposition, à l’écriture et au dessin de la classification et à la reconnaissance de l’écriture manuscrite
ms.assetid: 3a19db78-df14-43c2-9e3e-8cf674aa7b9c
title: Interface IInkAnalyzer (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bd1bca0a00cbe95c4d32b2dfad8afe6c5db8ad63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319622"
---
# <a name="iinkanalyzer-interface"></a>Interface IInkAnalyzer

Donne accès à l’analyse de la disposition, à l’écriture et au dessin de la classification et à la reconnaissance de l’écriture manuscrite

## <a name="members"></a>Membres

L’interface **IInkAnalyzer** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IInkAnalyzer** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IInkAnalyzer** possède ces méthodes.



| Méthode                                                                                                  | Description                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Abandon**](iinkanalyzer-abort.md)                                                                     | Annule l’opération d’analyse en cours.<br/>                                                                                                                                           |
| [**AddStroke**](iinkanalyzer-addstroke.md)                                                             | Ajoute des données de trait pour un seul trait à **IInkAnalyzer** et assigne l’identificateur de culture du thread d’entrée actif au trait.<br/>                                              |
| [**AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)                                       | Ajoute des données de trait pour un seul trait à **IInkAnalyzer** et assigne un identificateur de culture spécifique au trait.<br/>                                                             |
| [**AddStrokes**](iinkanalyzer-addstrokes.md)                                                           | Ajoute des données de trait pour plusieurs traits à **IInkAnalyzer** et assigne l’identificateur de culture du thread d’entrée actif aux traits.<br/>                                            |
| [**AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)                                     | Ajoute des données de trait pour plusieurs traits à **IInkAnalyzer** et assigne l’identificateur de culture spécifié aux traits.<br/>                                                        |
| [**AddStrokesToCustomRecognizer**](iinkanalyzer-addstrokestocustomrecognizer.md)                       | Ajoute des données de trait pour plusieurs traits à un nœud de reconnaissance personnalisé.<br/>                                                                                                                |
| [**AddStrokeToCustomRecognizer**](iinkanalyzer-addstroketocustomrecognizer.md)                         | Ajoute des données de trait pour un seul trait à un nœud de reconnaissance personnalisé.<br/>                                                                                                                 |
| [**Analyse**](iinkanalyzer-analyze.md)                                                                 | Effectue une analyse de l’encre synchrone.<br/>                                                                                                                                                |
| [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)                                             | Effectue une analyse d’encre asynchrone.<br/>                                                                                                                                               |
| [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md)                                                 | Efface les données de paquets de trait du **IInkAnalyzer**.<br/>                                                                                                                              |
| [**CreateAnalysisHint**](iinkanalyzer-createanalysishint.md)                                           | Ajoute un nouveau nœud d’indicateur d’analyse avec une zone infinie à la **IInkAnalyzer**.<br/>                                                                                                      |
| [**CreateContextNodes**](iinkanalyzer-createcontextnodes.md)                                           | Crée un objet [**IContextNodes**](icontextnodes.md) .<br/>                                                                                                                         |
| [**CreateCustomRecognizer**](iinkanalyzer-createcustomrecognizer.md)                                   | Crée un nouveau nœud de reconnaissance personnalisé pour **IInkAnalyzer**.<br/>                                                                                                                    |
| [**DeleteAnalysisHint**](iinkanalyzer-deleteanalysishint.md)                                           | Supprime un indicateur d’analyse de **IInkAnalyzer**.<br/>                                                                                                                               |
| [**FindInkLeafNodes**](iinkanalyzer-findinkleafnodes.md)                                               | Récupère tous les nœuds de feuille d’encre.<br/>                                                                                                                                              |
| [**FindInkLeafNodesForStrokes**](iinkanalyzer-findinkleafnodesforstrokes.md)                           | Récupère les nœuds de feuille d’encre qui contiennent les traits spécifiés.<br/>                                                                                                                  |
| [**FindLeafNodes**](iinkanalyzer-findleafnodes.md)                                                     | Récupère tous les nœuds terminaux.<br/>                                                                                                                                                  |
| [**FindNode**](iinkanalyzer-findnode.md)                                                               | Récupère l’objet [**IContextNode**](icontextnode.md) pour un identificateur global unique (Guid) spécifié.<br/>                                                                      |
| [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md)                                                 | Récupère tous les objets [**IContextNode**](icontextnode.md) du type spécifié.<br/>                                                                                          |
| [**FindNodesOfTypeForStrokes**](iinkanalyzer-findnodesoftypeforstrokes.md)                             | Récupère tous les objets [**IContextNode**](icontextnode.md) du type spécifié qui contiennent les traits spécifiés.<br/>                                                       |
| [**FindNodesOfTypeInSubTree**](iinkanalyzer-findnodesoftypeinsubtree.md)                               | Récupère tous les objets [**IContextNode**](icontextnode.md) du type spécifié qui sont des descendants de l’objet **IContextNode** spécifié.<br/>                            |
| [**FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)                                     | Récupère tous les objets [**IContextNode**](icontextnode.md) qui correspondent aux critères spécifiés.<br/>                                                                              |
| [**FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)                   | Récupère tous les objets [**IContextNode**](icontextnode.md) qui correspondent aux critères spécifiés et sont des descendants de l’objet **IContextNode** spécifié.<br/>                 |
| [**GetAlternates**](iinkanalyzer-getalternates.md)                                                     | Récupère 10 autres analyses d’analyse pour toutes les entrées manuscrites associées au **IInkAnalyzer**.<br/>                                                                                                |
| [**GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)                       | Récupère d’autres analyses pour les nœuds d’une collection [**IContextNodes**](icontextnodes.md) spécifiée.<br/>                                                                     |
| [**GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md)                                 | Récupère des alternatives d’analyse pour les traits avec les identificateurs de trait spécifiés.<br/>                                                                                              |
| [**GetAnalysisHints**](iinkanalyzer-getanalysishints.md)                                               | Récupère tous les objets [**IContextNode**](icontextnode.md) Hint d’analyse attachés au **IInkAnalyzer**.<br/>                                                        |
| [**GetAnalysisHintsByName**](iinkanalyzer-getanalysishintsbyname.md)                                   | Récupère tous les objets [**IContextNode**](icontextnode.md) Hint d’analyse attachés au **IInkAnalyzer** et portant le nom spécifié.<br/>                       |
| [**GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)                                               | Récupère les indicateurs qui contrôlent la manière dont le **IInkAnalyzer** effectue l’analyse de l’encre.<br/>                                                                                                      |
| [**GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)                                                   | Récupère la zone qui a été modifiée depuis la dernière opération d’analyse.<br/>                                                                                                            |
| [**GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)         | Récupère une collection ordonnée d’objets [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .<br/>                                                                              |
| [**GetNodesFromTextRange**](iinkanalyzer-getnodesfromtextrange.md)                                     | Récupère une collection d’objets [**IContextNode**](icontextnode.md) qui sont pertinents pour la plage de texte spécifiée pour les nœuds de contexte spécifiés.<br/>                             |
| [**GetRecognizedString**](iinkanalyzer-getrecognizedstring.md)                                         | Récupère la chaîne de résultat optimale de l’opération de reconnaissance pour l’ensemble de l’arborescence de nœuds de contexte dans **IInkAnalyzer**.<br/>                                                           |
| [**GetRootNode**](iinkanalyzer-getrootnode.md)                                                         | Récupère le [**IContextNode**](icontextnode.md) racine de l’arborescence de contexte de l’objet **IInkAnalyzer** .<br/>                                                                            |
| [**GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md)                                         | Récupère l’identificateur de paramètres régionaux du trait spécifié.<br/>                                                                                                                          |
| [**GetStrokeType**](iinkanalyzer-getstroketype.md)                                                     | Récupère le type du trait spécifié.<br/>                                                                                                                                       |
| [**GetTextRangeFromNodes**](iinkanalyzer-gettextrangefromnodes.md)                                     | Recherche la plage de texte dans la chaîne reconnue qui correspond à une collection d’objets [**IContextNode**](icontextnode.md) .<br/>                                                   |
| [**IsAnalyzing**](iinkanalyzer-isanalyzing.md)                                                         | Récupère une valeur indiquant si le **IInkAnalyzer** effectue une analyse de l’encre.<br/>                                                                                             |
| [**LoadResults**](iinkanalyzer-loadresults.md)                                                         | Charge les résultats d’analyse enregistrés dans le **IInkAnalyzer**.<br/>                                                                                                                           |
| [**ModifyTopAlternate**](iinkanalyzer-modifytopalternate.md)                                           | Remplace le en-tête supérieur actuel par le autre spécifié et efface le type de confirmation pour tous les objets [**IContextNode**](icontextnode.md) associés à l’autre.<br/> |
| [**ModifyTopAlternateWithConfirmation**](iinkanalyzer-modifytopalternatewithconfirmation.md)           | Remplace le [**IAnalysisAlternate**](ianalysisalternate.md)actuel par le haut de la valeur spécifiée.<br/>                                                                              |
| [**Reconcile**](iinkanalyzer-reconcile.md)                                                             | Détermine les parties des résultats de l’analyse qui ont été modifiées pendant l’analyse de l’encre en arrière-plan.<br/>                                                                                    |
| [**RemoveStroke**](iinkanalyzer-removestroke.md)                                                       | Supprime le trait spécifié du **IInkAnalyzer**.<br/>                                                                                                                           |
| [**RemoveStrokes**](iinkanalyzer-removestrokes.md)                                                     | Supprime les traits spécifiés du **IInkAnalyzer**.<br/>                                                                                                                          |
| [**SaveResults**](iinkanalyzer-saveresults.md)                                                         | Enregistre tous les résultats d’analyse pour un **IInkAnalyzer**.<br/>                                                                                                                               |
| [**SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)                                         | Enregistre les résultats d’analyse pour une collection de nœuds de contexte spécifique associée à un **IInkAnalyzer**.<br/>                                                                                |
| [**SaveResultsForStrokes**](iinkanalyzer-saveresultsforstrokes.md)                                     | Enregistre les résultats d’analyse pour les traits spécifiés associés à un **IInkAnalyzer**.<br/>                                                                                             |
| [**Recherche**](iinkanalyzer-search.md)                                                                   | Fournit une recherche basée sur une expression approximative et non sensible à la casse pour les traits d’écriture analysés et les traits de dessin analysés qui ont des types reconnus.<br/>                                      |
| [**SearchWithLanguageId**](iinkanalyzer-searchwithlanguageid.md)                                       | Fournit une recherche basée sur une expression approximative et non sensible à la casse pour les traits d’écriture analysés et les traits de dessin analysés qui ont des types reconnus.<br/>                                      |
| [**SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)                                               | Modifie les indicateurs qui contrôlent la manière dont le **IInkAnalyzer** effectue l’analyse de l’encre.<br/>                                                                                                       |
| [**SetDirtyRegion**](iinkanalyzer-setdirtyregion.md)                                                   | Modifie la zone qui a été modifiée depuis la dernière opération d’analyse.<br/>                                                                                                             |
| [**SetHighestPriorityInkAnalysisRecognizer**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md) | Déplace le [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) spécifié à la première position dans la liste de reconnaissance d’encre de l’objet **IInkAnalyzer** .<br/>                      |
| [**SetStrokeLanguageId**](iinkanalyzer-setstrokelanguageid.md)                                         | Modifie l’identificateur de paramètres régionaux pour le trait spécifié.<br/>                                                                                                                           |
| [**SetStrokesLanguageId**](iinkanalyzer-setstrokeslanguageid.md)                                       | Modifie l’identificateur de paramètres régionaux pour les traits spécifiés.<br/>                                                                                                                          |
| [**SetStrokesType**](iinkanalyzer-setstrokestype.md)                                                   | Modifie le type des traits spécifiés.<br/>                                                                                                                                        |
| [**SetStrokeType**](iinkanalyzer-setstroketype.md)                                                     | Modifie le type du trait spécifié.<br/>                                                                                                                                         |
| [**UpdateStrokesData**](iinkanalyzer-updatestrokesdata.md)                                             | Met à jour les données du paquet pour les traits spécifiés.<br/>                                                                                                                                |



 

## <a name="remarks"></a>Notes

**IInkAnalyzer** utilise les données de paquets de trait pour analyser l’encre et n’interagit pas directement avec la [**classe InkDisp**](inkdisp-class.md) ou les objets de [collection InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .

Pour ajouter ou supprimer des traits dans le **IInkAnalyzer** à des fins d’analyse, utilisez l’une des méthodes suivantes.

-   [**IInkAnalyzer :: AddStroke, méthode**](iinkanalyzer-addstroke.md)
-   [**IInkAnalyzer :: AddStrokes, méthode**](iinkanalyzer-addstrokes.md)
-   [**IInkAnalyzer :: RemoveStroke, méthode**](iinkanalyzer-removestroke.md)
-   [**IInkAnalyzer :: RemoveStrokes, méthode**](iinkanalyzer-removestrokes.md)

Ces méthodes mettent à jour la région modifiée (consultez la [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)), qui est la région pour laquelle les traits sont analysés au cours de l’opération d’analyse suivante.

Pour analyser l’encre, utilisez la méthode [**IInkAnalyzer :: Analyze**](iinkanalyzer-analyze.md) ou la méthode [**IInkAnalyzer :: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) . Pendant l’analyse, le **IInkAnalyzer** effectue l’analyse de la disposition, la classification des traits et la reconnaissance de l’écriture manuscrite.

Pour modifier les paramètres d’analyse de la disposition et de classification des traits, utilisez la propriété de [**méthode IInkAnalyzer :: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md) .

Pendant l’analyse, le **IInkAnalyzer** reçoit un certain nombre d’événements, y compris des événements générés au cours de l’analyse en arrière-plan. [**\_ IAnalysisProxyEvents**](-ianalysisproxyevents.md) prend en charge les fonctionnalités de proxy de données de **IInkAnalyzer**. Pour plus d’informations, consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md). Pour arrêter le processus d’analyse à partir d’un gestionnaire d’événements, appelez la [**méthode IInkAnalyzer :: Abort**](iinkanalyzer-abort.md).

Pour modifier la langue utilisée par l’analyseur d’encre pour reconnaître l’écriture manuscrite, utilisez la méthode [**IInkAnalyzer :: SetStrokeLanguageId**](iinkanalyzer-setstrokelanguageid.md) ou [**IInkAnalyzer :: SetStrokesLanguageId**](iinkanalyzer-setstrokeslanguageid.md). Pour modifier la façon dont l’analyseur d’encre classifie les traits spécifiques, utilisez la méthode [**IInkAnalyzer :: SetStrokeType**](iinkanalyzer-setstroketype.md) ou [**IInkAnalyzer :: SetStrokesType**](iinkanalyzer-setstrokestype.md).

Le **IInkAnalyzer** charge les informations de tous les détecteurs d’encre installés. La [**méthode IInkAnalyzer :: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) retourne une collection [**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md) contenant chaque [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)disponible. Si plusieurs reconnaissances d’encre prennent en charge une langue spécifique, utilisez la [**méthode IInkAnalyzer :: SetHighestPriorityInkAnalysisRecognizer**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md) pour définir le module de reconnaissance d’encre qui gère les traits pour cette langue.

L’utilisation des indicateurs d’analyse permet d’améliorer la précision de la reconnaissance en fournissant un contexte supplémentaire à l’analyseur d’encre. Les informations de contexte supplémentaires peuvent aider l’analyseur d’encre à limiter le nombre de résultats de reconnaissance possibles. Par exemple, vous pouvez affiner la portée en définissant Factoids et les mots attendus ou en structurant votre entrée dans un guide de reconnaissance. Pour plus d’informations sur la fourniture de contexte à l’analyseur d’encre, consultez :

-   [**IInkAnalyzer :: CreateAnalysisHint, méthode**](iinkanalyzer-createanalysishint.md)
-   [**IInkAnalyzer ::D méthode eleteAnalysisHint**](iinkanalyzer-deleteanalysishint.md)
-   [**IInkAnalyzer :: GetAnalysisHints, méthode**](iinkanalyzer-getanalysishints.md)
-   [**IInkAnalyzer :: GetAnalysisHintsByName, méthode**](iinkanalyzer-getanalysishintsbyname.md)

L’analyseur d’encres représente les résultats d’analyse sous la forme d’une chaîne ou sous la forme d’une arborescence d’objets [**IContextNode**](icontextnode.md) . Pour accéder à la chaîne reconnue, utilisez la [**méthode IInkAnalyzer :: GetRecognizedString**](iinkanalyzer-getrecognizedstring.md). Pour accéder à la racine de l’arborescence du nœud de contexte, utilisez la [**méthode IInkAnalyzer :: GetRootNode**](iinkanalyzer-getrootnode.md). L’analyseur d’encre présente les méthodes suivantes pour rechercher des nœuds de contexte ou du texte spécifiques.

-   [**IInkAnalyzer :: FindInkLeafNodes, méthode**](iinkanalyzer-findinkleafnodes.md)
-   [**IInkAnalyzer :: FindInkLeafNodesForStrokes, méthode**](iinkanalyzer-findinkleafnodesforstrokes.md)
-   [**IInkAnalyzer :: FindLeafNodes, méthode**](iinkanalyzer-findleafnodes.md)
-   [**IInkAnalyzer :: FindNode, méthode**](iinkanalyzer-findnode.md)
-   [**IInkAnalyzer :: FindNodesOfType, méthode**](iinkanalyzer-findnodesoftype.md)
-   [**IInkAnalyzer :: FindNodesOfTypeForStrokes, méthode**](iinkanalyzer-findnodesoftypeforstrokes.md)
-   [**IInkAnalyzer :: FindNodesOfTypeInSubTree, méthode**](iinkanalyzer-findnodesoftypeinsubtree.md)
-   [**IInkAnalyzer :: FindNodesWithCallBack, méthode**](iinkanalyzer-findnodeswithcallback.md)
-   [**IInkAnalyzer :: FindNodesWithCallBackInSubTree, méthode**](iinkanalyzer-findnodeswithcallbackinsubtree.md)

Pour utiliser d’autres résultats d’analyse, utilisez l’une des méthodes suivantes.

-   [**IInkAnalyzer :: GetAlternates, méthode**](iinkanalyzer-getalternates.md)
-   [**IInkAnalyzer :: GetAlternatesForContextNodes, méthode**](iinkanalyzer-getalternatesforcontextnodes.md)
-   [**IInkAnalyzer :: GetAlternatesForStrokes, méthode**](iinkanalyzer-getalternatesforstrokes.md)
-   [**IInkAnalyzer :: ModifyTopAlternate, méthode**](iinkanalyzer-modifytopalternate.md)
-   [**IInkAnalyzer :: ModifyTopAlternateWithConfirmation, méthode**](iinkanalyzer-modifytopalternatewithconfirmation.md)

Pour enregistrer les résultats de l’analyse, utilisez l’une des méthodes suivantes.

-   [**IInkAnalyzer :: SaveResults, méthode**](iinkanalyzer-saveresults.md)
-   [**IInkAnalyzer :: SaveResultsForNodes, méthode**](iinkanalyzer-saveresultsfornodes.md)
-   [**IInkAnalyzer :: SaveResultsForStrokes, méthode**](iinkanalyzer-saveresultsforstrokes.md)

Pour charger les résultats enregistrés, utilisez la [**méthode IInkAnalyzer :: LoadResults**](iinkanalyzer-loadresults.md).

Pour plus d’informations sur l’utilisation de **IInkAnalyzer** pour analyser l’encre, consultez [vue d’ensemble](ink-analysis-overview.md)de l’analyse de l’encre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

