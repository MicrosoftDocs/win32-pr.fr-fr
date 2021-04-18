---
title: Méthode IWMPMediaCollection setDeleted
description: La méthode setDeleted déplace l’élément multimédia spécifié vers le dossier éléments supprimés. | Méthode IWMPMediaCollection setDeleted
ms.assetid: 3fa7989e-8b98-44e1-93ca-8136aba358ea
keywords:
- méthode setDeleted lecteur Windows Media
- méthode setDeleted lecteur Windows Media, interface IWMPMediaCollection
- Interface IWMPMediaCollection lecteur Windows Media, méthode setDeleted
topic_type:
- apiref
api_name:
- IWMPMediaCollection.setDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ccf8cf2d36ab7e4aaf76fdbe5c28582650fcda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529018"
---
# <a name="iwmpmediacollectionsetdeleted-method"></a><span data-ttu-id="98e8a-107">IWMPMediaCollection :: setDeleted, méthode</span><span class="sxs-lookup"><span data-stu-id="98e8a-107">IWMPMediaCollection::setDeleted method</span></span>

<span data-ttu-id="98e8a-108">La `setDeleted` méthode déplace l’élément multimédia spécifié vers le dossier éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="98e8a-108">The `setDeleted` method moves the specified media item to the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="98e8a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98e8a-109">Syntax</span></span>


```CSharp
public void setDeleted(
  IWMPMedia pItem,
  System.Boolean varfIsDeleted
);
```


```VB

Public Sub setDeleted( _
  ByVal pItem As IWMPMedia, _
  ByVal varfIsDeleted As System.Boolean _
)
Implements IWMPMediaCollection.setDeleted
```





## <a name="parameters"></a><span data-ttu-id="98e8a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98e8a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98e8a-111">*pItem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="98e8a-111">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98e8a-112">Interface **wmplib. IWMPMedia** pour l’élément à déplacer.</span><span class="sxs-lookup"><span data-stu-id="98e8a-112">A **WMPLib.IWMPMedia** interface for the item to be moved.</span></span>

</dd> <dt>

<span data-ttu-id="98e8a-113">*varfIsDeleted* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="98e8a-113">*varfIsDeleted* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98e8a-114">Valeur **System. Boolean** qui spécifie si l’élément doit être déplacé vers le dossier éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="98e8a-114">A **System.Boolean** value that specifies whether the item should be moved to the deleted items folder.</span></span> <span data-ttu-id="98e8a-115">Cette valeur doit toujours être **true**.</span><span class="sxs-lookup"><span data-stu-id="98e8a-115">This value must always be **true**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98e8a-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="98e8a-116">Return value</span></span>

<span data-ttu-id="98e8a-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="98e8a-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="98e8a-118">Notes</span><span class="sxs-lookup"><span data-stu-id="98e8a-118">Remarks</span></span>

<span data-ttu-id="98e8a-119">Cette méthode ne supprime pas les fichiers de l’ordinateur de l’utilisateur, mais les déplace simplement dans le dossier éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="98e8a-119">This method does not remove files from the user's computer, it just moves them to the deleted items folder.</span></span>

<span data-ttu-id="98e8a-120">Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="98e8a-120">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="98e8a-121">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="98e8a-121">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="98e8a-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="98e8a-122">Examples</span></span>

<span data-ttu-id="98e8a-123">L’exemple suivant utilise `setDeleted` pour déplacer un élément multimédia particulier vers le dossier éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="98e8a-123">The following example uses `setDeleted` to move a particular media item to the deleted items folder.</span></span> <span data-ttu-id="98e8a-124">La méthode **IsDeleted** teste d’abord si l’élément a déjà été supprimé.</span><span class="sxs-lookup"><span data-stu-id="98e8a-124">The **isDeleted** method first tests whether the item has already been deleted.</span></span> <span data-ttu-id="98e8a-125">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="98e8a-125">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Test whether the media item has already been deleted.
if (!player.mediaCollection.isDeleted(media))
{
    // The item is available to be deleted; move it to the deleted items folder.
    player.mediaCollection.setDeleted(media, true);

    // Inform the user that the operation succeeded.
    System.Windows.Forms.MessageBox.Show("Item moved to deleted items folder.");
}
else
{
    // Tell the user the operation is unnecessary.
    System.Windows.Forms.MessageBox.Show("Item is already deleted!");
}
```


```VB

' Test whether the media item has already been deleted.
If (Not player.mediaCollection.isDeleted(media)) Then

    &#39; The item is available to be deleted move it to the deleted items folder.
    player.mediaCollection.setDeleted(media, True)

    &#39; Inform the user that the operation succeeded.
    System.Windows.Forms.MessageBox.Show(&quot;Item moved to deleted items folder.&quot;)

Else

    &#39; Tell the user the operation is unnecessary.
    System.Windows.Forms.MessageBox.Show(&quot;Item is already deleted!&quot;)

End If
```





## <a name="requirements"></a><span data-ttu-id="98e8a-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98e8a-126">Requirements</span></span>



| <span data-ttu-id="98e8a-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98e8a-127">Requirement</span></span> | <span data-ttu-id="98e8a-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="98e8a-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98e8a-129">Version</span><span class="sxs-lookup"><span data-stu-id="98e8a-129">Version</span></span><br/>   | <span data-ttu-id="98e8a-130">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="98e8a-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="98e8a-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="98e8a-131">Namespace</span></span><br/> | <span data-ttu-id="98e8a-132">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="98e8a-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="98e8a-133">Assembly</span><span class="sxs-lookup"><span data-stu-id="98e8a-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="98e8a-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="98e8a-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98e8a-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98e8a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98e8a-136">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="98e8a-136">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="98e8a-137">**Interface IWMPMediaCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="98e8a-137">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





