---
title: sh_section, mot clé
description: La section \ SH \_ \ Keyword spécifie que l’objet système est un handle d’une section.
keywords:
- sh_section mot clé MIDL
topic_type:
- apiref
api_name:
- sh_section keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 056112deb790e727206a5ac1a1a2a5043a68f5e1
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "106531242"
---
# <a name="sh_section-keyword"></a><span data-ttu-id="e4719-104">SH \_ section (mot clé)</span><span class="sxs-lookup"><span data-stu-id="e4719-104">sh\_section keyword</span></span>

<span data-ttu-id="e4719-105">Le mot clé de la **\_ section SH** spécifie qu’un `system_handle` contient un handle vers une section.</span><span class="sxs-lookup"><span data-stu-id="e4719-105">The **sh\_section** keyword specifies that a `system_handle` holds a handle to a section.</span></span>

``` syntax
[system_handle(sh_section)]

[system_handle(sh_section, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="e4719-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4719-106">Parameters</span></span>

<span data-ttu-id="e4719-107">Ce mot clé est un paramètre pour [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="e4719-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="e4719-108">La documentation [**system_handle**](system-handle.md) contient également des informations sur l’utilisation facultative du paramètre *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="e4719-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="e4719-109">Le comportement par défaut est défini `DUPLICATE_SAME_ACCESS` par les spécifications de [fonction **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="e4719-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4719-110">Notes</span><span class="sxs-lookup"><span data-stu-id="e4719-110">Remarks</span></span>

<span data-ttu-id="e4719-111">Pour pouvoir utiliser ce mot clé avec l' `system_handle` attribut, l' `-target` indicateur doit avoir la valeur `NT100` (ou une version ultérieure) lors de l’exécution de midl.exe.</span><span class="sxs-lookup"><span data-stu-id="e4719-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="e4719-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="e4719-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GiveSection([in, system_handle(sh_section)] HANDLE section);

    HRESULT GetSectionToWatch([out, system_handle(sh_section, SECTION_MAP_READ)] HANDLE* pSection);
}
```

## <a name="requirements"></a><span data-ttu-id="e4719-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4719-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="e4719-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4719-114">Minimum supported client</span></span> | <span data-ttu-id="e4719-115">Mise à jour anniversaire Windows 10 (version 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="e4719-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="e4719-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4719-116">Minimum supported server</span></span> | <span data-ttu-id="e4719-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="e4719-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="e4719-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4719-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4719-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="e4719-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="e4719-120">Objets et vues de section</span><span class="sxs-lookup"><span data-stu-id="e4719-120">Section Objects and Views</span></span>](/windows-hardware/drivers/kernel/section-objects-and-views)
</dt> <dt>

[<span data-ttu-id="e4719-121">Fonction **ZwCreateSection** (y compris les spécifications d’accès)</span><span class="sxs-lookup"><span data-stu-id="e4719-121">**ZwCreateSection** function (including access specifications)</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-zwcreatesection)
</dt> </dl>
