---
title: Propriété de débit binaire IWMPNetwork
description: La propriété de débit binaire obtient la vitesse de transmission actuelle en cours de réception.
ms.assetid: f7dda557-3954-45ed-9eac-6d27109e2dfa
keywords:
- propriété de la vitesse de transmission Windows Media Player
- propriété de la vitesse de transmission Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork lecteur Windows Media, propriété de vitesse de transmission
topic_type:
- apiref
api_name:
- IWMPNetwork.bitRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64039eb960a928f5268643e18d1a01b9034d5d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528662"
---
# <a name="iwmpnetworkbitrate-property"></a><span data-ttu-id="25837-106">IWMPNetwork :: transmission binaire, propriété</span><span class="sxs-lookup"><span data-stu-id="25837-106">IWMPNetwork::bitRate property</span></span>

<span data-ttu-id="25837-107">La propriété de **débit** binaire obtient la vitesse de transmission actuelle en cours de réception.</span><span class="sxs-lookup"><span data-stu-id="25837-107">The **bitRate** property gets the current bit rate being received.</span></span>

## <a name="syntax"></a><span data-ttu-id="25837-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25837-108">Syntax</span></span>


```CSharp
public System.Int32 bitRate {get; set;}
```


```VB

Public ReadOnly Property bitRate As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="25837-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="25837-109">Property value</span></span>

<span data-ttu-id="25837-110">**System. Int32** qui correspond à la vitesse de transmission.</span><span class="sxs-lookup"><span data-stu-id="25837-110">A **System.Int32** that is the bit rate.</span></span>

## <a name="remarks"></a><span data-ttu-id="25837-111">Notes</span><span class="sxs-lookup"><span data-stu-id="25837-111">Remarks</span></span>

<span data-ttu-id="25837-112">La valeur de cette propriété est une combinaison des vitesses de transmission des flux vidéo et audio.</span><span class="sxs-lookup"><span data-stu-id="25837-112">The value of this property is a combination of the bit rates of both video and audio streams.</span></span>

## <a name="examples"></a><span data-ttu-id="25837-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="25837-113">Examples</span></span>

<span data-ttu-id="25837-114">L’exemple suivant utilise la vitesse de **transmission** pour afficher le taux binaire actuel.</span><span class="sxs-lookup"><span data-stu-id="25837-114">The following example uses **bitRate** to display the current media bit rate.</span></span> <span data-ttu-id="25837-115">Les informations s’affichent dans une étiquette en réponse à l’événement **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="25837-115">The information is displayed in a label in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="25837-116">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="25837-116">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the bitRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.bitRate != 0)
            {
                bitRateLabel.Text = "Current Bit Rate: " + player.network.bitRate + " K bits/second";
            }
            break;

        default:
            break;
    }
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Display the bitRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.bitRate <> 0) Then

                bitRateLabel.Text = &quot;Current Bit Rate: &quot; + player.network.bitRate + &quot; K bits/second&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="25837-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25837-117">Requirements</span></span>



| <span data-ttu-id="25837-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25837-118">Requirement</span></span> | <span data-ttu-id="25837-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="25837-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25837-120">Version</span><span class="sxs-lookup"><span data-stu-id="25837-120">Version</span></span><br/>   | <span data-ttu-id="25837-121">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="25837-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="25837-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="25837-122">Namespace</span></span><br/> | <span data-ttu-id="25837-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="25837-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="25837-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="25837-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="25837-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="25837-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25837-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25837-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25837-127">**Interface IWMPNetwork (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="25837-127">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





