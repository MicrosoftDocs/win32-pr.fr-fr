---
title: IWMPNetwork propriété lostPackets
description: La propriété lostPackets obtient le nombre de paquets perdus.
ms.assetid: 611218d3-c4d3-4d4e-835c-1e7a956b2718
keywords:
- propriété lostPackets lecteur Windows Media
- propriété lostPackets lecteur Windows Media, interface IWMPNetwork
- Interface IWMPNetwork lecteur Windows Media, propriété lostPackets
topic_type:
- apiref
api_name:
- IWMPNetwork.lostPackets
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd1adac5f4aa8b1f58c023a556af04b8eae4bd8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530992"
---
# <a name="iwmpnetworklostpackets-property"></a><span data-ttu-id="e1ee0-106">IWMPNetwork :: lostPackets, propriété</span><span class="sxs-lookup"><span data-stu-id="e1ee0-106">IWMPNetwork::lostPackets property</span></span>

<span data-ttu-id="e1ee0-107">La propriété **lostPackets** obtient le nombre de paquets perdus.</span><span class="sxs-lookup"><span data-stu-id="e1ee0-107">The **lostPackets** property gets the number of packets lost.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1ee0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1ee0-108">Syntax</span></span>


```CSharp
public System.Int32 lostPackets {get; set;}
```


```VB

Public ReadOnly Property lostPackets As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="e1ee0-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e1ee0-109">Property value</span></span>

<span data-ttu-id="e1ee0-110">**System. Int32** qui correspond au nombre de paquets perdus.</span><span class="sxs-lookup"><span data-stu-id="e1ee0-110">A **System.Int32** that is the number of lost packets.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1ee0-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e1ee0-111">Remarks</span></span>

<span data-ttu-id="e1ee0-112">Cette propriété comprend uniquement les paquets de diffusion multimédia en continu et retourne zéro lors de l’utilisation du protocole HTTP, qui est sans perte.</span><span class="sxs-lookup"><span data-stu-id="e1ee0-112">This property includes streaming media packets only, and will return zero when using the HTTP protocol, which is lossless.</span></span>

<span data-ttu-id="e1ee0-113">Les paquets peuvent être perdus pour plusieurs raisons, telles que le type et la qualité de la connexion réseau.</span><span class="sxs-lookup"><span data-stu-id="e1ee0-113">Packets can be lost for a number of reasons, such as the type and quality of the network connection.</span></span>

<span data-ttu-id="e1ee0-114">Chaque fois que la lecture est arrêtée et redémarrée, cette propriété est réinitialisée à zéro.</span><span class="sxs-lookup"><span data-stu-id="e1ee0-114">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="e1ee0-115">La valeur n’est pas réinitialisée si la lecture est suspendue.</span><span class="sxs-lookup"><span data-stu-id="e1ee0-115">The value is not reset if playback is paused.</span></span> <span data-ttu-id="e1ee0-116">Cette propriété obtient des informations valides uniquement au moment de l’exécution lorsque l’URL pour la lecture est définie à l’aide de la propriété **AxWindowsMediaPlayer. URL** .</span><span class="sxs-lookup"><span data-stu-id="e1ee0-116">This property gets valid information only during run time when the URL for playback is set by using the **AxWindowsMediaPlayer.URL** property.</span></span>

## <a name="examples"></a><span data-ttu-id="e1ee0-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="e1ee0-117">Examples</span></span>

<span data-ttu-id="e1ee0-118">L’exemple de code suivant utilise **lostPackets** pour afficher le nombre total de paquets perdus pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="e1ee0-118">The following code example uses **lostPackets** to display the total number of packets lost during playback.</span></span> <span data-ttu-id="e1ee0-119">Les informations s’affichent dans une étiquette lorsque l’utilisateur clique sur un bouton.</span><span class="sxs-lookup"><span data-stu-id="e1ee0-119">The information is displayed in a label when the user clicks a button.</span></span> <span data-ttu-id="e1ee0-120">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="e1ee0-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void showLostPackets_Click(object sender, System.EventArgs e)
{
    lostPacketsLabel.Text = ("Packets lost: " + player.network.lostPackets.ToString());
}
```


```VB

Public Sub showLostPackets_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showLostPackets.Click

    lostPacketsLabel.Text = (&quot;Packets lost: &quot; + player.network.lostPackets.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="e1ee0-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1ee0-121">Requirements</span></span>



| <span data-ttu-id="e1ee0-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1ee0-122">Requirement</span></span> | <span data-ttu-id="e1ee0-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1ee0-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1ee0-124">Version</span><span class="sxs-lookup"><span data-stu-id="e1ee0-124">Version</span></span><br/>   | <span data-ttu-id="e1ee0-125">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="e1ee0-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e1ee0-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e1ee0-126">Namespace</span></span><br/> | <span data-ttu-id="e1ee0-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e1ee0-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e1ee0-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="e1ee0-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e1ee0-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e1ee0-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1ee0-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1ee0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1ee0-131">**Interface IWMPNetwork (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="e1ee0-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e1ee0-132">**AxWindowsMediaPlayer. URL (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="e1ee0-132">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> </dl>

 

 





