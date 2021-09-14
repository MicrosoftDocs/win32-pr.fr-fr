---
description: Se produit lorsque la classe InkRecognizerContext a généré des résultats après l’appel de la méthode de méthode BackgroundRecognizeWithAlternates.
ms.assetid: 5e86a4d5-c0a7-4283-81cc-ec3a26f74880
title: Événement InkRecognizerContext. RecognitionWithAlternates (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a7d35d8281305b0cb5f84114bb2f2fa0e718c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196267"
---
# <a name="inkrecognizercontextrecognitionwithalternates-event"></a>Événement InkRecognizerContext. RecognitionWithAlternates

Se produit lorsque la [**classe InkRecognizerContext**](inkrecognizercontext-class.md) a généré des résultats après l’appel de la méthode de [**méthode BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) .

## <a name="syntax"></a>Syntaxe


```C++
void RecognitionWithAlternates(
  [in] IInkRecognitionResult *RecognitionResult,
  [in] VARIANT               CustomData,
  [in] InkRecognitionStatus  RecognitionStatus
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RecognitionResult* \[ dans\]
</dt> <dd>

Résultat de la reconnaissance de l’événement.

</dd> <dt>

*CustomData* \[ dans\]
</dt> <dd>

Données personnalisées pour le résultat de la reconnaissance.

Pour plus d’informations sur la structure de la variante, consultez [utilisation de la bibliothèque com](using-the-com-library.md).

</dd> <dt>

*RecognitionStatus* \[ dans\]
</dt> <dd>

État de reconnaissance en tant que résultat de reconnaissance le plus récent.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le comportement de l’interface de programmation d’applications (API) est imprévisible si vous essayez d’accéder à l’objet [**InkRecognizerContext**](inkrecognizercontext-class.md) d’origine à partir du gestionnaire d’événements de reconnaissance. N’essayez pas de le faire. Au lieu de cela, si vous avez besoin de le faire, créez un indicateur et définissez-le dans le gestionnaire d’événements de [**reconnaissance**](inkrecognizercontext-recognition.md) . Vous pouvez ensuite interroger cet indicateur pour déterminer quand modifier les propriétés de **InkRecognizerContext** en dehors du gestionnaire d’événements.

Cette méthode d’événement est définie dans l' \_ interface IInkEvents. L' \_ interface IInkEvents implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IRERecognitionWithAlternates.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**InkRecognizerContext, classe**](inkrecognizercontext-class.md)
</dt> <dt>

[**Méthode BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)
</dt> <dt>

[**Recognize, méthode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[**Interface IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

