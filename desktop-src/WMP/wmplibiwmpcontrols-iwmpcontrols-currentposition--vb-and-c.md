---
title: IWMPControls propriété currentPosition
description: La propriété currentPosition obtient ou définit la position actuelle dans l’élément multimédia, en secondes, à partir du début.
ms.assetid: 48f5241e-7528-485e-bf47-d655ba842af2
keywords:
- propriété currentPosition lecteur Windows Media
- propriété currentPosition lecteur Windows Media, interface IWMPControls
- Interface IWMPControls lecteur Windows Media, propriété currentPosition
topic_type:
- apiref
api_name:
- IWMPControls.currentPosition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fee8c2c8244d6034069f21033978ce2883ff852d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544121"
---
# <a name="iwmpcontrolscurrentposition-property"></a><span data-ttu-id="9b126-106">IWMPControls :: currentPosition, propriété</span><span class="sxs-lookup"><span data-stu-id="9b126-106">IWMPControls::currentPosition property</span></span>

<span data-ttu-id="9b126-107">La propriété **CurrentPosition** obtient ou définit la position actuelle dans l’élément multimédia, en secondes, à partir du début.</span><span class="sxs-lookup"><span data-stu-id="9b126-107">The **currentPosition** property gets or sets the current position in the media item in seconds from the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b126-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b126-108">Syntax</span></span>


```CSharp
public System.Double currentPosition {get; set;}
```


```VB

Public Property currentPosition As System.Double
```





## <a name="property-value"></a><span data-ttu-id="9b126-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9b126-109">Property value</span></span>

<span data-ttu-id="9b126-110">**System. double** qui correspond à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="9b126-110">A **System.Double** that is the current position.</span></span>

## <a name="examples"></a><span data-ttu-id="9b126-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="9b126-111">Examples</span></span>

<span data-ttu-id="9b126-112">L’exemple suivant utilise **CurrentPosition** pour rechercher une position fournie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9b126-112">The following example uses **currentPosition** to seek to a position provided by the user.</span></span> <span data-ttu-id="9b126-113">En réponse à un clic sur un bouton, **CurrentPosition** est défini sur la valeur entrée dans une zone de texte appelée NewPosition.</span><span class="sxs-lookup"><span data-stu-id="9b126-113">In response to a button click, **currentPosition** is set to the value entered in a text box called newPosition.</span></span> <span data-ttu-id="9b126-114">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="9b126-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setPosition_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text);
}
```


```VB

Public Sub setPosition_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setPosition.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="9b126-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b126-115">Requirements</span></span>



| <span data-ttu-id="9b126-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b126-116">Requirement</span></span> | <span data-ttu-id="9b126-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b126-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b126-118">Version</span><span class="sxs-lookup"><span data-stu-id="9b126-118">Version</span></span><br/>   | <span data-ttu-id="9b126-119">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9b126-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="9b126-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9b126-120">Namespace</span></span><br/> | <span data-ttu-id="9b126-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="9b126-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="9b126-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="9b126-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9b126-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9b126-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b126-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b126-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b126-125">**Interface IWMPControls (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="9b126-125">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9b126-126">**IWMPControls. currentPositionString (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="9b126-126">**IWMPControls.currentPositionString (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)
</dt> </dl>

 

 





