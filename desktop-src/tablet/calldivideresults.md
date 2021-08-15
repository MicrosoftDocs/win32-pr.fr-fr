---
description: Récupère les résultats de l’analyse à partir de l’objet InkDivider.
ms.assetid: 7fc2bb5a-172f-4f4e-84dd-e31925f86982
title: CallDivideResults fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResults
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 2e5f3060f261ba84b70272ed358a7c544f2b0e1582de310ed759b4ea40714359
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967758"
---
# <a name="calldivideresults-function"></a>CallDivideResults fonction)

Récupère les résultats de l’analyse à partir de l’objet [**InkDivider**](inkdivider-class.md) .

Cette fonction n’est pas destinée à être utilisée par le code d’application.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI CallDivideResults(
  _In_  INT_PTR   hDivider,
  _Out_ int       aWordStrokeIds[],
  _Out_ int       aLineStrokeIds[],
  _Out_ int       aParagraphStrokeIds[],
  _Out_ int       aDrawingStrokeIds[],
  _Out_ SAFEARRAY **pastrWords,
  _Out_ SAFEARRAY **pastrLines,
  _Out_ SAFEARRAY **pastrParagraphs,
  _Out_ int       *aWordRotationCenterX,
  _Out_ int       *aWordRotationCenterY,
  _Out_ float     *aWordAngle,
  _Out_ int       *aLineRotationCenterX,
  _Out_ int       *aLineRotationCenterY,
  _Out_ float     *aLineAngle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDivider* \[ dans\]
</dt> <dd>

Handle de l’objet [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*aWordStrokeIds* \[ à\]
</dt> <dd>

Tableau d’identificateurs associés au mot passé à la classe [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*aLineStrokeIds* \[ à\]
</dt> <dd>

Tableau de propriétés d' [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) pour les objets [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) associés à la ligne passée à la classe [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*aParagraphStrokeIds* \[ à\]
</dt> <dd>

Tableau des propriétés d' [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) pour les objets [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) associés au paragraphe de la classe [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*aDrawingStrokeIds* \[ à\]
</dt> <dd>

Tableau de propriétés d' [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) pour les objets [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) associés au dessin à partir de la classe [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*pastrWords* \[ à\]
</dt> <dd>

Tableau de mots retournés par l’analyse de l’encre.

</dd> <dt>

*pastrLines* \[ à\]
</dt> <dd>

Tableau de lignes retournées par l’analyse de l’encre.

</dd> <dt>

*pastrParagraphs* \[ à\]
</dt> <dd>

Tableau de paragraphes renvoyés à partir de l’analyse de l’encre.

</dd> <dt>

*aWordRotationCenterX* \[ à\]
</dt> <dd>

Tableau des points centraux des mots le long de l’axe x à partir de l’analyse de l’encre.

</dd> <dt>

*aWordRotationCenterY* \[ à\]
</dt> <dd>

Tableau des points centraux des mots situés le long de l’axe des y à partir de l’analyse de l’encre.

</dd> <dt>

*aWordAngle* \[ à\]
</dt> <dd>

Tableau contenant les angles de rotation des mots pour obtenir les meilleurs résultats d’analyse.

</dd> <dt>

*aLineRotationCenterX* \[ à\]
</dt> <dd>

Tableau contenant les points centraux des lignes le long de l’axe x.

</dd> <dt>

*aLineRotationCenterY* \[ à\]
</dt> <dd>

Tableau contenant les points centraux des lignes le long de l’axe y.

</dd> <dt>

*aLineAngle* \[ à\]
</dt> <dd>

Tableau contenant les angles de rotation des lignes pour obtenir les meilleurs résultats d’analyse.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La fonction a réussi.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le paramètre *hDivider* n’est pas valide.<br/>                   |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Impossible d’allouer suffisamment de mémoire pour stocker les résultats.<br/> |



 

## <a name="remarks"></a>Remarques

Pour éviter les fuites de mémoire, vous devez libérer les ressources pour *pastrWords*, *pastrLines* et *pastrParagraphs*.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                             |
| Bibliothèque<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




