---
title: IWMPError. Item (VB et C)
description: La propriété Item ( \_ méthode d’extraction d’élément dans C \) obtient une interface IWMPErrorItem à l’index spécifié dans la file d’attente d’erreurs.
ms.assetid: acfaaaa5-eb13-4ba0-8417-4229adc62c5d
keywords:
- IWMPError. Item (VB et C) lecteur Windows Media
topic_type:
- apiref
api_name:
- IWMPError.Item (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9217ec772512171c828dd0dad06ec8fe3704dba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536022"
---
# <a name="iwmperroritem-vb-and-c"></a><span data-ttu-id="4eeb2-104">IWMPError. Item (VB et C#)</span><span class="sxs-lookup"><span data-stu-id="4eeb2-104">IWMPError.Item (VB and C#)</span></span>

<span data-ttu-id="4eeb2-105">La propriété **Item** (méthode d' **extraction d' \_ élément** en C#) obtient une interface **IWMPErrorItem** à l’index spécifié dans la file d’attente d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="4eeb2-105">The **Item** property (the **get\_Item** method in C#) gets an **IWMPErrorItem** interface at the specified index in the error queue.</span></span>


```
[Visual Basic]
ReadOnly Property Item(
  dwIndex As System.Integer
) As IWMPErrorItem
```




```
[C#]
IWMPErrorItem get_Item (
  System.Int32 dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="4eeb2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4eeb2-106">Parameters</span></span>

<span data-ttu-id="4eeb2-107">*dwIndex*</span><span class="sxs-lookup"><span data-stu-id="4eeb2-107">*dwIndex*</span></span>

<span data-ttu-id="4eeb2-108">**System. Int32** qui est l’index de base zéro d’une interface **IWMPErrorItem** dans la file d’attente d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="4eeb2-108">A **System.Int32** that is the zero-based index of an **IWMPErrorItem** interface in the error queue.</span></span>

## <a name="property-value"></a><span data-ttu-id="4eeb2-109">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="4eeb2-109">Property Value</span></span>

<span data-ttu-id="4eeb2-110">Interface **wmplib. IWMPErrorItem** .</span><span class="sxs-lookup"><span data-stu-id="4eeb2-110">A **WMPLib.IWMPErrorItem** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="4eeb2-111">Notes</span><span class="sxs-lookup"><span data-stu-id="4eeb2-111">Remarks</span></span>

<span data-ttu-id="4eeb2-112">Le lecteur Windows Media peut générer un certain nombre d’erreurs en réponse à une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4eeb2-112">Windows Media Player can generate a number of errors in response to an error condition.</span></span> <span data-ttu-id="4eeb2-113">Cette propriété obtient une erreur spécifique dans la file d’attente à l’aide d’un numéro d’index.</span><span class="sxs-lookup"><span data-stu-id="4eeb2-113">This property gets a specific error in the queue by using an index number.</span></span> <span data-ttu-id="4eeb2-114">Les numéros d’index de la file d’attente d’erreurs commencent par zéro.</span><span class="sxs-lookup"><span data-stu-id="4eeb2-114">The index numbers for the error queue begin with zero.</span></span>

<span data-ttu-id="4eeb2-115">Vous devez définir **IWMPSettings. enableErrorDialogs** sur **false** si vous choisissez d’afficher des messages d’erreur personnalisés.</span><span class="sxs-lookup"><span data-stu-id="4eeb2-115">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="4eeb2-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="4eeb2-116">Examples</span></span>

<span data-ttu-id="4eeb2-117">L’exemple suivant utilise la propriété **Item** (méthode d' **extraction d' \_ élément** en C#) dans un gestionnaire d’événements d’erreur pour récupérer et afficher des informations sur l’erreur la plus récente dans la file d’attente d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="4eeb2-117">The following example uses the **Item** property (the **get\_Item** method in C#) in an Error event handler to retrieve and display information about the most recent error in the error queue.</span></span> <span data-ttu-id="4eeb2-118">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="4eeb2-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_get_Item(object sender, System.EventArgs e)
{
    // Store the index of the most recent error.
    int max = (player.Error.errorCount - 1);

    // Get an interface for the most recent error item. Cast it to
    // a WMPLib.IWMPErrorItem2 interface to get all of the available functionality.
    WMPLib.IWMPErrorItem2 errItem = (WMPLib.IWMPErrorItem2)player.Error.get_Item(max);

    // Use the interface to access and store the error info.
    int errNum = errItem.errorCode;
    string errDesc = errItem.errorDescription;

    // Display the error info.
    System.Windows.Forms.MessageBox.Show(errNum.ToString() + ":  " + errDesc);
}
```


```VB

Public Sub player_ErrorEvent_get_Item(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the index of the most recent error.
    Dim max As Integer = (player.Error.errorCount - 1)

    &#39; Get an interface for the most recent error item. 
    Dim errItem As WMPLib.IWMPErrorItem2 = player.Error.Item(max)

    &#39; Use the interface to access and store the error info.
    Dim errNum As Integer = errItem.errorCode
    Dim errDesc As String = errItem.errorDescription

    &#39; Display the error info.
    System.Windows.Forms.MessageBox.Show(errNum.ToString() + &quot;:  &quot; + errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="4eeb2-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4eeb2-119">Requirements</span></span>



| <span data-ttu-id="4eeb2-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4eeb2-120">Requirement</span></span> | <span data-ttu-id="4eeb2-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="4eeb2-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4eeb2-122">Version</span><span class="sxs-lookup"><span data-stu-id="4eeb2-122">Version</span></span><br/>   | <span data-ttu-id="4eeb2-123">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="4eeb2-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="4eeb2-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4eeb2-124">Namespace</span></span><br/> | <span data-ttu-id="4eeb2-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="4eeb2-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4eeb2-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="4eeb2-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4eeb2-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4eeb2-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4eeb2-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4eeb2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eeb2-129">**Interface IWMPError (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4eeb2-129">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4eeb2-130">**Interface IWMPErrorItem (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4eeb2-130">**IWMPErrorItem Interface (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4eeb2-131">**IWMPSettings. enableErrorDialogs (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4eeb2-131">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





