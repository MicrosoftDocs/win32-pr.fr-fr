---
title: Propriété d’erreur IWMPMedia2
description: La propriété Error obtient une interface IWMPErrorItem si l’élément multimédia a une condition d’erreur.
ms.assetid: 57dc8aef-5f22-43da-87bc-fdc0c8ebe49b
keywords:
- Propriété d’erreur lecteur Windows Media
- Propriété d’erreur lecteur Windows Media, interface IWMPMedia2
- Interface IWMPMedia2 lecteur Windows Media, propriété erreur
topic_type:
- apiref
api_name:
- IWMPMedia2.Error
- IWMPMedia2.get_Error
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2179b4604efd03574c78261575ce02311cd18a0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527981"
---
# <a name="iwmpmedia2error-property"></a><span data-ttu-id="cb22f-106">IWMPMedia2 :: Error, propriété</span><span class="sxs-lookup"><span data-stu-id="cb22f-106">IWMPMedia2::Error property</span></span>

<span data-ttu-id="cb22f-107">La propriété **Error** obtient une interface **IWMPErrorItem** si l’élément multimédia a une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="cb22f-107">The **Error** property gets an **IWMPErrorItem** interface if the media item has an error condition.</span></span>

<span data-ttu-id="cb22f-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="cb22f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb22f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb22f-109">Syntax</span></span>


```CSharp
public IWMPErrorItem Error {get;}
```


```VB

Public ReadOnly Property Error As IWMPErrorItem
```





## <a name="property-value"></a><span data-ttu-id="cb22f-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="cb22f-110">Property value</span></span>

<span data-ttu-id="cb22f-111">Interface **wmplib. IWMPErrorItem** qui fournit l’accès aux informations sur la condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="cb22f-111">A **WMPLib.IWMPErrorItem** interface that provides access to information about the error condition.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb22f-112">Notes</span><span class="sxs-lookup"><span data-stu-id="cb22f-112">Remarks</span></span>

<span data-ttu-id="cb22f-113">Si l’élément multimédia ne peut pas être lu, cette propriété obtient une interface **IWMPErrorItem** qui contient des informations sur le problème rencontré.</span><span class="sxs-lookup"><span data-stu-id="cb22f-113">If the media item cannot be played, this property gets an **IWMPErrorItem** interface that contains information about the problem encountered.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb22f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb22f-114">Requirements</span></span>



| <span data-ttu-id="cb22f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb22f-115">Requirement</span></span> | <span data-ttu-id="cb22f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb22f-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb22f-117">Version</span><span class="sxs-lookup"><span data-stu-id="cb22f-117">Version</span></span><br/>   | <span data-ttu-id="cb22f-118">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="cb22f-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="cb22f-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cb22f-119">Namespace</span></span><br/> | <span data-ttu-id="cb22f-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="cb22f-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="cb22f-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="cb22f-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cb22f-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cb22f-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb22f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb22f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb22f-124">**IWMPErrorItem (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="cb22f-124">**IWMPErrorItem (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cb22f-125">**Interface IWMPMedia2 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="cb22f-125">**IWMPMedia2 Interface (VB and C#)**</span></span>](iwmpmedia2--vb-and-c.md)
</dt> </dl>

 

 





