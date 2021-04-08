---
description: Acquiert un pointeur d’octet vers le bloc de mémoire HGLOBAL qui est géré par l’interface COM IStream.
ms.assetid: ea25eb98-b841-4f5e-b428-3d9cb8176142
title: 'ISCardTypeConv :: GetAtIStreamMemory, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.GetAtIStreamMemory
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bdd828921f18c3d06edd2d41da189260a4ed4394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750036"
---
# <a name="iscardtypeconvgetatistreammemory-method"></a><span data-ttu-id="68d94-103">ISCardTypeConv :: GetAtIStreamMemory, méthode</span><span class="sxs-lookup"><span data-stu-id="68d94-103">ISCardTypeConv::GetAtIStreamMemory method</span></span>

<span data-ttu-id="68d94-104">\[La méthode **GetAtIStreamMemory** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="68d94-104">\[The **GetAtIStreamMemory** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="68d94-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="68d94-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="68d94-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="68d94-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="68d94-107">La méthode **GetAtIStreamMemory** acquiert un pointeur d’octet vers le bloc de mémoire HGLOBAL qui est géré par l’interface com **IStream** .</span><span class="sxs-lookup"><span data-stu-id="68d94-107">The **GetAtIStreamMemory** method acquires a byte pointer to the HGLOBAL memory block that is managed by the **IStream** COM interface.</span></span>

<span data-ttu-id="68d94-108">Il s’agit d’un moyen d’obtenir la mémoire sous l' **IStream** sans avoir à obtenir la valeur sizeof du bloc de mémoire en octets et à lire les octets dans un tableau d’octets temporaire à l’aide de l’interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="68d94-108">This is a way to get at the memory under the **IStream** without having to get the sizeof value for the memory block in bytes and read the bytes into a temporary byte array using the **IStream** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="68d94-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68d94-109">Syntax</span></span>


```C++
HRESULT GetAtIStreamMemory(
  [in]  LPSTREAM    pStrm,
  [out] LPBYTEARRAY *ppMem
);
```



## <a name="parameters"></a><span data-ttu-id="68d94-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68d94-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68d94-111">*pStrm* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="68d94-111">*pStrm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68d94-112">Pointeur vers l’interface com **IStream** qui gère le bloc de mémoire HGLOBAL.</span><span class="sxs-lookup"><span data-stu-id="68d94-112">A pointer to the **IStream** COM interface that manages the HGLOBAL memory block.</span></span>

</dd> <dt>

<span data-ttu-id="68d94-113">*ppMem* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="68d94-113">*ppMem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68d94-114">Pointeur vers le premier octet du bloc de mémoire HGLOBAL en cas de réussite ; Sinon, **null** si l’opération échoue.</span><span class="sxs-lookup"><span data-stu-id="68d94-114">A pointer to the first byte of the HGLOBAL memory block if successful; else, **NULL** if operation fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68d94-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="68d94-115">Return value</span></span>

<span data-ttu-id="68d94-116">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="68d94-116">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="68d94-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="68d94-117">Return code</span></span>                                                                                   | <span data-ttu-id="68d94-118">Description</span><span class="sxs-lookup"><span data-stu-id="68d94-118">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="68d94-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="68d94-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="68d94-120">Mémoire allouée avec succès.</span><span class="sxs-lookup"><span data-stu-id="68d94-120">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="68d94-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="68d94-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="68d94-122">Il y a un problème avec un ou plusieurs des paramètres transmis à la fonction.</span><span class="sxs-lookup"><span data-stu-id="68d94-122">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="68d94-123"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="68d94-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="68d94-124">Un paramètre de type pointeur était incorrect.</span><span class="sxs-lookup"><span data-stu-id="68d94-124">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="68d94-125"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="68d94-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="68d94-126">Mémoire libre insuffisante pour satisfaire la demande.</span><span class="sxs-lookup"><span data-stu-id="68d94-126">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="68d94-127">Notes</span><span class="sxs-lookup"><span data-stu-id="68d94-127">Remarks</span></span>

<span data-ttu-id="68d94-128">Le nombre de références **IStream** sera incrémenté pour chaque pointeur *ppMem* acquis.</span><span class="sxs-lookup"><span data-stu-id="68d94-128">The **IStream** reference count will be incremented for each *ppMem* pointer acquired.</span></span>

## <a name="requirements"></a><span data-ttu-id="68d94-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68d94-129">Requirements</span></span>



| <span data-ttu-id="68d94-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68d94-130">Requirement</span></span> | <span data-ttu-id="68d94-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="68d94-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68d94-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68d94-132">Minimum supported client</span></span><br/> | <span data-ttu-id="68d94-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="68d94-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="68d94-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68d94-134">Minimum supported server</span></span><br/> | <span data-ttu-id="68d94-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="68d94-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="68d94-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="68d94-136">End of client support</span></span><br/>    | <span data-ttu-id="68d94-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="68d94-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="68d94-138">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="68d94-138">End of server support</span></span><br/>    | <span data-ttu-id="68d94-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="68d94-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="68d94-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="68d94-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="68d94-141"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="68d94-141"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="68d94-142">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="68d94-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="68d94-143"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="68d94-143"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="68d94-144">DLL</span><span class="sxs-lookup"><span data-stu-id="68d94-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68d94-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68d94-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="68d94-146">IID</span><span class="sxs-lookup"><span data-stu-id="68d94-146">IID</span></span><br/>                      | <span data-ttu-id="68d94-147">IID \_ ISCardTypeConv est défini en tant que 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="68d94-147">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="68d94-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68d94-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68d94-149">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="68d94-149">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="68d94-150">Valeurs de retour de carte à puce</span><span class="sxs-lookup"><span data-stu-id="68d94-150">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
