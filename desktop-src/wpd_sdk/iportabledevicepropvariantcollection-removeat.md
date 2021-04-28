---
description: 'IPortableDevicePropVariantCollection :: RemoveAt, méthode-la méthode RemoveAt supprime l’élément stocké à l’emplacement spécifié par l’index donné.'
ms.assetid: cfee2454-5103-48ce-b9f7-1f76f5c18b6d
title: 'IPortableDevicePropVariantCollection :: RemoveAt, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5c62df57a95a9f5a8238ff61c4ca6dc3cb73ed36
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109941"
---
# <a name="iportabledevicepropvariantcollectionremoveat-method"></a><span data-ttu-id="b37ee-103">IPortableDevicePropVariantCollection :: RemoveAt, méthode</span><span class="sxs-lookup"><span data-stu-id="b37ee-103">IPortableDevicePropVariantCollection::RemoveAt method</span></span>

<span data-ttu-id="b37ee-104">La méthode **RemoveAt** supprime l’élément stocké à l’emplacement spécifié par l’index donné.</span><span class="sxs-lookup"><span data-stu-id="b37ee-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="b37ee-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b37ee-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="b37ee-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b37ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b37ee-107">*dwIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b37ee-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b37ee-108">Spécifie l’index de l’élément à supprimer.</span><span class="sxs-lookup"><span data-stu-id="b37ee-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b37ee-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b37ee-109">Return value</span></span>

<span data-ttu-id="b37ee-110">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b37ee-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b37ee-111">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b37ee-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b37ee-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b37ee-112">Return code</span></span>                                                                                  | <span data-ttu-id="b37ee-113">Description</span><span class="sxs-lookup"><span data-stu-id="b37ee-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="b37ee-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b37ee-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="b37ee-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="b37ee-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="b37ee-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b37ee-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="b37ee-117">L’index spécifié était hors limites.</span><span class="sxs-lookup"><span data-stu-id="b37ee-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b37ee-118">Notes </span><span class="sxs-lookup"><span data-stu-id="b37ee-118">Remarks</span></span>

<span data-ttu-id="b37ee-119">Vous devez spécifier un index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="b37ee-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="b37ee-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b37ee-120">Requirements</span></span>



| <span data-ttu-id="b37ee-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b37ee-121">Requirement</span></span> | <span data-ttu-id="b37ee-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="b37ee-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b37ee-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b37ee-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b37ee-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="b37ee-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="b37ee-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b37ee-125">Library</span></span><br/> | <dl> <span data-ttu-id="b37ee-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b37ee-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b37ee-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b37ee-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b37ee-128">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="b37ee-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




