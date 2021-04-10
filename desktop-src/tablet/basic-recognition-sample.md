---
description: Cette application montre comment vous pouvez créer une application de reconnaissance de l’écriture manuscrite simple. Ce programme crée un objet InkCollector pour activer l’écriture manuscrite dans la fenêtre et un objet de contexte de reconnaissance par défaut.
ms.assetid: 6dc94293-cdf7-4b90-a5e8-559f376add26
title: Exemple de reconnaissance de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19679a6d1642a94ed813ba0428654b6e03009ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867738"
---
# <a name="basic-recognition-sample"></a><span data-ttu-id="2088c-103">Exemple de reconnaissance de base</span><span class="sxs-lookup"><span data-stu-id="2088c-103">Basic Recognition Sample</span></span>

<span data-ttu-id="2088c-104">Cette application montre comment vous pouvez créer une application de reconnaissance de l' *écriture manuscrite* simple.</span><span class="sxs-lookup"><span data-stu-id="2088c-104">This application demonstrates how you can build a simple *handwriting* recognition application.</span></span>

<span data-ttu-id="2088c-105">Ce programme crée un objet [**InkCollector**](inkcollector-class.md) pour activer l' *écriture manuscrite* dans la fenêtre et un objet de *contexte de reconnaissance* par défaut.</span><span class="sxs-lookup"><span data-stu-id="2088c-105">This program creates an [**InkCollector**](inkcollector-class.md) object to *ink*-enable the window and a default *recognizer context* object.</span></span> <span data-ttu-id="2088c-106">Lors de la réception du « Recognize ! »</span><span class="sxs-lookup"><span data-stu-id="2088c-106">Upon receiving the "Recognize!"</span></span> <span data-ttu-id="2088c-107">commande, déclenchée à partir du menu de l’application, les traits d’encre collectés sont transmis au contexte du module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="2088c-107">command, fired from the application's menu, the collected ink strokes are passed to the recognizer context.</span></span> <span data-ttu-id="2088c-108">La meilleure chaîne de résultat est présentée dans une boîte de message.</span><span class="sxs-lookup"><span data-stu-id="2088c-108">The best result string is presented in a message box.</span></span>

## <a name="creating-the-recognizercontext-object"></a><span data-ttu-id="2088c-109">Création de l’objet RecognizerContext</span><span class="sxs-lookup"><span data-stu-id="2088c-109">Creating the RecognizerContext Object</span></span>

<span data-ttu-id="2088c-110">Dans la procédure WndProc pour l’application, quand le \_ message WM Create est reçu au démarrage, un nouveau contexte de module de reconnaissance qui utilise le module de reconnaissance par défaut est créé.</span><span class="sxs-lookup"><span data-stu-id="2088c-110">In the WndProc procedure for the application, when the WM\_CREATE message is received on startup, a new recognizer context that uses the default recognizer is created.</span></span> <span data-ttu-id="2088c-111">Ce contexte est utilisé pour toutes les reconnaissances dans l’application.</span><span class="sxs-lookup"><span data-stu-id="2088c-111">This context is used for all recognition in the application.</span></span>


```C++
case WM_CREATE:
{
    HRESULT hr;
    hr = CoCreateInstance(CLSID_InkRecognizerContext,
             NULL, CLSCTX_INPROC_SERVER, IID_IInkRecognizerContext,
             (void **) &g_pIInkRecoContext);
    if (FAILED(hr))
    {
        ::MessageBox(NULL, TEXT("There are no handwriting recognizers installed.\n"
            "You need to have at least one in order to run this sample.\nExiting."),
            gc_szAppName, MB_ICONERROR);
        return -1;
    }
  //...
```



## <a name="recognizing-the-strokes"></a><span data-ttu-id="2088c-112">Reconnaissance des traits</span><span class="sxs-lookup"><span data-stu-id="2088c-112">Recognizing the Strokes</span></span>

