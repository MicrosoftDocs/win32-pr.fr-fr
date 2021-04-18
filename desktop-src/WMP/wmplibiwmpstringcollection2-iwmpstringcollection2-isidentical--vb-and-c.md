---
title: Méthode IWMPStringCollection2 isIdentical
description: La méthode isIdentical retourne une valeur indiquant si l’objet représenté par l’interface fournie est le même que celui en cours.
ms.assetid: 826e7fd8-88f8-4a2a-9ca0-82a500099272
keywords:
- méthode isIdentical lecteur Windows Media
- méthode isIdentical lecteur Windows Media, interface IWMPStringCollection2
- Interface IWMPStringCollection2 lecteur Windows Media, méthode isIdentical
topic_type:
- apiref
api_name:
- IWMPStringCollection2.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb760dae213f28d44fbc707b4430cb151cfe578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533423"
---
# <a name="iwmpstringcollection2isidentical-method"></a><span data-ttu-id="5f8f2-106">IWMPStringCollection2 :: isIdentical, méthode</span><span class="sxs-lookup"><span data-stu-id="5f8f2-106">IWMPStringCollection2::isIdentical method</span></span>

<span data-ttu-id="5f8f2-107">La méthode **isIdentical** retourne une valeur indiquant si l’objet représenté par l’interface fournie est le même que celui en cours.</span><span class="sxs-lookup"><span data-stu-id="5f8f2-107">The **isIdentical** method returns a value indicating whether the object represented by the supplied interface is the same as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f8f2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f8f2-108">Syntax</span></span>


```CSharp
public System.Boolean isIdentical(
  IWMPStringCollection2 pIWMPStringCollection2
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPStringCollection2 As IWMPStringCollection2 _
) As System.Boolean
Implements IWMPStringCollection2.isIdentical
```





## <a name="parameters"></a><span data-ttu-id="5f8f2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f8f2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f8f2-110">*pIWMPStringCollection2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f8f2-110">*pIWMPStringCollection2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f8f2-111">Interface **wmplib. IWMPStringCollection2** qui représente l’objet à comparer avec l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="5f8f2-111">The **WMPLib.IWMPStringCollection2** interface that represents the object to compare with current one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f8f2-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5f8f2-112">Return value</span></span>

<span data-ttu-id="5f8f2-113">**System. Boolean** qui est le résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="5f8f2-113">The **System.Boolean** that is the result of the comparison.</span></span> <span data-ttu-id="5f8f2-114">La valeur **true** indique que les objets de collection de chaînes sont identiques.</span><span class="sxs-lookup"><span data-stu-id="5f8f2-114">A value of **true** indicates that the string collection objects are the same.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f8f2-115">Notes</span><span class="sxs-lookup"><span data-stu-id="5f8f2-115">Remarks</span></span>

<span data-ttu-id="5f8f2-116">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="5f8f2-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="5f8f2-117">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="5f8f2-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f8f2-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f8f2-118">Requirements</span></span>



| <span data-ttu-id="5f8f2-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f8f2-119">Requirement</span></span> | <span data-ttu-id="5f8f2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f8f2-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f8f2-121">Version</span><span class="sxs-lookup"><span data-stu-id="5f8f2-121">Version</span></span><br/>   | <span data-ttu-id="5f8f2-122">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="5f8f2-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="5f8f2-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5f8f2-123">Namespace</span></span><br/> | <span data-ttu-id="5f8f2-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="5f8f2-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="5f8f2-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="5f8f2-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5f8f2-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5f8f2-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f8f2-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f8f2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f8f2-128">**Interface IWMPStringCollection2 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="5f8f2-128">**IWMPStringCollection2 Interface (VB and C#)**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> </dl>

 

 





