---
description: Se produit lorsque le InkRecognizerContext a généré des résultats de la méthode BackgroundRecognize.
ms.assetid: 0cc319af-cd0b-4089-928b-cae6c86f6f61
title: Événement InkRecognizerContext. Recognition (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f6c4799f3366003d14451a19a7bea19ea35aadcce9226f25f1fe80a14ab19e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966938"
---
# <a name="inkrecognizercontextrecognition-event"></a>Événement InkRecognizerContext. Recognition

Se produit lorsque le [**InkRecognizerContext**](inkrecognizercontext-class.md) a généré des résultats de la méthode [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) .

## <a name="syntax"></a>Syntaxe


```C++
void Recognition(
  [in] BSTR                 RecognizedString,
  [in] VARIANT              CustomData,
  [in] InkRecognitionStatus RecognitionStatus
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RecognizedString* \[ dans\]
</dt> <dd>

Texte de résultat de la reconnaissance avec la confiance la plus élevée.

Pour plus d’informations sur le type de données BSTR, consultez la page [utilisation de la bibliothèque com](using-the-com-library.md).

</dd> <dt>

*CustomData* \[ dans\]
</dt> <dd>

Objet qui contient les données personnalisées pour le résultat de la reconnaissance.

Pour plus d’informations sur la structure de la variante, consultez [utilisation de la bibliothèque com](using-the-com-library.md).

</dd> <dt>

*RecognitionStatus* \[ dans\]
</dt> <dd>

État de reconnaissance en tant que résultat de reconnaissance le plus récent.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Le comportement de l’interface de programmation d’applications (API) est imprévisible si vous essayez d’accéder à l’objet [**InkRecognizerContext**](inkrecognizercontext-class.md) d’origine à partir du gestionnaire d’événements de reconnaissance. N’essayez pas de le faire. Au lieu de cela, si vous avez besoin de le faire, créez un indicateur et définissez-le dans le gestionnaire d’événements de [reconnaissance](ink-recognition.md) . Vous pouvez ensuite interroger cet indicateur pour déterminer quand modifier les propriétés de **InkRecognizerContext** en dehors du gestionnaire d’événements.

Cette méthode d’événement est définie dans l' \_ interface IInkEvents. L' \_ interface IInkEvents implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IRERecognition.

## <a name="requirements"></a>Configuration requise



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

[**Méthode BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)
</dt> <dt>

[**Énumération InkRecognitionStatus**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionstatus)
</dt> <dt>

[**Recognize, méthode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[**Interface IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

