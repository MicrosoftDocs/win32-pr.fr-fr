---
description: Obsolète. Le PenInputPanel a été remplacé par le panneau de saisie de texte (TIP). Se produit lorsque le focus d’entrée est modifié avant que l’objet PenInputPanel ait pu insérer une entrée d’utilisateur dans le contrôle attaché.
ms.assetid: a5928f78-29d6-40e8-8f87-17c188e51ba9
title: Événement PenInputPanel. InputFailed (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cc3234c73fc8ba47faa7d1f2ec89477a1bfb86b7c2abda263aff227c5961f1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934759"
---
# <a name="peninputpanelinputfailed-event"></a>Événement PenInputPanel. InputFailed

Action déconseillée. Le [**PenInputPanel**](peninputpanel-class.md) a été remplacé par le [panneau de saisie de texte (TIP)](text-input-panel-reference.md).

Se produit lorsque le focus d’entrée est modifié avant que l’objet [**PenInputPanel**](peninputpanel-class.md) ait pu insérer une entrée d’utilisateur dans le contrôle attaché.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT InputFailed(
  [in] long  hWnd,
  [in] long  Key,
  [in] BSTR  Text,
  [in] short ShiftKey
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* \[ dans\]
</dt> <dd>

Handle de fenêtre du contrôle qui a appelé l’objet [**PenInputPanel**](peninputpanel-class.md) .

</dd> <dt>

*Clé* \[ dans\]
</dt> <dd>

Touche virtuelle correspondant à la touche enfoncée.

</dd> <dt>

*Texte* \[ dans\]
</dt> <dd>

Chaîne qui doit être insérée dans le contrôle représenté par le paramètre *HWND* lorsque l’événement **InputFailed** a été déclenché.

Pour plus d’informations sur le type de données BSTR, consultez [utilisation de la bibliothèque com](using-the-com-library.md).

</dd> <dt>

*ShiftKey* \[ dans\]
</dt> <dd>

État des modificateurs de clavier, y compris les touches Maj, Maj, CTRL et ALT.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cet événement a la valeur, il retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

L’événement **InputFailed** se produit lorsque le focus d’entrée est modifié avant l’insertion de l’entrée utilisateur dans le contrôle attaché. Par exemple, si l’utilisateur entre de l’encre dans le bloc d’écriture, puis appuie sur un autre contrôle d’édition avant que le module de reconnaissance ait pu terminer, cet événement se déclenche.

À l’aide du handle de fenêtre passé dans cet événement, vous pouvez choisir d’insérer le texte vous-même lorsque cet événement se produit.

> [!Note]  
> à compter de Microsoft Windows XP édition Tablet PC 2005, l’événement **InputFailed** ne s’applique plus. Le texte est toujours inséré avant la modification du focus.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PenInputPanel**](peninputpanel-class.md)
</dt> </dl>

 

 




