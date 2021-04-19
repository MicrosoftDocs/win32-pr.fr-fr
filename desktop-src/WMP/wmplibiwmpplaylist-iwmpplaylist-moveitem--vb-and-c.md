---
title: Méthode IWMPPlaylist moveItem
description: La méthode moveItem modifie l’emplacement d’un élément multimédia dans la sélection.
ms.assetid: e82c820f-4640-4289-88c1-79a92e520f00
keywords:
- méthode moveItem lecteur Windows Media
- méthode moveItem lecteur Windows Media, interface IWMPPlaylist
- Interface IWMPPlaylist lecteur Windows Media, méthode moveItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.moveItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c2d5be745fc3dcf799eb7203e607e493b284b4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541663"
---
# <a name="iwmpplaylistmoveitem-method"></a><span data-ttu-id="4ffb6-106">IWMPPlaylist :: moveItem, méthode</span><span class="sxs-lookup"><span data-stu-id="4ffb6-106">IWMPPlaylist::moveItem method</span></span>

<span data-ttu-id="4ffb6-107">La méthode **moveItem** modifie l’emplacement d’un élément multimédia dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-107">The **moveItem** method changes the location of a media item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ffb6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ffb6-108">Syntax</span></span>


```CSharp
public void moveItem(
  System.Int32 lIndexOld,
  System.Int32 lIndexNew
);
```


```VB

Public Sub moveItem( _
  ByVal lIndexOld As System.Int32, _
  ByVal lIndexNew As System.Int32 _
)
Implements IWMPPlaylist.moveItem
```





## <a name="parameters"></a><span data-ttu-id="4ffb6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4ffb6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ffb6-110">*lIndexOld* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-110">*lIndexOld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ffb6-111">**System. Int32** qui est l’index d’origine.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-111">A **System.Int32** that is the original index.</span></span>

</dd> <dt>

<span data-ttu-id="4ffb6-112">*lIndexNew* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-112">*lIndexNew* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ffb6-113">**System. Int32** qui est le nouvel index.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-113">A **System.Int32** that is the new index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ffb6-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4ffb6-114">Return value</span></span>

<span data-ttu-id="4ffb6-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ffb6-116">Notes</span><span class="sxs-lookup"><span data-stu-id="4ffb6-116">Remarks</span></span>

<span data-ttu-id="4ffb6-117">Tous les éléments après l’élément inséré auront leurs numéros d’index augmentés d’une unité.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-117">All items after the inserted item will have their index numbers increased by one.</span></span>

<span data-ttu-id="4ffb6-118">Avant d’appeler cette méthode, vous devez disposer d’un accès complet à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-118">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="4ffb6-119">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ffb6-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ffb6-120">Requirements</span></span>



| <span data-ttu-id="4ffb6-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ffb6-121">Requirement</span></span> | <span data-ttu-id="4ffb6-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ffb6-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ffb6-123">Version</span><span class="sxs-lookup"><span data-stu-id="4ffb6-123">Version</span></span><br/>   | <span data-ttu-id="4ffb6-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="4ffb6-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="4ffb6-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4ffb6-125">Namespace</span></span><br/> | <span data-ttu-id="4ffb6-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="4ffb6-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4ffb6-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="4ffb6-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4ffb6-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4ffb6-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ffb6-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ffb6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ffb6-130">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4ffb6-130">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4ffb6-131">**IWMPSettings2. mediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4ffb6-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4ffb6-132">**IWMPSettings2. requestMediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4ffb6-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





