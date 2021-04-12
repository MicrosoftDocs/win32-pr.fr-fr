---
description: Le type de données de contexte de l' \_ énumération SCE \_ est un handle opaque fourni par le jeu de l’outil de configuration de la sécurité. Elle est utilisée par la \_ fonction PFSCE Query \_ info pour naviguer dans la base de données de sécurité.
ms.assetid: 05629c49-e36b-4045-93d0-d0f4bc09b08a
title: SCE_ENUMERATION_CONTEXT (scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e380f6f99d68ad63199c3b82f5aa1e5ace8ddf0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318222"
---
# <a name="sce_enumeration_context"></a><span data-ttu-id="60686-104">\_contexte d’énumération SCE \_</span><span class="sxs-lookup"><span data-stu-id="60686-104">SCE\_ENUMERATION\_CONTEXT</span></span>

<span data-ttu-id="60686-105">Le type de données de contexte de l' **\_ \_ énumération SCE** est un handle opaque fourni par le jeu de l’outil de configuration de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="60686-105">The **SCE\_ENUMERATION\_CONTEXT** data type is an opaque handle provided by the Security Configuration tool set.</span></span> <span data-ttu-id="60686-106">Elle est utilisée par la fonction [**PFSCE \_ query \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) pour naviguer dans la base de données de sécurité.</span><span class="sxs-lookup"><span data-stu-id="60686-106">It is used by the [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) function to navigate through the security database.</span></span>


```C++
typedef ULONG SCE_ENUMERATION_CONTEXT, *PSCE_ENUMERATION_CONTEXT;
```



## <a name="requirements"></a><span data-ttu-id="60686-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60686-107">Requirements</span></span>



| <span data-ttu-id="60686-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60686-108">Requirement</span></span> | <span data-ttu-id="60686-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="60686-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="60686-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60686-110">Minimum supported client</span></span><br/> | <span data-ttu-id="60686-111">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="60686-111">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="60686-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60686-112">Minimum supported server</span></span><br/> | <span data-ttu-id="60686-113">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="60686-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="60686-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="60686-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="60686-115"><dt>Scesvc. h</dt></span><span class="sxs-lookup"><span data-stu-id="60686-115"><dt>Scesvc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60686-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60686-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60686-117">**\_informations sur la requête PFSCE \_**</span><span class="sxs-lookup"><span data-stu-id="60686-117">**PFSCE\_QUERY\_INFO**</span></span>](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> </dl>

 

