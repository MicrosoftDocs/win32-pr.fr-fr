---
title: IWMPNetwork propriété receptionQuality
description: La propriété receptionQuality obtient le pourcentage de paquets qui n’ont pas été perdus au cours des 30 dernières secondes.
ms.assetid: 103e6b8f-e029-4f53-93ac-b516896a7594
keywords:
- propriété receptionQuality lecteur Windows Media
- propriété receptionQuality lecteur Windows Media, interface IWMPNetwork
- Interface IWMPNetwork lecteur Windows Media, propriété receptionQuality
topic_type:
- apiref
api_name:
- IWMPNetwork.receptionQuality
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3703ffa29183937874c40053bd3c7ae3c85d75d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535406"
---
# <a name="iwmpnetworkreceptionquality-property"></a><span data-ttu-id="af1a2-106">IWMPNetwork :: receptionQuality, propriété</span><span class="sxs-lookup"><span data-stu-id="af1a2-106">IWMPNetwork::receptionQuality property</span></span>

<span data-ttu-id="af1a2-107">La propriété **receptionQuality** obtient le pourcentage de paquets qui n’ont pas été perdus au cours des 30 dernières secondes.</span><span class="sxs-lookup"><span data-stu-id="af1a2-107">The **receptionQuality** property gets the percentage of packets not lost in the last 30 seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="af1a2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af1a2-108">Syntax</span></span>


```CSharp
public System.Int32 receptionQuality {get; set;}
```


```VB

Public ReadOnly Property receptionQuality As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="af1a2-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="af1a2-109">Property value</span></span>

<span data-ttu-id="af1a2-110">**System. Int32** qui est la qualité de la réception.</span><span class="sxs-lookup"><span data-stu-id="af1a2-110">A **System.Int32** that is the reception quality.</span></span>

## <a name="remarks"></a><span data-ttu-id="af1a2-111">Notes</span><span class="sxs-lookup"><span data-stu-id="af1a2-111">Remarks</span></span>

<span data-ttu-id="af1a2-112">Le nombre de paquets reçus, perdus et récupérés pendant la diffusion en continu est analysé une fois par seconde.</span><span class="sxs-lookup"><span data-stu-id="af1a2-112">The number of packets received, lost, and recovered during streaming is monitored once every second.</span></span> <span data-ttu-id="af1a2-113">La propriété **receptionQuality** obtient le pourcentage de paquets qui n’ont pas été perdus au cours des 30 dernières secondes.</span><span class="sxs-lookup"><span data-stu-id="af1a2-113">The **receptionQuality** property gets the percentage of packets not lost during the last 30 seconds.</span></span>

<span data-ttu-id="af1a2-114">Chaque fois que la lecture est arrêtée et redémarrée, cette propriété est réinitialisée à zéro.</span><span class="sxs-lookup"><span data-stu-id="af1a2-114">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="af1a2-115">La valeur n’est pas réinitialisée si la lecture est suspendue.</span><span class="sxs-lookup"><span data-stu-id="af1a2-115">The value is not reset if playback is paused.</span></span>

<span data-ttu-id="af1a2-116">Cette propriété obtient des informations valides uniquement au moment de l’exécution lorsque l’URL pour la lecture est définie à l’aide de la propriété **AxWindowsMediaPlayer. URL** .</span><span class="sxs-lookup"><span data-stu-id="af1a2-116">This property gets valid information only during run time when the URL for playback is set by using the **AxWindowsMediaPlayer.URL** property.</span></span>

## <a name="examples"></a><span data-ttu-id="af1a2-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="af1a2-117">Examples</span></span>

<span data-ttu-id="af1a2-118">L’exemple suivant utilise **receptionQuality** pour afficher le pourcentage de paquets reçus dans une étiquette, en réponse à l’événement **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="af1a2-118">The following example uses **receptionQuality** to display the percentage of packets received in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="af1a2-119">L’exemple utilise un minuteur avec un intervalle de 1 seconde pour mettre à jour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="af1a2-119">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="af1a2-120">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="af1a2-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Test whether content is playing. 
    if (e.newState == 3)
    {
        // Start the timer. Update the display every 10 seconds.
        timer.Interval = 10000;
        timer.Start();
    }
    else
    {
        // Not playing; stop the timer.
        timer.Stop();
    }
}

private void UpdateReceptionQuality(object sender, EventArgs e)
{
    receptionQualityLabel.Text = ("Packets recovered: " + player.network.receptionQuality.ToString() + "%");
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

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

Public Sub UpdateReceptionQuality(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    receptionQualityLabel.Text = (&quot;Packets recovered: &quot; + player.network.receptionQuality.ToString() + &quot;%&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="af1a2-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af1a2-121">Requirements</span></span>



| <span data-ttu-id="af1a2-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af1a2-122">Requirement</span></span> | <span data-ttu-id="af1a2-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="af1a2-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af1a2-124">Version</span><span class="sxs-lookup"><span data-stu-id="af1a2-124">Version</span></span><br/>   | <span data-ttu-id="af1a2-125">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="af1a2-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="af1a2-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="af1a2-126">Namespace</span></span><br/> | <span data-ttu-id="af1a2-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="af1a2-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="af1a2-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="af1a2-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="af1a2-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="af1a2-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af1a2-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af1a2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af1a2-131">**AxWindowsMediaPlayer. URL (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="af1a2-131">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="af1a2-132">**Interface IWMPNetwork (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="af1a2-132">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





