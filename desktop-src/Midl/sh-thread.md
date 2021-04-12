---
title: sh_thread, mot clé
description: Le \_ mot clé \ SH thread \ spécifie que l’objet système est un handle d’un thread.
keywords:
- sh_thread mot clé MIDL
topic_type:
- apiref
api_name:
- sh_thread keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 2c82dc41d2b1c7cba740c897ef6cea9094979cc3
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104211171"
---
# <a name="sh_thread-keyword"></a><span data-ttu-id="86abf-104">SH \_ (mot clé)</span><span class="sxs-lookup"><span data-stu-id="86abf-104">sh\_thread keyword</span></span>

<span data-ttu-id="86abf-105">Le mot clé de **\_ thread SH** spécifie qu’un `system_handle` contient un descripteur d’un thread.</span><span class="sxs-lookup"><span data-stu-id="86abf-105">The **sh\_thread** keyword specifies that a `system_handle` holds a handle to a thread.</span></span>

``` syntax
[system_handle(sh_thread)]

[system_handle(sh_thread, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="86abf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86abf-106">Parameters</span></span>

<span data-ttu-id="86abf-107">Ce mot clé est un paramètre pour [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="86abf-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="86abf-108">La documentation [**system_handle**](system-handle.md) contient également des informations sur l’utilisation facultative du paramètre *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="86abf-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="86abf-109">Le comportement par défaut est défini `DUPLICATE_SAME_ACCESS` par les spécifications de [fonction **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="86abf-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="86abf-110">Notes</span><span class="sxs-lookup"><span data-stu-id="86abf-110">Remarks</span></span>

<span data-ttu-id="86abf-111">Pour pouvoir utiliser ce mot clé avec l' `system_handle` attribut, l' `-target` indicateur doit avoir la valeur `NT100` (ou une version ultérieure) lors de l’exécution de midl.exe.</span><span class="sxs-lookup"><span data-stu-id="86abf-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="86abf-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="86abf-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT SetThread([in, system_handle(sh_process)] HANDLE threadHandle);
}
```

## <a name="requirements"></a><span data-ttu-id="86abf-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86abf-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="86abf-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86abf-114">Minimum supported client</span></span> | <span data-ttu-id="86abf-115">Mise à jour anniversaire Windows 10 (version 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="86abf-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="86abf-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86abf-116">Minimum supported server</span></span> | <span data-ttu-id="86abf-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="86abf-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="86abf-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86abf-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86abf-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="86abf-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="86abf-120">À propos des processus et des threads</span><span class="sxs-lookup"><span data-stu-id="86abf-120">About Processes and Threads</span></span>](../procthread/about-processes-and-threads.md)
</dt> <dt>

[<span data-ttu-id="86abf-121">Sécurité des threads et droits d’accès</span><span class="sxs-lookup"><span data-stu-id="86abf-121">Thread Security and Access Rights</span></span>](../procthread/thread-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="86abf-122">**CreateThread** , fonction</span><span class="sxs-lookup"><span data-stu-id="86abf-122">**CreateThread** function</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)
</dt> <dt>

[<span data-ttu-id="86abf-123">**OpenThread** fonction)</span><span class="sxs-lookup"><span data-stu-id="86abf-123">**OpenThread** function</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread)
</dt> </dl>