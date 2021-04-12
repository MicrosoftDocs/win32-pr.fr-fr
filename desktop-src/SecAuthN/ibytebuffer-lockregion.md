---
description: Restreint l’accès à une plage d’octets spécifiée dans l’objet de mémoire tampon.
ms.assetid: 7bcb3c1e-5739-41f7-a3aa-2943542943ed
title: 'IByteBuffer :: LockRegion, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.LockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ae227d11892b604ab1382cb328dc492e4596f278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210024"
---
# <a name="ibytebufferlockregion-method"></a><span data-ttu-id="26d86-103">IByteBuffer :: LockRegion, méthode</span><span class="sxs-lookup"><span data-stu-id="26d86-103">IByteBuffer::LockRegion method</span></span>

<span data-ttu-id="26d86-104">\[La méthode **LockRegion** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="26d86-104">\[The **LockRegion** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="26d86-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="26d86-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="26d86-106">L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="26d86-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="26d86-107">La méthode **LockRegion** restreint l’accès à une plage d’octets spécifiée dans l’objet buffer.</span><span class="sxs-lookup"><span data-stu-id="26d86-107">The **LockRegion** method restricts access to a specified range of bytes in the buffer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="26d86-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26d86-108">Syntax</span></span>


```C++
HRESULT LockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a><span data-ttu-id="26d86-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26d86-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26d86-110">*Liboffset* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26d86-110">*libOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26d86-111">Entier qui spécifie l’offset d’octet pour le début de la plage.</span><span class="sxs-lookup"><span data-stu-id="26d86-111">Integer that specifies the byte offset for the beginning of the range.</span></span>

</dd> <dt>

<span data-ttu-id="26d86-112">*CB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26d86-112">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26d86-113">Entier qui spécifie la longueur de la plage, en octets, à limiter.</span><span class="sxs-lookup"><span data-stu-id="26d86-113">Integer that specifies the length of the range, in bytes, to be restricted.</span></span>

</dd> <dt>

<span data-ttu-id="26d86-114">*dwLockType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26d86-114">*dwLockType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26d86-115">Spécifie les restrictions requises pour accéder à la plage.</span><span class="sxs-lookup"><span data-stu-id="26d86-115">Specifies the restrictions being requested on accessing the range.</span></span> <span data-ttu-id="26d86-116">Il peut s’agir de l’une des valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="26d86-116">This can be one of the values in the following table.</span></span>



| <span data-ttu-id="26d86-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="26d86-117">Value</span></span>                                                                                                                                                            | <span data-ttu-id="26d86-118">Signification</span><span class="sxs-lookup"><span data-stu-id="26d86-118">Meaning</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOCK_WRITE"></span><span id="lock_write"></span><dl> <span data-ttu-id="26d86-119"><dt>**écriture de verrou \_**</dt></span><span class="sxs-lookup"><span data-stu-id="26d86-119"><dt>**LOCK\_WRITE**</dt></span></span> </dl>             | <span data-ttu-id="26d86-120">La plage d’octets spécifiée peut être ouverte et lue un nombre quelconque de fois, mais l’écriture dans la plage verrouillée est interdite, à l’exception du propriétaire qui a obtenu ce verrou.</span><span class="sxs-lookup"><span data-stu-id="26d86-120">The specified range of bytes can be opened and read any number of times, but writing to the locked range is prohibited except for the owner that was granted this lock.</span></span><br/>                                                                      |
| <span id="LOCK_EXCLUSIVE"></span><span id="lock_exclusive"></span><dl> <span data-ttu-id="26d86-121"><dt>**VERROU \_ exclusif**</dt></span><span class="sxs-lookup"><span data-stu-id="26d86-121"><dt>**LOCK\_EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="26d86-122">L’écriture dans la plage d’octets spécifiée est interdite, à l’exception du propriétaire auquel ce verrou a été accordé.</span><span class="sxs-lookup"><span data-stu-id="26d86-122">Writing to the specified range of bytes is prohibited except for the owner that was granted this lock.</span></span><br/>                                                                                                                                       |
| <span id="LOCK_ONLYONCE"></span><span id="lock_onlyonce"></span><dl> <span data-ttu-id="26d86-123"><dt>**VERROUILLER \_ ONLYONCE**</dt></span><span class="sxs-lookup"><span data-stu-id="26d86-123"><dt>**LOCK\_ONLYONCE**</dt></span></span> </dl>    | <span data-ttu-id="26d86-124">Si ce verrou est accordé, aucun autre verrou \_ ONLYONCE de verrou ne peut être obtenu sur la plage.</span><span class="sxs-lookup"><span data-stu-id="26d86-124">If this lock is granted, no other LOCK\_ONLYONCE lock can be obtained on the range.</span></span> <span data-ttu-id="26d86-125">En général, ce type de verrou est un alias pour un autre type de verrou.</span><span class="sxs-lookup"><span data-stu-id="26d86-125">Usually this lock type is an alias for some other lock type.</span></span> <span data-ttu-id="26d86-126">Ainsi, les implémentations spécifiques peuvent avoir un comportement supplémentaire associé à ce type de verrou.</span><span class="sxs-lookup"><span data-stu-id="26d86-126">Thus, specific implementations can have additional behavior associated with this lock type.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26d86-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="26d86-127">Return value</span></span>

<span data-ttu-id="26d86-128">La valeur de retour est un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="26d86-128">The return value is an **HRESULT**.</span></span> <span data-ttu-id="26d86-129">La valeur S \_ OK indique que l’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="26d86-129">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="26d86-130">Notes</span><span class="sxs-lookup"><span data-stu-id="26d86-130">Remarks</span></span>

<span data-ttu-id="26d86-131">La plage d’octets peut s’étendre au-delà de la fin actuelle du flux.</span><span class="sxs-lookup"><span data-stu-id="26d86-131">The byte range can extend past the current end of the stream.</span></span> <span data-ttu-id="26d86-132">Le verrouillage au-delà de la fin d’un flux est utile comme méthode de communication entre les différentes instances du flux sans modifier les données qui font réellement partie du flux.</span><span class="sxs-lookup"><span data-stu-id="26d86-132">Locking beyond the end of a stream is useful as a method of communication between different instances of the stream without changing data that is actually part of the stream.</span></span>

<span data-ttu-id="26d86-133">Trois types de verrouillage peuvent être pris en charge : le verrouillage pour exclure d’autres enregistreurs, le verrouillage pour exclure d’autres lecteurs ou Writers et le verrouillage qui permet à un seul demandeur d’obtenir un verrou sur la plage donnée, qui est généralement un alias pour l’un des deux autres types de verrous.</span><span class="sxs-lookup"><span data-stu-id="26d86-133">Three types of locking can be supported: locking to exclude other writers, locking to exclude other readers or writers, and locking that allows only one requester to obtain a lock on the given range, which is usually an alias for one of the other two lock types.</span></span> <span data-ttu-id="26d86-134">Une instance de flux donnée peut prendre en charge l’un des deux premiers types, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="26d86-134">A given stream instance might support either of the first two types, or both.</span></span> <span data-ttu-id="26d86-135">Le type de verrou est spécifié par *dwLockType*, à l’aide d’une valeur issue de l’énumération [**LockType**](/windows/win32/api/objidl/ne-objidl-locktype) .</span><span class="sxs-lookup"><span data-stu-id="26d86-135">The lock type is specified by *dwLockType*, using a value from the [**LOCKTYPE**](/windows/win32/api/objidl/ne-objidl-locktype) enumeration.</span></span>

<span data-ttu-id="26d86-136">Toute région verrouillée avec la fonction **LockRegion** doit ensuite être déverrouillée explicitement en appelant [**IByteBuffer :: UnlockRegion**](ibytebuffer-unlockregion.md) avec exactement les mêmes valeurs pour les paramètres *liboffset*, *CB* et *dwLockType* .</span><span class="sxs-lookup"><span data-stu-id="26d86-136">Any region locked with **LockRegion** must later be explicitly unlocked by calling [**IByteBuffer::UnlockRegion**](ibytebuffer-unlockregion.md) with exactly the same values for the *libOffset*, *cb*, and *dwLockType* parameters.</span></span> <span data-ttu-id="26d86-137">La région doit être déverrouillée avant la libération du flux.</span><span class="sxs-lookup"><span data-stu-id="26d86-137">The region must be unlocked before the stream is released.</span></span> <span data-ttu-id="26d86-138">Deux régions adjacentes ne peuvent pas être verrouillées séparément, puis déverrouillées à l’aide d’un seul appel de déverrouillage.</span><span class="sxs-lookup"><span data-stu-id="26d86-138">Two adjacent regions cannot be locked separately and then unlocked with a single unlock call.</span></span>

## <a name="examples"></a><span data-ttu-id="26d86-139">Exemples</span><span class="sxs-lookup"><span data-stu-id="26d86-139">Examples</span></span>

<span data-ttu-id="26d86-140">L’exemple suivant illustre la restriction de l’accès à une plage d’octets.</span><span class="sxs-lookup"><span data-stu-id="26d86-140">The following example shows restricting access to a range of bytes.</span></span>


```C++
HRESULT  hr;

// Lock a region.
hr = pIByteBuff->LockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::LockRegion\n");
```



## <a name="requirements"></a><span data-ttu-id="26d86-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26d86-141">Requirements</span></span>



| <span data-ttu-id="26d86-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26d86-142">Requirement</span></span> | <span data-ttu-id="26d86-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="26d86-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26d86-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26d86-144">Minimum supported client</span></span><br/> | <span data-ttu-id="26d86-145">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26d86-145">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="26d86-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26d86-146">Minimum supported server</span></span><br/> | <span data-ttu-id="26d86-147">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26d86-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="26d86-148">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="26d86-148">End of client support</span></span><br/>    | <span data-ttu-id="26d86-149">Windows XP</span><span class="sxs-lookup"><span data-stu-id="26d86-149">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="26d86-150">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="26d86-150">End of server support</span></span><br/>    | <span data-ttu-id="26d86-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="26d86-151">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="26d86-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="26d86-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="26d86-153"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="26d86-153"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="26d86-154">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="26d86-154">Type library</span></span><br/>             | <dl> <span data-ttu-id="26d86-155"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="26d86-155"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="26d86-156">DLL</span><span class="sxs-lookup"><span data-stu-id="26d86-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26d86-157"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26d86-157"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="26d86-158">IID</span><span class="sxs-lookup"><span data-stu-id="26d86-158">IID</span></span><br/>                      | <span data-ttu-id="26d86-159">IID \_ IByteBuffer est défini en tant que E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="26d86-159">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

