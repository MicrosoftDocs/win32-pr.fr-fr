---
description: Définit la propriété LineHeight sur l’objet InkDivider.
ms.assetid: ce5e40c5-faa1-4d66-94f4-d5bd1a11ee4c
title: SetLineHeight fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetLineHeight
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: be4045e01ac890471536d95768668b633d8f2249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520629"
---
# <a name="setlineheight-function"></a>SetLineHeight fonction)

Définit la propriété [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) sur l’objet [**InkDivider**](inkdivider-class.md) .

Cette fonction d’assistance n’est pas destinée à être utilisée par le code d’application.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI SetLineHeight(
  _In_ INT_PTR hDivider,
  _In_ LONG    lLineHeight
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDivider* \[ dans\]
</dt> <dd>

Handle de l’objet [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*lLineHeight* \[ dans\]
</dt> <dd>

La propriété [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) de l’objet [**InkDivider**](inkdivider-class.md) , en unités HIMETRIC.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction peut retourner l’une de ces valeurs.



| Code de retour                                                                                  | Description                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | La fonction a réussi.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Le paramètre *pDivider* n’est pas valide.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                             |
| Bibliothèque<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 
