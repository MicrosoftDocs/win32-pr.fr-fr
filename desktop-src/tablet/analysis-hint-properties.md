---
description: 'Définit des identificateurs globaux uniques (GUID) pour les propriétés d’un nœud d’indicateur d’analyse (consultez IContextNode :: GetType).'
ms.assetid: 8300c792-a741-49de-a03b-f4840ea5d647
title: Propriétés de l’indicateur d’analyse (Iaguid. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AHP_ALLOWPARTIALDICTIONARYTERMS
- GUID_AHP_ANALYSISHINTNAME
- GUID_AHP_COERCETOFACTOID
- GUID_AHP_ENABLEDUNICODECHARACTERRANGES
- GUID_AHP_FACTOID
- GUID_AHP_GUIDE
- GUID_AHP_PREFIXTEXT
- GUID_AHP_SUFFIXTEXT
- GUID_AHP_TOPINKBREAKSONLY
- GUID_AHP_WORDLIST
- GUID_AHP_WORDMODE
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 8a7a25cfa94bb7f2354418ded2b35e3137364901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950886"
---
# <a name="analysis-hint-properties"></a>Propriétés de l’indicateur d’analyse

Définit des identificateurs globaux uniques (GUID) pour les propriétés d’un nœud d’indicateur d’analyse (consultez [**IContextNode :: GetType**](icontextnode-gettype.md)).

Le tableau suivant décrit les informations référencées par chaque constante.



| Constante                                                                                                                                                                                                                                  | Description                                                                                                                                               |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AHP_ALLOWPARTIALDICTIONARYTERMS"></span><span id="guid_ahp_allowpartialdictionaryterms"></span><dl> <dt>**GUID \_ AHP \_ ALLOWPARTIALDICTIONARYTERMS**</dt> </dl>       | Indique si les termes partiels du dictionnaire sont autorisés sur un indicateur d’analyse.<br/>                                                                              |
| <span id="GUID_AHP_ANALYSISHINTNAME"></span><span id="guid_ahp_analysishintname"></span><dl> <dt>**GUID \_ AHP \_ ANALYSISHINTNAME**</dt> </dl>                                        | Nom d’un indicateur d’analyse.<br/>                                                                                                                  |
| <span id="GUID_AHP_COERCETOFACTOID"></span><span id="guid_ahp_coercetofactoid"></span><dl> <dt>**GUID \_ AHP \_ COERCETOFACTOID**</dt> </dl>                                           | Indique si l’analyseur d’encre limite son analyse de l’encre dans la zone de l’indicateur pour se conformer au Factoid.<br/>                                          |
| <span id="GUID_AHP_ENABLEDUNICODECHARACTERRANGES"></span><span id="guid_ahp_enabledunicodecharacterranges"></span><dl> <dt>**GUID \_ AHP \_ ENABLEDUNICODECHARACTERRANGES**</dt> </dl> | L’indicateur contient un tableau de caractères qui représentent l’ensemble restreint de jeux de caractères Unicode pris en charge pris en charge par ce InkRecognizer.<br/> |
| <span id="GUID_AHP_FACTOID"></span><span id="guid_ahp_factoid"></span><dl> <dt>**GUID \_ AHP \_ FACTOID**</dt> </dl>                                                                   | Factoid sur un indicateur d’analyse.<br/>                                                                                                               |
| <span id="GUID_AHP_GUIDE"></span><span id="guid_ahp_guide"></span><dl> <dt>**\_Guide AHP \_ GUID**</dt> </dl>                                                                         | Structure [**InkAnalysisRecognizerGuide**](inkanalysisrecognizerguide.md) qui représente le repère d’un indicateur d’analyse.<br/>                 |
| <span id="GUID_AHP_PREFIXTEXT"></span><span id="guid_ahp_prefixtext"></span><dl> <dt>**GUID \_ AHP \_ PREFIXTEXT**</dt> </dl>                                                          | Texte de préfixe sur un indicateur d’analyse.<br/>                                                                                                           |
| <span id="GUID_AHP_SUFFIXTEXT"></span><span id="guid_ahp_suffixtext"></span><dl> <dt>**GUID \_ AHP \_ SUFFIXTEXT**</dt> </dl>                                                          | Texte de suffixe sur un indicateur d’analyse.<br/>                                                                                                           |
| <span id="GUID_AHP_TOPINKBREAKSONLY"></span><span id="guid_ahp_topinkbreaksonly"></span><dl> <dt>**GUID \_ AHP \_ TOPINKBREAKSONLY**</dt> </dl>                                        | Si les multiples segments dans les résultats de reconnaissance de l’encre sont désactivés.<br/>                                                                |
| <span id="GUID_AHP_WORDLIST"></span><span id="guid_ahp_wordlist"></span><dl> <dt>**AHP du GUID \_ \_**</dt> </dl>                                                                | Tableau de chaînes qui représente la liste de mots d’un indicateur d’analyse.<br/>                                                                       |
| <span id="GUID_AHP_WORDMODE"></span><span id="guid_ahp_wordmode"></span><dl> <dt>**GUID \_ AHP \_ WORDMODE**</dt> </dl>                                                                | Si l’analyseur d’encre établit une priorité pour les résultats à mots uniques sur les résultats à mots multiples pour un indicateur d’analyse.<br/>                                      |



## <a name="remarks"></a>Notes

Ces GUID sont utilisés pour identifier les propriétés que [**IInkAnalyzer**](iinkanalyzer.md) peut définir sur un nœud de contexte d’indicateur d’analyse (consultez [**IContextNode :: GetType**](icontextnode-gettype.md)).

Pour obtenir ou définir les propriétés d’un [**IContextNode**](icontextnode.md) en général, consultez [Propriétés du nœud de contexte](context-node-properties.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Iaguid. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés du nœud de contexte](context-node-properties.md)
</dt> <dt>

[Types de nœuds de contexte](context-node-types.md)
</dt> <dt>

[**IInkAnalyzer :: CreateAnalysisHint, méthode**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**IInkAnalyzer :: GetAnalysisHintsByName, méthode**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[**IContextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode::LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**IContextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




