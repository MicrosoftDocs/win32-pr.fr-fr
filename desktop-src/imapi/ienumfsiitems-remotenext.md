---
title: Méthode IEnumFsiItems RemoteNext
description: Prend en charge un client distant qui souhaite récupérer un nombre spécifié d’éléments dans la séquence d’énumération. | Méthode IEnumFsiItems RemoteNext
ms.assetid: a5ae59ed-08d7-4225-9aec-91049789e8fe
keywords:
- Méthode RemoteNext IMAPi
- Méthode RemoteNext IMAPi, interface IEnumFsiItems
- Interface IEnumFsiItems IMAPi, méthode RemoteNext
topic_type:
- apiref
api_name:
- IEnumFsiItems.RemoteNext
api_location:
- Imapi2fs.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e29d3f75cd8e2f83fcd21236661d0d1fa0dabef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530712"
---
# <a name="ienumfsiitemsremotenext-method"></a><span data-ttu-id="faaf4-107">IEnumFsiItems :: RemoteNext, méthode</span><span class="sxs-lookup"><span data-stu-id="faaf4-107">IEnumFsiItems::RemoteNext method</span></span>

<span data-ttu-id="faaf4-108">Prend en charge un client distant qui souhaite récupérer un nombre spécifié d’éléments dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="faaf4-108">Supports a remote client that wants to retrieve a specified number of items in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="faaf4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="faaf4-109">Syntax</span></span>


```C++
HRESULT RemoteNext(
  [in]  ULONG    celt,
  [out] IFsiItem **rgelt,
  [out] ULONG    *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="faaf4-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="faaf4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="faaf4-111">*celt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="faaf4-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faaf4-112">Nombre d’éléments à récupérer.</span><span class="sxs-lookup"><span data-stu-id="faaf4-112">Number of items to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="faaf4-113">*rgelt* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="faaf4-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="faaf4-114">Tableau d’interfaces [**IFsiItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem) .</span><span class="sxs-lookup"><span data-stu-id="faaf4-114">Array of [**IFsiItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem) interfaces.</span></span> <span data-ttu-id="faaf4-115">Lorsque vous avez terminé, vous devez libérer chaque interface dans rgelt.</span><span class="sxs-lookup"><span data-stu-id="faaf4-115">You must release each interface in rgelt when done.</span></span>

</dd> <dt>

<span data-ttu-id="faaf4-116">*pceltFetched* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="faaf4-116">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="faaf4-117">Nombre d’éléments retournés dans rgelt.</span><span class="sxs-lookup"><span data-stu-id="faaf4-117">Number of elements returned in rgelt.</span></span> <span data-ttu-id="faaf4-118">Vous pouvez affecter à *pceltFetched* la **valeur null** si *celt* est un.</span><span class="sxs-lookup"><span data-stu-id="faaf4-118">You can set *pceltFetched* to **NULL** if *celt* is one.</span></span> <span data-ttu-id="faaf4-119">Sinon, initialisez la valeur de *pceltFetched* à 0 avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="faaf4-119">Otherwise, initialize the value of *pceltFetched* to 0 before calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="faaf4-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="faaf4-120">Return value</span></span>

<span data-ttu-id="faaf4-121">\_Un OK est retourné lorsque le nombre d’éléments demandés (*celt*) est retourné avec succès ou que le nombre d’éléments retournés (*pceltFetched*) est inférieur au nombre d’éléments demandés.</span><span class="sxs-lookup"><span data-stu-id="faaf4-121">S\_OK is returned when the number of requested elements (*celt*) are returned successfully or the number of returned items (*pceltFetched*) is less than the number of requested elements.</span></span>

<span data-ttu-id="faaf4-122">D’autres codes de réussite peuvent être retournés à la suite de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="faaf4-122">Other success codes may be returned as a result of implementation.</span></span> <span data-ttu-id="faaf4-123">Les codes d’erreur suivants sont généralement renvoyés en cas d’échec de l’opération, mais ne représentent pas les seules valeurs d’erreur possibles :</span><span class="sxs-lookup"><span data-stu-id="faaf4-123">The following error codes are commonly returned on operation failure, but do not represent the only possible error values:</span></span>



| <span data-ttu-id="faaf4-124">Code de retour</span><span class="sxs-lookup"><span data-stu-id="faaf4-124">Return code</span></span>                                                                                   | <span data-ttu-id="faaf4-125">Description</span><span class="sxs-lookup"><span data-stu-id="faaf4-125">Description</span></span>                                                                     |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="faaf4-126"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="faaf4-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="faaf4-127">Le pointeur n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="faaf4-127">Pointer is not valid.</span></span><br/> <span data-ttu-id="faaf4-128">Valeur : 0x80004003</span><span class="sxs-lookup"><span data-stu-id="faaf4-128">Value: 0x80004003</span></span><br/>                   |
| <dl> <span data-ttu-id="faaf4-129"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="faaf4-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="faaf4-130">Impossible d’allouer la mémoire requise.</span><span class="sxs-lookup"><span data-stu-id="faaf4-130">Failed to allocate the required memory.</span></span><br/> <span data-ttu-id="faaf4-131">Valeur : 0x8007000E</span><span class="sxs-lookup"><span data-stu-id="faaf4-131">Value: 0x8007000E</span></span><br/> |
| <dl> <span data-ttu-id="faaf4-132"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="faaf4-132"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="faaf4-133">Un ou plusieurs arguments ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="faaf4-133">One or more arguments are not valid.</span></span><br/> <span data-ttu-id="faaf4-134">Valeur : 0x80070057</span><span class="sxs-lookup"><span data-stu-id="faaf4-134">Value: 0x80070057</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="faaf4-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="faaf4-135">Requirements</span></span>



| <span data-ttu-id="faaf4-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="faaf4-136">Requirement</span></span> | <span data-ttu-id="faaf4-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="faaf4-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="faaf4-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="faaf4-138">Minimum supported client</span></span><br/> | <span data-ttu-id="faaf4-139">Windows Vista, Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="faaf4-139">Windows Vista, Windows XP with SP2 \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="faaf4-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="faaf4-140">Minimum supported server</span></span><br/> | <span data-ttu-id="faaf4-141">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="faaf4-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="faaf4-142">MIDL</span><span class="sxs-lookup"><span data-stu-id="faaf4-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="faaf4-143"><dt>Imapi2fs. idl</dt></span><span class="sxs-lookup"><span data-stu-id="faaf4-143"><dt>Imapi2fs.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faaf4-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="faaf4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faaf4-145">**IEnumFsiItems**</span><span class="sxs-lookup"><span data-stu-id="faaf4-145">**IEnumFsiItems**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems)
</dt> <dt>

[<span data-ttu-id="faaf4-146">IEnumFsiItems :: suivant</span><span class="sxs-lookup"><span data-stu-id="faaf4-146">IEnumFsiItems::Next</span></span>](/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumfsiitems-next)
</dt> </dl>

 

 





