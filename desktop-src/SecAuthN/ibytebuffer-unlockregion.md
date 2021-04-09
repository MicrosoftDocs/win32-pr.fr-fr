---
description: 'Supprime les restrictions d’accès sur une plage d’octets précédemment restreinte à l’aide de IByteBuffer :: LockRegion.'
ms.assetid: f2a1162e-7fc7-4a55-befb-0b017edb9fe2
title: 'IByteBuffer :: UnlockRegion, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.UnlockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 92e49ba000177326ad14d3b83002613a15e96e18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952791"
---
# <a name="ibytebufferunlockregion-method"></a><span data-ttu-id="3778e-103">IByteBuffer :: UnlockRegion, méthode</span><span class="sxs-lookup"><span data-stu-id="3778e-103">IByteBuffer::UnlockRegion method</span></span>

<span data-ttu-id="3778e-104">\[La méthode **UnlockRegion** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="3778e-104">\[The **UnlockRegion** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3778e-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3778e-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3778e-106">L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="3778e-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="3778e-107">La méthode **UnlockRegion** supprime la restriction d’accès sur une plage d’octets précédemment restreinte à l’aide de [**IByteBuffer :: LockRegion**](ibytebuffer-lockregion.md).</span><span class="sxs-lookup"><span data-stu-id="3778e-107">The **UnlockRegion** method removes the access restriction on a range of bytes previously restricted by using [**IByteBuffer::LockRegion**](ibytebuffer-lockregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3778e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3778e-108">Syntax</span></span>


```C++
HRESULT UnlockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a><span data-ttu-id="3778e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3778e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3778e-110">*Liboffset* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3778e-110">*libOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3778e-111">Offset d’octet pour le début de la plage.</span><span class="sxs-lookup"><span data-stu-id="3778e-111">Byte offset for the beginning of the range.</span></span>

</dd> <dt>

<span data-ttu-id="3778e-112">*CB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3778e-112">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3778e-113">Longueur, en octets, de la plage à limiter.</span><span class="sxs-lookup"><span data-stu-id="3778e-113">Length, in bytes, of the range to be restricted.</span></span>

</dd> <dt>

<span data-ttu-id="3778e-114">*dwLockType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3778e-114">*dwLockType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3778e-115">Restrictions d’accès précédemment placées dans la plage.</span><span class="sxs-lookup"><span data-stu-id="3778e-115">Access restrictions previously placed on the range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3778e-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3778e-116">Return value</span></span>

<span data-ttu-id="3778e-117">La valeur de retour est un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3778e-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="3778e-118">La valeur S \_ OK indique que l’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="3778e-118">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="3778e-119">Notes</span><span class="sxs-lookup"><span data-stu-id="3778e-119">Remarks</span></span>

<span data-ttu-id="3778e-120">La méthode **IByteBuffer :: UnlockRegion** déverrouille une région précédemment verrouillée à l’aide de la méthode [**IByteBuffer :: LockRegion**](ibytebuffer-lockregion.md) .</span><span class="sxs-lookup"><span data-stu-id="3778e-120">The **IByteBuffer::UnlockRegion** method unlocks a region previously locked by using the [**IByteBuffer::LockRegion**](ibytebuffer-lockregion.md) method.</span></span> <span data-ttu-id="3778e-121">Les régions verrouillées doivent être déverrouillées par la suite en appelant **IByteBuffer :: UnlockRegion** avec exactement les mêmes valeurs pour les paramètres *liboffset*, *CB* et *dwLockType* .</span><span class="sxs-lookup"><span data-stu-id="3778e-121">Locked regions must later be explicitly unlocked by calling **IByteBuffer::UnlockRegion** with exactly the same values for the *libOffset*, *cb*, and *dwLockType* parameters.</span></span> <span data-ttu-id="3778e-122">La région doit être déverrouillée avant la libération du flux.</span><span class="sxs-lookup"><span data-stu-id="3778e-122">The region must be unlocked before the stream is released.</span></span> <span data-ttu-id="3778e-123">Deux régions adjacentes ne peuvent pas être verrouillées séparément, puis déverrouillées à l’aide d’un seul appel de déverrouillage.</span><span class="sxs-lookup"><span data-stu-id="3778e-123">Two adjacent regions cannot be locked separately and then unlocked with a single unlock call.</span></span>

## <a name="examples"></a><span data-ttu-id="3778e-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="3778e-124">Examples</span></span>

<span data-ttu-id="3778e-125">L’exemple suivant illustre le déverrouillage d’une plage d’octets.</span><span class="sxs-lookup"><span data-stu-id="3778e-125">The following example shows unlocking a range of bytes.</span></span>


```C++
HRESULT  hr;

// Unlock a region.
hr = pIByteBuff->UnlockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::UnlockRegion\n");
```



## <a name="requirements"></a><span data-ttu-id="3778e-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3778e-126">Requirements</span></span>



| <span data-ttu-id="3778e-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3778e-127">Requirement</span></span> | <span data-ttu-id="3778e-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="3778e-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3778e-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3778e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3778e-130">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3778e-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3778e-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3778e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3778e-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3778e-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3778e-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="3778e-133">End of client support</span></span><br/>    | <span data-ttu-id="3778e-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3778e-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="3778e-135">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="3778e-135">End of server support</span></span><br/>    | <span data-ttu-id="3778e-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3778e-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="3778e-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="3778e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="3778e-138"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3778e-138"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3778e-139">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="3778e-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="3778e-140"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3778e-140"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3778e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="3778e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3778e-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3778e-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3778e-143">IID</span><span class="sxs-lookup"><span data-stu-id="3778e-143">IID</span></span><br/>                      | <span data-ttu-id="3778e-144">IID \_ IByteBuffer est défini en tant que E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="3778e-144">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

