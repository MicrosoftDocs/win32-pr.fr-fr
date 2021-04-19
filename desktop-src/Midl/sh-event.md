---
title: sh_event, mot clé
description: Le \_ mot clé \ SH Event \ spécifie que l’objet système est un handle d’événement.
keywords:
- sh_event mot clé MIDL
topic_type:
- apiref
api_name:
- sh_event
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 1a9b6dc7cc9dc4de4abd5dcc88a53588167db59d
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "106543756"
---
# <a name="sh_event-keyword"></a><span data-ttu-id="b2e8b-104">SH \_ (mot clé)</span><span class="sxs-lookup"><span data-stu-id="b2e8b-104">sh\_event keyword</span></span>

<span data-ttu-id="b2e8b-105">Le mot clé **\_ Event SH** spécifie qu’un `system_handle` contient un descripteur d’événement.</span><span class="sxs-lookup"><span data-stu-id="b2e8b-105">The **sh\_event** keyword specifies that a `system_handle` holds a handle to an event.</span></span>

``` syntax
[system_handle(sh_event)]

[system_handle(sh_event, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="b2e8b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2e8b-106">Parameters</span></span>

<span data-ttu-id="b2e8b-107">Ce mot clé est un paramètre pour [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="b2e8b-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="b2e8b-108">La documentation [**system_handle**](system-handle.md) contient également des informations sur l’utilisation facultative du paramètre *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="b2e8b-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="b2e8b-109">Le comportement par défaut est défini `DUPLICATE_SAME_ACCESS` par les spécifications de [fonction **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="b2e8b-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2e8b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b2e8b-110">Remarks</span></span>

<span data-ttu-id="b2e8b-111">Pour pouvoir utiliser ce mot clé avec l' `system_handle` attribut, l' `-target` indicateur doit avoir la valeur `NT100` (ou une version ultérieure) lors de l’exécution de midl.exe.</span><span class="sxs-lookup"><span data-stu-id="b2e8b-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="b2e8b-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="b2e8b-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT NotifyThisEvent([in, system_handle(sh_event)] HANDLE listeningToThisEvent);
}
```

## <a name="requirements"></a><span data-ttu-id="b2e8b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2e8b-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="b2e8b-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2e8b-114">Minimum supported client</span></span> | <span data-ttu-id="b2e8b-115">Mise à jour anniversaire Windows 10 (version 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="b2e8b-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="b2e8b-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2e8b-116">Minimum supported server</span></span> | <span data-ttu-id="b2e8b-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="b2e8b-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="b2e8b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2e8b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2e8b-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="b2e8b-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="b2e8b-120">Objets d’événement</span><span class="sxs-lookup"><span data-stu-id="b2e8b-120">Event Objects</span></span>](../sync/event-objects.md)
</dt> <dt>

[<span data-ttu-id="b2e8b-121">Sécurité de l’objet de synchronisation et droits d’accès</span><span class="sxs-lookup"><span data-stu-id="b2e8b-121">Synchronization Object Security and Access Rights</span></span>](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="b2e8b-122">**CreateEvent** (fonction)</span><span class="sxs-lookup"><span data-stu-id="b2e8b-122">**CreateEvent** function</span></span>](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[<span data-ttu-id="b2e8b-123">**CreateEventEx** fonction)</span><span class="sxs-lookup"><span data-stu-id="b2e8b-123">**CreateEventEx** function</span></span>](/windows/win32/api/synchapi/nf-synchapi-createeventexa)
</dt> </dl>
