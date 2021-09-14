---
description: Pour créer un dictionnaire d’applications, il est nécessaire de définir la propriété de la plage de mots de l’objet RecognizerContext.
ms.assetid: 24dbf617-fa16-44f1-ba59-d4d99b8f1375
title: Utilisation d’un dictionnaire d’applications avec InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4bc919fc071f249611d42b8decb6ce4fb0b0f88
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235037"
---
# <a name="using-an-application-dictionary-with-inkedit"></a>Utilisation d’un dictionnaire d’applications avec InkEdit

Pour créer un dictionnaire d’applications, il est nécessaire de définir la propriété de la plage de [**mots**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) de l’objet [**RecognizerContext**](inkrecognizercontext-class.md) . Le contrôle [InkEdit](inkedit-control-reference.md) n’expose pas l’objet **RecognizerContext** . il n’est donc pas possible de définir directement **la propriété de la propriété** de la personne de l’objet **RecognizerContext** du contrôle InkEdit.

Pour utiliser un dictionnaire d’applications avec un contrôle [InkEdit](inkedit-control-reference.md) , vous devez extraire les traits du contrôle InkEdit, les transmettre à un nouvel objet [**RecognizerContext**](inkrecognizercontext-class.md) en attribuant à [**la propriété de**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) la propriété de la propriété de la propriété de la propriété de la [**valeur une valeur de la**](inkwordlist-class.md) propriété de la demande, stocker les résultats de cet objet **RecognizerContext** , puis retransmettre les résultats au contrôle InkEdit.

## <a name="example"></a>Exemple

Le code C suivant \# illustre un exemple de cette technique.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[InkEdit, contrôle](/previous-versions/ms552265(v=vs.100))
</dt> <dt>

[Classe Microsoft. Ink. RecognizerContext](/previous-versions/ms552546(v=vs.100))
</dt> <dt>

[Classe Microsoft. Ink. de la zone de texte](/previous-versions/ms827589(v=msdn.10))
</dt> </dl>

 

 
