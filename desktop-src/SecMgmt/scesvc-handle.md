---
description: Le \_ type de données handle SCESVC est un handle opaque fourni par le jeu de l’outil de configuration de la sécurité.
ms.assetid: 478d7d4b-7983-4247-b8be-2e2cd3327533
title: SCESVC_HANDLE (scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09fbc115326361e4cbfe1152361a70a36007a302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525713"
---
# <a name="scesvc_handle"></a><span data-ttu-id="74879-103">\_handle SCESVC</span><span class="sxs-lookup"><span data-stu-id="74879-103">SCESVC\_HANDLE</span></span>

<span data-ttu-id="74879-104">Le type de données **\_ handle SCESVC** est un handle opaque fourni par le jeu de l’outil de configuration de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="74879-104">The **SCESVC\_HANDLE** data type is an opaque handle provided by the Security Configuration tool set.</span></span> <span data-ttu-id="74879-105">Elle est utilisée par les méthodes des interfaces [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) et [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) pour transmettre des informations entre le composant logiciel enfichable Configuration de la sécurité et l’extension du composant logiciel enfichable.</span><span class="sxs-lookup"><span data-stu-id="74879-105">It is used by methods of the [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) and [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) interfaces to pass information between the Security Configuration snap-in and the snap-in extension.</span></span>


```C++
typedef PVOID SCESVC_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="74879-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74879-106">Requirements</span></span>



| <span data-ttu-id="74879-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74879-107">Requirement</span></span> | <span data-ttu-id="74879-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="74879-108">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="74879-109">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74879-109">Minimum supported client</span></span><br/> | <span data-ttu-id="74879-110">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74879-110">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="74879-111">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74879-111">Minimum supported server</span></span><br/> | <span data-ttu-id="74879-112">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74879-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="74879-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="74879-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="74879-114"><dt>Scesvc. h</dt></span><span class="sxs-lookup"><span data-stu-id="74879-114"><dt>Scesvc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74879-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74879-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74879-116">**ISceSvcAttachmentData**</span><span class="sxs-lookup"><span data-stu-id="74879-116">**ISceSvcAttachmentData**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)
</dt> <dt>

[<span data-ttu-id="74879-117">**ISceSvcAttachmentPersistInfo**</span><span class="sxs-lookup"><span data-stu-id="74879-117">**ISceSvcAttachmentPersistInfo**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo)
</dt> </dl>

 

 




