---
description: Toute reconnaissance pour les contrôles avec reconnaissance de l’encre se produit via un objet RecognizerContext. Les API de technologie Tablet PC vous permettent de définir la propriété Factoid sur un objet RecognizerContext.
ms.assetid: 453993a7-f055-4d84-870c-256d1ec17731
title: Définition du contexte pour les contrôles Ink-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 306ae4c76ce5187c930c24a10631ec703f684cc8a3e4b0a94f46414bddbd058f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091299"
---
# <a name="setting-context-for-ink-enabled-controls"></a>Définition du contexte pour les contrôles Ink-Enabled

Toute reconnaissance pour les contrôles avec reconnaissance de l’encre se produit via un objet [**RecognizerContext**](inkrecognizercontext-class.md) . Les API de technologie Tablet PC vous permettent de définir la propriété [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) sur un objet **RecognizerContext** .

Si vous créez une application compatible avec l’écriture manuscrite, utilisez les propriétés [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) et [**de la**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) zone de texte de l’objet [**RecognizerContext**](inkrecognizercontext-class.md) pour définir des contextes.

Vous pouvez transmettre les valeurs de chaîne des noms dans les étendues d’entrée définies dans l’énumération [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) à la propriété [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) , séparées par une ouverture ( ! et une fermeture). Par exemple, pour définir le contexte d’un objet [**RecognizerContext**](inkrecognizercontext-class.md) de façon à ce qu’il s’écarte des caractères utilisés dans une URL, utilisez la syntaxe indiquée dans les exemples C suivants \# :


```C++
theRecoContext.Factoid = "(!IS_URL)";
```



> [!Note]  
> les étendues d’entrée telles qu’elles sont définies dans l’énumération [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) remplacent les factoids disponibles dans les versions précédentes du kit de développement logiciel (SDK) de Windows XP Tablet PC Edition, bien que ces factoids continuent de fonctionner pour assurer la compatibilité descendante.

 

L’exemple C suivant \# définit la propriété [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) pour les codes postaux :


```C++
theRecognizerContext.Factoid = "(!IS_ADDRESS_POSTALCODE)";
```



Vous pouvez combiner des étendues d’entrée à l’aide de la syntaxe d’expression régulière d’écriture manuscrite. Pour plus d’informations sur l’utilisation de la syntaxe des expressions régulières, consultez [étendues d’entrée personnalisées avec des expressions régulières](custom-input-scopes-with-regular-expressions.md).

Vous pouvez définir des indicateurs de reconnaissance sur l’objet [**RecognizerContext**](inkrecognizercontext-class.md) pour affecter le comportement du module de reconnaissance. L’un de ces indicateurs est l’indicateur de **forçage** dans l’énumération [**InkRecognitionModes**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes) du **RecognizerContext**. L’indicateur de **forçage** force le module de reconnaissance à retourner un résultat qui correspond à la définition de la Factoid définie. Par exemple, si vous avez un formulaire qui oblige l’utilisateur à entrer une quantité numérique, il peut être utile de définir le **\_ nombre** Factoid et de définir la propriété [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) sur **force**. Dans cette instance, l’indicateur de **forçage** garantit que le module de reconnaissance retourne uniquement des nombres.

L’exemple C suivant \# définit la propriété [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) sur **force**:


```C++
theRecognizerContext.RecognitionFlags = RecognitionModes.Coerce;
```



Toutefois, soyez vigilant lorsque vous décidez de définir l’indicateur de **forçage** . L’indicateur force le module de reconnaissance à correspondre uniquement à la définition de Factoid. Par exemple, si vous définissez l' \_ \_ étendue d’entrée FULLTELEPHONENUMBER et l’indicateur de **forçage** , le module de reconnaissance retourne des résultats qui correspondent exactement à la définition de l’étendue de l' \_ entrée de FULLTELEPHONENUMBER de téléphone \_ uniquement. Si un utilisateur écrit « 911 » avec l' \_ \_ étendue d’entrée de téléphone FULLTELEPHONENUMBER et l’indicateur de **forçage** défini, le module de reconnaissance peut retourner une chaîne vide ou une chaîne aléatoire au format (xxx) xxx-xxxx (où X est un chiffre). Le format XXX ne correspond pas à la définition de l' \_ opérateur is Telephone \_ FULLTELEPHONENUMBER Factoid, même s’il s’agit d’un numéro de téléphone valide.

Pour obtenir la liste des formats pris en charge pour chaque étendue d’entrée, consultez la référence [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) .

Pour rétablir la valeur par défaut d’un champ pour le module de reconnaissance, affectez la valeur \_ par défaut à Factoid, comme dans l’exemple C suivant \# :


```C++
theRecgonizerContext.Factoid = "(!IS_DEFAULT)";
```



Pour les applications qui utilisent le contrôle [InkEdit](inkedit-control-reference.md) , définissez le type Factoid pour le contrôle en spécifiant :


```C++
InkEdit1.Factoid = "(!IS_INPUTSCOPE)"
```



Où `IS_INPUTSCOPE` est le nom de l’étendue d’entrée que vous souhaitez appliquer.

Le contrôle [InkEdit](inkedit-control-reference.md) n’expose pas un objet [**RecognizerContext**](inkrecognizercontext-class.md) . Vous pouvez toujours assigner le contexte à l’aide de la propriété [**Factoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid) du contrôle InkEdit, mais vous ne pouvez pas définir l’indicateur **WORDMODE** .

 

 
