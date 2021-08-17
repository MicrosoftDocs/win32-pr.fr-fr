---
description: Toutes les applications ne nécessitent pas l’utilisation de la reconnaissance, mais étant donné que la plupart des applications ont été conçues avec du texte comme type de données principal, la possibilité de convertir de l’encre en texte est très utile.
ms.assetid: 70d25839-6ddd-40db-8891-92da074d17b0
title: Reconnaissance de l’encre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26c3f1431aca97f41b4de9aef64108f3e619ef7b6f9239f46fdde9f7bf4ff3da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718291"
---
# <a name="ink-recognition"></a>Reconnaissance de l’encre

Toutes les applications ne nécessitent pas l’utilisation de la reconnaissance, mais étant donné que la plupart des applications ont été conçues avec du texte comme type de données principal, la possibilité de convertir de l’encre en texte est très utile. Vous pouvez utiliser les fonctionnalités de reconnaissance de l’API de la plateforme Tablet PC pour demander des informations sur les moteurs de reconnaissance disponibles, tels que les langues qu’ils reconnaissent. Vous pouvez ensuite envoyer une collection [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) à partir d’un objet [**Ink**](inkdisp-class.md) à un moteur de reconnaissance et retourner un objet [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) .

## <a name="recognizercontext-object"></a>Objet RecognizerContext

Un objet [**RecognizerContext**](inkrecognizercontext-class.md) est l’instanciation d’un module de reconnaissance donné. L’objet **RecognizerContext** vous permet de reconnaître une collection donnée de traits de façon synchrone ou asynchrone. En cas de reconnaissance asynchrone, l’objet **RecognizerContext** retourne l’objet [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) dans un rappel d’événement à l’application.

## <a name="recognizers-and-recognizer-objects"></a>Objets de reconnaissance et de reconnaissance

Un seul Tablet PC peut avoir un ou plusieurs module de reconnaissance disponibles. Vous pouvez interroger la collection du module de reconnaissance pour déterminer le module de reconnaissance à utiliser. Un module de reconnaissance fournit des informations spécifiques sur ses fonctionnalités, telles que la langue qu’il peut reconnaître et le fabricant.

Pour déterminer si au moins un module de reconnaissance est installé, instanciez un objet [**InkRecognizerContext**](inkrecognizercontext-class.md) comme indiqué dans les exemples de code C++ et C suivants \# . Si aucun module de reconnaissance n’est présent, cet appel à [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) échoue.


```C++
CComPtr<IInkRecognizerContext> g_pIInkRecoContext;
hr = CoCreateInstance(CLSID_InkRecognizerContext, 
      NULL, CLSCTX_INPROC_SERVER,
      IID_IInkRecognizerContext, 
(void **) &g_pIInkRecoContext);
if (FAILED(hr)) 
{
      ::MessageBox(NULL, TEXT("No recognizers installed.\nExiting."), 
      gc_szAppName, MB_ICONERROR);
      return -1;
}
```




```CSharp
try
{
  Recognizers recos = new Recognizers();//Check for recognizer.
  Recognizer defReco = recos.GetDefaultRecognizer();
  recoContext = defReco.CreateRecognizerContext();
}
catch
{
  MessageBox.Show("No recognizers installed.");
}
```



## <a name="recognitionresult-and-recognitionalternate-objects"></a>Objets RecognitionResult et RecognitionAlternate

Les résultats de la reconnaissance sont retournés dans un objet [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) . Les résultats contiennent une chaîne de résultat optimale dans la propriété de la [chaîne de caractères](/previous-versions/ms829602(v=msdn.10)) , ainsi qu’une collection de résultats alternatifs dans une collection [**RecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) . L’objet **RecognitionResult** peut être rendu persistant avec la collection [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) d’origine à partir de laquelle il a été généré.

## <a name="recognizerguide-structure"></a>RecognizerGuide, structure

Le Guide de reconnaissance peut se composer de lignes et de colonnes et donne au module de reconnaissance un meilleur contexte dans lequel effectuer la reconnaissance. Par exemple, vous pouvez dessiner des lignes horizontales sur l’écran d’un utilisateur, presque comme une feuille de papier en règle générale, qui indique où l’écriture manuscrite doit se produire (ce type de repère se compose uniquement de lignes et de colonnes). Si un utilisateur écrit sur les lignes, au lieu d’un espace arbitraire, la précision de la reconnaissance s’en trouve améliorée.

L’illustration suivante montre une structure [**RecognizerGuide**](inkrecognizerguide-class.md) avec deux lignes pour l’entrée.

![illustration illustrant le Guide de reconnaissance en deux lignes](images/9791100b-8279-4dd0-823f-0a38a0308a74.jpg)

L’illustration suivante montre une structure [**RecognizerGuide**](inkrecognizerguide-class.md) avec quatre colonnes et trois lignes.

![illustration illustrant le Guide de reconnaissance trois-par-quatre](images/d1bbf2d3-9653-49d7-bf48-c1b26645074c.jpg)

Pour plus d’informations sur l’utilisation de la structure [**RecognizerGuide**](inkrecognizerguide-class.md) , consultez la rubrique de référence **RecognizerGuide** .

 

 
