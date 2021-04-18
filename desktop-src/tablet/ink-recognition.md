---
description: Toutes les applications ne nécessitent pas l’utilisation de la reconnaissance, mais étant donné que la plupart des applications ont été conçues avec du texte comme type de données principal, la possibilité de convertir de l’encre en texte est très utile.
ms.assetid: 70d25839-6ddd-40db-8891-92da074d17b0
title: Reconnaissance de l’encre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca4ec6f897c797d86df96c5d9c2cfd5d80f16c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565264"
---
# <a name="ink-recognition"></a><span data-ttu-id="3af2d-103">Reconnaissance de l’encre</span><span class="sxs-lookup"><span data-stu-id="3af2d-103">Ink Recognition</span></span>

<span data-ttu-id="3af2d-104">Toutes les applications ne nécessitent pas l’utilisation de la reconnaissance, mais étant donné que la plupart des applications ont été conçues avec du texte comme type de données principal, la possibilité de convertir de l’encre en texte est très utile.</span><span class="sxs-lookup"><span data-stu-id="3af2d-104">Not all applications require the use of recognition, but because most applications were designed with text as their primary data type, the ability to convert ink into text is very valuable.</span></span> <span data-ttu-id="3af2d-105">Vous pouvez utiliser les fonctionnalités de reconnaissance de l’API de la plateforme Tablet PC pour demander des informations sur les moteurs de reconnaissance disponibles, tels que les langues qu’ils reconnaissent.</span><span class="sxs-lookup"><span data-stu-id="3af2d-105">You can use the recognition features of the Tablet PC platform API to query for information about the recognition engines that are available, such as what languages they recognize.</span></span> <span data-ttu-id="3af2d-106">Vous pouvez ensuite envoyer une collection [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) à partir d’un objet [**Ink**](inkdisp-class.md) à un moteur de reconnaissance et retourner un objet [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) .</span><span class="sxs-lookup"><span data-stu-id="3af2d-106">You can then send a [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection from an [**Ink**](inkdisp-class.md) object to a recognition engine and have it return a [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object.</span></span>

## <a name="recognizercontext-object"></a><span data-ttu-id="3af2d-107">Objet RecognizerContext</span><span class="sxs-lookup"><span data-stu-id="3af2d-107">RecognizerContext Object</span></span>

<span data-ttu-id="3af2d-108">Un objet [**RecognizerContext**](inkrecognizercontext-class.md) est l’instanciation d’un module de reconnaissance donné.</span><span class="sxs-lookup"><span data-stu-id="3af2d-108">A [**RecognizerContext**](inkrecognizercontext-class.md) object is the instantiation of a given recognizer.</span></span> <span data-ttu-id="3af2d-109">L’objet **RecognizerContext** vous permet de reconnaître une collection donnée de traits de façon synchrone ou asynchrone.</span><span class="sxs-lookup"><span data-stu-id="3af2d-109">The **RecognizerContext** object enables you to recognize a given collection of strokes synchronously or asynchronously.</span></span> <span data-ttu-id="3af2d-110">En cas de reconnaissance asynchrone, l’objet **RecognizerContext** retourne l’objet [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) dans un rappel d’événement à l’application.</span><span class="sxs-lookup"><span data-stu-id="3af2d-110">When recognizing asynchronously, the **RecognizerContext** object returns the [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object in an event callback to the application.</span></span>

## <a name="recognizers-and-recognizer-objects"></a><span data-ttu-id="3af2d-111">Objets de reconnaissance et de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="3af2d-111">Recognizers and Recognizer Objects</span></span>

<span data-ttu-id="3af2d-112">Un seul Tablet PC peut avoir un ou plusieurs module de reconnaissance disponibles.</span><span class="sxs-lookup"><span data-stu-id="3af2d-112">A single Tablet PC may have one or more recognizers available.</span></span> <span data-ttu-id="3af2d-113">Vous pouvez interroger la collection du module de reconnaissance pour déterminer le module de reconnaissance à utiliser.</span><span class="sxs-lookup"><span data-stu-id="3af2d-113">You can query the recognizer's collection to determine which recognizer to use.</span></span> <span data-ttu-id="3af2d-114">Un module de reconnaissance fournit des informations spécifiques sur ses fonctionnalités, telles que la langue qu’il peut reconnaître et le fabricant.</span><span class="sxs-lookup"><span data-stu-id="3af2d-114">A recognizer provides specific information about its capabilities such as the language it can recognize and the manufacturer.</span></span>

<span data-ttu-id="3af2d-115">Pour déterminer si au moins un module de reconnaissance est installé, instanciez un objet [**InkRecognizerContext**](inkrecognizercontext-class.md) comme indiqué dans les exemples de code C++ et C suivants \# .</span><span class="sxs-lookup"><span data-stu-id="3af2d-115">To determine whether at least one recognizer is installed, instantiate an [**InkRecognizerContext**](inkrecognizercontext-class.md) object as shown in the following C++ and C\# code examples.</span></span> <span data-ttu-id="3af2d-116">Si aucun module de reconnaissance n’est présent, cet appel à [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) échoue.</span><span class="sxs-lookup"><span data-stu-id="3af2d-116">If a recognizer is not present, this call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) fails.</span></span>


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



## <a name="recognitionresult-and-recognitionalternate-objects"></a><span data-ttu-id="3af2d-117">Objets RecognitionResult et RecognitionAlternate</span><span class="sxs-lookup"><span data-stu-id="3af2d-117">RecognitionResult and RecognitionAlternate Objects</span></span>

<span data-ttu-id="3af2d-118">Les résultats de la reconnaissance sont retournés dans un objet [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) .</span><span class="sxs-lookup"><span data-stu-id="3af2d-118">The results of the recognition are returned in a [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object.</span></span> <span data-ttu-id="3af2d-119">Les résultats contiennent une chaîne de résultat optimale dans la propriété de la [chaîne de caractères](/previous-versions/ms829602(v=msdn.10)) , ainsi qu’une collection de résultats alternatifs dans une collection [**RecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) .</span><span class="sxs-lookup"><span data-stu-id="3af2d-119">The results contain a best result string in the [TopString](/previous-versions/ms829602(v=msdn.10)) property, as well as a collection of alternative results in a [**RecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) collection.</span></span> <span data-ttu-id="3af2d-120">L’objet **RecognitionResult** peut être rendu persistant avec la collection [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) d’origine à partir de laquelle il a été généré.</span><span class="sxs-lookup"><span data-stu-id="3af2d-120">The **RecognitionResult** object can be persisted with the original [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection from which it was generated.</span></span>

## <a name="recognizerguide-structure"></a><span data-ttu-id="3af2d-121">RecognizerGuide, structure</span><span class="sxs-lookup"><span data-stu-id="3af2d-121">RecognizerGuide Structure</span></span>

<span data-ttu-id="3af2d-122">Le Guide de reconnaissance peut se composer de lignes et de colonnes et donne au module de reconnaissance un meilleur contexte dans lequel effectuer la reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="3af2d-122">The recognizer guide can consist of rows and columns, and gives the recognizer a better context in which to perform recognition.</span></span> <span data-ttu-id="3af2d-123">Par exemple, vous pouvez dessiner des lignes horizontales sur l’écran d’un utilisateur, presque comme une feuille de papier en règle générale, qui indique où l’écriture manuscrite doit se produire (ce type de repère se compose uniquement de lignes et de colonnes).</span><span class="sxs-lookup"><span data-stu-id="3af2d-123">For example, you can draw horizontal lines on a user's screen, almost like a ruled piece of paper, that show where handwriting should occur (this type of guide would consist only of rows, and no columns).</span></span> <span data-ttu-id="3af2d-124">Si un utilisateur écrit sur les lignes, au lieu d’un espace arbitraire, la précision de la reconnaissance s’en trouve améliorée.</span><span class="sxs-lookup"><span data-stu-id="3af2d-124">If a user writes on the lines, instead of some arbitrary space, recognition accuracy improves.</span></span>

<span data-ttu-id="3af2d-125">L’illustration suivante montre une structure [**RecognizerGuide**](inkrecognizerguide-class.md) avec deux lignes pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="3af2d-125">The following illustration shows a [**RecognizerGuide**](inkrecognizerguide-class.md) structure with two lines for input.</span></span>

![illustration illustrant le Guide de reconnaissance en deux lignes](images/9791100b-8279-4dd0-823f-0a38a0308a74.jpg)

<span data-ttu-id="3af2d-127">L’illustration suivante montre une structure [**RecognizerGuide**](inkrecognizerguide-class.md) avec quatre colonnes et trois lignes.</span><span class="sxs-lookup"><span data-stu-id="3af2d-127">The following illustration shows a [**RecognizerGuide**](inkrecognizerguide-class.md) structure with four columns and three rows.</span></span>

![illustration illustrant le Guide de reconnaissance trois-par-quatre](images/d1bbf2d3-9653-49d7-bf48-c1b26645074c.jpg)

<span data-ttu-id="3af2d-129">Pour plus d’informations sur l’utilisation de la structure [**RecognizerGuide**](inkrecognizerguide-class.md) , consultez la rubrique de référence **RecognizerGuide** .</span><span class="sxs-lookup"><span data-stu-id="3af2d-129">For more information about using the [**RecognizerGuide**](inkrecognizerguide-class.md) structure, see the **RecognizerGuide** reference topic.</span></span>

 

 
