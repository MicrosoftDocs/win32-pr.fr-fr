---
title: Événement d’erreur de l’objet AxWindowsMediaPlayer
description: L’événement d’erreur se produit lorsque le contrôle du lecteur Windows Media a une condition d’erreur.
ms.assetid: d28c18a9-c650-4169-989b-8727b7a5a831
keywords:
- Événement d’erreur de l’objet AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- Error Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cfd3571538aa2cdd263a9f5d57e479e73818806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523024"
---
# <a name="error-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="18882-104">Événement d’erreur de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="18882-104">Error Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="18882-105">L’événement d’erreur se produit lorsque le contrôle du lecteur Windows Media a une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="18882-105">The Error event occurs when the Windows Media Player control has an error condition.</span></span>

``` syntax
[C#]
private void player_ErrorEvent(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_ErrorEvent(  
  sender As Object,  
  e As System.EventArgs
) Handles player.ErrorEvent
```

## <a name="event-data"></a><span data-ttu-id="18882-106">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="18882-106">Event Data</span></span>

<span data-ttu-id="18882-107">Cet événement ne contient pas de données.</span><span class="sxs-lookup"><span data-stu-id="18882-107">This event does not contain data.</span></span>

## <a name="examples"></a><span data-ttu-id="18882-108">Exemples</span><span class="sxs-lookup"><span data-stu-id="18882-108">Examples</span></span>

<span data-ttu-id="18882-109">L’exemple suivant crée un gestionnaire d’événements pour l’événement d’erreur afin d’afficher le texte de description de la première erreur dans la file d’attente d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="18882-109">The following example creates an event handler for the Error event to display the description text for the first error in the error queue.</span></span> <span data-ttu-id="18882-110">L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="18882-110">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the Error event.
player.ErrorEvent += new EventHandler(player_ErrorEvent);

private void player_ErrorEvent(object sender, System.EventArgs e)
{
    // Get the description of the first error. 
    string errDesc = player.Error.get_Item(0).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc);
}
```


```VB

Public Sub player_ErrorEvent(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the description of the first error. 
    Dim errDesc As String = player.Error.Item(0).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="18882-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18882-111">Requirements</span></span>



| <span data-ttu-id="18882-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18882-112">Requirement</span></span> | <span data-ttu-id="18882-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="18882-113">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18882-114">Version</span><span class="sxs-lookup"><span data-stu-id="18882-114">Version</span></span><br/>   | <span data-ttu-id="18882-115">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="18882-115">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="18882-116">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="18882-116">Namespace</span></span><br/> | <span data-ttu-id="18882-117">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="18882-117">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="18882-118">Assembly</span><span class="sxs-lookup"><span data-stu-id="18882-118">Assembly</span></span><br/>  | <dl> <span data-ttu-id="18882-119"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="18882-119"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18882-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18882-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18882-121">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="18882-121">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="18882-122">**IWMPError. Item (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="18882-122">**IWMPError.Item (VB and C#)**</span></span>](iwmperror-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="18882-123">**IWMPErrorItem. errorDescription (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="18882-123">**IWMPErrorItem.errorDescription (VB and C#)**</span></span>](wmplibiwmperroritem-iwmperroritem-errordescription--vb-and-c.md)
</dt> </dl>

 

 





