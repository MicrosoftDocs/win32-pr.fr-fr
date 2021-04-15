---
description: Récupère des informations d’analyse à partir de l’objet InkDivider.
ms.assetid: 1b073da4-80f4-48f4-8ff6-b21793c173a8
title: CallDivide fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivide
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 0084811ee471bee8fe67653dace49fa83642a7fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524404"
---
# <a name="calldivide-function"></a>CallDivide fonction)

Récupère des informations d’analyse à partir de l’objet [**InkDivider**](inkdivider-class.md) .

Cette fonction n’est pas destinée à être utilisée par le code d’application.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI CallDivide(
  _In_  INT_PTR hDivider,
  _In_  int     *pWordSize,
  _In_  int     *pLineSize,
  _In_  int     *pParagraphSize,
  _In_  int     *pDrawingSize,
  _Out_ int     *pWordCount,
  _Out_ int     *pLineCount,
  _Out_ int     *pParagraphCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDivider* \[ dans\]
</dt> <dd>

Handle de l’objet [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*pWordSize* \[ dans\]
</dt> <dd>

Taille du mot retourné par l’objet [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*pLineSize* \[ dans\]
</dt> <dd>

Taille de la ligne retournée par l’objet [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*pParagraphSize* \[ dans\]
</dt> <dd>

Taille du paragraphe retourné par l’objet [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*pDrawingSize* \[ dans\]
</dt> <dd>

Taille du dessin retourné par l’objet [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*pWordCount* \[ à\]
</dt> <dd>

Nombre de mots retournés par l’analyse de l’encre.

</dd> <dt>

*pLineCount* \[ à\]
</dt> <dd>

Nombre de lignes retournées par l’analyse de l’encre.

</dd> <dt>

*pParagraphCount* \[ à\]
</dt> <dd>

Nombre de paragraphes renvoyés par l’analyse de l’encre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction peut retourner l’une de ces valeurs.



| Code de retour                                                                                  | Description                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | La fonction a réussi.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Un ou plusieurs paramètres ne sont pas valides.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                             |
| Bibliothèque<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




