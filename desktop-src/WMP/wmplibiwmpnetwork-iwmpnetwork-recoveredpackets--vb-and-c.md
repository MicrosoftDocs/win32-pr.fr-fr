---
title: IWMPNetwork propriété recoveredPackets
description: La propriété recoveredPackets obtient le nombre de paquets récupérés.
ms.assetid: 90fcefcd-2bd7-4fb5-8337-36bec5d44e60
keywords:
- propriété recoveredPackets lecteur Windows Media
- propriété recoveredPackets lecteur Windows Media, interface IWMPNetwork
- Interface IWMPNetwork lecteur Windows Media, propriété recoveredPackets
topic_type:
- apiref
api_name:
- IWMPNetwork.recoveredPackets
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe9fb8b44249be30289abb2f8922343285ca074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525665"
---
# <a name="iwmpnetworkrecoveredpackets-property"></a><span data-ttu-id="314ef-106">IWMPNetwork :: recoveredPackets, propriété</span><span class="sxs-lookup"><span data-stu-id="314ef-106">IWMPNetwork::recoveredPackets property</span></span>

<span data-ttu-id="314ef-107">La propriété **recoveredPackets** obtient le nombre de paquets récupérés.</span><span class="sxs-lookup"><span data-stu-id="314ef-107">The **recoveredPackets** property gets the number of recovered packets.</span></span>

## <a name="syntax"></a><span data-ttu-id="314ef-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="314ef-108">Syntax</span></span>


```CSharp
public System.Int32 recoveredPackets {get; set;}
```


```VB

Public ReadOnly Property recoveredPackets As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="314ef-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="314ef-109">Property value</span></span>

<span data-ttu-id="314ef-110">**System. Int32** qui correspond au nombre de paquets récupérés.</span><span class="sxs-lookup"><span data-stu-id="314ef-110">A **System.Int32** that is the number of recovered packets.</span></span>

## <a name="remarks"></a><span data-ttu-id="314ef-111">Notes</span><span class="sxs-lookup"><span data-stu-id="314ef-111">Remarks</span></span>

<span data-ttu-id="314ef-112">Chaque fois que la lecture est arrêtée et redémarrée, cette propriété est réinitialisée à zéro.</span><span class="sxs-lookup"><span data-stu-id="314ef-112">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="314ef-113">La valeur n’est pas réinitialisée si la lecture est suspendue.</span><span class="sxs-lookup"><span data-stu-id="314ef-113">The value is not reset if playback is paused.</span></span>

<span data-ttu-id="314ef-114">Cette propriété obtient des informations valides uniquement au moment de l’exécution lorsque l’URL pour la lecture est définie à l’aide de la propriété **AxWindowsMediaPlayer. URL** .</span><span class="sxs-lookup"><span data-stu-id="314ef-114">This property gets valid information only during run time when the URL for playback is set by using the **AxWindowsMediaPlayer.URL** property.</span></span> <span data-ttu-id="314ef-115">La valeur sera égale à zéro lors de l’utilisation du protocole HTTP, qui est sans perte.</span><span class="sxs-lookup"><span data-stu-id="314ef-115">The value will be zero when using the HTTP protocol, which is lossless.</span></span>

## <a name="examples"></a><span data-ttu-id="314ef-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="314ef-116">Examples</span></span>

<span data-ttu-id="314ef-117">L’exemple suivant utilise **recoveredPackets** pour afficher le nombre de paquets récupérés dans une étiquette, en réponse à l’événement **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="314ef-117">The following example uses **recoveredPackets** to display the number of recovered packets in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="314ef-118">L’exemple utilise un minuteur avec un intervalle de 1 seconde pour mettre à jour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="314ef-118">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="314ef-119">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="314ef-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


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

private void UpdateRecoveredPackets(object sender, EventArgs e)
{
    recoveredPacketsLabel.Text = ("Packets recovered: " + player.network.recoveredPackets.ToString());
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

Public Sub UpdateRecoveredPackets(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    recoveredPacketsLabel.Text = (&quot;Packets recovered: &quot; + player.network.recoveredPackets.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="314ef-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="314ef-120">Requirements</span></span>



| <span data-ttu-id="314ef-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="314ef-121">Requirement</span></span> | <span data-ttu-id="314ef-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="314ef-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="314ef-123">Version</span><span class="sxs-lookup"><span data-stu-id="314ef-123">Version</span></span><br/>   | <span data-ttu-id="314ef-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="314ef-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="314ef-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="314ef-125">Namespace</span></span><br/> | <span data-ttu-id="314ef-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="314ef-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="314ef-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="314ef-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="314ef-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="314ef-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="314ef-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="314ef-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="314ef-130">**AxWindowsMediaPlayer. URL (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="314ef-130">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="314ef-131">**Interface IWMPNetwork (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="314ef-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





