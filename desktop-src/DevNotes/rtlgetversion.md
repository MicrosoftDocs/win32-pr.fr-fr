---
description: Obtient des informations de version sur le système d’exploitation en cours d’exécution.
ms.assetid: F04F0981-A07D-4B38-9DE4-B8461EAFC19F
title: RtlGetVersion, fonction (Ntddk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetVersion
api_type:
- DllExport
api_location:
- Ntdll.dll
- NtosKrnl.exe
ms.openlocfilehash: a6a026ee55a6ccd75162915729070ad76f621bc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110438"
---
# <a name="rtlgetversion-function"></a><span data-ttu-id="ba5b9-103">RtlGetVersion fonction)</span><span class="sxs-lookup"><span data-stu-id="ba5b9-103">RtlGetVersion function</span></span>

<span data-ttu-id="ba5b9-104">Obtient des informations de version sur le système d’exploitation en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ba5b9-104">Gets version information about the currently running operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba5b9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba5b9-105">Syntax</span></span>


```C++
NTSTATUS RtlGetVersion(
  _Out_ PRTL_OSVERSIONINFOW lpVersionInformation
);
```



## <a name="parameters"></a><span data-ttu-id="ba5b9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba5b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba5b9-107">*lpVersionInformation* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ba5b9-107">*lpVersionInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba5b9-108">Pointeur vers une structure [**\_ OSVERSIONINFOW RTL**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfow) ou une structure [**\_ OSVERSIONINFOEXW RTL**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfoexw) qui contient les informations de version relatives au système d’exploitation en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ba5b9-108">Pointer to either a [**RTL\_OSVERSIONINFOW**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfow) structure or a [**RTL\_OSVERSIONINFOEXW**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfoexw) structure that contains the version information about the currently running operating system.</span></span> <span data-ttu-id="ba5b9-109">Un appelant spécifie la structure d’entrée utilisée en affectant à la taille du membre **dwOSVersionInfoSize** de la structure la taille en octets de la structure utilisée.</span><span class="sxs-lookup"><span data-stu-id="ba5b9-109">A caller specifies which input structure is used by setting the **dwOSVersionInfoSize** member of the structure to the size in bytes of the structure that is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba5b9-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ba5b9-110">Return value</span></span>

<span data-ttu-id="ba5b9-111">Retourne l’état \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="ba5b9-111">Returns STATUS\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba5b9-112">Notes</span><span class="sxs-lookup"><span data-stu-id="ba5b9-112">Remarks</span></span>

<span data-ttu-id="ba5b9-113">**RtlGetVersion** est l’équivalent de la fonction [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="ba5b9-113">**RtlGetVersion** is the equivalent of the [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) function in the Windows SDK.</span></span> <span data-ttu-id="ba5b9-114">Consultez l’exemple dans le SDK Windows qui montre comment obtenir la version du système.</span><span class="sxs-lookup"><span data-stu-id="ba5b9-114">See the example in the Windows SDK that shows how to get the system version.</span></span>

<span data-ttu-id="ba5b9-115">Quand vous utilisez **RtlGetVersion** pour déterminer si une version particulière du système d’exploitation est en cours d’exécution, un appelant doit vérifier les numéros de version qui sont supérieurs ou égaux au numéro de version requis.</span><span class="sxs-lookup"><span data-stu-id="ba5b9-115">When using **RtlGetVersion** to determine whether a particular version of the operating system is running, a caller should check for version numbers that are greater than or equal to the required version number.</span></span> <span data-ttu-id="ba5b9-116">Cela garantit qu’un test de version est correctement effectué pour les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="ba5b9-116">This ensures that a version test succeeds for later versions of Windows.</span></span>

<span data-ttu-id="ba5b9-117">Étant donné que les fonctionnalités du système d’exploitation peuvent être ajoutées à une DLL redistribuable, la vérification des numéros de version majeure et mineure n’est pas la méthode la plus fiable pour vérifier la présence d’une fonctionnalité système spécifique.</span><span class="sxs-lookup"><span data-stu-id="ba5b9-117">Because operating system features can be added in a redistributable DLL, checking only the major and minor version numbers is not the most reliable way to verify the presence of a specific system feature.</span></span> <span data-ttu-id="ba5b9-118">Un pilote doit utiliser [**RtlVerifyVersionInfo**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlverifyversioninfo) pour tester la présence d’une fonctionnalité système spécifique.</span><span class="sxs-lookup"><span data-stu-id="ba5b9-118">A driver should use [**RtlVerifyVersionInfo**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlverifyversioninfo) to test for the presence of a specific system feature.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba5b9-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba5b9-119">Requirements</span></span>



| <span data-ttu-id="ba5b9-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba5b9-120">Requirement</span></span> | <span data-ttu-id="ba5b9-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba5b9-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba5b9-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba5b9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ba5b9-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba5b9-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="ba5b9-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba5b9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ba5b9-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba5b9-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="ba5b9-126">Plateforme cible</span><span class="sxs-lookup"><span data-stu-id="ba5b9-126">Target platform</span></span><br/>          | <dl> <span data-ttu-id="ba5b9-127"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="ba5b9-127"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl>                  |
| <span data-ttu-id="ba5b9-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="ba5b9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba5b9-129"><dt>Ntddk. h (inclure Ntddk. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba5b9-129"><dt>Ntddk.h (include Ntddk.h)</dt></span></span> </dl>                                                     |
| <span data-ttu-id="ba5b9-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ba5b9-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="ba5b9-131"><dt>Ntdll. lib ; </dt> <dt>NtosKrnl. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba5b9-131"><dt>Ntdll.lib; </dt> <dt>NtosKrnl.lib</dt></span></span> </dl> |
| <span data-ttu-id="ba5b9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ba5b9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba5b9-133"><dt>Ntdll.dll ; </dt> <dt>NtosKrnl.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ba5b9-133"><dt>Ntdll.dll; </dt> <dt>NtosKrnl.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba5b9-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba5b9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba5b9-135">**PsGetVersion**</span><span class="sxs-lookup"><span data-stu-id="ba5b9-135">**PsGetVersion**</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-psgetversion)
</dt> </dl>

 

 
