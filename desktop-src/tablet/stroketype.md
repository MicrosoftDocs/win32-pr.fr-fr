---
description: Indique si un trait doit être analysé dans le cadre d’un dessin ou dans le cadre de l’écriture.
ms.assetid: 3f4c4522-ada7-4759-bca7-88b2a71f36ea
title: Énumération StrokeType (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrokeType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 3b59be130c6c7055bb7636760451dcadf5acf841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204038"
---
# <a name="stroketype-enumeration"></a>Énumération StrokeType

Indique si un trait doit être analysé dans le cadre d’un dessin ou dans le cadre de l’écriture.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum StrokeType { 
  StrokeType_Unclassified  = 0,
  StrokeType_Writing       = 1,
  StrokeType_Drawing       = 2
} StrokeType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="StrokeType_Unclassified"></span><span id="stroketype_unclassified"></span><span id="STROKETYPE_UNCLASSIFIED"></span>**StrokeType non \_ classé**
</dt> <dd>

Le trait peut faire partie d’un dessin ou d’une partie de l’écriture.

</dd> <dt>

<span id="StrokeType_Writing"></span><span id="stroketype_writing"></span><span id="STROKETYPE_WRITING"></span>**\_Écriture StrokeType**
</dt> <dd>

Le trait fait partie de l’écriture.

</dd> <dt>

<span id="StrokeType_Drawing"></span><span id="stroketype_drawing"></span><span id="STROKETYPE_DRAWING"></span>**\_Dessin StrokeType**
</dt> <dd>

Le trait fait partie d’un dessin.

</dd> </dl>

## <a name="examples"></a>Exemples

L’exemple suivant montre une partie d’un gestionnaire d’événements Stroke, implémentée de façon similaire à l' [exemple de récepteurs d’événements C++](c---event-sinks-sample.md). Le trait ajouté est vérifié pour voir si le haut de son cadre englobant a été dessiné sous une marge, `drawingMargin` . Dans ce cas, l’objet [**IInkAnalyzer**](iinkanalyzer.md) , `m_spInkAnalyzer` , est défini pour analyser le trait comme un trait de dessin, plutôt que comme un trait d’écriture manuscrite. `CheckHResult` est une fonction qui accepte un `HRESULT` et une chaîne, et lève une exception créée avec la chaîne si le `HRESULT` n’a pas **réussi**.


```C++
IInkRectangle* bounds;
CheckHResult(pStroke->GetBoundingBox(IBBM_Default, &bounds), "IInkStrokeDisp::GetBoundingBox failed");
long top;
CheckHResult(bounds->get_Top(&top), "IInkRectangle::get_Top failed");
if (top > drawingMargin)
{
    long strokeId;
    CheckHResult(pStroke->get_ID(&strokeId), "IInkStrokeDisp::get_ID failed");
    m_pInkAnalyzer->SetStrokeType(strokeId, StrokeType_Drawing);
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IInkAnalyzer :: SetStrokeType, méthode**](iinkanalyzer-setstroketype.md)
</dt> </dl>

 

 




