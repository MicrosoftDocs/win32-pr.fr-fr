---
title: IWMPControls Stop, méthode
description: La méthode Stop arrête la lecture de l’élément multimédia. | IWMPControls Stop, méthode
ms.assetid: 4be601af-6321-4115-a94d-cfc9228991cb
keywords:
- méthode Stop lecteur Windows Media
- méthode Stop lecteur Windows Media, interface IWMPControls
- Interface IWMPControls Windows Media Player, stop, méthode
topic_type:
- apiref
api_name:
- IWMPControls.stop
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a73271098340ea0cf0a645472b5ef6333ae0f4b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528989"
---
# <a name="iwmpcontrolsstop-method"></a><span data-ttu-id="6976e-107">IWMPControls :: Stop, méthode</span><span class="sxs-lookup"><span data-stu-id="6976e-107">IWMPControls::stop method</span></span>

<span data-ttu-id="6976e-108">La méthode **Stop** arrête la lecture de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="6976e-108">The **stop** method stops playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="6976e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6976e-109">Syntax</span></span>


```CSharp
public void stop();
```


```VB

Public Sub stop()
Implements IWMPControls.stop
```





## <a name="parameters"></a><span data-ttu-id="6976e-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6976e-110">Parameters</span></span>

<span data-ttu-id="6976e-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="6976e-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6976e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6976e-112">Return value</span></span>

<span data-ttu-id="6976e-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6976e-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6976e-114">Notes</span><span class="sxs-lookup"><span data-stu-id="6976e-114">Remarks</span></span>

<span data-ttu-id="6976e-115">Cette méthode force le lecteur Windows Media à libérer toutes les ressources système qu’il utilise, telles que le périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="6976e-115">This method causes Windows Media Player to release any system resources it is using, such as the audio device.</span></span> <span data-ttu-id="6976e-116">Toutefois, l’élément multimédia actuel n’est pas libéré.</span><span class="sxs-lookup"><span data-stu-id="6976e-116">The current media item, however, is not released.</span></span>

<span data-ttu-id="6976e-117">Lorsque le lecteur Windows Media est arrêté, la position de lecture actuelle dans l’élément multimédia est réinitialisée au début de l’élément.</span><span class="sxs-lookup"><span data-stu-id="6976e-117">When Windows Media Player is stopped, the current playback position in the media item is reset to the beginning of the item.</span></span> <span data-ttu-id="6976e-118">Par la suite, l’appel de **IWMPControls. Play** démarre la lecture à partir du début de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="6976e-118">Subsequently calling **IWMPControls.play** will start playback from the beginning of the media item.</span></span> <span data-ttu-id="6976e-119">Pour arrêter une opération de lecture sans modifier la position actuelle, utilisez la méthode **IWMPControls. pause** .</span><span class="sxs-lookup"><span data-stu-id="6976e-119">To halt a play operation without changing the current position, use the **IWMPControls.pause** method.</span></span>

## <a name="examples"></a><span data-ttu-id="6976e-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="6976e-120">Examples</span></span>

<span data-ttu-id="6976e-121">L’exemple suivant utilise **Stop** pour arrêter l’élément multimédia en cours en réponse à l’événement Click d’un bouton.</span><span class="sxs-lookup"><span data-stu-id="6976e-121">The following example uses **stop** to stop the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="6976e-122">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="6976e-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void stopButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("stop"))
    {
        controls.stop();
    }
}
```


```VB

Public Sub stopButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles stopButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;stop&quot;)) Then

        controls.stop()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="6976e-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6976e-123">Requirements</span></span>



| <span data-ttu-id="6976e-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6976e-124">Requirement</span></span> | <span data-ttu-id="6976e-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="6976e-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6976e-126">Version</span><span class="sxs-lookup"><span data-stu-id="6976e-126">Version</span></span><br/>   | <span data-ttu-id="6976e-127">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="6976e-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6976e-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6976e-128">Namespace</span></span><br/> | <span data-ttu-id="6976e-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="6976e-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6976e-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="6976e-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6976e-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6976e-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6976e-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6976e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6976e-133">**Interface IWMPControls (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="6976e-133">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6976e-134">**IWMPControls. Next (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="6976e-134">**IWMPControls.next (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6976e-135">**IWMPControls. pause (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="6976e-135">**IWMPControls.pause (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6976e-136">**IWMPControls. Play (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="6976e-136">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6976e-137">**IWMPControls. Previous (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="6976e-137">**IWMPControls.previous (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> </dl>

 

 





