---
description: 'Les méthodes que vous devez implémenter pour créer un module de reconnaissance de l’encre sont appelées par les API de la plateforme Tablet PC et non directement par une application compatible avec l’écriture manuscrite. Les étapes suivantes représentent une séquence d’appel typique pour l’implémentation de ces méthodes : la DLL est chargée. Une&\# 160 ; Le descripteur HRECOGNIZER est créé. Une&\# 160 ; Le descripteur HRECOCONTEXT est créé. Les options et les modes de reconnaissance sont définis pour ce contexte. Les traits sont ajoutés aux données d’encre. L’entrée est terminée. L’encre est reconnue. Les résultats de la reconnaissance sont retournés. Le descripteur HRECOCONTEXT est détruit. Le descripteur HRECOGNIZER est détruit. La séquence d’appel est également illustrée dans la structure de code suivante : C + + CreateRecognizer (CLSID, &HREC); while (plus d’éléments manuscrits à reconnaître...) {//Créer un contexte, une fois par pièce d’encre pour être reconnu, HRC = CreateContext (HREC, &HRC);//fonctions permettant de configurer les options et les modes pour ce contexte SetGuide (HRC, pGuide, 0); SetFactoid (HRC, 5, téléphone); uniquement en cas d’application avec Forms SetFlags (HRC, RECOFLAG \_ WORDMODE);//rare, uniquement si vous souhaitiez utiliser le mode Word, aucun dictionnaire, ou segmentation unique SetWordList (HRC, HWL);//ajouter tous les traits dans ce morceau d’encre lorsque (plus de traits...) {AddStroke (HRC, NULL, 800, pPacket, pXForm);//un appel par trait} EndInkInput (HRC); Cela obtient le processus reconnu par l’encre (HRC); S’il s’agit d’une application simple, elle l’appelle pour une réponse simple GetBestResultString (HRC, longueur, mémoire tampon); S’il s’agit d’une application complexe, elle l’appelle pour obtenir une réponse complète GetLatticePtr (HRC, &pLattice); Détruisez le contexte DestroyContext (HRC); }//Appelé juste avant que l’application n’arrête DestroyRecognizer (HREC);'
ms.assetid: 484ba140-788f-4b71-9cc7-9baa919d9936
title: Séquence d’appel classique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 832ea396c1d73748c4636d2cad5e17529b8d54df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296018"
---
# <a name="typical-calling-sequence"></a>Séquence d’appel classique

Les méthodes que vous devez implémenter pour créer un module de reconnaissance de l’encre sont appelées par les API de la plateforme Tablet PC et non directement par une application compatible avec l’écriture manuscrite.

Les étapes suivantes représentent une séquence d’appel typique pour l’implémentation de ces méthodes :

1.  La DLL est chargée.
2.  Un descripteur [HRECOGNIZER](hrecognizer-handle.md) est créé.
3.  Un descripteur [HRECOCONTEXT](hrecocontext-handle.md) est créé.
4.  Les options et les modes de reconnaissance sont définis pour ce contexte.
5.  Les traits sont ajoutés aux données d’encre.
6.  L’entrée est terminée.
7.  L’encre est reconnue.
8.  Les résultats de la reconnaissance sont retournés.
9.  Le descripteur [HRECOCONTEXT](hrecocontext-handle.md) est détruit.
10. Le descripteur [HRECOGNIZER](hrecognizer-handle.md) est détruit.

La séquence d’appel est également illustrée dans la structure de code suivante :


```C++
CreateRecognizer(CLSID, &hrec);
while (more pieces of ink to recognize ... )
{
  // Create a context, once per piece of ink to be recognized
  hrc = CreateContext(hrec, &hrc);

  // Functions to set up options and modes for this context
  SetGuide(hrc, pGuide, 0);
  SetFactoid(hrc, 5, PHONE); // only if in application with forms
  SetFlags(hrc, RECOFLAG_WORDMODE); // rare, only if wanting word mode, no out-of-dictionary, or single segmentation
  SetWordList(hrc, hwl);

  // Adding all the strokes in this piece of ink
  while (more strokes ... )
  {
    AddStroke(hrc, NULL, 800, pPacket, pXForm);  // one call per stroke
  }
  EndInkInput(hrc);

  // This gets the ink recognized
  Process(hrc);

  // If this is a simple application, it calls this for a simple answer
  GetBestResultString(hrc, length, buffer);

  // If this is a complex application, it calls this for a complete answer
  GetLatticePtr(hrc, &pLattice);

  // Destroy the context
  DestroyContext(hrc);
}
// Called just before the application shuts down
DestroyRecognizer(hrec);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API de reconnaissance](recognizer-apis.md)
</dt> <dt>

[Architecture de l’API de reconnaissance](recognition-api-architecture.md)
</dt> </dl>

 

 



