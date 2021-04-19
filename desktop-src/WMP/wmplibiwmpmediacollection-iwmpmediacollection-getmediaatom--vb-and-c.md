---
title: Méthode IWMPMediaCollection getMediaAtom
description: La méthode getMediaAtom retourne l’index d’un attribut spécifié dans le jeu d’attributs disponibles.
ms.assetid: 01e3d073-677b-4939-96d3-63ae96eaa25d
keywords:
- méthode getMediaAtom lecteur Windows Media
- méthode getMediaAtom lecteur Windows Media, interface IWMPMediaCollection
- Interface IWMPMediaCollection lecteur Windows Media, méthode getMediaAtom
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getMediaAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08487cf60c351ff4f8e0741209655cb78c30c3f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531137"
---
# <a name="iwmpmediacollectiongetmediaatom-method"></a><span data-ttu-id="0ff2b-106">IWMPMediaCollection :: getMediaAtom, méthode</span><span class="sxs-lookup"><span data-stu-id="0ff2b-106">IWMPMediaCollection::getMediaAtom method</span></span>

<span data-ttu-id="0ff2b-107">La `getMediaAtom` méthode retourne l’index d’un attribut spécifié dans le jeu d’attributs disponibles.</span><span class="sxs-lookup"><span data-stu-id="0ff2b-107">The `getMediaAtom` method returns the index of a specified attribute within the set of available attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ff2b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ff2b-108">Syntax</span></span>


```CSharp
public System.Int32 getMediaAtom(
  System.String bstrItemName
);
```


```VB

Public Function getMediaAtom( _
  ByVal bstrItemName As System.String _
) As System.Int32
Implements IWMPMediaCollection.getMediaAtom
```





## <a name="parameters"></a><span data-ttu-id="0ff2b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ff2b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ff2b-110">*bstrItemName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0ff2b-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ff2b-111">**System. String** qui est le nom de l’élément pour lequel l’index doit être récupéré.</span><span class="sxs-lookup"><span data-stu-id="0ff2b-111">The **System.String** that is the name of the item for which the index should be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ff2b-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0ff2b-112">Return value</span></span>

<span data-ttu-id="0ff2b-113">**System. Int32** qui est l’index.</span><span class="sxs-lookup"><span data-stu-id="0ff2b-113">The **System.Int32** that is the index.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ff2b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="0ff2b-114">Remarks</span></span>

<span data-ttu-id="0ff2b-115">Le numéro d’index récupéré avec cette méthode peut être passé à **IWMPMedia. getItemInfoByAtom** pour accéder aux valeurs d’attribut.</span><span class="sxs-lookup"><span data-stu-id="0ff2b-115">The index number retrieved with this method can be passed to the **IWMPMedia.getItemInfoByAtom** to access attribute values.</span></span> <span data-ttu-id="0ff2b-116">Cette technique est généralement plus efficace lorsque vous utilisez des sélections volumineuses que l’accès à une valeur d’attribut par nom via **IWMPMedia. getItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="0ff2b-116">This technique is generally more efficient when working with large playlists than accessing an attribute value by name through **IWMPMedia.getItemInfo**.</span></span>

<span data-ttu-id="0ff2b-117">Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="0ff2b-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="0ff2b-118">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="0ff2b-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ff2b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ff2b-119">Requirements</span></span>



| <span data-ttu-id="0ff2b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ff2b-120">Requirement</span></span> | <span data-ttu-id="0ff2b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ff2b-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ff2b-122">Version</span><span class="sxs-lookup"><span data-stu-id="0ff2b-122">Version</span></span><br/>   | <span data-ttu-id="0ff2b-123">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="0ff2b-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="0ff2b-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0ff2b-124">Namespace</span></span><br/> | <span data-ttu-id="0ff2b-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0ff2b-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0ff2b-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="0ff2b-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0ff2b-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0ff2b-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ff2b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ff2b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ff2b-129">**IWMPMedia. getItemInfo (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="0ff2b-129">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0ff2b-130">**IWMPMedia. getItemInfoByAtom (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="0ff2b-130">**IWMPMedia.getItemInfoByAtom (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0ff2b-131">**Interface IWMPMediaCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="0ff2b-131">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





