---
description: Convertit un tableau d’octets défini en tant que SAFEARRAY en une mémoire tampon universelle d’octets (objet IStream).
ms.assetid: faa07bb5-cfdb-4181-b86a-f82a9c6b251a
title: 'ISCardTypeConv :: ConvertSafeArrayToByteBuffer, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertSafeArrayToByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: aa6503f474d96e3c25da3f2780ac43976b6507a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951123"
---
# <a name="iscardtypeconvconvertsafearraytobytebuffer-method"></a><span data-ttu-id="1c73d-103">ISCardTypeConv :: ConvertSafeArrayToByteBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="1c73d-103">ISCardTypeConv::ConvertSafeArrayToByteBuffer method</span></span>

<span data-ttu-id="1c73d-104">\[La méthode **ConvertSafeArrayToByteBuffer** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="1c73d-104">\[The **ConvertSafeArrayToByteBuffer** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1c73d-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="1c73d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1c73d-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="1c73d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="1c73d-107">La méthode **ConvertSafeArrayToByteBuffer** convertit un tableau d’octets défini en tant que SAFEARRAY en une mémoire tampon universelle d’octets (objet **IStream** ).</span><span class="sxs-lookup"><span data-stu-id="1c73d-107">The **ConvertSafeArrayToByteBuffer** method converts a byte array defined as a SAFEARRAY into a universal buffer of bytes (**IStream** object).</span></span>

<span data-ttu-id="1c73d-108">La mémoire tampon d’octets créée est un flux mappé sur un bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="1c73d-108">The byte buffer created is a stream mapped over a memory block.</span></span> <span data-ttu-id="1c73d-109">Pour accéder à la mémoire tampon ou la gérer, utilisez les méthodes fournies par l’interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="1c73d-109">To access or manage the buffer, use the methods provided by the **IStream** interface.</span></span> <span data-ttu-id="1c73d-110">Une fonctionnalité unique de cette implémentation de tableau est que lorsque vous appelez la méthode **IStream :: Release** , la mémoire sous-jacente est libérée pour vous.</span><span class="sxs-lookup"><span data-stu-id="1c73d-110">A unique feature about this array implementation is that when you call the **IStream::Release** method, the underlying memory will be released for you.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c73d-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c73d-111">Syntax</span></span>


```C++
HRESULT ConvertSafeArrayToByteBuffer(
  [in]  LPSAFEARRAY  pbyArray,
  [out] LPBYTEBUFFER *ppbyBuff
);
```



## <a name="parameters"></a><span data-ttu-id="1c73d-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c73d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c73d-113">*pbyArray* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1c73d-113">*pbyArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c73d-114">Pointeur vers le SAFEARRAY à convertir.</span><span class="sxs-lookup"><span data-stu-id="1c73d-114">Pointer to the SAFEARRAY to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="1c73d-115">*ppbyBuff* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1c73d-115">*ppbyBuff* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c73d-116">Pointeur vers l’objet **IStream** à retourner.</span><span class="sxs-lookup"><span data-stu-id="1c73d-116">Pointer to the **IStream** object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c73d-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1c73d-117">Return value</span></span>

<span data-ttu-id="1c73d-118">La méthode retourne l’une des valeurs possibles suivantes :</span><span class="sxs-lookup"><span data-stu-id="1c73d-118">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="1c73d-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1c73d-119">Return code</span></span>                                                                                   | <span data-ttu-id="1c73d-120">Description</span><span class="sxs-lookup"><span data-stu-id="1c73d-120">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1c73d-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1c73d-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1c73d-122">Mémoire allouée avec succès.</span><span class="sxs-lookup"><span data-stu-id="1c73d-122">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="1c73d-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1c73d-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1c73d-124">Il y a un problème avec un ou plusieurs des paramètres transmis à la fonction.</span><span class="sxs-lookup"><span data-stu-id="1c73d-124">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="1c73d-125"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="1c73d-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1c73d-126">Un paramètre de type pointeur était incorrect.</span><span class="sxs-lookup"><span data-stu-id="1c73d-126">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="1c73d-127"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="1c73d-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1c73d-128">Mémoire libre insuffisante pour satisfaire la demande.</span><span class="sxs-lookup"><span data-stu-id="1c73d-128">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="1c73d-129">Notes</span><span class="sxs-lookup"><span data-stu-id="1c73d-129">Remarks</span></span>

<span data-ttu-id="1c73d-130">La mémoire allouée est déplaçable.</span><span class="sxs-lookup"><span data-stu-id="1c73d-130">Memory allocated is moveable.</span></span> <span data-ttu-id="1c73d-131">Utilisez la méthode **IStream :: Release** pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="1c73d-131">Use the **IStream::Release** method to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c73d-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c73d-132">Requirements</span></span>



| <span data-ttu-id="1c73d-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c73d-133">Requirement</span></span> | <span data-ttu-id="1c73d-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c73d-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c73d-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c73d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1c73d-136">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c73d-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1c73d-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c73d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1c73d-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c73d-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1c73d-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="1c73d-139">End of client support</span></span><br/>    | <span data-ttu-id="1c73d-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1c73d-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="1c73d-141">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="1c73d-141">End of server support</span></span><br/>    | <span data-ttu-id="1c73d-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1c73d-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="1c73d-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="1c73d-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c73d-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c73d-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="1c73d-145">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="1c73d-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="1c73d-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1c73d-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1c73d-147">DLL</span><span class="sxs-lookup"><span data-stu-id="1c73d-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c73d-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c73d-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1c73d-149">IID</span><span class="sxs-lookup"><span data-stu-id="1c73d-149">IID</span></span><br/>                      | <span data-ttu-id="1c73d-150">IID \_ ISCardTypeConv est défini en tant que 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="1c73d-150">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="1c73d-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c73d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c73d-152">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="1c73d-152">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="1c73d-153">Valeurs de retour de carte à puce</span><span class="sxs-lookup"><span data-stu-id="1c73d-153">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
