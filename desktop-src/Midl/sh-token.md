---
title: sh_token, mot clé
description: Le \_ mot clé \ SH Token \ spécifie que l’objet système est un handle de jeton.
keywords:
- sh_token mot clé MIDL
topic_type:
- apiref
api_name:
- sh_token keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: a33b070af5cd43a095fd6ad45a0dee86f1868171
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "106523093"
---
# <a name="sh_token-keyword"></a><span data-ttu-id="b075e-104">\_mot clé de jeton SH</span><span class="sxs-lookup"><span data-stu-id="b075e-104">sh\_token keyword</span></span>

<span data-ttu-id="b075e-105">Le mot clé de **\_ jeton SH** spécifie qu’un `system_handle` contient un descripteur d’un jeton.</span><span class="sxs-lookup"><span data-stu-id="b075e-105">The **sh\_token** keyword specifies that a `system_handle` holds a handle to a token.</span></span>

``` syntax
[system_handle(sh_token)]

[system_handle(sh_token, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="b075e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b075e-106">Parameters</span></span>

<span data-ttu-id="b075e-107">Ce mot clé est un paramètre pour [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="b075e-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="b075e-108">La documentation [**system_handle**](system-handle.md) contient également des informations sur l’utilisation facultative du paramètre *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="b075e-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="b075e-109">Le comportement par défaut est défini `DUPLICATE_SAME_ACCESS` par les spécifications de [fonction **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="b075e-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="b075e-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b075e-110">Remarks</span></span>

<span data-ttu-id="b075e-111">Pour pouvoir utiliser ce mot clé avec l' `system_handle` attribut, l' `-target` indicateur doit avoir la valeur `NT100` (ou une version ultérieure) lors de l’exécution de midl.exe.</span><span class="sxs-lookup"><span data-stu-id="b075e-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="b075e-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="b075e-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT SetToken([in, system_handle(sh_token)] HANDLE token);

    HRESULT GetToken([out, system_handle(sh_token, TOKEN_QUERY)] HANDLE* pToken);
}
```

## <a name="requirements"></a><span data-ttu-id="b075e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b075e-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="b075e-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b075e-114">Minimum supported client</span></span> | <span data-ttu-id="b075e-115">Mise à jour anniversaire Windows 10 (version 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="b075e-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="b075e-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b075e-116">Minimum supported server</span></span> | <span data-ttu-id="b075e-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="b075e-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="b075e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b075e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b075e-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="b075e-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="b075e-120">Jetons d’accès</span><span class="sxs-lookup"><span data-stu-id="b075e-120">Access Tokens</span></span>](../secauthz/access-tokens.md)
</dt> <dt>

[<span data-ttu-id="b075e-121">Droits d’accès pour les objets Access-Token</span><span class="sxs-lookup"><span data-stu-id="b075e-121">Access Rights for Access-Token Objects</span></span>](../secauthz/access-rights-for-access-token-objects.md)
</dt> </dl>
