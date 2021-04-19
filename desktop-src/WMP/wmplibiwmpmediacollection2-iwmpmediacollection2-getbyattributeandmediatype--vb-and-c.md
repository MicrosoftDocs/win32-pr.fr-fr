---
title: Méthode IWMPMediaCollection2 getByAttributeAndMediaType
description: La méthode getByAttributeAndMediaType retourne une interface IWMPPlaylist qui fournit l’accès aux éléments multimédias qui ont un attribut et un type de média spécifiés.
ms.assetid: dce9cef4-1d12-4bee-a75d-42274556c5bc
keywords:
- méthode getByAttributeAndMediaType lecteur Windows Media
- méthode getByAttributeAndMediaType lecteur Windows Media, interface IWMPMediaCollection2
- Interface IWMPMediaCollection2 lecteur Windows Media, méthode getByAttributeAndMediaType
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getByAttributeAndMediaType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb1ee4e9421b4546cdc8ace6173dacab5034b905
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531136"
---
# <a name="iwmpmediacollection2getbyattributeandmediatype-method"></a><span data-ttu-id="49807-106">IWMPMediaCollection2 :: getByAttributeAndMediaType, méthode</span><span class="sxs-lookup"><span data-stu-id="49807-106">IWMPMediaCollection2::getByAttributeAndMediaType method</span></span>

<span data-ttu-id="49807-107">La `getByAttributeAndMediaType` méthode retourne une interface **IWMPPlaylist** qui fournit l’accès aux éléments multimédias qui ont un attribut et un type de média spécifiés.</span><span class="sxs-lookup"><span data-stu-id="49807-107">The `getByAttributeAndMediaType` method returns an **IWMPPlaylist** interface that provides access to media items that have a specified attribute and media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="49807-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49807-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAttributeAndMediaType(
  System.String bstrAttribute,
  System.String bstrValue,
  System.String bstrMediaType
);
```


```VB

Public Function getByAttributeAndMediaType( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String, _
  ByVal bstrMediaType As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getByAttributeAndMediaType
```





## <a name="parameters"></a><span data-ttu-id="49807-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49807-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49807-110">*bstrAttribute* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49807-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49807-111">**System. String** qui est l’attribut spécifié.</span><span class="sxs-lookup"><span data-stu-id="49807-111">The **System.String** that is the specified attribute.</span></span>

</dd> <dt>

<span data-ttu-id="49807-112">*bstrValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49807-112">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49807-113">**System. String** qui est la valeur spécifiée pour l’attribut spécifié dans *bstrAttribute*.</span><span class="sxs-lookup"><span data-stu-id="49807-113">The **System.String** that is the specified value for the attribute that is specified in *bstrAttribute*.</span></span>

</dd> <dt>

<span data-ttu-id="49807-114">*bstrMediaType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49807-114">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49807-115">**System. String** qui est le type de média spécifié.</span><span class="sxs-lookup"><span data-stu-id="49807-115">The **System.String** that is the specified media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49807-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49807-116">Return value</span></span>

<span data-ttu-id="49807-117">Interface **wmplib. IWMPPlaylist** pour la sélection récupérée.</span><span class="sxs-lookup"><span data-stu-id="49807-117">A **WMPLib.IWMPPlaylist** interface for the retrieved playlist.</span></span>

## <a name="requirements"></a><span data-ttu-id="49807-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49807-118">Requirements</span></span>



| <span data-ttu-id="49807-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49807-119">Requirement</span></span> | <span data-ttu-id="49807-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="49807-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49807-121">Version</span><span class="sxs-lookup"><span data-stu-id="49807-121">Version</span></span><br/>   | <span data-ttu-id="49807-122">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="49807-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="49807-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="49807-123">Namespace</span></span><br/> | <span data-ttu-id="49807-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="49807-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="49807-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="49807-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="49807-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="49807-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49807-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49807-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49807-128">**Interface IWMPMediaCollection2 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="49807-128">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="49807-129">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="49807-129">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





