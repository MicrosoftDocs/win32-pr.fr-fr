---
title: IWMPNetwork propriété receivedPackets
description: La propriété receivedPackets obtient le nombre de paquets reçus.
ms.assetid: 2a79dc81-4c7a-45d6-bc2b-b19ff5704c3b
keywords:
- propriété receivedPackets lecteur Windows Media
- propriété receivedPackets lecteur Windows Media, interface IWMPNetwork
- Interface IWMPNetwork lecteur Windows Media, propriété receivedPackets
topic_type:
- apiref
api_name:
- IWMPNetwork.receivedPackets
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90c62b4d90039f07177e8fcdc971cb66e0044aee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541532"
---
# <a name="iwmpnetworkreceivedpackets-property"></a><span data-ttu-id="95962-106">IWMPNetwork :: receivedPackets, propriété</span><span class="sxs-lookup"><span data-stu-id="95962-106">IWMPNetwork::receivedPackets property</span></span>

<span data-ttu-id="95962-107">La propriété **receivedPackets** obtient le nombre de paquets reçus.</span><span class="sxs-lookup"><span data-stu-id="95962-107">The **receivedPackets** property gets the number of packets received.</span></span>

## <a name="syntax"></a><span data-ttu-id="95962-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95962-108">Syntax</span></span>


```CSharp
public System.Int32 receivedPackets {get; set;}
```


```VB

Public ReadOnly Property receivedPackets As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="95962-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="95962-109">Property value</span></span>

<span data-ttu-id="95962-110">**System. Int32** qui correspond au nombre de paquets reçus.</span><span class="sxs-lookup"><span data-stu-id="95962-110">A **System.Int32** that is the number of packets received.</span></span>

## <a name="remarks"></a><span data-ttu-id="95962-111">Notes</span><span class="sxs-lookup"><span data-stu-id="95962-111">Remarks</span></span>

<span data-ttu-id="95962-112">Chaque fois que la lecture est arrêtée et redémarrée, cette propriété est réinitialisée à zéro.</span><span class="sxs-lookup"><span data-stu-id="95962-112">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="95962-113">La valeur n’est pas réinitialisée si la lecture est suspendue.</span><span class="sxs-lookup"><span data-stu-id="95962-113">The value is not reset if playback is paused.</span></span>

## <a name="examples"></a><span data-ttu-id="95962-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="95962-114">Examples</span></span>

<span data-ttu-id="95962-115">L’exemple suivant utilise **receivedPackets** pour afficher le nombre de paquets reçus.</span><span class="sxs-lookup"><span data-stu-id="95962-115">The following example uses **receivedPackets** to display the number of packets received.</span></span> <span data-ttu-id="95962-116">Les informations s’affichent dans une étiquette en réponse à l’événement **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="95962-116">The information is displayed in a label in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="95962-117">L’exemple utilise un minuteur avec un intervalle de 1 seconde pour mettre à jour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="95962-117">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="95962-118">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="95962-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Test whether packets may be arriving.
    switch (e.newState)
    {
        // If WMPPlayState is Stopped, Paused, ScanForward, ScanReverse, Waiting, MediaEnded
        // or Transitioning then stop the timer. 
        case 1: 
        case 2: 
        case 4: 
        case 5: 
        case 7: 
        case 8: 
        case 9: 
            timer.Stop();
            break;

        // If WMPPlayState is Playing or Buffering then set the timer interval and start the timer.
        default:
            timer.Interval = 1000;
            timer.Start();
            break;
    }
}

private void UpdateReceivedPackets(object sender, EventArgs e)
{
    receivedPacketsLabel.Text = ("Packets received: " + player.network.receivedPackets.ToString());
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

Public Sub UpdateReceivedPackets(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    receivedPacketsLabel.Text = (&quot;Packets received: &quot; + player.network.receivedPackets.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="95962-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95962-119">Requirements</span></span>



| <span data-ttu-id="95962-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95962-120">Requirement</span></span> | <span data-ttu-id="95962-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="95962-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95962-122">Version</span><span class="sxs-lookup"><span data-stu-id="95962-122">Version</span></span><br/>   | <span data-ttu-id="95962-123">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="95962-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="95962-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="95962-124">Namespace</span></span><br/> | <span data-ttu-id="95962-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="95962-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="95962-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="95962-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="95962-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="95962-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95962-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95962-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95962-129">**Interface IWMPNetwork (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="95962-129">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





