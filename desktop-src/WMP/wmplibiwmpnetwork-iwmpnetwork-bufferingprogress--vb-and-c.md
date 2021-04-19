---
title: IWMPNetwork propriété bufferingProgress
description: La propriété bufferingProgress obtient le pourcentage de la mise en mémoire tampon terminée.
ms.assetid: 8dc9f31e-7c34-4714-a633-d92c3da3052b
keywords:
- propriété bufferingProgress lecteur Windows Media
- propriété bufferingProgress lecteur Windows Media, interface IWMPNetwork
- Interface IWMPNetwork lecteur Windows Media, propriété bufferingProgress
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1da8a27ba41e5c4e201a5bdf0197992c30bce80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535252"
---
# <a name="iwmpnetworkbufferingprogress-property"></a><span data-ttu-id="c25ea-106">IWMPNetwork :: bufferingProgress, propriété</span><span class="sxs-lookup"><span data-stu-id="c25ea-106">IWMPNetwork::bufferingProgress property</span></span>

<span data-ttu-id="c25ea-107">La propriété **bufferingProgress** obtient le pourcentage de la mise en mémoire tampon terminée.</span><span class="sxs-lookup"><span data-stu-id="c25ea-107">The **bufferingProgress** property gets the percentage of buffering completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c25ea-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c25ea-108">Syntax</span></span>


```CSharp
public System.Int32 bufferingProgress {get; set;}
```


```VB

Public ReadOnly Property bufferingProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="c25ea-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c25ea-109">Property value</span></span>

<span data-ttu-id="c25ea-110">**System. Int32** qui correspond à la progression de la mise en mémoire tampon exprimée en pourcentage.</span><span class="sxs-lookup"><span data-stu-id="c25ea-110">A **System.Int32** that is the buffering progress expressed as a percentage.</span></span>

## <a name="remarks"></a><span data-ttu-id="c25ea-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c25ea-111">Remarks</span></span>

<span data-ttu-id="c25ea-112">Chaque fois que la lecture est arrêtée et redémarrée, cette propriété est réinitialisée à zéro.</span><span class="sxs-lookup"><span data-stu-id="c25ea-112">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="c25ea-113">Elle n’est pas réinitialisée si la lecture est suspendue.</span><span class="sxs-lookup"><span data-stu-id="c25ea-113">It is not reset if playback is paused.</span></span>

<span data-ttu-id="c25ea-114">La mise en mémoire tampon s’applique uniquement au contenu de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="c25ea-114">Buffering applies only to streaming content.</span></span> <span data-ttu-id="c25ea-115">Cette propriété obtient des informations valides uniquement au moment de l’exécution lorsque l’URL pour la lecture est définie à l’aide de la propriété **AxWindowsMediaPlayer. URL** .</span><span class="sxs-lookup"><span data-stu-id="c25ea-115">This property gets valid information only during run time when the URL for playback is set using the **AxWindowsMediaPlayer.URL** property.</span></span>

<span data-ttu-id="c25ea-116">Utilisez **AxWindowsMediaPlayer. \_ WMPOCXEvents \_ BufferingEvent** pour déterminer à quel moment la mise en mémoire tampon démarre ou s’arrête.</span><span class="sxs-lookup"><span data-stu-id="c25ea-116">Use the **AxWindowsMediaPlayer.\_WMPOCXEvents\_BufferingEvent** to determine when buffering starts or stops.</span></span>

## <a name="examples"></a><span data-ttu-id="c25ea-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="c25ea-117">Examples</span></span>

<span data-ttu-id="c25ea-118">L’exemple suivant utilise **bufferingProgress** pour afficher le pourcentage de mise en mémoire tampon effectuée dans une étiquette, en réponse à l’événement de mise en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c25ea-118">The following example uses **bufferingProgress** to display the percentage of buffering completed in a label, in response to the Buffering Event.</span></span> <span data-ttu-id="c25ea-119">L’exemple utilise un minuteur avec un intervalle de 1 seconde pour mettre à jour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="c25ea-119">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="c25ea-120">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="c25ea-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


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

// Update the buffering progress in a timer event handler.
private void UpdateBufferingProgress(object sender, EventArgs e)
{
    bufferingProgressLabel.Text = ("Buffering progress: " + player.network.bufferingProgress + " percent complete");
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

&#39; Update the buffering progress in a timer event handler.
Public Sub UpdateBufferingProgress(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    bufferingProgressLabel.Text = (&quot;Buffering progress: &quot; + player.network.bufferingProgress + &quot; percent complete&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="c25ea-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c25ea-121">Requirements</span></span>



| <span data-ttu-id="c25ea-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c25ea-122">Requirement</span></span> | <span data-ttu-id="c25ea-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c25ea-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c25ea-124">Version</span><span class="sxs-lookup"><span data-stu-id="c25ea-124">Version</span></span><br/>   | <span data-ttu-id="c25ea-125">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="c25ea-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c25ea-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c25ea-126">Namespace</span></span><br/> | <span data-ttu-id="c25ea-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c25ea-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c25ea-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="c25ea-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c25ea-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c25ea-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c25ea-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c25ea-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c25ea-131">**AxWindowsMediaPlayer. URL (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="c25ea-131">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c25ea-132">**AxWindowsMediaPlayer. Buffering, événement (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="c25ea-132">**AxWindowsMediaPlayer.Buffering Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[<span data-ttu-id="c25ea-133">**Interface IWMPNetwork (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="c25ea-133">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





