---
title: Propriété de fréquence de IWMPNetwork
description: La propriété Parate obtient la fréquence d’images vidéo actuelle.
ms.assetid: 800ecf3d-3b2c-48f9-8fc4-c7c32757749a
keywords:
- propriété pafréquence Windows Media Player
- propriété de fréquence d’images lecteur Windows Media, interface IWMPNetwork
- Interface IWMPNetwork lecteur Windows Media, propriété cadence
topic_type:
- apiref
api_name:
- IWMPNetwork.frameRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c338a116588fa9f1c552feff15f220e08b0f66e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532529"
---
# <a name="iwmpnetworkframerate-property"></a><span data-ttu-id="a6918-106">IWMPNetwork :: cadence, propriété</span><span class="sxs-lookup"><span data-stu-id="a6918-106">IWMPNetwork::frameRate property</span></span>

<span data-ttu-id="a6918-107">La **propriété Parate obtient la fréquence** d’images vidéo actuelle.</span><span class="sxs-lookup"><span data-stu-id="a6918-107">The **frameRate** property gets the current video frame rate.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6918-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6918-108">Syntax</span></span>


```CSharp
public System.Int32 frameRate {get; set;}
```


```VB

Public ReadOnly Property frameRate As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="a6918-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a6918-109">Property value</span></span>

<span data-ttu-id="a6918-110">**System. Int32** qui correspond à la fréquence d’images actuelle en images par centaines de secondes.</span><span class="sxs-lookup"><span data-stu-id="a6918-110">A **System.Int32** that is the current frame rate in frames per hundred seconds.</span></span>

> [!Note]  
> <span data-ttu-id="a6918-111">Bien que la propriété **encodedFrameRate** mesure la fréquence d’images encodée en images par seconde **, la propriété** Parate mesure la fréquence d’images actuelle en images par centaines de secondes.</span><span class="sxs-lookup"><span data-stu-id="a6918-111">Although the **encodedFrameRate** property measures the encoded frame rate in frames per second, the **frameRate** property measures the current frame rate in frames per hundred seconds.</span></span> <span data-ttu-id="a6918-112">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="a6918-112">See Remarks.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="a6918-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a6918-113">Remarks</span></span>

<span data-ttu-id="a6918-114">La valeur de la fréquence d’images actuelle est retournée en images par centaines de secondes.</span><span class="sxs-lookup"><span data-stu-id="a6918-114">The current frame rate value is returned in frames per hundred seconds.</span></span> <span data-ttu-id="a6918-115">Par exemple, une valeur de 2998 indique 29,98 images par seconde (FPS).</span><span class="sxs-lookup"><span data-stu-id="a6918-115">For example, a value of 2998 indicates 29.98 frames per second (fps).</span></span>

## <a name="examples"></a><span data-ttu-id="a6918-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="a6918-116">Examples</span></span>

<span data-ttu-id="a6918-117">L’exemple de code suivant utilise une **cadence** pour afficher la fréquence d’images spécifiée lors de l’encodage du fichier.</span><span class="sxs-lookup"><span data-stu-id="a6918-117">The following code example uses **frameRate** to display the frame rate specified when the file was encoded.</span></span> <span data-ttu-id="a6918-118">Les informations s’affichent dans une étiquette en réponse à l’événement **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="a6918-118">The information is displayed in a label in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="a6918-119">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="a6918-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the frameRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.frameRate != 0)
            {
                frameRateLabel.Text = "Current Frame Rate: " + player.network.frameRate + " K bits/second";
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

    &#39; Display the frameRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.frameRate <> 0) Then

                frameRateLabel.Text = &quot;Current Frame Rate: &quot; + player.network.frameRate + &quot; K bits/second&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="a6918-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6918-120">Requirements</span></span>



| <span data-ttu-id="a6918-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6918-121">Requirement</span></span> | <span data-ttu-id="a6918-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6918-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6918-123">Version</span><span class="sxs-lookup"><span data-stu-id="a6918-123">Version</span></span><br/>   | <span data-ttu-id="a6918-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a6918-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a6918-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a6918-125">Namespace</span></span><br/> | <span data-ttu-id="a6918-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a6918-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a6918-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="a6918-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a6918-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a6918-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6918-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6918-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6918-130">**Interface IWMPNetwork (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="a6918-130">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a6918-131">**IWMPNetwork. encodedFrameRate (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="a6918-131">**IWMPNetwork.encodedFrameRate (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)
</dt> </dl>

 

 





