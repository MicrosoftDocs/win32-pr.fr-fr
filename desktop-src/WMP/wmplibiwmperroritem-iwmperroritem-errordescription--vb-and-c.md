---
title: Propriété errorDescription IWMPErrorItem
description: La propriété errorDescription obtient une description de l’erreur.
ms.assetid: a9914c24-1d10-422a-bcba-80be9fb85108
keywords:
- propriété errorDescription Windows Media Player
- propriété errorDescription lecteur Windows Media, interface IWMPErrorItem
- Interface IWMPErrorItem lecteur Windows Media, propriété errorDescription
topic_type:
- apiref
api_name:
- IWMPErrorItem.errorDescription
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8725099d1ce49eae8f378b2571dc4030f60611e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526439"
---
# <a name="iwmperroritemerrordescription-property"></a><span data-ttu-id="cc884-106">IWMPErrorItem :: errorDescription, propriété</span><span class="sxs-lookup"><span data-stu-id="cc884-106">IWMPErrorItem::errorDescription property</span></span>

<span data-ttu-id="cc884-107">La propriété **errorDescription** obtient une description de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="cc884-107">The **errorDescription** property gets a description of the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc884-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc884-108">Syntax</span></span>


```CSharp
public System.String errorDescription {get; set;}
```


```VB

Public ReadOnly Property errorDescription As System.String
```





## <a name="property-value"></a><span data-ttu-id="cc884-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="cc884-109">Property value</span></span>

<span data-ttu-id="cc884-110">**System. String** qui est la description de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="cc884-110">A **System.String** that is the error description.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc884-111">Notes</span><span class="sxs-lookup"><span data-stu-id="cc884-111">Remarks</span></span>

<span data-ttu-id="cc884-112">Vous devez définir **IWMPSettings. enableErrorDialogs** sur **false** si vous choisissez d’afficher des messages d’erreur personnalisés.</span><span class="sxs-lookup"><span data-stu-id="cc884-112">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="cc884-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="cc884-113">Examples</span></span>

<span data-ttu-id="cc884-114">L’exemple suivant utilise **errorDescription** dans un gestionnaire d’événements d’erreur pour afficher la description de l’erreur à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cc884-114">The following example uses **errorDescription** in an Error event handler to display the error description to the user.</span></span> <span data-ttu-id="cc884-115">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="cc884-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_errorDescription(object sender, System.EventArgs e)
{
    // Get the error description for the first error item.
    string errDesc = player.Error.get_Item(0).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show("Error: " + errDesc);
}
```


```VB

Public Sub player_ErrorEvent_errorDescription(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the error description for the first error item.
    Dim errDesc As String = player.Error.Item(0).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(&quot;Error: &quot; + errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="cc884-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc884-116">Requirements</span></span>



| <span data-ttu-id="cc884-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc884-117">Requirement</span></span> | <span data-ttu-id="cc884-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc884-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc884-119">Version</span><span class="sxs-lookup"><span data-stu-id="cc884-119">Version</span></span><br/>   | <span data-ttu-id="cc884-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="cc884-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="cc884-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cc884-121">Namespace</span></span><br/> | <span data-ttu-id="cc884-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="cc884-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="cc884-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="cc884-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cc884-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cc884-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc884-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc884-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc884-126">**Interface IWMPErrorItem (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="cc884-126">**IWMPErrorItem Interface (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cc884-127">**IWMPSettings. enableErrorDialogs (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="cc884-127">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





