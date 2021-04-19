---
title: Propriété IWMPMedia Name
description: La propriété Name obtient ou définit le nom de l’élément multimédia.
ms.assetid: d1057871-bccf-4f84-9b1d-74c41a8f7f7c
keywords:
- propriété Name du lecteur Windows Media
- propriété Name lecteur Windows Media, interface IWMPMedia
- Interface IWMPMedia lecteur Windows Media, propriété nom
topic_type:
- apiref
api_name:
- IWMPMedia.name
- IWMPMedia.get_name
- IWMPMedia.put_name
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c526fc9847b06d0f7b6f4ebadf71761fd29a9d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544046"
---
# <a name="iwmpmedianame-property"></a><span data-ttu-id="8a279-106">IWMPMedia :: Name, propriété</span><span class="sxs-lookup"><span data-stu-id="8a279-106">IWMPMedia::name property</span></span>

<span data-ttu-id="8a279-107">La propriété **Name** obtient ou définit le nom de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="8a279-107">The **name** property gets or sets the name of the media item.</span></span>

<span data-ttu-id="8a279-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="8a279-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a279-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a279-109">Syntax</span></span>


```CSharp
public System.String name {get; set;}
```


```VB

Public Property name As System.String
```





## <a name="property-value"></a><span data-ttu-id="8a279-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="8a279-110">Property value</span></span>

<span data-ttu-id="8a279-111">**System. String** qui est le nom de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="8a279-111">A **System.String** that is the name of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a279-112">Notes</span><span class="sxs-lookup"><span data-stu-id="8a279-112">Remarks</span></span>

<span data-ttu-id="8a279-113">Avant d’utiliser cette propriété, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="8a279-113">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="8a279-114">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="8a279-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8a279-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="8a279-115">Examples</span></span>

<span data-ttu-id="8a279-116">L’exemple suivant utilise **Name** pour modifier le nom de l’élément multimédia en cours.</span><span class="sxs-lookup"><span data-stu-id="8a279-116">The following example uses **name** to change the name of the current media item.</span></span> <span data-ttu-id="8a279-117">Une zone de texte permet à l’utilisateur d’entrer un nouveau nom, et le nom est modifié en réponse à l’événement de clic d’un bouton.</span><span class="sxs-lookup"><span data-stu-id="8a279-117">A text box allows the user to enter a new name, and the name is changed in response to the Click event of a button.</span></span> <span data-ttu-id="8a279-118">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="8a279-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setNewName_Click(object sender, System.EventArgs e)
{
    // ...Add code to ensure that the TextBox contains a valid value.

    // Store a WMPLib.IWMPMedia3 interface to the current media item. 
    WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

    // Change the name. 
    cm.name = nameText.Text;
}
```


```VB

Public Sub setNewName_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setNewName.Click

    &#39; ...Add code to ensure that the TextBox contains a valid value.

    &#39; Store a WMPLib.IWMPMedia3 interface to the current media item. 
    Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

    &#39; Change the name. 
    cm.name = nameText.Text

End Sub
```





## <a name="requirements"></a><span data-ttu-id="8a279-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a279-119">Requirements</span></span>



| <span data-ttu-id="8a279-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a279-120">Requirement</span></span> | <span data-ttu-id="8a279-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a279-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a279-122">Version</span><span class="sxs-lookup"><span data-stu-id="8a279-122">Version</span></span><br/>   | <span data-ttu-id="8a279-123">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8a279-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="8a279-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8a279-124">Namespace</span></span><br/> | <span data-ttu-id="8a279-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="8a279-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="8a279-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="8a279-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8a279-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8a279-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a279-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a279-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a279-129">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="8a279-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





