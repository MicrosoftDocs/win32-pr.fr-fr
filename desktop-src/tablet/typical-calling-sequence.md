---
description: 'Les méthodes que vous devez implémenter pour créer un module de reconnaissance de l’encre sont appelées par les API de la plateforme Tablet PC et non directement par une application compatible avec l’écriture manuscrite. Les étapes suivantes représentent une séquence d’appel typique pour l’implémentation de ces méthodes : la DLL est chargée. Une&\# 160 ; Le descripteur HRECOGNIZER est créé. Une&\# 160 ; Le descripteur HRECOCONTEXT est créé. Les options et les modes de reconnaissance sont définis pour ce contexte. Les traits sont ajoutés aux données d’encre. L’entrée est terminée. L’encre est reconnue. Les résultats de la reconnaissance sont retournés. Le descripteur HRECOCONTEXT est détruit. Le descripteur HRECOGNIZER est détruit. La séquence d’appel est également illustrée dans la structure de code suivante : C + + CreateRecognizer (CLSID, &HREC); while (plus d’éléments manuscrits à reconnaître...) {//Créer un contexte, une fois par pièce d’encre pour être reconnu, HRC = CreateContext (HREC, &HRC);//fonctions permettant de configurer les options et les modes pour ce contexte SetGuide (HRC, pGuide, 0); SetFactoid (HRC, 5, téléphone); uniquement en cas d’application avec Forms SetFlags (HRC, RECOFLAG \_ WORDMODE);//rare, uniquement si vous souhaitiez utiliser le mode Word, aucun dictionnaire, ou segmentation unique SetWordList (HRC, HWL);//ajouter tous les traits dans ce morceau d’encre lorsque (plus de traits...) {AddStroke (HRC, NULL, 800, pPacket, pXForm);//un appel par trait} EndInkInput (HRC); Cela obtient le processus reconnu par l’encre (HRC); S’il s’agit d’une application simple, elle l’appelle pour une réponse simple GetBestResultString (HRC, longueur, mémoire tampon); S’il s’agit d’une application complexe, elle l’appelle pour obtenir une réponse complète GetLatticePtr (HRC, &pLattice); Détruisez le contexte DestroyContext (HRC); }//Appelé juste avant que l’application n’arrête DestroyRecognizer (HREC);'
ms.assetid: 484ba140-788f-4b71-9cc7-9baa919d9936
title: Séquence d’appel classique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 832ea396c1d73748c4636d2cad5e17529b8d54df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521020"
---
# <a name="typical-calling-sequence"></a><span data-ttu-id="6c51c-103">Séquence d’appel classique</span><span class="sxs-lookup"><span data-stu-id="6c51c-103">Typical Calling Sequence</span></span>

<span data-ttu-id="6c51c-104">Les méthodes que vous devez implémenter pour créer un module de reconnaissance de l’encre sont appelées par les API de la plateforme Tablet PC et non directement par une application compatible avec l’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="6c51c-104">The methods you must implement to create an ink recognizer are called by the Tablet PC Platform APIs and not directly by an ink-enabled application.</span></span>

<span data-ttu-id="6c51c-105">Les étapes suivantes représentent une séquence d’appel typique pour l’implémentation de ces méthodes :</span><span class="sxs-lookup"><span data-stu-id="6c51c-105">The following steps represent a typical calling sequence for the implementation of these methods:</span></span>

1.  <span data-ttu-id="6c51c-106">La DLL est chargée.</span><span class="sxs-lookup"><span data-stu-id="6c51c-106">The DLL is loaded.</span></span>
2.  <span data-ttu-id="6c51c-107">Un descripteur [HRECOGNIZER](hrecognizer-handle.md) est créé.</span><span class="sxs-lookup"><span data-stu-id="6c51c-107">An [HRECOGNIZER](hrecognizer-handle.md) handle is created.</span></span>
3.  <span data-ttu-id="6c51c-108">Un descripteur [HRECOCONTEXT](hrecocontext-handle.md) est créé.</span><span class="sxs-lookup"><span data-stu-id="6c51c-108">An [HRECOCONTEXT](hrecocontext-handle.md) handle is created.</span></span>
4.  <span data-ttu-id="6c51c-109">Les options et les modes de reconnaissance sont définis pour ce contexte.</span><span class="sxs-lookup"><span data-stu-id="6c51c-109">Recognizer options and modes are set for this context.</span></span>
5.  <span data-ttu-id="6c51c-110">Les traits sont ajoutés aux données d’encre.</span><span class="sxs-lookup"><span data-stu-id="6c51c-110">Strokes are added to the ink data.</span></span>
6.  <span data-ttu-id="6c51c-111">L’entrée est terminée.</span><span class="sxs-lookup"><span data-stu-id="6c51c-111">Input is ended.</span></span>
7.  <span data-ttu-id="6c51c-112">L’encre est reconnue.</span><span class="sxs-lookup"><span data-stu-id="6c51c-112">The ink is recognized.</span></span>
8.  <span data-ttu-id="6c51c-113">Les résultats de la reconnaissance sont retournés.</span><span class="sxs-lookup"><span data-stu-id="6c51c-113">The recognition results are returned.</span></span>
9.  <span data-ttu-id="6c51c-114">Le descripteur [HRECOCONTEXT](hrecocontext-handle.md) est détruit.</span><span class="sxs-lookup"><span data-stu-id="6c51c-114">The [HRECOCONTEXT](hrecocontext-handle.md) handle is destroyed.</span></span>
10. <span data-ttu-id="6c51c-115">Le descripteur [HRECOGNIZER](hrecognizer-handle.md) est détruit.</span><span class="sxs-lookup"><span data-stu-id="6c51c-115">The [HRECOGNIZER](hrecognizer-handle.md) handle is destroyed.</span></span>

<span data-ttu-id="6c51c-116">La séquence d’appel est également illustrée dans la structure de code suivante :</span><span class="sxs-lookup"><span data-stu-id="6c51c-116">The calling sequence is also illustrated in the following code outline:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6c51c-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6c51c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c51c-118">API de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="6c51c-118">Recognizer APIs</span></span>](recognizer-apis.md)
</dt> <dt>

[<span data-ttu-id="6c51c-119">Architecture de l’API de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="6c51c-119">Recognition API Architecture</span></span>](recognition-api-architecture.md)
</dt> </dl>

 

 



