---
title: IWMPNetwork propriété encodedFrameRate
description: La propriété encodedFrameRate obtient la fréquence d’images vidéo spécifiée par l’auteur du contenu.
ms.assetid: 4faf5675-5bf3-485d-802f-a1f900ddae63
keywords:
- propriété encodedFrameRate lecteur Windows Media
- propriété encodedFrameRate lecteur Windows Media, interface IWMPNetwork
- Interface IWMPNetwork lecteur Windows Media, propriété encodedFrameRate
topic_type:
- apiref
api_name:
- IWMPNetwork.encodedFrameRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b4176a9c2492d0ce34ffd0936c48dbdef065d1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539510"
---
# <a name="iwmpnetworkencodedframerate-property"></a><span data-ttu-id="75f7d-106">IWMPNetwork :: encodedFrameRate, propriété</span><span class="sxs-lookup"><span data-stu-id="75f7d-106">IWMPNetwork::encodedFrameRate property</span></span>

<span data-ttu-id="75f7d-107">La propriété **encodedFrameRate** obtient la fréquence d’images vidéo spécifiée par l’auteur du contenu.</span><span class="sxs-lookup"><span data-stu-id="75f7d-107">The **encodedFrameRate** property gets the video frame rate specified by the content author.</span></span>

## <a name="syntax"></a><span data-ttu-id="75f7d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75f7d-108">Syntax</span></span>


```CSharp
public System.Int32 encodedFrameRate {get; set;}
```


```VB

Public ReadOnly Property encodedFrameRate As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="75f7d-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="75f7d-109">Property value</span></span>

<span data-ttu-id="75f7d-110">**System. Int32** qui correspond à la fréquence d’images encodée en images par seconde (FPS).</span><span class="sxs-lookup"><span data-stu-id="75f7d-110">A **System.Int32** that is the encoded frame rate in frames per second (fps).</span></span>

> [!Note]  
> <span data-ttu-id="75f7d-111">Bien que la propriété **encodedFrameRate** mesure la fréquence d’images encodée en images par seconde **, la propriété** Parate mesure la fréquence d’images actuelle en images par centaines de secondes.</span><span class="sxs-lookup"><span data-stu-id="75f7d-111">Although the **encodedFrameRate** property measures the encoded frame rate in frames per second, the **frameRate** property measures the current frame rate in frames per hundred seconds.</span></span>

 

## <a name="examples"></a><span data-ttu-id="75f7d-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="75f7d-112">Examples</span></span>

<span data-ttu-id="75f7d-113">L’exemple de code suivant utilise **encodedFrameRate** pour afficher la fréquence d’images spécifiée lors de l’encodage du fichier.</span><span class="sxs-lookup"><span data-stu-id="75f7d-113">The following code example uses **encodedFrameRate** to display the frame rate specified when the file was encoded.</span></span> <span data-ttu-id="75f7d-114">Les informations s’affichent dans une étiquette, en réponse à l’événement **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="75f7d-114">The information is displayed in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="75f7d-115">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="75f7d-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the encodedFrameRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.encodedFrameRate != 0)
            {
                encodedFrameRateLabel.Text = "Current Encoded Frame Rate: " + player.network.encodedFrameRate + " K bits/second";
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

    &#39; Display the encodedFrameRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.encodedFrameRate <> 0) Then

                encodedFrameRateLabel.Text = &quot;Current Encoded Frame Rate: &quot; + player.network.encodedFrameRate + &quot; K bits/second&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="75f7d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75f7d-116">Requirements</span></span>



| <span data-ttu-id="75f7d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75f7d-117">Requirement</span></span> | <span data-ttu-id="75f7d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="75f7d-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75f7d-119">Version</span><span class="sxs-lookup"><span data-stu-id="75f7d-119">Version</span></span><br/>   | <span data-ttu-id="75f7d-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="75f7d-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="75f7d-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="75f7d-121">Namespace</span></span><br/> | <span data-ttu-id="75f7d-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="75f7d-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="75f7d-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="75f7d-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="75f7d-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="75f7d-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75f7d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75f7d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75f7d-126">**Interface IWMPNetwork (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="75f7d-126">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="75f7d-127">**IWMPNetwork. cadence (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="75f7d-127">**IWMPNetwork.frameRate (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)
</dt> </dl>

 

 





