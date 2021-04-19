---
description: Pour créer un dictionnaire d’applications, il est nécessaire de définir la propriété de la plage de mots de l’objet RecognizerContext.
ms.assetid: 24dbf617-fa16-44f1-ba59-d4d99b8f1375
title: Utilisation d’un dictionnaire d’applications avec InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4bc919fc071f249611d42b8decb6ce4fb0b0f88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512959"
---
# <a name="using-an-application-dictionary-with-inkedit"></a><span data-ttu-id="8464c-103">Utilisation d’un dictionnaire d’applications avec InkEdit</span><span class="sxs-lookup"><span data-stu-id="8464c-103">Using an Application Dictionary with InkEdit</span></span>

<span data-ttu-id="8464c-104">Pour créer un dictionnaire d’applications, il est nécessaire de définir la propriété de la plage de [**mots**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) de l’objet [**RecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="8464c-104">To create an application dictionary, it is necessary to set the [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) property of the [**RecognizerContext**](inkrecognizercontext-class.md) object.</span></span> <span data-ttu-id="8464c-105">Le contrôle [InkEdit](inkedit-control-reference.md) n’expose pas l’objet **RecognizerContext** . il n’est donc pas possible de définir directement **la propriété de la propriété** de la personne de l’objet **RecognizerContext** du contrôle InkEdit.</span><span class="sxs-lookup"><span data-stu-id="8464c-105">The [InkEdit](inkedit-control-reference.md) control does not expose the **RecognizerContext** object, so it is not possible to directly set the **WordList** property of the InkEdit control's **RecognizerContext** object.</span></span>

<span data-ttu-id="8464c-106">Pour utiliser un dictionnaire d’applications avec un contrôle [InkEdit](inkedit-control-reference.md) , vous devez extraire les traits du contrôle InkEdit, les transmettre à un nouvel objet [**RecognizerContext**](inkrecognizercontext-class.md) en attribuant à [**la propriété de**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) la propriété de la propriété de la propriété de la propriété de la [**valeur une valeur de la**](inkwordlist-class.md) propriété de la demande, stocker les résultats de cet objet **RecognizerContext** , puis retransmettre les résultats au contrôle InkEdit.</span><span class="sxs-lookup"><span data-stu-id="8464c-106">To use an application dictionary with an [InkEdit](inkedit-control-reference.md) control, you must take the strokes out of the InkEdit control, pass them to a new [**RecognizerContext**](inkrecognizercontext-class.md) object with the [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) property set to a [**WordList**](inkwordlist-class.md) containing the application dictionary, store the results from this **RecognizerContext** object, and then pass the results back to the InkEdit control.</span></span>

## <a name="example"></a><span data-ttu-id="8464c-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="8464c-107">Example</span></span>

<span data-ttu-id="8464c-108">Le code C suivant \# illustre un exemple de cette technique.</span><span class="sxs-lookup"><span data-stu-id="8464c-108">The following C\# code shows an example of this technique.</span></span>


```C++
private RecognizerContext rc;
private WordList wl;
private int wlSelStart;
private int wlSelLen;
private bool isRecoPending = false;

private void Form1_Load(object sender, EventArgs e)
{
  //event handlers must be attached for dictionary to work.
  inkEdit1.Recognition += new Microsoft.Ink.InkEditRecognitionEventHandler(inkEdit1_Recognition);
  inkEdit1.TextChanged += new EventHandler(inkEdit1_TextChanged);

  //create a WordList that contains the application dictionary
  wl = new WordList();
  //...
  //Add dictionary terms to the WordList
  //...

  // create a RecognizerContext for the WordList
  rc = inkEdit1.Recognizer.CreateRecognizerContext();
  rc.Factoid = Factoid.WordList;

  //set the RecognizerContext WordList to the newly created WordList
  rc.WordList = wl;

  //create a delegate for the new RecognizerContext
  rc.RecognitionWithAlternates += new

  RecognizerContextRecognitionWithAlternatesEventHandler(rc_Recognition);
}

void inkEdit1_TextChanged(object sender, EventArgs e)
{
  if (isRecoPending)
  {
    isRecoPending = false;
    rc.BackgroundRecognizeWithAlternates();
  }
}

private void inkEdit1_Recognition(object sender,
Microsoft.Ink.InkEditRecognitionEventArgs e)
{
  //store the start of the selection in wlSelStart
  wlSelStart = inkEdit1.SelectionStart;

  //store the length of the selection in wlSelLen
  wlSelLen = e.RecognitionResult.TopString.Length;

  //copy the strokes from the InkEdit control into the new
  // RecognizerContext
  rc.Strokes = e.RecognitionResult.Strokes.Ink.Clone().Strokes;
  isRecoPending = true;
}

private void rc_Recognition(object sender,
Microsoft.Ink.RecognizerContextRecognitionWithAlternatesEventArgs e)
{
  if (inkEdit1.InvokeRequired)
  {
    inkEdit1.Invoke(new RecognizerContextRecognitionWithAlternatesEventHandler(rc_Recognition),
      new object[] { sender, e });
    return;
  }

  //set the insertion point in the InkEdit control
  inkEdit1.SelectionStart = wlSelStart;
  inkEdit1.SelectionLength = wlSelLen;
  //insert the result from the new RecognizerContext 
  //into the InkEdit control
  inkEdit1.SelectedText = e.Result.TopString;
  inkEdit1.SelectionStart = inkEdit1.SelectionStart +
  e.Result.TopString.Length;
}

// Event handler for the form's closed event
private void Form1_Closed(object sender, System.EventArgs e)
{
  inkEdit1.Dispose();
  inkEdit1 = null;
  rc.Dispose();
  rc = null;
}
```



## <a name="related-topics"></a><span data-ttu-id="8464c-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8464c-109">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8464c-110">[InkEdit, contrôle](/previous-versions/ms552265(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="8464c-110">[InkEdit Control](/previous-versions/ms552265(v=vs.100))</span></span>
</dt> <dt>

<span data-ttu-id="8464c-111">[Classe Microsoft. Ink. RecognizerContext](/previous-versions/ms552546(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="8464c-111">[Microsoft.Ink.RecognizerContext Class](/previous-versions/ms552546(v=vs.100))</span></span>
</dt> <dt>

<span data-ttu-id="8464c-112">[Classe Microsoft. Ink. de la zone de texte](/previous-versions/ms827589(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="8464c-112">[Microsoft.Ink.Wordlist Class](/previous-versions/ms827589(v=msdn.10))</span></span>
</dt> </dl>

 

 
