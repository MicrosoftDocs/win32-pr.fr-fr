---
description: 'IPortableDeviceKeyCollection :: RemoveAt, méthode-la méthode RemoveAt supprime l’élément stocké à l’emplacement spécifié par l’index donné.'
ms.assetid: 70f220be-d70b-4a25-8e16-82ed42adf2c4
title: 'IPortableDeviceKeyCollection :: RemoveAt, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 3ec2b1137e7959a646c2943ab1aa7a5c3428d3c0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109940"
---
# <a name="iportabledevicekeycollectionremoveat-method"></a><span data-ttu-id="2ca9a-103">IPortableDeviceKeyCollection :: RemoveAt, méthode</span><span class="sxs-lookup"><span data-stu-id="2ca9a-103">IPortableDeviceKeyCollection::RemoveAt method</span></span>

<span data-ttu-id="2ca9a-104">La méthode **RemoveAt** supprime l’élément stocké à l’emplacement spécifié par l’index donné.</span><span class="sxs-lookup"><span data-stu-id="2ca9a-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ca9a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ca9a-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="2ca9a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2ca9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ca9a-107">*dwIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ca9a-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ca9a-108">Spécifie l’index de l’élément à supprimer.</span><span class="sxs-lookup"><span data-stu-id="2ca9a-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ca9a-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2ca9a-109">Return value</span></span>

<span data-ttu-id="2ca9a-110">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2ca9a-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2ca9a-111">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2ca9a-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2ca9a-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2ca9a-112">Return code</span></span>                                                                                  | <span data-ttu-id="2ca9a-113">Description</span><span class="sxs-lookup"><span data-stu-id="2ca9a-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="2ca9a-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2ca9a-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="2ca9a-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="2ca9a-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="2ca9a-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2ca9a-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="2ca9a-117">L’index spécifié était hors limites.</span><span class="sxs-lookup"><span data-stu-id="2ca9a-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2ca9a-118">Notes </span><span class="sxs-lookup"><span data-stu-id="2ca9a-118">Remarks</span></span>

<span data-ttu-id="2ca9a-119">Vous devez spécifier un index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="2ca9a-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ca9a-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ca9a-120">Requirements</span></span>



| <span data-ttu-id="2ca9a-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ca9a-121">Requirement</span></span> | <span data-ttu-id="2ca9a-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ca9a-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca9a-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="2ca9a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="2ca9a-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ca9a-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="2ca9a-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2ca9a-125">Library</span></span><br/> | <dl> <span data-ttu-id="2ca9a-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ca9a-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ca9a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ca9a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ca9a-128">**Interface IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="2ca9a-128">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> </dl>

 

 




