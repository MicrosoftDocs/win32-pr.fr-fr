---
title: IWMPErrorItem errorCode, propriété
description: La propriété errorCode obtient le code d’erreur actuel.
ms.assetid: 00719067-685d-4ef2-9eec-72c7892fcdb9
keywords:
- propriété errorCode Windows Media Player
- propriété errorCode lecteur Windows Media, interface IWMPErrorItem
- Interface IWMPErrorItem lecteur Windows Media, errorCode, propriété
topic_type:
- apiref
api_name:
- IWMPErrorItem.errorCode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f284d5655fc1f4007695a1f681c744a9c5c6fc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541727"
---
# <a name="iwmperroritemerrorcode-property"></a><span data-ttu-id="55d42-106">IWMPErrorItem :: errorCode, propriété</span><span class="sxs-lookup"><span data-stu-id="55d42-106">IWMPErrorItem::errorCode property</span></span>

<span data-ttu-id="55d42-107">La propriété **ErrorCode** obtient le code d’erreur actuel.</span><span class="sxs-lookup"><span data-stu-id="55d42-107">The **errorCode** property gets the current error code.</span></span>

## <a name="syntax"></a><span data-ttu-id="55d42-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55d42-108">Syntax</span></span>


```CSharp
public System.Int32 errorCode {get; set;}
```


```VB

Public ReadOnly Property errorCode As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="55d42-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="55d42-109">Property value</span></span>

<span data-ttu-id="55d42-110">**System. Int32** qui correspond au code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="55d42-110">A **System.Int32** that is the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="55d42-111">Notes</span><span class="sxs-lookup"><span data-stu-id="55d42-111">Remarks</span></span>

<span data-ttu-id="55d42-112">Vous devez définir **IWMPSettings. enableErrorDialogs** sur **false** si vous choisissez d’afficher des messages d’erreur personnalisés.</span><span class="sxs-lookup"><span data-stu-id="55d42-112">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="55d42-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="55d42-113">Examples</span></span>

<span data-ttu-id="55d42-114">L’exemple suivant utilise **ErrorCode** dans un gestionnaire d’événements d’erreur pour afficher le code d’erreur à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="55d42-114">The following example uses **errorCode** in an Error event handler to display the error code to the user.</span></span> <span data-ttu-id="55d42-115">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="55d42-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_errorCode(object sender, System.EventArgs e)
{
    // Get the error code for the first error item.
    int errCode = player.Error.get_Item(0).errorCode;

    // Display the error code.
    System.Windows.Forms.MessageBox.Show("Error number: " + errCode.ToString());
}
```


```VB

Public Sub player_ErrorEvent_errorCode(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the error code for the first error item.
    Dim errCode As Integer = player.Error.Item(0).errorCode

    &#39; Display the error code.
    System.Windows.Forms.MessageBox.Show(&quot;Error number: &quot; + errCode.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="55d42-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55d42-116">Requirements</span></span>



| <span data-ttu-id="55d42-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55d42-117">Requirement</span></span> | <span data-ttu-id="55d42-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="55d42-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55d42-119">Version</span><span class="sxs-lookup"><span data-stu-id="55d42-119">Version</span></span><br/>   | <span data-ttu-id="55d42-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="55d42-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="55d42-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="55d42-121">Namespace</span></span><br/> | <span data-ttu-id="55d42-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="55d42-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="55d42-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="55d42-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="55d42-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="55d42-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55d42-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55d42-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55d42-126">**Interface IWMPErrorItem (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="55d42-126">**IWMPErrorItem Interface (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="55d42-127">**IWMPSettings. enableErrorDialogs (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="55d42-127">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





