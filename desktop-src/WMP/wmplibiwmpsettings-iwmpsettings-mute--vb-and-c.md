---
title: IWMPSettings muet, propriété
description: La propriété Mute obtient ou définit une valeur indiquant si l’audio est muet.
ms.assetid: d99e47db-70cc-41e0-aca9-b765b075e7b4
keywords:
- propriété muet Windows Media Player
- propriété muet lecteur Windows Media, interface IWMPSettings
- Interface IWMPSettings lecteur Windows Media, propriété muet
topic_type:
- apiref
api_name:
- IWMPSettings.mute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67518bb9a6eccee13e4cc262f37341d30689439e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535424"
---
# <a name="iwmpsettingsmute-property"></a><span data-ttu-id="bb5ea-106">IWMPSettings :: Mute, propriété</span><span class="sxs-lookup"><span data-stu-id="bb5ea-106">IWMPSettings::mute property</span></span>

<span data-ttu-id="bb5ea-107">La propriété **Mute** obtient ou définit une valeur indiquant si l’audio est muet.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-107">The **mute** property gets or sets a value indicating whether audio is muted.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb5ea-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb5ea-108">Syntax</span></span>


```CSharp
public System.Boolean mute {get; set;}
```


```VB

Public Property mute As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="bb5ea-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="bb5ea-109">Property value</span></span>

<span data-ttu-id="bb5ea-110">Valeur **System. Boolean** indiquant si l’audio est muet.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-110">A **System.Boolean** value indicating whether audio is muted.</span></span> <span data-ttu-id="bb5ea-111">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-111">The default is **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="bb5ea-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="bb5ea-112">Examples</span></span>

<span data-ttu-id="bb5ea-113">L’exemple suivant permet de créer une case à cocher et de basculer la propriété **muet** sur muet et de désactiver l’audio lorsque l’état activé de la case est modifié.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-113">The following example creates a check box, and toggles the **mute** property to mute and un-mute audio when the checked state of the box is changed.</span></span> <span data-ttu-id="bb5ea-114">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-114">**AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void Mute_CheckStateChanged(object sender, System.EventArgs e)
{
    System.Windows.Forms.CheckBox Mute = (System.Windows.Forms.CheckBox)sender;

    // Change the check box text depending on the checked state.
    Mute.Text = Mute.Checked ? "Un-mute Audio" : Mute.Text = "Mute Audio";

    // Use the checked state to set the mute property. 
    player.settings.mute = Mute.Checked;
}
```


```VB

Public Sub Mute_CheckStateChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles Mute.CheckStateChanged

    Dim cb As System.Windows.Forms.CheckBox = sender

    &#39;  Change the check box text depending on the checked state.
    If (cb.Checked) Then

        cb.Text = &quot;Un-mute Audio&quot;

    Else

        cb.Text = &quot;Mute Audio&quot;

    End If

    &#39;  Use the checked state to set the mute property. 
    player.settings.mute = cb.Checked

End Sub
```





## <a name="requirements"></a><span data-ttu-id="bb5ea-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb5ea-115">Requirements</span></span>



| <span data-ttu-id="bb5ea-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb5ea-116">Requirement</span></span> | <span data-ttu-id="bb5ea-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb5ea-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb5ea-118">Version</span><span class="sxs-lookup"><span data-stu-id="bb5ea-118">Version</span></span><br/>   | <span data-ttu-id="bb5ea-119">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="bb5ea-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="bb5ea-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bb5ea-120">Namespace</span></span><br/> | <span data-ttu-id="bb5ea-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="bb5ea-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="bb5ea-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="bb5ea-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="bb5ea-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="bb5ea-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb5ea-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb5ea-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb5ea-125">**Interface IWMPSettings (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="bb5ea-125">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bb5ea-126">**IWMPSettings. rate (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="bb5ea-126">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





