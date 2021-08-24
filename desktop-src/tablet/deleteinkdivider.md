---
description: Supprime un objet InkDivider et libère les ressources associées.
ms.assetid: adf772e0-2829-4410-83c4-45a24bf3a848
title: DeleteInkDivider fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteInkDivider
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 526186dd2a867f8fb3ee9201ca13df6afd43cb02f8361da202a036dde8e9fb56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709519"
---
# <a name="deleteinkdivider-function"></a>DeleteInkDivider fonction)

Supprime un objet [**InkDivider**](inkdivider-class.md) et libère les ressources associées.

Cette fonction n’est pas destinée à être utilisée par le code d’application.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI DeleteInkDivider(
  _In_ INT_PTR hDivider
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDivider* \[ dans\]
</dt> <dd>

Handle de l’objet [**InkDivider**](inkdivider-class.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction peut retourner l’une de ces valeurs.



| Code de retour                                                                                  | Description                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | S_OK<br/>                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Le paramètre *hDivider* n’est pas valide.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                             |
| Bibliothèque<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




