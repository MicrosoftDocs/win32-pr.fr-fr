---
title: sh_process, mot clé
description: Le \_ mot clé \ SH process \ spécifie que l’objet système est un handle d’un processus.
keywords:
- sh_process mot clé MIDL
topic_type:
- apiref
api_name:
- sh_process
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 3652c6889c687173bbf7b397cddff4659c0329f1
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "106545190"
---
# <a name="sh_process-keyword"></a><span data-ttu-id="dbd39-104">SH \_ Process (mot clé)</span><span class="sxs-lookup"><span data-stu-id="dbd39-104">sh\_process keyword</span></span>

<span data-ttu-id="dbd39-105">Le mot clé de **\_ processus SH** spécifie qu’un `system_handle` contient un descripteur d’un processus.</span><span class="sxs-lookup"><span data-stu-id="dbd39-105">The **sh\_process** keyword specifies that a `system_handle` holds a handle to a process.</span></span>

``` syntax
[system_handle(sh_process)]

[system_handle(sh_process, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="dbd39-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dbd39-106">Parameters</span></span>

<span data-ttu-id="dbd39-107">Ce mot clé est un paramètre pour [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="dbd39-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="dbd39-108">La documentation [**system_handle**](system-handle.md) contient également des informations sur l’utilisation facultative du paramètre *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="dbd39-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="dbd39-109">Le comportement par défaut est défini `DUPLICATE_SAME_ACCESS` par les spécifications de [fonction **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="dbd39-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbd39-110">Notes</span><span class="sxs-lookup"><span data-stu-id="dbd39-110">Remarks</span></span>

<span data-ttu-id="dbd39-111">Pour pouvoir utiliser ce mot clé avec l' `system_handle` attribut, l' `-target` indicateur doit avoir la valeur `NT100` (ou une version ultérieure) lors de l’exécution de midl.exe.</span><span class="sxs-lookup"><span data-stu-id="dbd39-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="dbd39-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="dbd39-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GetStubProcess([out, system_handle(sh_process)] HANDLE* processHandle);

    HRESULT WatchProcess([in, system_handle(sh_process, PROCESS_QUERY_INFORMATION | PROCESS_QUERY_LIMITED_INFORMATION)] HANDLE processHandle);
}
```

## <a name="requirements"></a><span data-ttu-id="dbd39-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dbd39-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="dbd39-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbd39-114">Minimum supported client</span></span> | <span data-ttu-id="dbd39-115">Mise à jour anniversaire Windows 10 (version 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="dbd39-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="dbd39-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbd39-116">Minimum supported server</span></span> | <span data-ttu-id="dbd39-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="dbd39-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="dbd39-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbd39-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbd39-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="dbd39-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="dbd39-120">À propos des processus et des threads</span><span class="sxs-lookup"><span data-stu-id="dbd39-120">About Processes and Threads</span></span>](../procthread/about-processes-and-threads.md)
</dt> <dt>

[<span data-ttu-id="dbd39-121">Sécurité des processus et droits d’accès</span><span class="sxs-lookup"><span data-stu-id="dbd39-121">Process Security and Access Rights</span></span>](../procthread/process-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="dbd39-122">Fonction **CreateProcess**</span><span class="sxs-lookup"><span data-stu-id="dbd39-122">**CreateProcess** function</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)
</dt> <dt>

[<span data-ttu-id="dbd39-123">**OpenProcess** , fonction</span><span class="sxs-lookup"><span data-stu-id="dbd39-123">**OpenProcess** function</span></span>](/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)
</dt> </dl>