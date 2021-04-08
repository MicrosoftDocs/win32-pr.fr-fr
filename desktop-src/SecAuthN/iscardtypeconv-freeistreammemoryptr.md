---
description: Libère le pointeur d’octet pointant vers le bloc de mémoire HGLOBAL géré par une interface COM IStream.
ms.assetid: a76c97a9-d0e9-4eb0-9f97-15f22111187d
title: 'ISCardTypeConv :: FreeIStreamMemoryPtr, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.FreeIStreamMemoryPtr
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 12912b8130ed6e1ccaa995f88069b59e96f57c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756874"
---
# <a name="iscardtypeconvfreeistreammemoryptr-method"></a><span data-ttu-id="0f3f2-103">ISCardTypeConv :: FreeIStreamMemoryPtr, méthode</span><span class="sxs-lookup"><span data-stu-id="0f3f2-103">ISCardTypeConv::FreeIStreamMemoryPtr method</span></span>

<span data-ttu-id="0f3f2-104">\[La méthode **FreeIStreamMemoryPtr** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="0f3f2-104">\[The **FreeIStreamMemoryPtr** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0f3f2-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0f3f2-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0f3f2-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="0f3f2-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="0f3f2-107">La méthode **FreeIStreamMemoryPtr** libère le pointeur d’octet pointant vers le bloc de mémoire HGLOBAL géré par une interface com **IStream** .</span><span class="sxs-lookup"><span data-stu-id="0f3f2-107">The **FreeIStreamMemoryPtr** method frees the byte pointer pointing to the HGLOBAL memory block managed by an **IStream** COM interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f3f2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f3f2-108">Syntax</span></span>


```C++
HRESULT FreeIStreamMemoryPtr(
  [in] LPSTREAM pStrm,
  [in] LPBYTE   pMem
);
```



## <a name="parameters"></a><span data-ttu-id="0f3f2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f3f2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f3f2-110">*pStrm* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0f3f2-110">*pStrm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f3f2-111">Pointeur vers l’interface **IStream** qui gère le bloc de mémoire pointé par *pMem*.</span><span class="sxs-lookup"><span data-stu-id="0f3f2-111">Pointer to the **IStream** interface that manages the memory block pointed to by *pMem*.</span></span>

</dd> <dt>

<span data-ttu-id="0f3f2-112">*PMEM* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0f3f2-112">*pMem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f3f2-113">Pointeur vers le bloc de mémoire géré par l’interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="0f3f2-113">Pointer to the memory block managed by the **IStream** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f3f2-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0f3f2-114">Return value</span></span>

<span data-ttu-id="0f3f2-115">La méthode retourne l’une des valeurs possibles suivantes :</span><span class="sxs-lookup"><span data-stu-id="0f3f2-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="0f3f2-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0f3f2-116">Return code</span></span>                                                                                   | <span data-ttu-id="0f3f2-117">Description</span><span class="sxs-lookup"><span data-stu-id="0f3f2-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0f3f2-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0f3f2-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0f3f2-119">Mémoire allouée avec succès.</span><span class="sxs-lookup"><span data-stu-id="0f3f2-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="0f3f2-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0f3f2-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0f3f2-121">Il y a un problème avec un ou plusieurs des paramètres transmis à la fonction.</span><span class="sxs-lookup"><span data-stu-id="0f3f2-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="0f3f2-122"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="0f3f2-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0f3f2-123">Un paramètre de type pointeur était incorrect.</span><span class="sxs-lookup"><span data-stu-id="0f3f2-123">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="0f3f2-124"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="0f3f2-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0f3f2-125">Mémoire libre insuffisante pour satisfaire la demande.</span><span class="sxs-lookup"><span data-stu-id="0f3f2-125">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="0f3f2-126">Notes</span><span class="sxs-lookup"><span data-stu-id="0f3f2-126">Remarks</span></span>

<span data-ttu-id="0f3f2-127">Cette fonction libère complètement et correctement le pointeur d’octet pointant vers le bloc de mémoire HGLOBAL géré par l’interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="0f3f2-127">This function completely and cleanly releases the byte pointer pointing to the HGLOBAL memory block managed by the **IStream** interface.</span></span> <span data-ttu-id="0f3f2-128">Le pointeur d’octet est acquis par un appel à [**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md).</span><span class="sxs-lookup"><span data-stu-id="0f3f2-128">The byte pointer is acquired by a call to [**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f3f2-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f3f2-129">Requirements</span></span>



| <span data-ttu-id="0f3f2-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f3f2-130">Requirement</span></span> | <span data-ttu-id="0f3f2-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f3f2-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f3f2-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f3f2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0f3f2-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f3f2-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0f3f2-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f3f2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0f3f2-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f3f2-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0f3f2-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="0f3f2-136">End of client support</span></span><br/>    | <span data-ttu-id="0f3f2-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0f3f2-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="0f3f2-138">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="0f3f2-138">End of server support</span></span><br/>    | <span data-ttu-id="0f3f2-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0f3f2-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="0f3f2-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f3f2-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f3f2-141"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f3f2-141"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="0f3f2-142">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="0f3f2-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="0f3f2-143"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0f3f2-143"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0f3f2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0f3f2-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f3f2-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f3f2-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0f3f2-146">IID</span><span class="sxs-lookup"><span data-stu-id="0f3f2-146">IID</span></span><br/>                      | <span data-ttu-id="0f3f2-147">IID \_ ISCardTypeConv est défini en tant que 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="0f3f2-147">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0f3f2-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f3f2-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f3f2-149">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="0f3f2-149">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="0f3f2-150">Valeurs de retour de carte à puce</span><span class="sxs-lookup"><span data-stu-id="0f3f2-150">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> <dt>

[<span data-ttu-id="0f3f2-151">**GetAtIStreamMemory**</span><span class="sxs-lookup"><span data-stu-id="0f3f2-151">**GetAtIStreamMemory**</span></span>](iscardtypeconv-getatistreammemory.md)
</dt> </dl>

 

 
