---
description: Récupère les propriétés d’ID pour les objets IInkStrokeDisp du mot, de la ligne, du paragraphe ou du dessin correspondants, déterminés par l’analyse de l’encre.
ms.assetid: f05ffa3b-2a47-46fe-bb8f-e682aa094b69
title: CallDivideResultsStrokeIds fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResultsStrokeIds
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: ee690c9564df3b8c75eca6eec8eeb88b7531f4ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294054"
---
# <a name="calldivideresultsstrokeids-function"></a>CallDivideResultsStrokeIds fonction)

Récupère les propriétés d' [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) pour les objets [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) du mot, de la ligne, du paragraphe ou du dessin correspondants, déterminés par l’analyse de l’encre.

Cette fonction n’est pas destinée à être utilisée par le code d’application.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI CallDivideResultsStrokeIds(
  _In_  INT_PTR hDivider,
  _Out_ int     aWordStrokeIds[],
  _Out_ int     aLineStrokeIds[],
  _Out_ int     aParagraphStrokeIds[],
  _Out_ int     aDrawingStrokeIds[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDivider* \[ dans\]
</dt> <dd>

Handle de l’objet de [séparateur](the-divider-object.md) .

</dd> <dt>

*\[ aWordStrokeIds \]* en \[ sortie\]
</dt> <dd>

Tableau des ID de trait de l’encre dans le mot.

</dd> <dt>

*\[ aLineStrokeIds \]* en \[ sortie\]
</dt> <dd>

Tableau des ID de trait de l’encre dans la ligne.

</dd> <dt>

*\[ aParagraphStrokeIds \]* en \[ sortie\]
</dt> <dd>

Tableau des ID de trait de l’encre dans le paragraphe.

</dd> <dt>

*\[ aDrawingStrokeIds \]* en \[ sortie\]
</dt> <dd>

Tableau des ID de trait de l’encre dans le dessin.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette fonction peut retourner l’une de ces valeurs.



| Code de retour                                                                                  | Description                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | La fonction a réussi.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Le paramètre *hDivider* n’est pas valide.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                             |
| Bibliothèque<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




