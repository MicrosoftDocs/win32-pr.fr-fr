---
description: Crée une mémoire tampon universelle d’octets mappés à un objet IStream (IByteBuffer).
ms.assetid: 8015c7e8-2cbb-4ba8-9bd0-2f84751840f1
title: 'ISCardTypeConv :: CreateByteBuffer, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ab69c8061d2e2740e652e29b2fe6407574fe7076
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034575"
---
# <a name="iscardtypeconvcreatebytebuffer-method"></a><span data-ttu-id="605b5-103">ISCardTypeConv :: CreateByteBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="605b5-103">ISCardTypeConv::CreateByteBuffer method</span></span>

<span data-ttu-id="605b5-104">\[La méthode **CreateByteBuffer** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="605b5-104">\[The **CreateByteBuffer** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="605b5-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="605b5-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="605b5-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="605b5-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="605b5-107">La méthode **CreateByteBuffer** crée une mémoire tampon universelle d’octets mappés dans un objet **IStream** ([**IByteBuffer**](ibytebuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="605b5-107">The **CreateByteBuffer** method creates a universal buffer of bytes mapped into an **IStream** ([**IByteBuffer**](ibytebuffer.md)) object.</span></span>

<span data-ttu-id="605b5-108">La mémoire tampon d’octets créée est un flux mappé sur un bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="605b5-108">The byte buffer created is a stream mapped over a memory block.</span></span> <span data-ttu-id="605b5-109">Pour accéder à la mémoire tampon ou la gérer, utilisez les méthodes fournies par l’interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="605b5-109">To access or manage the buffer, use the methods provided by the **IStream** interface.</span></span> <span data-ttu-id="605b5-110">Une fonctionnalité unique de cette implémentation de tableau est que lorsque vous appelez la méthode **IStream :: Release** , la mémoire sous-jacente est libérée pour vous.</span><span class="sxs-lookup"><span data-stu-id="605b5-110">A unique feature about this array implementation is that when you call the **IStream::Release** method, the underlying memory will be released for you.</span></span>

## <a name="syntax"></a><span data-ttu-id="605b5-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="605b5-111">Syntax</span></span>


```C++
HRESULT CreateByteBuffer(
  [in]  DWORD        dwAllocSize,
  [out] LPBYTEBUFFER *ppbyBuff
);
```



## <a name="parameters"></a><span data-ttu-id="605b5-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="605b5-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="605b5-113">*dwAllocSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="605b5-113">*dwAllocSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="605b5-114">Taille en octets de la mémoire à allouer pour le tableau.</span><span class="sxs-lookup"><span data-stu-id="605b5-114">Size in bytes of the memory to be allocated for the array.</span></span>

</dd> <dt>

<span data-ttu-id="605b5-115">*ppbyBuff* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="605b5-115">*ppbyBuff* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="605b5-116">Pointeur vers l’objet IStream à retourner.</span><span class="sxs-lookup"><span data-stu-id="605b5-116">Pointer to the IStream object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="605b5-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="605b5-117">Return value</span></span>

<span data-ttu-id="605b5-118">Les valeurs de retour possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="605b5-118">The possible return values are the following:</span></span>



| <span data-ttu-id="605b5-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="605b5-119">Return code</span></span>                                                                                   | <span data-ttu-id="605b5-120">Description</span><span class="sxs-lookup"><span data-stu-id="605b5-120">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="605b5-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="605b5-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="605b5-122">Mémoire allouée avec succès.</span><span class="sxs-lookup"><span data-stu-id="605b5-122">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="605b5-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="605b5-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="605b5-124">Il y a un problème avec un ou plusieurs des paramètres transmis à la fonction.</span><span class="sxs-lookup"><span data-stu-id="605b5-124">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="605b5-125"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="605b5-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="605b5-126">Mémoire libre insuffisante pour satisfaire la demande.</span><span class="sxs-lookup"><span data-stu-id="605b5-126">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="605b5-127">Notes</span><span class="sxs-lookup"><span data-stu-id="605b5-127">Remarks</span></span>

<span data-ttu-id="605b5-128">La mémoire allouée est déplaçable.</span><span class="sxs-lookup"><span data-stu-id="605b5-128">Memory allocated is movable.</span></span> <span data-ttu-id="605b5-129">Utilisez la méthode **IStream :: Release** pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="605b5-129">Use the **IStream::Release** method to free the memory.</span></span>

<span data-ttu-id="605b5-130">Pour créer un tableau d’octets C/C++ classique, appelez [**CreateByteArray**](iscardtypeconv-createbytearray.md).</span><span class="sxs-lookup"><span data-stu-id="605b5-130">To create a typical C/C++ byte array, call [**CreateByteArray**](iscardtypeconv-createbytearray.md).</span></span>

<span data-ttu-id="605b5-131">Pour créer un SAFEARRAY Automation de caractères non signés (octets), appelez [**CreateSafeArray**](iscardtypeconv-createsafearray.md).</span><span class="sxs-lookup"><span data-stu-id="605b5-131">To create an Automation SAFEARRAY of unsigned characters (bytes), call [**CreateSafeArray**](iscardtypeconv-createsafearray.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="605b5-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="605b5-132">Requirements</span></span>



| <span data-ttu-id="605b5-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="605b5-133">Requirement</span></span> | <span data-ttu-id="605b5-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="605b5-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="605b5-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="605b5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="605b5-136">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="605b5-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="605b5-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="605b5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="605b5-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="605b5-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="605b5-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="605b5-139">End of client support</span></span><br/>    | <span data-ttu-id="605b5-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="605b5-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="605b5-141">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="605b5-141">End of server support</span></span><br/>    | <span data-ttu-id="605b5-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="605b5-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="605b5-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="605b5-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="605b5-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="605b5-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="605b5-145">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="605b5-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="605b5-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="605b5-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="605b5-147">DLL</span><span class="sxs-lookup"><span data-stu-id="605b5-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="605b5-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="605b5-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="605b5-149">IID</span><span class="sxs-lookup"><span data-stu-id="605b5-149">IID</span></span><br/>                      | <span data-ttu-id="605b5-150">IID \_ ISCardTypeConv est défini en tant que 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="605b5-150">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="605b5-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="605b5-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="605b5-152">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="605b5-152">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="605b5-153">Valeurs de retour de carte à puce</span><span class="sxs-lookup"><span data-stu-id="605b5-153">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> <dt>

[<span data-ttu-id="605b5-154">**CreateByteArray**</span><span class="sxs-lookup"><span data-stu-id="605b5-154">**CreateByteArray**</span></span>](iscardtypeconv-createbytearray.md)
</dt> <dt>

[<span data-ttu-id="605b5-155">**CreateSafeArray**</span><span class="sxs-lookup"><span data-stu-id="605b5-155">**CreateSafeArray**</span></span>](iscardtypeconv-createsafearray.md)
</dt> </dl>

 

 
