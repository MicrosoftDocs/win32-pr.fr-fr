---
title: IWMPError propriété errorCount
description: La propriété errorCount obtient le nombre d’erreurs dans la file d’attente d’erreurs.
ms.assetid: a30750c8-2025-4087-bd2b-f313ccbde38c
keywords:
- propriété errorCount lecteur Windows Media
- propriété errorCount lecteur Windows Media, interface IWMPError
- Interface IWMPError lecteur Windows Media, propriété errorCount
topic_type:
- apiref
api_name:
- IWMPError.errorCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b62c16f07260847c91f1c9f18885587444a4ceb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541485"
---
# <a name="iwmperrorerrorcount-property"></a><span data-ttu-id="afd31-106">IWMPError :: errorCount, propriété</span><span class="sxs-lookup"><span data-stu-id="afd31-106">IWMPError::errorCount property</span></span>

<span data-ttu-id="afd31-107">La propriété **errorCount** obtient le nombre d’erreurs dans la file d’attente d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="afd31-107">The **errorCount** property gets the number of errors in the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="afd31-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="afd31-108">Syntax</span></span>


```CSharp
public System.Int32 errorCount {get; set;}
```


```VB

Public ReadOnly Property errorCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="afd31-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="afd31-109">Property value</span></span>

<span data-ttu-id="afd31-110">**System. Int32** qui correspond au nombre d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="afd31-110">A **System.Int32** that is the number of errors.</span></span>

## <a name="remarks"></a><span data-ttu-id="afd31-111">Notes</span><span class="sxs-lookup"><span data-stu-id="afd31-111">Remarks</span></span>

<span data-ttu-id="afd31-112">Vous devez définir **IWMPSettings. enableErrorDialogs** sur **false** si vous choisissez d’afficher des messages d’erreur personnalisés.</span><span class="sxs-lookup"><span data-stu-id="afd31-112">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="afd31-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="afd31-113">Examples</span></span>

<span data-ttu-id="afd31-114">L’exemple suivant utilise **errorCount** dans un gestionnaire d’événements d’erreur pour avertir l’utilisateur de l’erreur la plus récente dans la file d’attente d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="afd31-114">The following example uses **errorCount** in an Error event handler to alert the user about the most recent error in the error queue.</span></span> <span data-ttu-id="afd31-115">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="afd31-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_errorCount(object sender, System.EventArgs e)
{
    // Store the number of errors in the queue.
    int max = player.Error.errorCount;

    // Get the description of the last error. Error items start at zero,
    // so the item index will always be one less than the error count.
    string errDesc = player.Error.get_Item(max-1).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc);
}
```


```VB

Public Sub player_ErrorEvent_errorCount(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the number of errors in the queue.
    Dim max As Integer = player.Error.errorCount

    &#39; Get the description of the last error. Error items start at zero,
    &#39; so the item index will always be one less than the error count.
    Dim errDesc As String = player.Error.Item(max - 1).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="afd31-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="afd31-116">Requirements</span></span>



| <span data-ttu-id="afd31-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="afd31-117">Requirement</span></span> | <span data-ttu-id="afd31-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="afd31-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afd31-119">Version</span><span class="sxs-lookup"><span data-stu-id="afd31-119">Version</span></span><br/>   | <span data-ttu-id="afd31-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="afd31-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="afd31-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="afd31-121">Namespace</span></span><br/> | <span data-ttu-id="afd31-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="afd31-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="afd31-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="afd31-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="afd31-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="afd31-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afd31-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="afd31-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afd31-126">**Interface IWMPError (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="afd31-126">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="afd31-127">**IWMPSettings. enableErrorDialogs (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="afd31-127">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





