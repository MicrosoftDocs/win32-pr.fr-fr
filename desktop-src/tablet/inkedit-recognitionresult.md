---
description: 'Se produit lorsque le contrôle InkEdit obtient les résultats manuellement à partir d’un appel à la méthode InkEdit :: Recognize ou automatiquement après le déclenchement du délai d’attente de reconnaissance.'
ms.assetid: 09618be0-fe49-494f-940f-79ff8352097e
title: Événement InkEdit. RecognitionResult (. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37ef71d38be31f32c59919a9ce4f24fd90b2d188d86a26e81821f6f7987da31d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939079"
---
# <a name="inkeditrecognitionresult-event"></a>Événement InkEdit. RecognitionResult

Se produit lorsque le contrôle [InkEdit](inkedit-control-reference.md) obtient les résultats manuellement à partir d’un appel à la méthode [**InkEdit :: Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) ou automatiquement après le déclenchement du délai d’attente de reconnaissance.

## <a name="syntax"></a>Syntaxe


```C++
void RecognitionResult(
  [in] IInkRecognitionResult *RecognitionResult
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RecognitionResult* \[ dans\]
</dt> <dd>

Objet [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) qui contient le résultat de la reconnaissance.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode d’événement est définie dans l’interface **\_ IInkEditEvents** . L’interface **\_ IInkEditEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IeeRecognitionResult.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>« Y2. h » (nécessite également l' \_ entrée i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Recognize, méthode \[ contrôle InkEdit\]**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)
</dt> </dl>

 

