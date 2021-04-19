---
title: IWMPPlaylistCollection isDeleted, méthode
description: La méthode isDeleted retourne une valeur indiquant si la sélection spécifiée se trouve dans le dossier éléments supprimés.
ms.assetid: 02bc4b9f-6149-4fe2-8417-6484b22f2d74
keywords:
- isDeleted, méthode Windows Media Player
- isDeleted, méthode lecteur Windows Media, interface IWMPPlaylistCollection
- Interface IWMPPlaylistCollection lecteur Windows Media, méthode isDeleted
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.isDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d4ce4a314378c5a4a211a52b99ea1b36ae1fda8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529651"
---
# <a name="iwmpplaylistcollectionisdeleted-method"></a><span data-ttu-id="978b3-106">IWMPPlaylistCollection :: isDeleted, méthode</span><span class="sxs-lookup"><span data-stu-id="978b3-106">IWMPPlaylistCollection::isDeleted method</span></span>

<span data-ttu-id="978b3-107">La méthode **IsDeleted** retourne une valeur indiquant si la sélection spécifiée se trouve dans le dossier éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="978b3-107">The **isDeleted** method returns a value indicating whether the specified playlist is in the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="978b3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="978b3-108">Syntax</span></span>


```CSharp
public System.Boolean isDeleted(
  IWMPPlaylist pItem
);
```


```VB

Public Function isDeleted( _
  ByVal pItem As IWMPPlaylist _
) As System.Boolean
Implements IWMPPlaylistCollection.isDeleted
```





## <a name="parameters"></a><span data-ttu-id="978b3-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="978b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="978b3-110">*pItem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="978b3-110">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="978b3-111">Interface **wmplib. IWMPPlaylist** pour la sélection interrogée.</span><span class="sxs-lookup"><span data-stu-id="978b3-111">A **WMPLib.IWMPPlaylist** interface for the queried playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="978b3-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="978b3-112">Return value</span></span>

<span data-ttu-id="978b3-113">**System. Boolean** qui spécifie si la sélection a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="978b3-113">A **System.Boolean** that specifies whether the playlist was deleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="978b3-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="978b3-114">Requirements</span></span>



| <span data-ttu-id="978b3-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="978b3-115">Requirement</span></span> | <span data-ttu-id="978b3-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="978b3-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="978b3-117">Version</span><span class="sxs-lookup"><span data-stu-id="978b3-117">Version</span></span><br/>   | <span data-ttu-id="978b3-118">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="978b3-118">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="978b3-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="978b3-119">Namespace</span></span><br/> | <span data-ttu-id="978b3-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="978b3-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="978b3-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="978b3-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="978b3-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="978b3-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="978b3-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="978b3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="978b3-124">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="978b3-124">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="978b3-125">**Interface IWMPPlaylistCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="978b3-125">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





