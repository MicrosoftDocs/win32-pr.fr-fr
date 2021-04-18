---
title: IWMPControls méthode Previous
description: La méthode Previous définit l’élément précédent dans la playlist comme élément actuel.
ms.assetid: 380524f5-e8b6-45c4-9f6c-3dbb49b1ac9f
keywords:
- méthode précédente lecteur Windows Media
- méthode précédente lecteur Windows Media, interface IWMPControls
- Interface IWMPControls lecteur Windows Media, méthode précédente
topic_type:
- apiref
api_name:
- IWMPControls.previous
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823038205a026afb7141491f562698eb60515a5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533321"
---
# <a name="iwmpcontrolsprevious-method"></a><span data-ttu-id="9ea3e-106">IWMPControls ::p méthode précédent</span><span class="sxs-lookup"><span data-stu-id="9ea3e-106">IWMPControls::previous method</span></span>

<span data-ttu-id="9ea3e-107">La méthode **Previous** définit l’élément précédent dans la playlist comme élément actuel.</span><span class="sxs-lookup"><span data-stu-id="9ea3e-107">The **previous** method sets the previous item in the playlist as the current item.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ea3e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ea3e-108">Syntax</span></span>


```CSharp
public void previous();
```


```VB

Public Sub previous()
Implements IWMPControls.previous
```





## <a name="parameters"></a><span data-ttu-id="9ea3e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ea3e-109">Parameters</span></span>

<span data-ttu-id="9ea3e-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="9ea3e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9ea3e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9ea3e-111">Return value</span></span>

<span data-ttu-id="9ea3e-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9ea3e-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ea3e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="9ea3e-113">Remarks</span></span>

<span data-ttu-id="9ea3e-114">Si la sélection se trouve sur la première entrée lors de l’appel de la méthode **précédente** , la dernière entrée de la sélection deviendra celle en cours.</span><span class="sxs-lookup"><span data-stu-id="9ea3e-114">If the playlist is on the first entry when **previous** is invoked, the last entry in the playlist will become the current one.</span></span>

## <a name="examples"></a><span data-ttu-id="9ea3e-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="9ea3e-115">Examples</span></span>

<span data-ttu-id="9ea3e-116">L’exemple suivant utilise **Previous** pour passer à l’élément précédent de la sélection actuelle en réponse à l’événement Click d’un bouton.</span><span class="sxs-lookup"><span data-stu-id="9ea3e-116">The following example uses **previous** to move to the previous item in the current playlist in response to the Click event of a button.</span></span> <span data-ttu-id="9ea3e-117">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="9ea3e-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void previousButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("previous"))
    {
        controls.previous();
    }
}
```


```VB

Public Sub previousButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles previousButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;previous&quot;)) Then

        controls.previous()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="9ea3e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ea3e-118">Requirements</span></span>



| <span data-ttu-id="9ea3e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ea3e-119">Requirement</span></span> | <span data-ttu-id="9ea3e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ea3e-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ea3e-121">Version</span><span class="sxs-lookup"><span data-stu-id="9ea3e-121">Version</span></span><br/>   | <span data-ttu-id="9ea3e-122">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9ea3e-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="9ea3e-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9ea3e-123">Namespace</span></span><br/> | <span data-ttu-id="9ea3e-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="9ea3e-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="9ea3e-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="9ea3e-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9ea3e-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9ea3e-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ea3e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ea3e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ea3e-128">**Interface IWMPControls (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="9ea3e-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9ea3e-129">**IWMPControls. Next (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="9ea3e-129">**IWMPControls.next (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9ea3e-130">**IWMPControls. Stop (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="9ea3e-130">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> </dl>

 

 





