---
title: Méthode IWMPPlaylist setItemInfo
description: La méthode setItemInfo définit la valeur d’un attribut de la sélection actuelle.
ms.assetid: b3874298-8fbe-47a4-b696-cef0382aec7c
keywords:
- méthode setItemInfo lecteur Windows Media
- méthode setItemInfo lecteur Windows Media, interface IWMPPlaylist
- Interface IWMPPlaylist lecteur Windows Media, méthode setItemInfo
topic_type:
- apiref
api_name:
- IWMPPlaylist.setItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce882d050f1ce7839fe3589fced3a87d9052fec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526778"
---
# <a name="iwmpplaylistsetiteminfo-method"></a><span data-ttu-id="89afb-106">IWMPPlaylist :: setItemInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="89afb-106">IWMPPlaylist::setItemInfo method</span></span>

<span data-ttu-id="89afb-107">La méthode **setItemInfo** définit la valeur d’un attribut de la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="89afb-107">The **setItemInfo** method sets the value of an attribute of the current playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="89afb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89afb-108">Syntax</span></span>


```CSharp
public void setItemInfo(
  System.String bstrName,
  System.String bstrValue
);
```


```VB

Public Sub setItemInfo( _
  ByVal bstrName As System.String, _
  ByVal bstrValue As System.String _
)
Implements IWMPPlaylist.setItemInfo
```





## <a name="parameters"></a><span data-ttu-id="89afb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89afb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89afb-110">*bstrName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="89afb-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89afb-111">**System. String** qui est le nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="89afb-111">A **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="89afb-112">*bstrValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="89afb-112">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89afb-113">**System. String** qui est la valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="89afb-113">A **System.String** that is the attribute value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89afb-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="89afb-114">Return value</span></span>

<span data-ttu-id="89afb-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="89afb-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="89afb-116">Notes</span><span class="sxs-lookup"><span data-stu-id="89afb-116">Remarks</span></span>

<span data-ttu-id="89afb-117">Avant d’appeler cette méthode, vous devez disposer d’un accès complet à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="89afb-117">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="89afb-118">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="89afb-118">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="89afb-119">Consultez la propriété [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) pour obtenir un exemple de code qui utilise cette propriété.</span><span class="sxs-lookup"><span data-stu-id="89afb-119">See the [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="89afb-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89afb-120">Requirements</span></span>



| <span data-ttu-id="89afb-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89afb-121">Requirement</span></span> | <span data-ttu-id="89afb-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="89afb-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89afb-123">Version</span><span class="sxs-lookup"><span data-stu-id="89afb-123">Version</span></span><br/>   | <span data-ttu-id="89afb-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="89afb-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="89afb-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="89afb-125">Namespace</span></span><br/> | <span data-ttu-id="89afb-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="89afb-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="89afb-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="89afb-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="89afb-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="89afb-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89afb-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89afb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89afb-130">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="89afb-130">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="89afb-131">**IWMPPlaylist. getItemInfo (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="89afb-131">**IWMPPlaylist.getItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="89afb-132">**IWMPSettings2. mediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="89afb-132">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="89afb-133">**IWMPSettings2. requestMediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="89afb-133">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





