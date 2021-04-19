---
title: IWMPNetwork propriété framesSkipped
description: La propriété framesSkipped obtient le nombre total de trames ignorées lors de la lecture.
ms.assetid: eedecfa9-0c82-4800-979e-ca85fb78c480
keywords:
- propriété framesSkipped lecteur Windows Media
- propriété framesSkipped lecteur Windows Media, interface IWMPNetwork
- Interface IWMPNetwork lecteur Windows Media, propriété framesSkipped
topic_type:
- apiref
api_name:
- IWMPNetwork.framesSkipped
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8409cec50089111184f96e4463f57cc9c4fbae07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545480"
---
# <a name="iwmpnetworkframesskipped-property"></a><span data-ttu-id="ce0b6-106">IWMPNetwork :: framesSkipped, propriété</span><span class="sxs-lookup"><span data-stu-id="ce0b6-106">IWMPNetwork::framesSkipped property</span></span>

<span data-ttu-id="ce0b6-107">La propriété **framesSkipped** obtient le nombre total de trames ignorées lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="ce0b6-107">The **framesSkipped** property gets the total number of frames skipped during playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce0b6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce0b6-108">Syntax</span></span>


```CSharp
public System.Int32 framesSkipped {get; set;}
```


```VB

Public ReadOnly Property framesSkipped As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="ce0b6-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ce0b6-109">Property value</span></span>

<span data-ttu-id="ce0b6-110">**System. Int32** qui correspond au nombre de trames ignorées.</span><span class="sxs-lookup"><span data-stu-id="ce0b6-110">A **System.Int32** that is the number of frames skipped.</span></span>

## <a name="examples"></a><span data-ttu-id="ce0b6-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="ce0b6-111">Examples</span></span>

<span data-ttu-id="ce0b6-112">L’exemple de code suivant utilise **framesSkipped** pour afficher le nombre total de trames ignorées lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="ce0b6-112">The following code example uses **framesSkipped** to display the total number of frames skipped during playback.</span></span> <span data-ttu-id="ce0b6-113">Les informations s’affichent dans une étiquette lorsque l’utilisateur clique sur un bouton.</span><span class="sxs-lookup"><span data-stu-id="ce0b6-113">The information is displayed in a label when the user clicks a button.</span></span> <span data-ttu-id="ce0b6-114">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="ce0b6-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void showFramesSkipped_Click(object sender, System.EventArgs e)
{
    framesSkippedLabel.Text = ("Frames skipped: " + player.network.framesSkipped.ToString());
}
```


```VB

Public Sub showFramesSkipped_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showFramesSkipped.Click

    framesSkippedLabel.Text = (&quot;Frames skipped: &quot; + player.network.framesSkipped.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="ce0b6-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce0b6-115">Requirements</span></span>



| <span data-ttu-id="ce0b6-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce0b6-116">Requirement</span></span> | <span data-ttu-id="ce0b6-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce0b6-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce0b6-118">Version</span><span class="sxs-lookup"><span data-stu-id="ce0b6-118">Version</span></span><br/>   | <span data-ttu-id="ce0b6-119">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="ce0b6-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ce0b6-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ce0b6-120">Namespace</span></span><br/> | <span data-ttu-id="ce0b6-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ce0b6-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ce0b6-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="ce0b6-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ce0b6-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ce0b6-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce0b6-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce0b6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce0b6-125">**Interface IWMPNetwork (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="ce0b6-125">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





