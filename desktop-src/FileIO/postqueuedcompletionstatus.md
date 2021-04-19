---
description: Publie un paquet de terminaison d’e/s sur un port de terminaison d’e/s.
ms.assetid: 69a9b1e5-2d40-42de-a14a-f7b6f29bf571
title: PostQueuedCompletionStatus, fonction (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostQueuedCompletionStatus
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: f12de10032df7fec32dd9a577353dd20c0f4eaa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528282"
---
# <a name="postqueuedcompletionstatus-function"></a><span data-ttu-id="3d027-103">PostQueuedCompletionStatus fonction)</span><span class="sxs-lookup"><span data-stu-id="3d027-103">PostQueuedCompletionStatus function</span></span>

<span data-ttu-id="3d027-104">Publie un paquet de terminaison d’e/s sur un port de terminaison d’e/s.</span><span class="sxs-lookup"><span data-stu-id="3d027-104">Posts an I/O completion packet to an I/O completion port.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d027-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d027-105">Syntax</span></span>


```C++
BOOL WINAPI PostQueuedCompletionStatus(
  _In_     HANDLE       CompletionPort,
  _In_     DWORD        dwNumberOfBytesTransferred,
  _In_     ULONG_PTR    dwCompletionKey,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a><span data-ttu-id="3d027-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3d027-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d027-107">*CompletionPort* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3d027-107">*CompletionPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d027-108">Handle vers un port de terminaison d’e/s sur lequel le paquet d’achèvement d’e/s doit être publié.</span><span class="sxs-lookup"><span data-stu-id="3d027-108">A handle to an I/O completion port to which the I/O completion packet is to be posted.</span></span>

</dd> <dt>

<span data-ttu-id="3d027-109">*dwNumberOfBytesTransferred* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3d027-109">*dwNumberOfBytesTransferred* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d027-110">Valeur à retourner via le paramètre *lpNumberOfBytesTransferred* de la fonction [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="3d027-110">The value to be returned through the *lpNumberOfBytesTransferred* parameter of the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="3d027-111">*dwCompletionKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3d027-111">*dwCompletionKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d027-112">Valeur à retourner via le paramètre *lpCompletionKey* de la fonction [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="3d027-112">The value to be returned through the *lpCompletionKey* parameter of the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="3d027-113">*lpOverlapped* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="3d027-113">*lpOverlapped* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3d027-114">Valeur à retourner via le paramètre *lpOverlapped* de la fonction [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="3d027-114">The value to be returned through the *lpOverlapped* parameter of the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d027-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3d027-115">Return value</span></span>

<span data-ttu-id="3d027-116">Si la fonction réussit, la valeur de retour est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="3d027-116">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="3d027-117">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="3d027-117">If the function fails, the return value is zero.</span></span> <span data-ttu-id="3d027-118">Pour afficher les informations d’erreur étendues, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="3d027-118">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span></span>

## <a name="remarks"></a><span data-ttu-id="3d027-119">Notes</span><span class="sxs-lookup"><span data-stu-id="3d027-119">Remarks</span></span>

<span data-ttu-id="3d027-120">Le paquet d’achèvement d’e/s répondra à un appel en suspens de la fonction [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="3d027-120">The I/O completion packet will satisfy an outstanding call to the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span> <span data-ttu-id="3d027-121">Cette fonction retourne avec les trois valeurs passées comme deuxième, troisième et quatrième paramètres de l’appel à **PostQueuedCompletionStatus**.</span><span class="sxs-lookup"><span data-stu-id="3d027-121">This function returns with the three values passed as the second, third, and fourth parameters of the call to **PostQueuedCompletionStatus**.</span></span> <span data-ttu-id="3d027-122">Le système n’utilise pas ou ne valide pas ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="3d027-122">The system does not use or validate these values.</span></span> <span data-ttu-id="3d027-123">En particulier, le paramètre *lpOverlapped* n’a pas besoin de pointer vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="3d027-123">In particular, the *lpOverlapped* parameter need not point to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="3d027-124">Dans Windows 8 et Windows Server 2012, cette fonction est prise en charge par les technologies suivantes.</span><span class="sxs-lookup"><span data-stu-id="3d027-124">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="3d027-125">Technology</span><span class="sxs-lookup"><span data-stu-id="3d027-125">Technology</span></span>                                           | <span data-ttu-id="3d027-126">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d027-126">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="3d027-127">Protocole SMB (Server Message Block) 3,0</span><span class="sxs-lookup"><span data-stu-id="3d027-127">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="3d027-128">Oui</span><span class="sxs-lookup"><span data-stu-id="3d027-128">Yes</span></span><br/> |
| <span data-ttu-id="3d027-129">Basculement transparent SMB 3,0 (TFO)</span><span class="sxs-lookup"><span data-stu-id="3d027-129">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="3d027-130">Oui</span><span class="sxs-lookup"><span data-stu-id="3d027-130">Yes</span></span><br/> |
| <span data-ttu-id="3d027-131">SMB 3,0 avec des partages de fichiers avec montée en puissance parallèle (SO)</span><span class="sxs-lookup"><span data-stu-id="3d027-131">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="3d027-132">Oui</span><span class="sxs-lookup"><span data-stu-id="3d027-132">Yes</span></span><br/> |
| <span data-ttu-id="3d027-133">Système de fichiers Volume partagé de cluster (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="3d027-133">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="3d027-134">Oui</span><span class="sxs-lookup"><span data-stu-id="3d027-134">Yes</span></span><br/> |
| <span data-ttu-id="3d027-135">Système de fichiers résilient (ReFS)</span><span class="sxs-lookup"><span data-stu-id="3d027-135">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="3d027-136">Oui</span><span class="sxs-lookup"><span data-stu-id="3d027-136">Yes</span></span><br/> |



 

<span data-ttu-id="3d027-137">CsvFs effectue une redirection des e/s pour les fichiers compressés.</span><span class="sxs-lookup"><span data-stu-id="3d027-137">CsvFs will do redirected IO for compressed files.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d027-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d027-138">Requirements</span></span>



| <span data-ttu-id="3d027-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d027-139">Requirement</span></span> | <span data-ttu-id="3d027-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d027-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d027-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d027-141">Minimum supported client</span></span><br/> | <span data-ttu-id="3d027-142">Applications de bureau Windows XP- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="3d027-142">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="3d027-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d027-143">Minimum supported server</span></span><br/> | <span data-ttu-id="3d027-144">Applications de bureau Windows Server 2003 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="3d027-144">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="3d027-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="3d027-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d027-146"><dt>IoAPI. h (inclure Windows. h); </dt> <dt>WinBase. h sur Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP (incluant Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d027-146"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3d027-147">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3d027-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="3d027-148"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d027-148"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                  |
| <span data-ttu-id="3d027-149">DLL</span><span class="sxs-lookup"><span data-stu-id="3d027-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d027-150"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d027-150"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a><span data-ttu-id="3d027-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d027-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d027-152">**CreateIoCompletionPort**</span><span class="sxs-lookup"><span data-stu-id="3d027-152">**CreateIoCompletionPort**</span></span>](createiocompletionport.md)
</dt> <dt>

[<span data-ttu-id="3d027-153">Fonctions de gestion de fichiers</span><span class="sxs-lookup"><span data-stu-id="3d027-153">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="3d027-154">**GetQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="3d027-154">**GetQueuedCompletionStatus**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[<span data-ttu-id="3d027-155">**AVEC chevauchement**</span><span class="sxs-lookup"><span data-stu-id="3d027-155">**OVERLAPPED**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)
</dt> </dl>

 

