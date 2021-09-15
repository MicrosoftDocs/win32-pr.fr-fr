---
description: Teste si l’objet InkDivider peut utiliser la classe InkRecognizerContext pour analyser des mots.
ms.assetid: fd848fcc-5258-401f-8b51-b9d57da173da
title: RecognizerContextSet fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognizerContextSet
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 51e75b810c2103afed2e8ac8a28706b9c9af5da0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411439"
---
# <a name="recognizercontextset-function"></a>RecognizerContextSet fonction)

Teste si l’objet [**InkDivider**](inkdivider-class.md) peut utiliser la classe [**InkRecognizerContext**](inkrecognizercontext-class.md) pour analyser des mots.

Cette fonction n’est pas destinée à être utilisée par le code d’application.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI RecognizerContextSet(
  _In_ INT_PTR hDivider
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDivider* \[ dans\]
</dt> <dd>

Handle de l’objet [**InkDivider**](inkdivider-class.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette fonction peut retourner l’une de ces valeurs.



| Code de retour                                                                                  | Description                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | La fonction a réussi.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Le paramètre *pDivider* n’est pas valide.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                             |
| Bibliothèque<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




