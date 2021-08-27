---
description: Cette application montre comment vous pouvez créer une application de reconnaissance de l’écriture manuscrite simple. Ce programme crée un objet InkCollector pour activer l’écriture manuscrite dans la fenêtre et un objet de contexte de reconnaissance par défaut.
ms.assetid: 6dc94293-cdf7-4b90-a5e8-559f376add26
title: Exemple de reconnaissance de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf45aa7695866e1cf413ea42b7c377b07ea84984ecf2cc3f44da93ff868072d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111139"
---
# <a name="basic-recognition-sample"></a>Exemple de reconnaissance de base

Cette application montre comment vous pouvez créer une application de reconnaissance de l' *écriture manuscrite* simple.

Ce programme crée un objet [**InkCollector**](inkcollector-class.md) pour activer l' *écriture manuscrite* dans la fenêtre et un objet de *contexte de reconnaissance* par défaut. Lors de la réception du « Recognize ! » commande, déclenchée à partir du menu de l’application, les traits d’encre collectés sont transmis au contexte du module de reconnaissance. La meilleure chaîne de résultat est présentée dans une boîte de message.

## <a name="creating-the-recognizercontext-object"></a>Création de l’objet RecognizerContext

Dans la procédure WndProc pour l’application, quand le \_ message WM Create est reçu au démarrage, un nouveau contexte de module de reconnaissance qui utilise le module de reconnaissance par défaut est créé. Ce contexte est utilisé pour toutes les reconnaissances dans l’application.


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



## <a name="recognizing-the-strokes"></a>Reconnaissance des traits

La commande Recognize est reçue quand l’utilisateur clique sur Recognize ! . Le code obtient un pointeur vers le [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) d’entrée manuscrite (pIInkStrokes) de l’objet [**InkDisp**](inkdisp-class.md) , puis passe le **InkStrokes** au contexte de module de reconnaissance à l’aide d’un appel aux \_ traits PutRef.


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



Le code appelle ensuite la méthode [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) de l’objet [**InkRecognizerContext**](inkrecognizercontext-class.md) , en passant un pointeur vers un objet [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) pour contenir les résultats.


```C++
              // Recognize
              IInkRecognitionResult* pIInkRecoResult = NULL;
              hr = g_pIInkRecoContext->Recognize(&pIInkRecoResult);
              if (SUCCEEDED(hr)) 
              {
```



Enfin, le code utilise la propriété de [**chaîne**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topstring) de l’objet [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) pour récupérer le résultat de la reconnaissance supérieure dans une variable de chaîne, libère l’objet **IInkRecognitionResult** et affiche la chaîne dans une boîte de message.


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



Veillez à réinitialiser le contexte du module de reconnaissance entre les utilisations.


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



 

 
