---
title: sh_socket, mot clé
description: Le \_ mot clé \ SH Socket \ spécifie que l’objet système est un handle d’un Socket.
keywords:
- sh_socket mot clé MIDL
topic_type:
- apiref
api_name:
- sh_socket keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 5f5d2506f66f89cd47ecf3f011c8071b79e64177
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "106538035"
---
# <a name="sh_socket-keyword"></a><span data-ttu-id="1c281-104">\_mot clé de socket SH</span><span class="sxs-lookup"><span data-stu-id="1c281-104">sh\_socket keyword</span></span>

<span data-ttu-id="1c281-105">Le mot clé de **\_ Socket SH** spécifie qu’un `system_handle` contient un handle vers un Socket.</span><span class="sxs-lookup"><span data-stu-id="1c281-105">The **sh\_socket** keyword specifies that a `system_handle` holds a handle to a socket.</span></span>

``` syntax
[system_handle(sh_socket)]

[system_handle(sh_socket, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="1c281-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c281-106">Parameters</span></span>

<span data-ttu-id="1c281-107">Ce mot clé est un paramètre pour [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="1c281-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="1c281-108">La documentation [**system_handle**](system-handle.md) contient également des informations sur l’utilisation facultative du paramètre *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="1c281-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="1c281-109">Le comportement par défaut est défini `DUPLICATE_SAME_ACCESS` par les spécifications de [fonction **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="1c281-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c281-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1c281-110">Remarks</span></span>

<span data-ttu-id="1c281-111">Pour pouvoir utiliser ce mot clé avec l' `system_handle` attribut, l' `-target` indicateur doit avoir la valeur `NT100` (ou une version ultérieure) lors de l’exécution de midl.exe.</span><span class="sxs-lookup"><span data-stu-id="1c281-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="1c281-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="1c281-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT ListenToSocket([in, system_handle(sh_socket)] HANDLE socket);
}
```

## <a name="requirements"></a><span data-ttu-id="1c281-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c281-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="1c281-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c281-114">Minimum supported client</span></span> | <span data-ttu-id="1c281-115">Mise à jour anniversaire Windows 10 (version 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="1c281-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="1c281-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c281-116">Minimum supported server</span></span> | <span data-ttu-id="1c281-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="1c281-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="1c281-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c281-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c281-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="1c281-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="1c281-120">Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="1c281-120">Windows Sockets 2</span></span>](../winsock/windows-sockets-start-page-2.md)
</dt> </dl>
