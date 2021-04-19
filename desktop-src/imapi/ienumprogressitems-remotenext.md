---
title: Méthode IEnumProgressItems RemoteNext
description: Prend en charge un client distant qui souhaite récupérer un nombre spécifié d’éléments dans la séquence d’énumération. | Méthode IEnumProgressItems RemoteNext
ms.assetid: c5f85ca3-1bad-49fd-9e67-d41135cd837d
keywords:
- Méthode RemoteNext IMAPi
- Méthode RemoteNext IMAPi, interface IEnumProgressItems
- Interface IEnumProgressItems IMAPi, méthode RemoteNext
topic_type:
- apiref
api_name:
- IEnumProgressItems.RemoteNext
api_location:
- Imapi2fs.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a088a1be640c6653a8a8ccd8b00cf21bd027ecd7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106525834"
---
# <a name="ienumprogressitemsremotenext-method"></a><span data-ttu-id="d1173-107">IEnumProgressItems :: RemoteNext, méthode</span><span class="sxs-lookup"><span data-stu-id="d1173-107">IEnumProgressItems::RemoteNext method</span></span>

<span data-ttu-id="d1173-108">Prend en charge un client distant qui souhaite récupérer un nombre spécifié d’éléments dans la séquence d’énumération</span><span class="sxs-lookup"><span data-stu-id="d1173-108">Supports a remote client that wants to retrieve a specified number of items in the enumeration sequence</span></span>

## <a name="syntax"></a><span data-ttu-id="d1173-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1173-109">Syntax</span></span>


```C++
HRESULT RemoteNext(
  [in]  ULONG         celt,
  [out] IProgressItem **rgelt,
  [out] ULONG         *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="d1173-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1173-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1173-111">*celt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d1173-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1173-112">Nombre d’éléments à récupérer.</span><span class="sxs-lookup"><span data-stu-id="d1173-112">Number of items to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="d1173-113">*rgelt* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d1173-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1173-114">Tableau d’interfaces [**IProgressItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem) .</span><span class="sxs-lookup"><span data-stu-id="d1173-114">Array of [**IProgressItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem) interfaces.</span></span> <span data-ttu-id="d1173-115">Lorsque vous avez terminé, vous devez libérer chaque interface dans rgelt.</span><span class="sxs-lookup"><span data-stu-id="d1173-115">You must release each interface in rgelt when done.</span></span>

</dd> <dt>

<span data-ttu-id="d1173-116">*pceltFetched* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d1173-116">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1173-117">Nombre d’éléments retournés dans rgelt.</span><span class="sxs-lookup"><span data-stu-id="d1173-117">Number of elements returned in rgelt.</span></span> <span data-ttu-id="d1173-118">Vous pouvez affecter à *pceltFetched* la **valeur null** si *celt* est un.</span><span class="sxs-lookup"><span data-stu-id="d1173-118">You can set *pceltFetched* to **NULL** if *celt* is one.</span></span> <span data-ttu-id="d1173-119">Sinon, initialisez la valeur de *pceltFetched* à 0 avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="d1173-119">Otherwise, initialize the value of *pceltFetched* to 0 before calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1173-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d1173-120">Return value</span></span>

<span data-ttu-id="d1173-121">\_Un OK est retourné lorsque le nombre d’éléments demandés (*celt*) est retourné avec succès ou que le nombre d’éléments retournés (*pceltFetched*) est inférieur au nombre d’éléments demandés.</span><span class="sxs-lookup"><span data-stu-id="d1173-121">S\_OK is returned when the number of requested elements (*celt*) are returned successfully or the number of returned items (*pceltFetched*) is less than the number of requested elements.</span></span>

<span data-ttu-id="d1173-122">D’autres codes de réussite peuvent être retournés à la suite de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="d1173-122">Other success codes may be returned as a result of implementation.</span></span> <span data-ttu-id="d1173-123">Les codes d’erreur suivants sont généralement renvoyés en cas d’échec de l’opération, mais ne représentent pas les seules valeurs d’erreur possibles :</span><span class="sxs-lookup"><span data-stu-id="d1173-123">The following error codes are commonly returned on operation failure, but do not represent the only possible error values:</span></span>



| <span data-ttu-id="d1173-124">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d1173-124">Return code</span></span>                                                                                   | <span data-ttu-id="d1173-125">Description</span><span class="sxs-lookup"><span data-stu-id="d1173-125">Description</span></span>                                                                     |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d1173-126"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="d1173-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d1173-127">Le pointeur n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d1173-127">Pointer is not valid.</span></span><br/> <span data-ttu-id="d1173-128">Valeur : 0x80004003</span><span class="sxs-lookup"><span data-stu-id="d1173-128">Value: 0x80004003</span></span><br/>                   |
| <dl> <span data-ttu-id="d1173-129"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="d1173-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d1173-130">Impossible d’allouer la mémoire requise.</span><span class="sxs-lookup"><span data-stu-id="d1173-130">Failed to allocate the required memory.</span></span><br/> <span data-ttu-id="d1173-131">Valeur : 0x8007000E</span><span class="sxs-lookup"><span data-stu-id="d1173-131">Value: 0x8007000E</span></span><br/> |
| <dl> <span data-ttu-id="d1173-132"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d1173-132"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d1173-133">Un ou plusieurs arguments ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="d1173-133">One or more arguments are not valid.</span></span><br/> <span data-ttu-id="d1173-134">Valeur : 0x80070057</span><span class="sxs-lookup"><span data-stu-id="d1173-134">Value: 0x80070057</span></span><br/>    |
| <dl> <span data-ttu-id="d1173-135"><dt>**E \_ Inattendue**</dt></span><span class="sxs-lookup"><span data-stu-id="d1173-135"><dt> **E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="d1173-136">Une défaillance inattendue s'est produite.</span><span class="sxs-lookup"><span data-stu-id="d1173-136">An unexpected failure occurred.</span></span><br/> <span data-ttu-id="d1173-137">Valeur : 0x8000FFFF</span><span class="sxs-lookup"><span data-stu-id="d1173-137">Value: 0x8000FFFF</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="d1173-138">Notes</span><span class="sxs-lookup"><span data-stu-id="d1173-138">Remarks</span></span>

<span data-ttu-id="d1173-139">Si le nombre d’éléments restants dans la séquence est inférieur au nombre demandé, il récupère les éléments restants.</span><span class="sxs-lookup"><span data-stu-id="d1173-139">If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1173-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1173-140">Requirements</span></span>



| <span data-ttu-id="d1173-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1173-141">Requirement</span></span> | <span data-ttu-id="d1173-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1173-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1173-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1173-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d1173-144">Windows Vista, Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1173-144">Windows Vista, Windows XP with SP2 \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="d1173-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1173-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d1173-146">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1173-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d1173-147">MIDL</span><span class="sxs-lookup"><span data-stu-id="d1173-147">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d1173-148"><dt>Imapi2fs. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d1173-148"><dt>Imapi2fs.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1173-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1173-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1173-150">**IEnumProgressItems**</span><span class="sxs-lookup"><span data-stu-id="d1173-150">**IEnumProgressItems**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems)
</dt> <dt>

[<span data-ttu-id="d1173-151">IEnumProgressItems :: suivant</span><span class="sxs-lookup"><span data-stu-id="d1173-151">IEnumProgressItems::Next</span></span>](/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumprogressitems-next)
</dt> </dl>

 

 





