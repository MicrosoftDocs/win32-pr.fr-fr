---
description: Définit des identificateurs globaux uniques (GUID) pour les propriétés d’un IContextNode.
ms.assetid: 14992253-c384-43c1-9465-e015ea2348db
title: Propriétés du nœud de contexte (Iaguid. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_CNP_ALIGNMENTLEVEL
- GUID_CNP_ASCENDERS
- GUID_CNP_BASELINE
- GUID_CNP_CONFIDENCELEVEL
- GUID_CNP_CUSTOMRECOGNIZERID
- GUID_CNP_DESCENDERS
- GUID_CNP_MIDLINE
- GUID_CNP_NODEDATA
- GUID_CNP_RECOGNIZEDSTRING
- GUID_CNP_ROTATEDBOUNDINGBOX
- GUID_CNP_SEMANTICTYPE
- GUID_CNP_SHAPENAME
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 8eb1034516c62e2121f835951d1f04db5710d275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861770"
---
# <a name="context-node-properties"></a>Propriétés du nœud de contexte

Définit des identificateurs globaux uniques (GUID) pour les propriétés d’un [**IContextNode**](icontextnode.md).

Le tableau suivant décrit les informations référencées par chaque constante.



| Constante                                                                                                                                                                                                 | Description                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_CNP_ALIGNMENTLEVEL"></span><span id="guid_cnp_alignmentlevel"></span><dl> <dt>**GUID \_ CNP \_ ALIGNMENTLEVEL**</dt> </dl>             | Niveau d’alignement d’un paragraphe.<br/>                                                                                                               |
| <span id="GUID_CNP_ASCENDERS"></span><span id="guid_cnp_ascenders"></span><dl> <dt>**GUID \_ CNP \_ ascendants**</dt> </dl>                            | Hampes supérieures d’un mot d’encre.<br/>                                                                                                                     |
| <span id="GUID_CNP_BASELINE"></span><span id="guid_cnp_baseline"></span><dl> <dt>**\_ligne de \_ base GUID CNP**</dt> </dl>                               | Ligne de base d’un mot encre.<br/>                                                                                                                      |
| <span id="GUID_CNP_CONFIDENCELEVEL"></span><span id="guid_cnp_confidencelevel"></span><dl> <dt>**GUID \_ CNP \_ CONFIDENCELEVEL**</dt> </dl>          | Niveau de confiance dans les résultats de la reconnaissance.<br/>                                                                                                  |
| <span id="GUID_CNP_CUSTOMRECOGNIZERID"></span><span id="guid_cnp_customrecognizerid"></span><dl> <dt>**GUID \_ CNP \_ CUSTOMRECOGNIZERID**</dt> </dl> | Identificateur du module de reconnaissance d’encre personnalisé pour un nœud de reconnaissance personnalisé.<br/>                                                                         |
| <span id="GUID_CNP_DESCENDERS"></span><span id="guid_cnp_descenders"></span><dl> <dt>**GUID \_ CNP les \_ descendants**</dt> </dl>                         | Descendants d’un mot d’encre.<br/>                                                                                                                    |
| <span id="GUID_CNP_MIDLINE"></span><span id="guid_cnp_midline"></span><dl> <dt>**GUID \_ CNP- \_ média**</dt> </dl>                                  | La médiane d’un mot manuscrit.<br/>                                                                                                                       |
| <span id="GUID_CNP_NODEDATA"></span><span id="guid_cnp_nodedata"></span><dl> <dt>**GUID \_ CNP \_ NODEDATA**</dt> </dl>                               | Données d’image ou données texte d’une image ou d’un mot de texte.<br/>                                                                                           |
| <span id="GUID_CNP_RECOGNIZEDSTRING"></span><span id="guid_cnp_recognizedstring"></span><dl> <dt>**GUID \_ CNP \_ RECOGNIZEDSTRING**</dt> </dl>       | Chaîne reconnue.<br/>                                                                                                                            |
| <span id="GUID_CNP_ROTATEDBOUNDINGBOX"></span><span id="guid_cnp_rotatedboundingbox"></span><dl> <dt>**GUID \_ CNP \_ ROTATEDBOUNDINGBOX**</dt> </dl> | Rectangle englobant pivoté.<br/>                                                                                                                         |
| <span id="GUID_CNP_SEMANTICTYPE"></span><span id="guid_cnp_semantictype"></span><dl> <dt>**GUID \_ CNP \_ SEMANTICTYPE**</dt> </dl>                   | La propriété contient des informations sur les types sémantiques utilisés pour la définition d’une annotation, par exemple s’il s’agit d’une légende, d’un commentaire, etc.<br/> |
| <span id="GUID_CNP_SHAPENAME"></span><span id="guid_cnp_shapename"></span><dl> <dt>**GUID \_ CNP \_ SHAPENAME**</dt> </dl>                            | Nom de forme d’un nœud de dessin d’encre.<br/>                                                                                                            |



## <a name="remarks"></a>Notes

Ces GUID sont utilisés pour identifier les propriétés que [**IInkAnalyzer**](iinkanalyzer.md) peut définir sur un [**IContextNode**](icontextnode.md). L’analyseur d’encre définit des données de propriété basées sur le type du nœud de contexte (consultez [**IContextNode :: GetType**](icontextnode-gettype.md)).

Pour obtenir ou définir des propriétés spécifiques aux nœuds d’indicateurs d’analyse, consultez Propriétés de l' [**indicateur d’analyse**](analysis-hint-properties.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Iaguid. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de l’indicateur d’analyse](analysis-hint-properties.md)
</dt> <dt>

[Types de nœuds de contexte](context-node-types.md)
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

 

 




