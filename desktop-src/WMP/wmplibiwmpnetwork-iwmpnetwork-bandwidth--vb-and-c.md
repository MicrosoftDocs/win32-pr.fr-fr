---
title: Propriété de bande passante IWMPNetwork
description: La propriété bandWidth obtient la bande passante actuelle de l’élément multimédia.
ms.assetid: 4355aa14-bca7-4b46-aad5-3e3796a54735
keywords:
- propriété de bande passante lecteur Windows Media
- propriété de bande passante lecteur Windows Media, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, propriété bandWidth
topic_type:
- apiref
api_name:
- IWMPNetwork.bandWidth
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df9a55f9d5c6724c428b75a4171c2e8b7ca13d18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533032"
---
# <a name="iwmpnetworkbandwidth-property"></a><span data-ttu-id="a4266-106">IWMPNetwork :: bandWidth, propriété</span><span class="sxs-lookup"><span data-stu-id="a4266-106">IWMPNetwork::bandWidth property</span></span>

<span data-ttu-id="a4266-107">La propriété **Bandwidth** obtient la bande passante actuelle de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="a4266-107">The **bandWidth** property gets the current bandwidth of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4266-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4266-108">Syntax</span></span>


```CSharp
public System.Int32 bandWidth {get; set;}
```


```VB

Public ReadOnly Property bandWidth As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="a4266-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a4266-109">Property value</span></span>

<span data-ttu-id="a4266-110">**System. Int32** qui correspond à la bande passante.</span><span class="sxs-lookup"><span data-stu-id="a4266-110">A **System.Int32** that is the bandwidth.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4266-111">Notes</span><span class="sxs-lookup"><span data-stu-id="a4266-111">Remarks</span></span>

<span data-ttu-id="a4266-112">La valeur récupérée via **AxWindowsMediaPlayer. URL** sera égale à zéro si l’URL n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="a4266-112">The value retrieved through **AxWindowsMediaPlayer.URL** will be zero if the URL is not set.</span></span> <span data-ttu-id="a4266-113">Cette propriété est valide uniquement pour le média de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="a4266-113">This property is valid only for streaming media.</span></span>

## <a name="examples"></a><span data-ttu-id="a4266-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="a4266-114">Examples</span></span>

<span data-ttu-id="a4266-115">L’exemple suivant utilise la **bande passante** pour afficher la bande passante du support actuel.</span><span class="sxs-lookup"><span data-stu-id="a4266-115">The following example uses **bandWidth** to display the current media bandwidth.</span></span> <span data-ttu-id="a4266-116">Les informations s’affichent dans une étiquette en réponse à l’événement **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="a4266-116">The information is displayed in a label in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="a4266-117">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="a4266-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the bandwidth when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.bandWidth != 0)
            {
                bandWidthLabel.Text = "Current Bandwidth: " + player.network.bandWidth + " K bits/second";
            }
            else
            {
                bandWidthLabel.Text = "Bandwidth is only available for streaming media.";
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

    &#39; Display the bandWidth when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.bandWidth <> 0) Then

                bandWidthLabel.Text = &quot;Current Bandwidth: &quot; + player.network.bandWidth + &quot; K bits/second&quot;

            Else

                bandWidthLabel.Text = &quot;Bandwidth is only available for streaming media.&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="a4266-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4266-118">Requirements</span></span>



| <span data-ttu-id="a4266-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4266-119">Requirement</span></span> | <span data-ttu-id="a4266-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4266-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4266-121">Version</span><span class="sxs-lookup"><span data-stu-id="a4266-121">Version</span></span><br/>   | <span data-ttu-id="a4266-122">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a4266-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a4266-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a4266-123">Namespace</span></span><br/> | <span data-ttu-id="a4266-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a4266-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a4266-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="a4266-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a4266-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a4266-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4266-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4266-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4266-128">**AxWindowsMediaPlayer. URL (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="a4266-128">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a4266-129">**Interface IWMPNetwork (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="a4266-129">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





