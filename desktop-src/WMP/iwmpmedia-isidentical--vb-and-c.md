---
title: IWMPMedia. isIdentical (VB et C)
description: La propriété isIdentical (méthode obtenir \_ isIdentical dans C \) obtient une valeur indiquant si l’élément multimédia spécifié est le même que celui actuel.
ms.assetid: 1406a0ff-2dc8-4cde-8b71-4a39b8608fb1
keywords:
- IWMPMedia. isIdentical (VB et C) lecteur Windows Media
topic_type:
- apiref
api_name:
- IWMPMedia.isIdentical (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3a488ad300362c1f8dccfd0fa6f6c7e4dee7676
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545599"
---
# <a name="iwmpmediaisidentical-vb-and-c"></a><span data-ttu-id="d9143-104">IWMPMedia. isIdentical (VB et C#)</span><span class="sxs-lookup"><span data-stu-id="d9143-104">IWMPMedia.isIdentical (VB and C#)</span></span>

<span data-ttu-id="d9143-105">La propriété **isIdentical** (méthode **obtenir \_ isIdentical** en C#) obtient une valeur indiquant si l’élément multimédia spécifié est le même que celui actuel.</span><span class="sxs-lookup"><span data-stu-id="d9143-105">The **isIdentical** property (the **get\_isIdentical** method in C#) gets a value indicating whether the specified media item is the same as the current one.</span></span>


```
[Visual Basic]
ReadOnly Property isIdentical(
  pIWMPMedia As IWMPMedia
) As System.Boolean
```




```
[C#]
System.Boolean get_isIdentical (
  IWMPMedia pIWMPMedia
);
```



## <a name="parameters"></a><span data-ttu-id="d9143-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9143-106">Parameters</span></span>

<span data-ttu-id="d9143-107">*pIWMPMedia*</span><span class="sxs-lookup"><span data-stu-id="d9143-107">*pIWMPMedia*</span></span>

<span data-ttu-id="d9143-108">Interface **wmplib. IWMPMedia** de l’élément multimédia à comparer avec l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="d9143-108">A **WMPLib.IWMPMedia** interface to the media item to be compared with the current media item.</span></span>

## <a name="property-value"></a><span data-ttu-id="d9143-109">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="d9143-109">Property Value</span></span>

<span data-ttu-id="d9143-110">Valeur **System. Boolean** qui indique si les deux éléments multimédias sont identiques.</span><span class="sxs-lookup"><span data-stu-id="d9143-110">A **System.Boolean** value that indicates whether the two media items are identical.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9143-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d9143-111">Remarks</span></span>

<span data-ttu-id="d9143-112">**IWMPMedia. isIdentical** est une propriété de Visual Basic qui accepte un paramètre.</span><span class="sxs-lookup"><span data-stu-id="d9143-112">**IWMPMedia.isIdentical** is a property in Visual Basic that takes a parameter.</span></span> <span data-ttu-id="d9143-113">En C#, on parle de méthode **IWMPMedia. obten \_ isIdentical** .</span><span class="sxs-lookup"><span data-stu-id="d9143-113">In C# it is referred to as the **IWMPMedia.get\_isIdentical** method.</span></span>

## <a name="examples"></a><span data-ttu-id="d9143-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="d9143-114">Examples</span></span>

<span data-ttu-id="d9143-115">L’exemple suivant utilise la propriété **isIdentical** (méthode **obtenir \_ isIdentical** en C#) pour vérifier si un élément multimédia nommé newMedia est le même que l’élément multimédia en cours.</span><span class="sxs-lookup"><span data-stu-id="d9143-115">The following example uses the **isIdentical** property (the **get\_isIdentical** method in C#) to check whether a media item named newMedia is the same as the current media item.</span></span> <span data-ttu-id="d9143-116">Si ce n’est pas le cas, le nouvel élément multimédia est lu.</span><span class="sxs-lookup"><span data-stu-id="d9143-116">If they are not the same, the new media item is played.</span></span> <span data-ttu-id="d9143-117">Dans le cas contraire, le média actuel continue de s’exécuter sans interruption.</span><span class="sxs-lookup"><span data-stu-id="d9143-117">Otherwise, the current media continues to play uninterrupted.</span></span> <span data-ttu-id="d9143-118">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="d9143-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
if (newMedia.get_isIdentical(player.currentMedia) != true)
{
    // Change the current media to the new media item.
    player.currentMedia = newMedia;

    // Play the new media item.
    player.Ctlcontrols.play();
}
```


```VB

If (newMedia.isIdentical(player.currentMedia) <> True) Then

    &#39; Change the current media to the new media item.
    player.currentMedia = newMedia

    &#39; Play the new media item.
    player.Ctlcontrols.play()

End If
```





## <a name="requirements"></a><span data-ttu-id="d9143-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9143-119">Requirements</span></span>



| <span data-ttu-id="d9143-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d9143-120">Requirement</span></span> | <span data-ttu-id="d9143-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9143-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9143-122">Version</span><span class="sxs-lookup"><span data-stu-id="d9143-122">Version</span></span><br/>   | <span data-ttu-id="d9143-123">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="d9143-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d9143-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d9143-124">Namespace</span></span><br/> | <span data-ttu-id="d9143-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d9143-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d9143-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="d9143-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d9143-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d9143-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9143-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9143-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9143-129">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="d9143-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





