---
title: Méthode IWMPError clearErrorQueue
description: La méthode clearErrorQueue efface les erreurs de la file d’attente des erreurs. | Méthode IWMPError clearErrorQueue
ms.assetid: a8e8e666-56e4-4e75-9ed5-2714d272ce7c
keywords:
- méthode clearErrorQueue lecteur Windows Media
- méthode clearErrorQueue lecteur Windows Media, interface IWMPError
- Interface IWMPError lecteur Windows Media, méthode clearErrorQueue
topic_type:
- apiref
api_name:
- IWMPError.clearErrorQueue
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c3f422a9bc32049106d83c970bd8d2c9b2110f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542741"
---
# <a name="iwmperrorclearerrorqueue-method"></a><span data-ttu-id="46aae-107">IWMPError :: clearErrorQueue, méthode</span><span class="sxs-lookup"><span data-stu-id="46aae-107">IWMPError::clearErrorQueue method</span></span>

<span data-ttu-id="46aae-108">La méthode **clearErrorQueue** efface les erreurs de la file d’attente des erreurs.</span><span class="sxs-lookup"><span data-stu-id="46aae-108">The **clearErrorQueue** method clears the errors from the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="46aae-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46aae-109">Syntax</span></span>


```CSharp
public void clearErrorQueue();
```


```VB

Public Sub clearErrorQueue()
Implements IWMPError.clearErrorQueue
```





## <a name="parameters"></a><span data-ttu-id="46aae-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46aae-110">Parameters</span></span>

<span data-ttu-id="46aae-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="46aae-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="46aae-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="46aae-112">Return value</span></span>

<span data-ttu-id="46aae-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="46aae-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="46aae-114">Notes</span><span class="sxs-lookup"><span data-stu-id="46aae-114">Remarks</span></span>

<span data-ttu-id="46aae-115">Utilisez cette méthode pour effacer la file d’attente d’erreurs après le traitement d’une série d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="46aae-115">Use this method to clear the error queue after a series of errors has been processed.</span></span>

<span data-ttu-id="46aae-116">Vous devez définir **IWMPSettings. enableErrorDialogs** sur **false** si vous choisissez d’afficher des messages d’erreur personnalisés.</span><span class="sxs-lookup"><span data-stu-id="46aae-116">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="46aae-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="46aae-117">Examples</span></span>

<span data-ttu-id="46aae-118">L’exemple suivant utilise **clearErrorQueue** dans un gestionnaire d’événements d’erreur pour vider la file d’attente d’erreurs une fois que toutes les descriptions d’erreur ont été affichées.</span><span class="sxs-lookup"><span data-stu-id="46aae-118">The following example uses **clearErrorQueue** in an Error event handler to empty the error queue after all error descriptions have been displayed.</span></span> <span data-ttu-id="46aae-119">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="46aae-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_clearErrorQueue(object sender, System.EventArgs e)
{
    // Store the number of errors in the queue.
    int max = player.Error.errorCount;

    // Loop through the list of errors.
    for (int i = 0; i < max; i++)
    {
        // Get the description for this error.
        string errDesc = player.Error.get_Item(i).errorDescription;

        // Display the error message.
        System.Windows.Forms.MessageBox.Show(errDesc);
    }

    // Clear the error queue to prepare for the next group of errors.
    player.Error.clearErrorQueue();
}
```


```VB

Public Sub player_ErrorEvent_clearErrorQueue(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the number of errors in the queue.
    Dim max As Integer = player.Error.errorCount

    &#39; Loop through the list of errors.
    For i As Integer = 0 To (max - 1)

        &#39; Get the description for this error.
        Dim errDesc As String = player.Error.Item(i).errorDescription

        &#39; Display the error message.
        System.Windows.Forms.MessageBox.Show(errDesc)

    Next i

    &#39; Clear the error queue to prepare for the next group of errors.
    player.Error.clearErrorQueue()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="46aae-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46aae-120">Requirements</span></span>



| <span data-ttu-id="46aae-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46aae-121">Requirement</span></span> | <span data-ttu-id="46aae-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="46aae-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46aae-123">Version</span><span class="sxs-lookup"><span data-stu-id="46aae-123">Version</span></span><br/>   | <span data-ttu-id="46aae-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="46aae-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="46aae-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="46aae-125">Namespace</span></span><br/> | <span data-ttu-id="46aae-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="46aae-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="46aae-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="46aae-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="46aae-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="46aae-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46aae-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46aae-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46aae-130">**Interface IWMPError (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="46aae-130">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="46aae-131">**IWMPSettings. enableErrorDialogs (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="46aae-131">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





