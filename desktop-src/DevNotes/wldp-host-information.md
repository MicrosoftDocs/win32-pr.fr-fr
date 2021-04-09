---
description: Structure identifiant l’hôte et le fichier source à évaluer.
ms.assetid: 547EF59E-7DE5-45E4-948F-109547FAAEE7
title: Structure WLDP_HOST_INFORMATION (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_INFORMATION
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: ad20be7fa5887e42c09248d04e14f5ff8cffcd54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033593"
---
# <a name="wldp_host_information-structure"></a><span data-ttu-id="096e0-103">Structure des informations de l' \_ hôte WLDP \_</span><span class="sxs-lookup"><span data-stu-id="096e0-103">WLDP\_HOST\_INFORMATION structure</span></span>

<span data-ttu-id="096e0-104">Structure identifiant l’hôte et le fichier source à évaluer.</span><span class="sxs-lookup"><span data-stu-id="096e0-104">A structure identifying the host and source file to be evaluated.</span></span>

## <a name="syntax"></a><span data-ttu-id="096e0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="096e0-105">Syntax</span></span>


```C++
typedef struct _WLDP_HOST_INFORMATION {
  DWORD        dwRevision;
  WLDP_HOST_ID dwHostId;
  PCWSTR       szSource;
  HANDLE       hSource;
} WLDP_HOST_INFORMATION, *PWLDP_HOST_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="096e0-106">Membres</span><span class="sxs-lookup"><span data-stu-id="096e0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="096e0-107">**dwRevision**</span><span class="sxs-lookup"><span data-stu-id="096e0-107">**dwRevision**</span></span>
</dt> <dd>

<span data-ttu-id="096e0-108">Doit être **WLDP \_ \_ \_ révision des informations** de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="096e0-108">Must be **WLDP\_HOST\_INFORMATION\_REVISION**.</span></span>

</dd> <dt>

<span data-ttu-id="096e0-109">**dwHostId**</span><span class="sxs-lookup"><span data-stu-id="096e0-109">**dwHostId**</span></span>
</dt> <dd>

<span data-ttu-id="096e0-110">Valeur d’énumération de l' [**\_ \_ ID d’hôte WLDP**](wldp-host-id.md) qui décrit l’ID d’hôte.</span><span class="sxs-lookup"><span data-stu-id="096e0-110">Enumeration value from [**WLDP\_HOST\_ID**](wldp-host-id.md) that describes the host ID.</span></span>

</dd> <dt>

<span data-ttu-id="096e0-111">**szSource**</span><span class="sxs-lookup"><span data-stu-id="096e0-111">**szSource**</span></span>
</dt> <dd>

<span data-ttu-id="096e0-112">Chemin d’accès complet et nom de script avec l’extension.</span><span class="sxs-lookup"><span data-stu-id="096e0-112">Full path and script name with the extension.</span></span> <span data-ttu-id="096e0-113">NULL pour **l' \_ ID d’hôte WLDP \_ \_ Global**, ou l’exécution manuelle du script.</span><span class="sxs-lookup"><span data-stu-id="096e0-113">NULL for **WLDP\_HOST\_ID\_GLOBAL**, or manual script execution.</span></span>

</dd> <dt>

<span data-ttu-id="096e0-114">**hSource**</span><span class="sxs-lookup"><span data-stu-id="096e0-114">**hSource**</span></span>
</dt> <dd>

<span data-ttu-id="096e0-115">En plus du nom, l’appelant peut spécifier un handle vers le fichier utilisé pour la validation.</span><span class="sxs-lookup"><span data-stu-id="096e0-115">In addition to the name, the caller can specify a handle to the file used for validation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="096e0-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="096e0-116">Requirements</span></span>



| <span data-ttu-id="096e0-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="096e0-117">Requirement</span></span> | <span data-ttu-id="096e0-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="096e0-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="096e0-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="096e0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="096e0-120">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="096e0-120">Windows 8 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="096e0-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="096e0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="096e0-122">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="096e0-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="096e0-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="096e0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="096e0-124"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="096e0-124"><dt>Wldp.h</dt></span></span> </dl> |



 

 




