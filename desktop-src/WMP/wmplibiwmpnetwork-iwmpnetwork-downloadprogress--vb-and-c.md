---
title: IWMPNetwork propriété downloadProgress
description: La propriété downloadProgress obtient le pourcentage de téléchargement terminé.
ms.assetid: 40568c81-5bb5-45d9-b654-31072608663d
keywords:
- propriété downloadProgress lecteur Windows Media
- propriété downloadProgress lecteur Windows Media, interface IWMPNetwork
- Interface IWMPNetwork lecteur Windows Media, propriété downloadProgress
topic_type:
- apiref
api_name:
- IWMPNetwork.downloadProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b10b767845ac951e1364e15c7f6f1d729882e0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539511"
---
# <a name="iwmpnetworkdownloadprogress-property"></a><span data-ttu-id="42500-106">IWMPNetwork ::d propriété ownloadProgress</span><span class="sxs-lookup"><span data-stu-id="42500-106">IWMPNetwork::downloadProgress property</span></span>

<span data-ttu-id="42500-107">La propriété **downloadProgress** obtient le pourcentage de téléchargement terminé.</span><span class="sxs-lookup"><span data-stu-id="42500-107">The **downloadProgress** property gets the percentage of downloading completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="42500-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42500-108">Syntax</span></span>


```CSharp
public System.Int32 downloadProgress {get; set;}
```


```VB

Public ReadOnly Property downloadProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="42500-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="42500-109">Property value</span></span>

<span data-ttu-id="42500-110">**System. Int32** qui est la progression du téléchargement exprimée sous forme de pourcentage.</span><span class="sxs-lookup"><span data-stu-id="42500-110">A **System.Int32** that is the download progress expressed as a percentage.</span></span>

## <a name="remarks"></a><span data-ttu-id="42500-111">Notes</span><span class="sxs-lookup"><span data-stu-id="42500-111">Remarks</span></span>

<span data-ttu-id="42500-112">Lorsque le contrôle du lecteur Windows Media est connecté à un fichier multimédia numérique qui peut être lu et téléchargé en même temps, la propriété **downloadProgress** obtient le pourcentage du fichier total téléchargé.</span><span class="sxs-lookup"><span data-stu-id="42500-112">When the Windows Media Player control is connected to a digital media file that can be played and downloaded at the same time, the **downloadProgress** property gets the percentage of the total file that has been downloaded.</span></span> <span data-ttu-id="42500-113">Cette fonctionnalité est actuellement prise en charge uniquement pour les fichiers multimédias numériques téléchargés à partir de serveurs Web.</span><span class="sxs-lookup"><span data-stu-id="42500-113">This feature is currently supported only for digital media files downloaded from web servers.</span></span> <span data-ttu-id="42500-114">Un fichier de l’un des formats suivants peut être téléchargé et lu simultanément :</span><span class="sxs-lookup"><span data-stu-id="42500-114">A file of any of the following formats can be downloaded and played simultaneously:</span></span>

-   <span data-ttu-id="42500-115">ASF (Advanced Systems Format)</span><span class="sxs-lookup"><span data-stu-id="42500-115">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="42500-116">Audio Windows Media (WMA)</span><span class="sxs-lookup"><span data-stu-id="42500-116">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="42500-117">Vidéo Windows Media (WMV)</span><span class="sxs-lookup"><span data-stu-id="42500-117">Windows Media Video (WMV)</span></span>
-   <span data-ttu-id="42500-118">MP3</span><span class="sxs-lookup"><span data-stu-id="42500-118">MP3</span></span>
-   <span data-ttu-id="42500-119">MPEG4</span><span class="sxs-lookup"><span data-stu-id="42500-119">MPEG</span></span>
-   <span data-ttu-id="42500-120">WAV</span><span class="sxs-lookup"><span data-stu-id="42500-120">WAV</span></span>

<span data-ttu-id="42500-121">En outre, certains fichiers AVI peuvent être téléchargés et lus simultanément.</span><span class="sxs-lookup"><span data-stu-id="42500-121">In addition, some AVI files can be downloaded and played simultaneously.</span></span>

<span data-ttu-id="42500-122">Utilisez **AxWindowsMediaPlayer. \_ WMPOCXEvents \_ BufferingEvent** pour déterminer à quel moment la mise en mémoire tampon démarre ou s’arrête.</span><span class="sxs-lookup"><span data-stu-id="42500-122">Use the **AxWindowsMediaPlayer.\_WMPOCXEvents\_BufferingEvent** to determine when buffering starts or stops.</span></span>

## <a name="examples"></a><span data-ttu-id="42500-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="42500-123">Examples</span></span>

<span data-ttu-id="42500-124">L’exemple de code suivant utilise **downloadProgress** pour afficher le pourcentage de téléchargement effectué.</span><span class="sxs-lookup"><span data-stu-id="42500-124">The following code example uses **downloadProgress** to display the percentage of downloading completed.</span></span> <span data-ttu-id="42500-125">Les informations s’affichent dans une étiquette, en réponse à l’événement de **mise en mémoire tampon** .</span><span class="sxs-lookup"><span data-stu-id="42500-125">The information is displayed in a label, in response to the **Buffering** Event.</span></span> <span data-ttu-id="42500-126">L’exemple utilise un minuteur avec un intervalle de 1 seconde pour mettre à jour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="42500-126">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="42500-127">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="42500-127">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Determine whether buffering has started or stopped.
    if (e.start == true)
    {
        // Set the timer interval at one second (1000 miliseconds).
        timer.Interval = 1000;
        
        // Start the timer.
        timer.Start();
    }
    else
    {
        // Buffering is complete. Stop the timer.
        timer.Stop();
    }
}

// Update the download progress in a timer event handler.
private void UpdateDownloadProgress(object sender, EventArgs e)
{
    downloadProgressLabel.Text = ("Download progress: " + player.network.downloadProgress + " percent complete");
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

    &#39; Test whether packets may be arriving.
    Select Case e.newState

    &#39; If WMPPlayState is Stopped, Paused, ScanForward, ScanReverse, Waiting, MediaEnded
    &#39; or Transitioning then stop the timer. 
        Case 1
        Case 2
        Case 4
        Case 5
        Case 7
        Case 8
        Case 9
            timer.Stop()

        &#39; If WMPPlayState is Playing or Buffering then set the timer interval and start the timer.
        Case Else
            timer.Interval = 1000
            timer.Start()

    End Select

End Sub

&#39; Update the download progress in a timer event handler.
Public Sub UpdateDownloadProgress(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    downloadProgressLabel.Text = (&quot;Download progress: &quot; + player.network.downloadProgress + &quot; percent complete&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="42500-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42500-128">Requirements</span></span>



| <span data-ttu-id="42500-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42500-129">Requirement</span></span> | <span data-ttu-id="42500-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="42500-130">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42500-131">Version</span><span class="sxs-lookup"><span data-stu-id="42500-131">Version</span></span><br/>   | <span data-ttu-id="42500-132">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="42500-132">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="42500-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="42500-133">Namespace</span></span><br/> | <span data-ttu-id="42500-134">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="42500-134">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="42500-135">Assembly</span><span class="sxs-lookup"><span data-stu-id="42500-135">Assembly</span></span><br/>  | <dl> <span data-ttu-id="42500-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="42500-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42500-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42500-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42500-138">**AxWindowsMediaPlayer. Buffering, événement (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="42500-138">**AxWindowsMediaPlayer.Buffering Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[<span data-ttu-id="42500-139">**Interface IWMPNetwork (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="42500-139">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





