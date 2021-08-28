---
description: Ces constantes définissent des valeurs qui spécifient le type d’objets IContextNode.
ms.assetid: 333db79e-f503-4545-84fd-7c1a39a96728
title: Types de nœuds de contexte (Iaguid. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_CNT_ANALYSISHINT
- GUID_CNT_CUSTOMRECOGNIZER
- GUID_CNT_IMAGE
- GUID_CNT_INKBULLET
- GUID_CNT_INKDRAWING
- GUID_CNT_INKWORD
- GUID_CNT_LINE
- GUID_CNT_OBJECT
- GUID_CNT_PARAGRAPH
- GUID_CNT_ROOT
- GUID_CNT_TEXTWORD
- GUID_CNT_UNCLASSIFIEDINKNODE
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 2bb2064cc72b398d290fa78606b31bd37208535e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473885"
---
# <a name="context-node-types"></a>Types de nœuds de contexte

Ces constantes définissent des valeurs qui spécifient le type d’objets [**IContextNode**](icontextnode.md) .




| Constante/valeur | Description | 
|----------------|-------------|
| <span id="GUID_CNT_ANALYSISHINT"></span><span id="guid_cnt_analysishint"></span><dl><dt><strong>GUID_CNT_ANALYSISHINT</strong></dt><dt>(ANALYSISHINT)</dt></dl> | Représente un nœud qui contient des informations de contexte supplémentaires pour une région que le <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> utilise pour améliorer son analyse.<br /> | 
| <span id="GUID_CNT_CUSTOMRECOGNIZER"></span><span id="guid_cnt_customrecognizer"></span><dl><dt><strong>GUID_CNT_CUSTOMRECOGNIZER</strong></dt><dt>(CUSTOMRECOGNIZER)</dt></dl> | Représente un nœud utilisé pour une opération de reconnaissance unique.<br /> Tous les traits et les nœuds qui se trouvent dans un nœud de reconnaissance personnalisé sont reconnus par une opération de reconnaissance indépendante et ne sont pas analysés par le <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a>.<br /> Un nœud de reconnaissance personnalisé doit être l’enfant direct du nœud racine de l’analyseur d’encre.<br /> Un nœud de reconnaissance personnalisé peut contenir les types d’éléments enfants suivants :<br /><ul><li>N’importe quel nombre de nœuds UnclassifiedInk.</li><li>N’importe quel nombre de nœuds d’objet.</li><li>N’importe quel nombre de nœuds de ligne.</li><li>N’importe quel nombre de nœuds InkWord.</li><li>N’importe quel nombre de nœuds avec une valeur Guid inconnue.</li></ul> | 
| <span id="GUID_CNT_IMAGE"></span><span id="guid_cnt_image"></span><dl><dt><strong>GUID_CNT_IMAGE</strong></dt><dt>(image)</dt></dl> | Représente un nœud pour une région à deux dimensions où des images non manuscrites peuvent exister dans le document.<br /> <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> ne produit pas de nœuds d’image. Utilisez <a href="icontextnode-createsubnode.md"><strong>IContextNode :: CreateSubNode</strong></a> pour ajouter un nœud d’image à l’arborescence du nœud de contexte. Le <strong>IInkAnalyzer</strong> utilise ensuite les régions définies par le nœud image pour déterminer si une encre annote l’image non manuscrite.<br /> Un nœud d’image ne peut pas avoir d’éléments enfants.<br /> | 
| <span id="GUID_CNT_INKBULLET"></span><span id="guid_cnt_inkbullet"></span><dl><dt><strong>GUID_CNT_INKBULLET</strong></dt><dt>(INKBULLET)</dt></dl> | Le ContextNodeType InkBullet représente une collection de traits qui composent une puce dans une liste à puces.<br /> Un ContextNode de type InkBullet ne peut pas avoir d’enfants. Il peut uniquement être un enfant d’un paragraphe ContextNode. Un seul InkBullet peut apparaître dans un ContextNode de paragraphe unique.<br /> | 
| <span id="GUID_CNT_INKDRAWING"></span><span id="guid_cnt_inkdrawing"></span><dl><dt><strong>GUID_CNT_INKDRAWING</strong></dt><dt>(INKDRAWING)</dt></dl> | Représente un nœud pour une collection de traits qui constitue un dessin.<br /> Les dessins sont des traits qui sont déterminés comme étant des formes ou des croquis abstraits. Il s’agit généralement de traits qui ne sont pas classés comme traits d’écriture.<br /> Un nœud de dessin d’encre ne peut pas avoir d’éléments enfants.<br /> | 
| <span id="GUID_CNT_INKWORD"></span><span id="guid_cnt_inkword"></span><dl><dt><strong>GUID_CNT_INKWORD</strong></dt><dt>(INKWORD)</dt></dl> | Représente un nœud pour une collection de traits qui constitue un regroupement logique pour former un mot reconnaissable.<br /> Un nœud de mot Ink ne peut pas contenir d’éléments enfants.<br /> | 
| <span id="GUID_CNT_LINE"></span><span id="guid_cnt_line"></span><dl><dt><strong>GUID_CNT_LINE</strong></dt><dt>(ligne)</dt></dl> | Représente un nœud pour une ligne de mots.<br /> Un nœud de ligne peut contenir les types d’éléments enfants suivants :<br /><ul><li>N’importe quel nombre de nœuds de mots manuscrits.</li><li>Un nombre quelconque de nœuds de mots de texte.</li><li>N’importe quel nombre de nœuds avec une valeur <strong>GUID</strong> inconnue.</li></ul> | 
| <span id="GUID_CNT_OBJECT"></span><span id="guid_cnt_object"></span><dl><dt><strong>GUID_CNT_OBJECT</strong></dt><dt>(objet)</dt></dl> | Représente un nœud pour un objet retourné à partir d’un module de reconnaissance personnalisé « Object ».<br /> Un nœud d’objet ne peut pas contenir d’éléments enfants.<br /> Seuls les nœuds de reconnaissance personnalisés peuvent contenir des nœuds d’objet.<br /> | 
| <span id="GUID_CNT_PARAGRAPH"></span><span id="guid_cnt_paragraph"></span><dl><dt><strong>GUID_CNT_PARAGRAPH</strong></dt><dt>(paragraphe)</dt></dl> | Représente un nœud pour une collection de nœuds qui constitue un regroupement logique de lignes.<br /> La définition exacte d’un paragraphe est déterminée par les moteurs d’analyse. En général, un paragraphe contient des groupes de lignes qui sont redistribuées ensemble si la zone qui contient les lignes a été redimensionnée.<br /> Un nœud de paragraphe peut contenir les types d’éléments enfants suivants :<br /><ul><li>N’importe quel nombre de nœuds de puces manuscrits.</li><li>N’importe quel nombre de nœuds de ligne.</li><li>N’importe quel nombre de nœuds avec une valeur <strong>GUID</strong> inconnue.</li></ul> | 
| <span id="GUID_CNT_ROOT"></span><span id="guid_cnt_root"></span><dl><dt><strong>GUID_CNT_ROOT</strong></dt><dt>(racine)</dt></dl> | Représente un nœud pour le nœud supérieur d’une arborescence de nœuds qui décrivent les résultats de l’analyse de l’encre.<br /> Les nœuds racine sont généralement obtenus à partir de la méthode de <a href="iinkanalyzer-getrootnode.md"><strong>méthode IInkAnalyzer :: GetRootNode</strong></a> .<br /> Un nœud racine peut contenir les types d’éléments enfants suivants :<br /><ul><li>Un nombre quelconque de nœuds d’indicateurs d’analyse.</li><li>N’importe quel nombre de nœuds de reconnaissance personnalisés.</li><li>N’importe quel nombre de nœuds image.</li><li>N’importe quel nombre de nœuds de dessin de l’encre.</li><li>N’importe quel nombre de nœuds de région d’écriture.</li><li>N’importe quel nombre de nœuds d’encre non classifiés.</li><li>N’importe quel nombre de nœuds avec une valeur <strong>GUID</strong> inconnue.</li></ul> | 
| <span id="GUID_CNT_TEXTWORD"></span><span id="guid_cnt_textword"></span><dl><dt><strong>GUID_CNT_TEXTWORD</strong></dt><dt>(TEXTWORD)</dt></dl> | Représente un nœud pour la région à deux dimensions où tout texte non manuscrit peut exister dans le document.<br /> <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> ne produit pas de nœuds de mots de texte. Utilisez <a href="icontextnode-createsubnode.md"><strong>IContextNode :: CreateSubNode</strong></a> pour ajouter un nœud de mot de texte à l’arborescence du nœud de contexte. Le <strong>IInkAnalyzer</strong> utilise ensuite les régions définies par le nœud mot de texte pour déterminer si une encre annote le texte non manuscrit.<br /> Les futurs reconnaisseurs peuvent utiliser la région définie par un nœud de mot de texte pour déterminer si une encre annote le mot non manuscrit.<br /> Un nœud de mot de texte ne peut pas avoir d’éléments enfants<br /> | 
| <span id="GUID_CNT_UNCLASSIFIEDINKNODE"></span><span id="guid_cnt_unclassifiedinknode"></span><dl><dt><strong>GUID_CNT_UNCLASSIFIEDINKNODE</strong></dt><dt>(UnclassifiedInk)</dt></dl> | Représente un nœud pour tous les traits qui n’ont pas encore été classifiés ou reconnus.<br /> Un nœud d’encre non classifié ne peut pas avoir d’éléments enfants.<br /> | 




## <a name="remarks"></a>Remarques

Pour plus d’informations sur les différents types de nœuds de contexte, consultez [vue d’ensemble de l’analyse d’encre](ink-analysis-overview.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Iaguid. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IContextNode::CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**IContextNode::CreateSubNode**](icontextnode-createsubnode.md)
</dt> <dt>

[**IContextNode :: GetType**](icontextnode-gettype.md)
</dt> <dt>

[**IInkAnalyzer :: CreateAnalysisHint, méthode**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**IInkAnalyzer :: CreateCustomRecognizer, méthode**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[**IInkAnalyzer :: FindNodesOfType, méthode**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**IInkAnalyzer :: FindNodesOfTypeForStrokes, méthode**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**IInkAnalyzer :: FindNodesOfTypeInSubTree, méthode**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




