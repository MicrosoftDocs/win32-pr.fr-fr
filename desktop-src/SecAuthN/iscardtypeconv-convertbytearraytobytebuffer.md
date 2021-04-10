---
description: Convertit un tableau d’octets C/C++ classique en une mémoire tampon universelle d’octets (objet IStream).
ms.assetid: 512c561a-63f1-463e-9bae-9bec1ebdbe9b
title: 'ISCardTypeConv :: ConvertByteArrayToByteBuffer, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteArrayToByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 406e7aecb7e86802ad67c07669ca199b158ad954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867838"
---
# <a name="iscardtypeconvconvertbytearraytobytebuffer-method"></a><span data-ttu-id="3e777-103">ISCardTypeConv :: ConvertByteArrayToByteBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="3e777-103">ISCardTypeConv::ConvertByteArrayToByteBuffer method</span></span>

<span data-ttu-id="3e777-104">\[La méthode **ConvertByteArrayToByteBuffer** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="3e777-104">\[The **ConvertByteArrayToByteBuffer** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3e777-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3e777-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3e777-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="3e777-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="3e777-107">La méthode **ConvertByteArrayToByteBuffer** convertit un tableau d’octets C/C++ classique en une mémoire tampon universelle d’octets (objet **IStream** ).</span><span class="sxs-lookup"><span data-stu-id="3e777-107">The **ConvertByteArrayToByteBuffer** method converts a typical C/C++ byte array into a universal buffer of bytes (**IStream** object).</span></span>

<span data-ttu-id="3e777-108">La mémoire tampon d’octets créée est un flux mappé sur un bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="3e777-108">The byte buffer created is a stream mapped over a memory block.</span></span> <span data-ttu-id="3e777-109">Pour accéder à la mémoire tampon ou la gérer, utilisez les méthodes fournies par l’interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="3e777-109">To access or manage the buffer, use the methods provided by the **IStream** interface.</span></span> <span data-ttu-id="3e777-110">Une fonctionnalité unique de cette implémentation de tableau est que lorsque vous appelez la méthode **IStream :: Release** , la mémoire sous-jacente est libérée pour vous.</span><span class="sxs-lookup"><span data-stu-id="3e777-110">A unique feature about this array implementation is that when you call the **IStream::Release** method, the underlying memory will be released for you.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e777-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e777-111">Syntax</span></span>


```C++
HRESULT ConvertByteArrayToByteBuffer(
  [in]  LPBYTE       pbyArray,
  [in]  DWORD        dwArraySize,
  [out] LPBYTEBUFFER *ppbyBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="3e777-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e777-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e777-113">*pbyArray* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3e777-113">*pbyArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e777-114">Pointeur vers le tableau d’octets à convertir.</span><span class="sxs-lookup"><span data-stu-id="3e777-114">Pointer to the array of bytes to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="3e777-115">*dwArraySize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3e777-115">*dwArraySize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e777-116">Taille du tableau d’octets à convertir.</span><span class="sxs-lookup"><span data-stu-id="3e777-116">Size of the byte array to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="3e777-117">*ppbyBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3e777-117">*ppbyBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e777-118">Pointeur vers l’objet **IStream** à retourner.</span><span class="sxs-lookup"><span data-stu-id="3e777-118">Pointer to the **IStream** object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e777-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3e777-119">Return value</span></span>

<span data-ttu-id="3e777-120">La méthode retourne l’une des valeurs possibles suivantes :</span><span class="sxs-lookup"><span data-stu-id="3e777-120">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="3e777-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3e777-121">Return code</span></span>                                                                                   | <span data-ttu-id="3e777-122">Description</span><span class="sxs-lookup"><span data-stu-id="3e777-122">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3e777-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3e777-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3e777-124">Mémoire allouée avec succès.</span><span class="sxs-lookup"><span data-stu-id="3e777-124">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="3e777-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3e777-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3e777-126">Il y a un problème avec un ou plusieurs des paramètres transmis à la fonction.</span><span class="sxs-lookup"><span data-stu-id="3e777-126">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="3e777-127"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="3e777-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3e777-128">Un paramètre de type pointeur était incorrect.</span><span class="sxs-lookup"><span data-stu-id="3e777-128">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="3e777-129"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="3e777-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3e777-130">Mémoire libre insuffisante pour satisfaire la demande.</span><span class="sxs-lookup"><span data-stu-id="3e777-130">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="3e777-131">Notes</span><span class="sxs-lookup"><span data-stu-id="3e777-131">Remarks</span></span>

<span data-ttu-id="3e777-132">La mémoire allouée est déplaçable.</span><span class="sxs-lookup"><span data-stu-id="3e777-132">Memory allocated is movable.</span></span> <span data-ttu-id="3e777-133">Utilisez la méthode **IStream :: Release** pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="3e777-133">Use the **IStream::Release** method to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e777-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e777-134">Requirements</span></span>



| <span data-ttu-id="3e777-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e777-135">Requirement</span></span> | <span data-ttu-id="3e777-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e777-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e777-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e777-137">Minimum supported client</span></span><br/> | <span data-ttu-id="3e777-138">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e777-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3e777-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e777-139">Minimum supported server</span></span><br/> | <span data-ttu-id="3e777-140">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e777-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3e777-141">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="3e777-141">End of client support</span></span><br/>    | <span data-ttu-id="3e777-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e777-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="3e777-143">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="3e777-143">End of server support</span></span><br/>    | <span data-ttu-id="3e777-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3e777-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="3e777-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e777-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e777-146"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e777-146"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="3e777-147">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="3e777-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="3e777-148"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3e777-148"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3e777-149">DLL</span><span class="sxs-lookup"><span data-stu-id="3e777-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e777-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e777-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3e777-151">IID</span><span class="sxs-lookup"><span data-stu-id="3e777-151">IID</span></span><br/>                      | <span data-ttu-id="3e777-152">IID \_ ISCardTypeConv est défini en tant que 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="3e777-152">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="3e777-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e777-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e777-154">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="3e777-154">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="3e777-155">Valeurs de retour de carte à puce</span><span class="sxs-lookup"><span data-stu-id="3e777-155">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
