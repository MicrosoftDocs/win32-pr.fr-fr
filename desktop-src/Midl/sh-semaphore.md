---
title: sh_semaphore, mot clé
description: Le \_ mot clé \ SH Semaphore \ spécifie que l’objet système est un descripteur d’un sémaphore.
keywords:
- sh_semaphore mot clé MIDL
topic_type:
- apiref
api_name:
- sh_semaphore
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 2a5c33e4c44b67e3106a48cde244abaf13f41ad5
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "106545189"
---
# <a name="sh_semaphore-keyword"></a><span data-ttu-id="de9e1-104">SH \_ (mot clé)</span><span class="sxs-lookup"><span data-stu-id="de9e1-104">sh\_semaphore keyword</span></span>

<span data-ttu-id="de9e1-105">Le mot clé de **\_ sémaphore SH** spécifie qu’un `system_handle` contient un descripteur d’un sémaphore.</span><span class="sxs-lookup"><span data-stu-id="de9e1-105">The **sh\_semaphore** keyword specifies that a `system_handle` holds a handle to a semaphore.</span></span>

``` syntax
[system_handle(sh_semaphore)]

[system_handle(sh_semaphore, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="de9e1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de9e1-106">Parameters</span></span>

<span data-ttu-id="de9e1-107">Ce mot clé est un paramètre pour [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="de9e1-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="de9e1-108">La documentation [**system_handle**](system-handle.md) contient également des informations sur l’utilisation facultative du paramètre *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="de9e1-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="de9e1-109">Le comportement par défaut est défini `DUPLICATE_SAME_ACCESS` par les spécifications de [fonction **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="de9e1-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="de9e1-110">Notes</span><span class="sxs-lookup"><span data-stu-id="de9e1-110">Remarks</span></span>

<span data-ttu-id="de9e1-111">Pour pouvoir utiliser ce mot clé avec l' `system_handle` attribut, l' `-target` indicateur doit avoir la valeur `NT100` (ou une version ultérieure) lors de l’exécution de midl.exe.</span><span class="sxs-lookup"><span data-stu-id="de9e1-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="de9e1-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="de9e1-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT SignalThisSemaphore([in, system_handle(sh_semaphore)] HANDLE semaphore);
}
```

## <a name="requirements"></a><span data-ttu-id="de9e1-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de9e1-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="de9e1-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de9e1-114">Minimum supported client</span></span> | <span data-ttu-id="de9e1-115">Mise à jour anniversaire Windows 10 (version 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="de9e1-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="de9e1-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de9e1-116">Minimum supported server</span></span> | <span data-ttu-id="de9e1-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="de9e1-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="de9e1-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de9e1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de9e1-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="de9e1-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="de9e1-120">Objets Semaphore</span><span class="sxs-lookup"><span data-stu-id="de9e1-120">Semaphore Objects</span></span>](../sync/semaphore-objects.md)
</dt> <dt>

[<span data-ttu-id="de9e1-121">Sécurité de l’objet de synchronisation et droits d’accès</span><span class="sxs-lookup"><span data-stu-id="de9e1-121">Synchronization Object Security and Access Rights</span></span>](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="de9e1-122">**CreateSemaphore,** fonction)</span><span class="sxs-lookup"><span data-stu-id="de9e1-122">**CreateSemaphore** function</span></span>](/windows/win32/api/winbase/nf-winbase-createsemaphorea)
</dt> <dt>

[<span data-ttu-id="de9e1-123">**CreateSemaphoreEx** fonction)</span><span class="sxs-lookup"><span data-stu-id="de9e1-123">**CreateSemaphoreEx** function</span></span>](/windows/win32/api/winbase/nf-winbase-createsemaphoreexa)
</dt> </dl>
