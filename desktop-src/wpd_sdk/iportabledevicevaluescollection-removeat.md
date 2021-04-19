---
description: La méthode RemoveAt supprime l’élément stocké à l’emplacement spécifié par l’index donné.
ms.assetid: 380212b6-5e71-406b-8236-e06672505f17
title: 'IPortableDeviceValuesCollection :: RemoveAt, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 004e8d855e79075fe3ae83bbde695e42487963f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532502"
---
# <a name="iportabledevicevaluescollectionremoveat-method"></a><span data-ttu-id="f846a-103">IPortableDeviceValuesCollection :: RemoveAt, méthode</span><span class="sxs-lookup"><span data-stu-id="f846a-103">IPortableDeviceValuesCollection::RemoveAt method</span></span>

<span data-ttu-id="f846a-104">La méthode **RemoveAt** supprime l’élément stocké à l’emplacement spécifié par l’index donné.</span><span class="sxs-lookup"><span data-stu-id="f846a-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="f846a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f846a-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="f846a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f846a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f846a-107">*dwIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f846a-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f846a-108">Spécifie l’index de l’élément à supprimer.</span><span class="sxs-lookup"><span data-stu-id="f846a-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f846a-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f846a-109">Return value</span></span>

<span data-ttu-id="f846a-110">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f846a-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f846a-111">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f846a-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f846a-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f846a-112">Return code</span></span>                                                                                  | <span data-ttu-id="f846a-113">Description</span><span class="sxs-lookup"><span data-stu-id="f846a-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="f846a-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f846a-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="f846a-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="f846a-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="f846a-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f846a-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="f846a-117">L’index spécifié était hors limites.</span><span class="sxs-lookup"><span data-stu-id="f846a-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f846a-118">Notes</span><span class="sxs-lookup"><span data-stu-id="f846a-118">Remarks</span></span>

<span data-ttu-id="f846a-119">Vous devez spécifier un index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="f846a-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="f846a-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f846a-120">Requirements</span></span>



| <span data-ttu-id="f846a-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f846a-121">Requirement</span></span> | <span data-ttu-id="f846a-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f846a-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f846a-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="f846a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f846a-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="f846a-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="f846a-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f846a-125">Library</span></span><br/> | <dl> <span data-ttu-id="f846a-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f846a-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f846a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f846a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f846a-128">**Interface IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="f846a-128">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




