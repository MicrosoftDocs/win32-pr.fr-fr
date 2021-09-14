---
description: Spécifie le repère ou la zone où l’encre est dessinée et reconnue.
ms.assetid: 5bd874ff-003b-4471-b4ef-50731007dc5a
title: InkAnalysisRecognizerGuide, structure (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalysisRecognizerGuide
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: eab5b1d09354f021f2c0a7e66a41b53e761d51e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127220092"
---
# <a name="inkanalysisrecognizerguide-structure"></a>InkAnalysisRecognizerGuide, structure

Spécifie le repère ou la zone où l’encre est dessinée et reconnue.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct InkAnalysisRecognizerGuide {
  RECT rectWritingBox;
  RECT rectDrawnBox;
  long cRows;
  long cColumns;
  long midline;
} InkAnalysisRecognizerGuide;
```



## <a name="members"></a>Membres

<dl> <dt>

**rectWritingBox**
</dt> <dd>

Zone d’écriture invisible du Guide de reconnaissance dans laquelle l’écriture peut réellement avoir lieu.

</dd> <dt>

**rectDrawnBox**
</dt> <dd>

Rectangle qui est dessiné sur l’écran du Tablet PC et dans lequel l’écriture a lieu.

</dd> <dt>

**cRows**
</dt> <dd>

Nombre de lignes dans la zone Guide de reconnaissance.

</dd> <dt>

**cColumns**
</dt> <dd>

Nombre de colonnes dans la zone Guide de reconnaissance.

</dd> <dt>

**médian**
</dt> <dd>

Hauteur de la médiane de la boîte du Guide de reconnaissance. La hauteur de la ligne médiane est la distance entre la ligne de base et la ligne médiane de la zone dessinée.

</dd> </dl>

## <a name="remarks"></a>Notes

Un **InkAnalysisRecognizerGuide** définit une zone d’entrée attendue, par exemple une ligne ou des zones, pour les caractères. Une structure **InkAnalysisRecognizerGuide** peut être définie uniquement sur un nœud de contexte d’indicateur d’analyse (consultez [**IContextNode :: GetType**](icontextnode-gettype.md)). Le [**IInkAnalyzer**](iinkanalyzer.md) utilise l’emplacement du nœud de l’indicateur d’analyse et les emplacements des traits d’encre pour associer un trait au nœud de l’indicateur d’analyse. Tout trait avec une association au nœud de l’indicateur d’analyse aura le **InkAnalysisRecognizerGuide** spécifié utilisé lorsqu’il est reconnu par un **IInkAnalyzer**, à condition que le **IInkAnalyzer** prenne en charge **InkAnalysisRecognizerGuide**. Les valeurs exprimées dans la classe **InkAnalysisRecognizerGuide** sont toujours relatives à l’emplacement du nœud d’indicateur d’analyse et sont spécifiées dans les coordonnées de l’espace d’encre.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de l’indicateur d’analyse](analysis-hint-properties.md)
</dt> <dt>

[**IInkAnalyzer :: CreateAnalysisHint, méthode**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