<span data-ttu-id="2088c-113">La commande Recognize est reçue quand l’utilisateur clique sur Recognize !</span><span class="sxs-lookup"><span data-stu-id="2088c-113">The recognize command is received when the user clicks the Recognize!</span></span> <span data-ttu-id="2088c-114">.</span><span class="sxs-lookup"><span data-stu-id="2088c-114">menu item.</span></span> <span data-ttu-id="2088c-115">Le code obtient un pointeur vers le [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) d’entrée manuscrite (pIInkStrokes) de l’objet [**InkDisp**](inkdisp-class.md) , puis passe le **InkStrokes** au contexte de module de reconnaissance à l’aide d’un appel aux \_ traits PutRef.</span><span class="sxs-lookup"><span data-stu-id="2088c-115">The code gets a pointer to the ink [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) (pIInkStrokes) off of the [**InkDisp**](inkdisp-class.md) object, and then passes the **InkStrokes** to the recognizer context using a call to putref\_Strokes.</span></span>


```C++
 case WM_COMMAND:
  //...
  else if (wParam == ID_RECOGNIZE)
  {
      // change cursor to the system's Hourglass
      HCURSOR hCursor = ::SetCursor(::LoadCursor(NULL, IDC_WAIT));
      // Get a pointer to the ink stroke collection
      // This collection is a snapshot of the entire ink object
      IInkStrokes* pIInkStrokes = NULL;
      HRESULT hr = g_pIInkDisp->get_Strokes(&pIInkStrokes);
      if (SUCCEEDED(hr)) 
      {
          // Pass the stroke collection to the recognizer context
          hr = g_pIInkRecoContext->putref_Strokes(pIInkStrokes);
          if (SUCCEEDED(hr)) 
          {
```



<span data-ttu-id="2088c-116">Le code appelle ensuite la méthode [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) de l’objet [**InkRecognizerContext**](inkrecognizercontext-class.md) , en passant un pointeur vers un objet [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) pour contenir les résultats.</span><span class="sxs-lookup"><span data-stu-id="2088c-116">The code then calls the [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) method of the [**InkRecognizerContext**](inkrecognizercontext-class.md) object, passing in a pointer to an [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object to hold the results.</span></span>


```C++
              // Recognize
              IInkRecognitionResult* pIInkRecoResult = NULL;
              hr = g_pIInkRecoContext->Recognize(&pIInkRecoResult);
              if (SUCCEEDED(hr)) 
              {
```



<span data-ttu-id="2088c-117">Enfin, le code utilise la propriété de [**chaîne**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topstring) de l’objet [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) pour récupérer le résultat de la reconnaissance supérieure dans une variable de chaîne, libère l’objet **IInkRecognitionResult** et affiche la chaîne dans une boîte de message.</span><span class="sxs-lookup"><span data-stu-id="2088c-117">Finally, the code uses the [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object's [**TopString**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topstring) property retrieve the top recognition result into a string variable, releases the **IInkRecognitionResult** object, and displays the string in a message box.</span></span>


```C++
                  // Get the best result of the recognition 
                  BSTR bstrBestResult = NULL;
                  hr = pIInkRecoResult->get_TopString(&bstrBestResult);
                  pIInkRecoResult->Release();
                  pIInkRecoResult = NULL;

                  // Show the result string
                  if (SUCCEEDED(hr) && bstrBestResult)
                  {
                      MessageBoxW(hwnd, bstrBestResult, 
                                  L"Recognition Results", MB_OK);
                      SysFreeString(bstrBestResult);
                  }  }
        
```



<span data-ttu-id="2088c-118">Veillez à réinitialiser le contexte du module de reconnaissance entre les utilisations.</span><span class="sxs-lookup"><span data-stu-id="2088c-118">Be sure to reset the recognizer context between usages.</span></span>


```
              // Reset the recognizer context
              g_pIInkRecoContext->putref_Strokes(NULL);
          }
          pIInkStrokes->Release();
      }
      // restore the cursor
      ::SetCursor(hCursor);
  }
```



 

 
