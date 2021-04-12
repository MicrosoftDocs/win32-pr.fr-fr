---
description: Permet d’effectuer la reconnaissance de l’encre, de récupérer le résultat de la reconnaissance et de récupérer d’autres fonctionnalités. InkRecognizerContext permet aux différents module de reconnaissance installés sur un système d’utiliser la reconnaissance manuscrite pour traiter l’entrée de manière appropriée.
ms.assetid: 2b39fd32-831d-4606-8600-b52aaa7ed882
title: InkRecognizerContext, classe (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRecognizerContext
- InkRecognizerContext.IInkRecognizerContext
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: afe5469cabf6764ed9b02fdcffcc8c1bedaca1d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203249"
---
# <a name="inkrecognizercontext-class"></a>InkRecognizerContext, classe

Permet d’effectuer la reconnaissance de l’encre, de récupérer le résultat de la reconnaissance et de récupérer d’autres fonctionnalités. **InkRecognizerContext** permet aux différents module de reconnaissance installés sur un système d’utiliser la reconnaissance manuscrite pour traiter l’entrée de manière appropriée.

**InkRecognizerContext** possède les types de membres suivants :

-   [Événements](#events)
-   [Interfaces](#interfaces)
-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="events"></a>Événements

La classe **InkRecognizerContext** contient ces événements.



| Événement                                                                               | Description                                                                                                                                                                                            |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Reconnaissance**](inkrecognizercontext-recognition.md)                             | Se produit lorsque le InkRecognizerContext a généré des résultats de la méthode BackgroundRecognize.<br/>                                                                                             |
| [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) | Se produit lorsque le **InkRecognizerContext** a généré des résultats après l’appel de la méthode [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)<br/> |



 

### <a name="interfaces"></a>Interfaces

La classe **InkRecognizerContext** définit ces interfaces.



| Interface                 | Description                                                                    |
|:--------------------------|:-------------------------------------------------------------------------------|
| **IInkRecognizerContext** | Cet objet implémente l’interface com **IInkRecognizerContext** .<br/> |



 

### <a name="methods"></a>Méthodes

La classe **InkRecognizerContext** possède ces méthodes.



| Méthode                                                                                              | Description                                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)                             | Spécifie que le module de reconnaissance doit reconnaître les traits associés et déclencher un événement de [**reconnaissance**](inkrecognizercontext-recognition.md) lorsque la reconnaissance est terminée.<br/>                                                                |
| [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) | Spécifie que le module de reconnaissance doit reconnaître les traits associés et déclencher un événement [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) lorsque la reconnaissance est terminée.<br/>                                    |
| [**Répliqué**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                                                      | Crée un **InkRecognizerContext** en double.<br/>                                                                                                                                                                                               |
| [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput)                                             | Met fin à l’entrée d’encre dans le **InkRecognizerContext**.<br/>                                                                                                                                                                                             |
| [**IsStringSupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported)                                 | Indique si le dictionnaire système, le dictionnaire de l’utilisateur ou la [**liste de mots**](inkwordlist-class.md) contient une chaîne spécifiée.<br/>                                                                                                             |
| [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)                                                 | Effectue la reconnaissance sur une collection [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) et retourne les résultats de la reconnaissance.<br/>                                                                                                                          |
| [**StopBackgroundRecognition**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-stopbackgroundrecognition)                 | Termine la reconnaissance en arrière-plan qui a été démarrée avec un appel à [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) ou [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates).<br/> |



 

### <a name="properties"></a>Propriétés

La classe **InkRecognizerContext** possède les propriétés suivantes.



| Propriété                                                                                   | Type d’accès           | Description                                                                                                                                                |
|:-------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CharacterAutoCompletion**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_characterautocompletionmode)<br/> | Lecture/écriture<br/> | Obtient ou définit le mode de saisie semi-automatique de caractères, qui détermine quand des caractères ou des mots sont reconnus.<br/>                                         |
| [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)<br/>                                 | Lecture/écriture<br/> | Obtient ou définit le nom de chaîne du Factoid utilisé par l’objet **InkRecognizerContext** .<br/>                                                        |
| [**Guide**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide)<br/>                                     | Lecture/écriture<br/> | Obtient ou définit le [**InkRecognizerGuide**](inkrecognizerguide-class.md) à utiliser pour l’entrée d’encre.<br/>                                                   |
| [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext)<br/>                           | Lecture/écriture<br/> | Obtient ou définit les caractères qui précèdent la collection [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) dans l’objet **InkRecognizerContext** .<br/> |
| [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags)<br/>               | Lecture/écriture<br/> | Obtient ou définit les indicateurs qui spécifient comment le module de reconnaissance interprète l’encre et détermine la chaîne de résultat.<br/>                                     |
| [**Module de reconnaissance**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognizer)<br/>                           | Lecture/écriture<br/> | Obtient ou définit l’objet [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) utilisé par l’objet **InkRecognizerContext** .<br/>                                   |
| [**Traits**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes)<br/>                                 | Lecture/écriture<br/> | Obtient ou définit la collection [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) associée à l’objet **InkRecognizerContext** .<br/>                    |
| [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext)<br/>                           | Lecture/écriture<br/> | Obtient ou définit les caractères qui viennent après la collection [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) dans l’objet **InkRecognizerContext** .<br/>  |
| [**Mots**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)<br/>                               | Lecture/écriture<br/> | Obtient ou définit l’objet [**InkWordList**](inkwordlist-class.md) utilisé pour améliorer les résultats de la reconnaissance.<br/>                               |



 

## <a name="remarks"></a>Notes

Cet objet peut être instancié en appelant la méthode [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

Il existe deux types de reconnaissance : l’arrière-plan (asynchrone) ou le premier plan (synchrone). La reconnaissance en arrière-plan est démarrée par un appel aux méthodes [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) ou [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) , se produit sur un thread d’arrière-plan et signale les résultats à l’application via un mécanisme d’événement. La reconnaissance de premier plan n’est pas retournée tant que la reconnaissance n’est pas terminée, rendant ainsi les résultats de la reconnaissance disponibles pour le thread appelant sans écouter l’événement de reconnaissance.

L’encre est traitée en continu en arrière-plan. Si un [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) est ajouté à la collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) à laquelle le **InkRecognizerContext** fait référence, le **IInkStrokeDisp** est alors immédiatement reconnu. Pour plus d’informations, consultez les notes dans la rubrique relative à la méthode [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput) .

Toute reconnaissance se produit par le biais d’un contexte de reconnaissance. Le contexte définit les paramètres pour une session de reconnaissance unique. Elle reçoit l’encre qui doit être reconnue et définit les contraintes sur l’entrée d’encre et sur la sortie de reconnaissance. Les contraintes qui peuvent être définies sur le contexte incluent le langage, le dictionnaire et la grammaire en cours d’utilisation.

> [!Note]  
> La définition de propriétés autres que les [**traits**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) ou les propriétés [**CharacterAutoCompletion**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_characterautocompletionmode) ne fonctionne que si la collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) est **null**. Vous devez définir les autres propriétés avant d’attacher la collection InkStrokes au **InkRecognizerContext**, ou vous devez définir la collection InkStrokes sur la **valeur null** , puis définir les autres propriétés. Si vous affectez la valeur **null** à la collection InkStrokes, puis définissez les autres propriétés, vous devrez peut-être rattacher la collection InkStrokes. Cela est dû au fait que la reconnaissance démarre juste après que vous avez affecté le InkStrokes au **InkRecognizerContext**. Lorsqu’un appel est effectué pour [**reconnaître la méthode \[ InkRecognizeContext \] classe**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) ou [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize), les résultats d’appel peuvent être déjà disponibles.

 

Pour améliorer les performances de votre application, supprimez votre objet **InkRecognizerContext** lorsqu’il n’est plus nécessaire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[Collection InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

