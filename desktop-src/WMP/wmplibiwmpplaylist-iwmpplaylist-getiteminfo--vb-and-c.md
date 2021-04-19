---
title: Méthode IWMPPlaylist getItemInfo
description: La méthode getItemInfo retourne la valeur d’un attribut playlist spécifié par Name.
ms.assetid: 62e882d6-66bb-450c-9700-b99d30dd42fa
keywords:
- méthode getItemInfo lecteur Windows Media
- méthode getItemInfo lecteur Windows Media, interface IWMPPlaylist
- Interface IWMPPlaylist lecteur Windows Media, méthode getItemInfo
topic_type:
- apiref
api_name:
- IWMPPlaylist.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ced433b13f5af2d1df8c12dba023b7fbb55c5f7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542684"
---
# <a name="iwmpplaylistgetiteminfo-method"></a><span data-ttu-id="52da6-106">IWMPPlaylist :: getItemInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="52da6-106">IWMPPlaylist::getItemInfo method</span></span>

<span data-ttu-id="52da6-107">La méthode **getItemInfo** retourne la valeur d’un attribut playlist spécifié par Name.</span><span class="sxs-lookup"><span data-stu-id="52da6-107">The **getItemInfo** method returns the value of a playlist attribute specified by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="52da6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52da6-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.String bstrName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrName As System.String _
) As System.String
Implements IWMPPlaylist.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="52da6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="52da6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52da6-110">*bstrName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="52da6-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52da6-111">**System. String** qui est le nom de l’attribut playlist.</span><span class="sxs-lookup"><span data-stu-id="52da6-111">A **System.String** that is the name of the playlist attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52da6-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="52da6-112">Return value</span></span>

<span data-ttu-id="52da6-113">**System. String** qui est la valeur de l’attribut playlist.</span><span class="sxs-lookup"><span data-stu-id="52da6-113">A **System.String** that is the value of the playlist attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="52da6-114">Notes</span><span class="sxs-lookup"><span data-stu-id="52da6-114">Remarks</span></span>

<span data-ttu-id="52da6-115">Avant d’utiliser cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="52da6-115">Before using this method, you must have read access to the library.</span></span> <span data-ttu-id="52da6-116">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="52da6-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="52da6-117">Consultez la propriété [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) pour obtenir un exemple de code qui utilise cette propriété.</span><span class="sxs-lookup"><span data-stu-id="52da6-117">See the [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="52da6-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52da6-118">Requirements</span></span>



| <span data-ttu-id="52da6-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52da6-119">Requirement</span></span> | <span data-ttu-id="52da6-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="52da6-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52da6-121">Version</span><span class="sxs-lookup"><span data-stu-id="52da6-121">Version</span></span><br/>   | <span data-ttu-id="52da6-122">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="52da6-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="52da6-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="52da6-123">Namespace</span></span><br/> | <span data-ttu-id="52da6-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="52da6-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="52da6-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="52da6-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="52da6-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="52da6-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52da6-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52da6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52da6-128">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="52da6-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="52da6-129">**IWMPPlaylist. setItemInfo (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="52da6-129">**IWMPPlaylist.setItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





