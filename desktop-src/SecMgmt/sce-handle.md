---
description: Le \_ type de données du handle SCE est un handle opaque fourni par le jeu de l’outil de configuration de la sécurité. Elle est utilisée par \_ les informations de requête PFSCE \_ et \_ \_ les fonctions de prise en charge d’PFSCE Set info pour transmettre des informations entre la pièce jointe et la base de données de sécurité.
ms.assetid: 8db91e6f-b31e-40c6-a158-b4b3b00ba0c0
title: SCE_HANDLE (scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fef21dbe03d97dfa14537d5df132ba3cb222643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112658"
---
# <a name="sce_handle"></a><span data-ttu-id="5c7ee-104">\_handle SCE</span><span class="sxs-lookup"><span data-stu-id="5c7ee-104">SCE\_HANDLE</span></span>

<span data-ttu-id="5c7ee-105">Le type de données du **\_ handle SCE** est un handle opaque fourni par le jeu de l’outil de configuration de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="5c7ee-105">The **SCE\_HANDLE** data type is an opaque handle provided by the Security Configuration tool set.</span></span> <span data-ttu-id="5c7ee-106">Elle est utilisée par [**les \_ \_ informations de requête PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) et les fonctions de prise en charge d' [**PFSCE \_ Set \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) pour transmettre des informations entre la pièce jointe et la base de données de sécurité.</span><span class="sxs-lookup"><span data-stu-id="5c7ee-106">It is used by [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) and [**PFSCE\_SET\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) support functions to pass information between the attachment and the security database.</span></span>


```C++
typedef PVOID SCE_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="5c7ee-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c7ee-107">Requirements</span></span>



| <span data-ttu-id="5c7ee-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c7ee-108">Requirement</span></span> | <span data-ttu-id="5c7ee-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c7ee-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5c7ee-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c7ee-110">Minimum supported client</span></span><br/> | <span data-ttu-id="5c7ee-111">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c7ee-111">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5c7ee-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c7ee-112">Minimum supported server</span></span><br/> | <span data-ttu-id="5c7ee-113">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c7ee-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5c7ee-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="5c7ee-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c7ee-115"><dt>Scesvc. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c7ee-115"><dt>Scesvc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c7ee-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c7ee-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c7ee-117">**\_informations sur la requête PFSCE \_**</span><span class="sxs-lookup"><span data-stu-id="5c7ee-117">**PFSCE\_QUERY\_INFO**</span></span>](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> <dt>

[<span data-ttu-id="5c7ee-118">**PFSCE \_ définir des \_ informations**</span><span class="sxs-lookup"><span data-stu-id="5c7ee-118">**PFSCE\_SET\_INFO**</span></span>](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)
</dt> </dl>

 

