---
title: sh_pipe, mot clé
description: Le \_ mot clé \ SH pipe \ spécifie que l’objet système est un handle vers un canal.
keywords:
- sh_pipe mot clé MIDL
topic_type:
- apiref
api_name:
- sh_pipe
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 9f9deab2bf5a751d3b2d5956d4d33a1d5b347e18
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "106531440"
---
# <a name="sh_pipe-keyword"></a><span data-ttu-id="5241b-104">\_mot clé de canal SH</span><span class="sxs-lookup"><span data-stu-id="5241b-104">sh\_pipe keyword</span></span>

<span data-ttu-id="5241b-105">Le mot clé de **\_ canal SH** spécifie qu’un `system_handle` contient un handle vers un canal.</span><span class="sxs-lookup"><span data-stu-id="5241b-105">The **sh\_pipe** keyword specifies that a `system_handle` holds a handle to a pipe.</span></span>

``` syntax
[system_handle(sh_pipe)]

[system_handle(sh_pipe, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="5241b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5241b-106">Parameters</span></span>

<span data-ttu-id="5241b-107">Ce mot clé est un paramètre pour [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="5241b-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="5241b-108">La documentation [**system_handle**](system-handle.md) contient également des informations sur l’utilisation facultative du paramètre *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="5241b-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="5241b-109">Le comportement par défaut est défini `DUPLICATE_SAME_ACCESS` par les spécifications de [fonction **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="5241b-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="5241b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="5241b-110">Remarks</span></span>

<span data-ttu-id="5241b-111">Pour pouvoir utiliser ce mot clé avec l' `system_handle` attribut, l' `-target` indicateur doit avoir la valeur `NT100` (ou une version ultérieure) lors de l’exécution de midl.exe.</span><span class="sxs-lookup"><span data-stu-id="5241b-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="5241b-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="5241b-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GetNewPipe([out, system_handle(sh_pipe)] HANDLE* mySidePipe);

    HRESULT PutReadOnlyPipe([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE theirSidePipe);
}
```

## <a name="requirements"></a><span data-ttu-id="5241b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5241b-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="5241b-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5241b-114">Minimum supported client</span></span> | <span data-ttu-id="5241b-115">Mise à jour anniversaire Windows 10 (version 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="5241b-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="5241b-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5241b-116">Minimum supported server</span></span> | <span data-ttu-id="5241b-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="5241b-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="5241b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5241b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5241b-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="5241b-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="5241b-120">À propos des canaux</span><span class="sxs-lookup"><span data-stu-id="5241b-120">About Pipes</span></span>](../ipc/about-pipes.md)
</dt> <dt>

[<span data-ttu-id="5241b-121">Sécurité des fichiers et droits d’accès</span><span class="sxs-lookup"><span data-stu-id="5241b-121">File Security and Access Rights</span></span>](../fileio/file-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="5241b-122">**CreatePipe** fonction)</span><span class="sxs-lookup"><span data-stu-id="5241b-122">**CreatePipe** function</span></span>](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe)
</dt> <dt>

[<span data-ttu-id="5241b-123">**CreateNamedPipe** fonction)</span><span class="sxs-lookup"><span data-stu-id="5241b-123">**CreateNamedPipe** function</span></span>](/windows/win32/api/winbase/nf-winbase-createnamedpipea)
</dt> </dl>
