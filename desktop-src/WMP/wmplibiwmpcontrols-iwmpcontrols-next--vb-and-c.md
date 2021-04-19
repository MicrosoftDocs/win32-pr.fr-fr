---
title: IWMPControls méthode Next
description: La méthode suivante définit l’élément suivant dans la sélection comme élément actuel.
ms.assetid: 3f82ef25-a1e0-4845-b0ed-dd6463719577
keywords:
- méthode suivante lecteur Windows Media
- méthode Next lecteur Windows Media, interface IWMPControls
- IWMPControls interface Windows Media Player, Next, méthode
topic_type:
- apiref
api_name:
- IWMPControls.next
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8444ba7d9209759cb64c4b582e1af9d074332ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540051"
---
# <a name="iwmpcontrolsnext-method"></a><span data-ttu-id="6ef90-106">IWMPControls :: Next, méthode</span><span class="sxs-lookup"><span data-stu-id="6ef90-106">IWMPControls::next method</span></span>

<span data-ttu-id="6ef90-107">La méthode **suivante** définit l’élément suivant dans la sélection comme élément actuel.</span><span class="sxs-lookup"><span data-stu-id="6ef90-107">The **next** method sets the next item in the playlist as the current item.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ef90-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ef90-108">Syntax</span></span>


```CSharp
public void next();
```


```VB

Public Sub next()
Implements IWMPControls.next
```





## <a name="parameters"></a><span data-ttu-id="6ef90-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ef90-109">Parameters</span></span>

<span data-ttu-id="6ef90-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="6ef90-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6ef90-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6ef90-111">Return value</span></span>

<span data-ttu-id="6ef90-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6ef90-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ef90-113">Notes</span><span class="sxs-lookup"><span data-stu-id="6ef90-113">Remarks</span></span>

<span data-ttu-id="6ef90-114">Si la sélection se trouve sur la dernière entrée **lors de** l’appel de la méthode, la première entrée de la sélection devient la dernière.</span><span class="sxs-lookup"><span data-stu-id="6ef90-114">If the playlist is on the last entry when **next** is invoked, the first entry in the playlist will become the current one.</span></span>

<span data-ttu-id="6ef90-115">Pour les sélections côté serveur, cette méthode passe à l’élément suivant dans la sélection côté serveur, et non à la sélection du client.</span><span class="sxs-lookup"><span data-stu-id="6ef90-115">For server-side playlists, this method skips to the next item in the server-side playlist, not the client playlist.</span></span>

<span data-ttu-id="6ef90-116">Lors de la lecture d’un DVD, cette méthode passe au chapitre logique suivant dans la séquence de lecture, qui peut ne pas être le chapitre suivant de la sélection.</span><span class="sxs-lookup"><span data-stu-id="6ef90-116">When playing a DVD, this method skips to the next logical chapter in the playback sequence, which may not be the next chapter in the playlist.</span></span> <span data-ttu-id="6ef90-117">Lors de la diffusion d’images continues sur DVD, cette méthode passe à l’image suivante.</span><span class="sxs-lookup"><span data-stu-id="6ef90-117">When playing DVD still images, this method skips to the next image.</span></span>

## <a name="examples"></a><span data-ttu-id="6ef90-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="6ef90-118">Examples</span></span>

<span data-ttu-id="6ef90-119">L’exemple suivant utilise **Next** pour passer à l’élément suivant dans la sélection en cours en réponse à l’événement Click d’un bouton.</span><span class="sxs-lookup"><span data-stu-id="6ef90-119">The following example uses **next** to move to the next item in the current playlist in response to the Click event of a button.</span></span> <span data-ttu-id="6ef90-120">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="6ef90-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void nextButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("next"))
    {
        controls.next();
    }
}
```


```VB

Public Sub nextButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles nextButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;next&quot;)) Then

        controls.next()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="6ef90-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ef90-121">Requirements</span></span>



| <span data-ttu-id="6ef90-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ef90-122">Requirement</span></span> | <span data-ttu-id="6ef90-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ef90-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ef90-124">Version</span><span class="sxs-lookup"><span data-stu-id="6ef90-124">Version</span></span><br/>   | <span data-ttu-id="6ef90-125">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="6ef90-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6ef90-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6ef90-126">Namespace</span></span><br/> | <span data-ttu-id="6ef90-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="6ef90-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6ef90-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="6ef90-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6ef90-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6ef90-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ef90-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ef90-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ef90-131">**Interface IWMPControls (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="6ef90-131">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6ef90-132">**IWMPControls. Previous (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="6ef90-132">**IWMPControls.previous (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6ef90-133">**IWMPControls. Stop (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="6ef90-133">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> </dl>

 

 





