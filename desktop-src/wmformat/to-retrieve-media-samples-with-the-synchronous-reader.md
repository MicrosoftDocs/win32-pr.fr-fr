---
title: Pour récupérer des exemples de médias avec le lecteur synchrone
description: Pour récupérer des exemples de médias avec le lecteur synchrone
ms.assetid: 7e228a0b-e29d-485e-b2ef-81c0311ca828
keywords:
- ASF (Advanced Systems Format), récupération des exemples de supports
- ASF (format des systèmes avancés), récupération des exemples de média
- ASF (Advanced Systems Format), lecteurs synchrones
- ASF (format des systèmes avancés), lecteurs synchrones
- lecteurs synchrones, récupération d’exemples de médias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fd341ea9616b18a5e65cfa8c1134e0f1be44b5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381510"
---
# <a name="to-retrieve-media-samples-with-the-synchronous-reader"></a><span data-ttu-id="bc833-108">Pour récupérer des exemples de médias avec le lecteur synchrone</span><span class="sxs-lookup"><span data-stu-id="bc833-108">To Retrieve Media Samples with the Synchronous Reader</span></span>

<span data-ttu-id="bc833-109">Vous devez demander chaque exemple l’un après l’autre à partir du lecteur synchrone.</span><span class="sxs-lookup"><span data-stu-id="bc833-109">You must request each sample one at a time from the synchronous reader.</span></span> <span data-ttu-id="bc833-110">Vous bénéficiez ainsi d’un plus grand contrôle sur les exemples que vous recevez et le moment où vous les recevez.</span><span class="sxs-lookup"><span data-stu-id="bc833-110">This gives you more control over the samples you receive and when you receive them.</span></span>

<span data-ttu-id="bc833-111">Utilisez la méthode [**IWMSyncReader :: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) pour récupérer un exemple.</span><span class="sxs-lookup"><span data-stu-id="bc833-111">Use the [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) method to retrieve a sample.</span></span> <span data-ttu-id="bc833-112">Vous devez passer principalement des pointeurs vers des variables qui seront remplies avec des informations sur l’exemple récupéré en tant que paramètres.</span><span class="sxs-lookup"><span data-stu-id="bc833-112">You need to pass mostly pointers to variables that will be filled with information about the sample retrieved as parameters.</span></span> <span data-ttu-id="bc833-113">Le seul paramètre d’entrée est *wStreamNum*.</span><span class="sxs-lookup"><span data-stu-id="bc833-113">The only input parameter is *wStreamNum*.</span></span> <span data-ttu-id="bc833-114">Si vous transmettez un numéro de flux, **GetNextSample** récupère l’échantillon suivant avec le numéro de flux spécifié.</span><span class="sxs-lookup"><span data-stu-id="bc833-114">If you pass a stream number, **GetNextSample** will retrieve the next sample with the specified stream number.</span></span> <span data-ttu-id="bc833-115">Si vous transmettez zéro pour *wStreamNum*, l’exemple suivant qui se produit chronologiquement dans le fichier est récupéré.</span><span class="sxs-lookup"><span data-stu-id="bc833-115">If you pass zero for *wStreamNum*, the next sample that occurs chronologically in the file is retrieved.</span></span>

<span data-ttu-id="bc833-116">Par défaut, le lecteur synchrone récupère tous les échantillons des sorties d’un fichier dans l’ordre chronologique.</span><span class="sxs-lookup"><span data-stu-id="bc833-116">By default, the synchronous reader retrieves all of the samples from the outputs in a file in chronological order.</span></span> <span data-ttu-id="bc833-117">Si vous appelez **GetNextSample** et qu’il n’y a plus d’exemples à obtenir, il retournera NS \_ E \_ no \_ More \_ , qui est un code d’erreur qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="bc833-117">If you call **GetNextSample** and there are no more samples to get, it will return NS\_E\_NO\_MORE\_SAMPLES, which is a failed error code.</span></span> <span data-ttu-id="bc833-118">Lors du codage par conséquent, vous pouvez simplement parcourir les exemples jusqu’à ce que la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="bc833-118">When coding therefore, you can simply loop through samples until the method fails.</span></span>

> [!Note]  
> <span data-ttu-id="bc833-119">Pour vous assurer que le lecteur synchrone fournit des durées d’échantillonnage correctes pour les flux vidéo, vous devez d’abord configurer la sortie du flux.</span><span class="sxs-lookup"><span data-stu-id="bc833-119">To ensure that the synchronous reader delivers correct sample durations for video streams, you must first configure the stream output.</span></span> <span data-ttu-id="bc833-120">Appelez la méthode [**IWMSyncReader :: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting) pour définir le \_ paramètre g wszVideoSampleDurations sur **true**.</span><span class="sxs-lookup"><span data-stu-id="bc833-120">Call the [**IWMSyncReader::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting) method to set the g\_wszVideoSampleDurations setting to **TRUE**.</span></span>

 

<span data-ttu-id="bc833-121">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="bc833-121">Example Code</span></span>

<span data-ttu-id="bc833-122">L’exemple de code suivant montre comment utiliser **GetNextSample** pour récupérer tous les exemples d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="bc833-122">The following example code shows how to use **GetNextSample** to retrieve all samples in a file.</span></span>


```C++
// Loop through all the samples in the file.
do
{
   // Get the next sample.
   hr = pSyncReader->GetNextSample(0,
                                   &pMyBuffer,
                                   &cnsSampleTime,
                                   &cnsSampleDuration,
                                   &dwFlags,
                                   &dwOutputNumber,
                                   NULL);

   if(SUCCEEDED(hr))
   {
      // TODO: Process the sample in whatever way is appropriate 
      // to your application. When finished, clean up.
      pMyBuffer->Release();
      pMyBuffer = NULL;
      cnsSampleTime     = 0;
      cnsSampleDuration = 0;
      dwFlags           = 0;
      dwOutputNumber    = 0;
   }
} 
while (SUCCEEDED(hr));

```



## <a name="related-topics"></a><span data-ttu-id="bc833-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc833-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc833-124">**Interface IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="bc833-124">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="bc833-125">**Lecture des fichiers avec le lecteur synchrone**</span><span class="sxs-lookup"><span data-stu-id="bc833-125">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




