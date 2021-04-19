---
title: sh_reg_key, mot clé
description: Le \_ mot clé \ SH reg \_ key \ spécifie que l’objet système est un handle de clé de registre.
keywords:
- sh_reg_key mot clé MIDL
topic_type:
- apiref
api_name:
- sh_reg_key keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: cec526bed766534f82d5a1bc24c55050dea814ed
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "106540912"
---
# <a name="sh_reg_key-keyword"></a><span data-ttu-id="e5c53-104">SH \_ reg \_ Key (mot clé)</span><span class="sxs-lookup"><span data-stu-id="e5c53-104">sh\_reg\_key keyword</span></span>

<span data-ttu-id="e5c53-105">Le mot clé **SH \_ \_ reg** spécifie qu’un `system_handle` contient un handle vers une clé de registre.</span><span class="sxs-lookup"><span data-stu-id="e5c53-105">The **sh\_reg\_key** keyword specifies that a `system_handle` holds a handle to a registry key.</span></span>

``` syntax
[system_handle(sh_reg_key)]

[system_handle(sh_reg_key, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="e5c53-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5c53-106">Parameters</span></span>

<span data-ttu-id="e5c53-107">Ce mot clé est un paramètre pour [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="e5c53-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="e5c53-108">La documentation [**system_handle**](system-handle.md) contient également des informations sur l’utilisation facultative du paramètre *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="e5c53-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="e5c53-109">Le comportement par défaut est défini `DUPLICATE_SAME_ACCESS` par les spécifications de [fonction **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="e5c53-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5c53-110">Notes</span><span class="sxs-lookup"><span data-stu-id="e5c53-110">Remarks</span></span>

<span data-ttu-id="e5c53-111">Pour pouvoir utiliser ce mot clé avec l' `system_handle` attribut, l' `-target` indicateur doit avoir la valeur `NT100` (ou une version ultérieure) lors de l’exécution de midl.exe.</span><span class="sxs-lookup"><span data-stu-id="e5c53-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="e5c53-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="e5c53-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GetConfigurationKey([out, system_handle(sh_reg_key)] HANDLE* key);

    HRESULT SetKeyForWatch([in, system_handle(sh_reg_key, KEY_READ)] HANDLE watchKey);
}
```

## <a name="requirements"></a><span data-ttu-id="e5c53-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5c53-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="e5c53-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5c53-114">Minimum supported client</span></span> | <span data-ttu-id="e5c53-115">Mise à jour anniversaire Windows 10 (version 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="e5c53-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="e5c53-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5c53-116">Minimum supported server</span></span> | <span data-ttu-id="e5c53-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="e5c53-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="e5c53-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5c53-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5c53-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="e5c53-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="e5c53-120">Registre</span><span class="sxs-lookup"><span data-stu-id="e5c53-120">Registry</span></span>](../sysinfo/registry.md)
</dt> <dt>

[<span data-ttu-id="e5c53-121">Sécurité de la clé de Registre et droits d’accès</span><span class="sxs-lookup"><span data-stu-id="e5c53-121">Registry Key Security and Access Rights</span></span>](../sysinfo/registry-key-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="e5c53-122">Fonction **RegOpenKeyEx**</span><span class="sxs-lookup"><span data-stu-id="e5c53-122">**RegOpenKeyEx** function</span></span>](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)
</dt> <dt>
