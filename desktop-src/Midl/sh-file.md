---
title: sh_file, mot clé
description: Le fichier \ SH \_ \ Keyword spécifie que l’objet système est un handle de fichier.
keywords:
- sh_file mot clé MIDL
topic_type:
- apiref
api_name:
- pointer_default
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: f7d2ae0ef4a8166f90700267fa8459525ad4be2f
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104321362"
---
# <a name="sh_file-keyword"></a><span data-ttu-id="b5791-104">\_fichier sh (mot clé)</span><span class="sxs-lookup"><span data-stu-id="b5791-104">sh\_file keyword</span></span>

<span data-ttu-id="b5791-105">Le mot clé **\_ fichier sh** spécifie qu’un `system_handle` contient un descripteur d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="b5791-105">The **sh\_file** keyword specifies that a `system_handle` holds a handle to a file.</span></span>

``` syntax
[system_handle(sh_file)]

[system_handle(sh_file, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="b5791-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5791-106">Parameters</span></span>

<span data-ttu-id="b5791-107">Ce mot clé est un paramètre pour [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="b5791-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="b5791-108">La documentation [**system_handle**](system-handle.md) contient également des informations sur l’utilisation facultative du paramètre *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="b5791-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="b5791-109">Le comportement par défaut est défini `DUPLICATE_SAME_ACCESS` par les spécifications de [fonction **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="b5791-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5791-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b5791-110">Remarks</span></span>

<span data-ttu-id="b5791-111">Pour pouvoir utiliser ce mot clé avec l' `system_handle` attribut, l' `-target` indicateur doit avoir la valeur `NT100` (ou une version ultérieure) lors de l’exécution de midl.exe.</span><span class="sxs-lookup"><span data-stu-id="b5791-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="b5791-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="b5791-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT WriteThisFile([in, system_handle(sh_file)] HANDLE file);

    HRESULT GetFileToRead([out, system_handle(sh_file, READ_CONTROL | SYNCHRONIZE | FILE_READ_DATA | FILE_READ_keywordS | FILE_READ_EA)] HANDLE* pReadThisFile);
}
```

## <a name="requirements"></a><span data-ttu-id="b5791-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5791-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="b5791-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5791-114">Minimum supported client</span></span> | <span data-ttu-id="b5791-115">Mise à jour anniversaire Windows 10 (version 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="b5791-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="b5791-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5791-116">Minimum supported server</span></span> | <span data-ttu-id="b5791-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="b5791-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="b5791-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5791-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5791-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="b5791-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="b5791-120">Sécurité des fichiers et droits d’accès</span><span class="sxs-lookup"><span data-stu-id="b5791-120">File Security and Access Rights</span></span>](../fileio/file-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="b5791-121">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="b5791-121">DirectComposition</span></span>](/windows/win32/api/_directcomp/)
</dt> <dt>

[<span data-ttu-id="b5791-122">**DCompositionCreateSurfaceHandle** fonction)</span><span class="sxs-lookup"><span data-stu-id="b5791-122">**DCompositionCreateSurfaceHandle** function</span></span>](/windows/win32/api/dcomp/nf-dcomp-dcompositioncreatesurfacehandle)
</dt> <dt>
