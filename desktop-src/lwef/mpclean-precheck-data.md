---
title: Structure MPCLEAN_PRECHECK_DATA (MpClient. h)
description: Données de notification transmises à la fonction de rappel de prévérification propre.
ms.assetid: 65B3B116-6E83-46F5-AE2B-92A41AE39480
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPCLEAN_PRECHECK_DATA
- PMPCLEAN_PRECHECK_DATA des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPCLEAN_PRECHECK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc3d67e0c71c95db49b633feeb3048cc9f104b2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464907"
---
# <a name="mpclean_precheck_data-structure"></a><span data-ttu-id="56b7d-105">\_Structure de données de PRÉVÉRIFICATION MPCLEAN \_</span><span class="sxs-lookup"><span data-stu-id="56b7d-105">MPCLEAN\_PRECHECK\_DATA structure</span></span>

<span data-ttu-id="56b7d-106">Données de notification transmises à la fonction de rappel de prévérification propre.</span><span class="sxs-lookup"><span data-stu-id="56b7d-106">Notification data passed to clean precheck callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="56b7d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56b7d-107">Syntax</span></span>


```C++
typedef struct tagMPCLEAN_PRECHECK_DATA {
  PMPRESOURCE_INFO     BlockedResourceInfo;
  BlockingResourceInfo PMPRESOURCE_INFO;
} MPCLEAN_PRECHECK_DATA, *PMPCLEAN_PRECHECK_DATA;
```



## <a name="members"></a><span data-ttu-id="56b7d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="56b7d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="56b7d-109">**BlockedResourceInfo**</span><span class="sxs-lookup"><span data-stu-id="56b7d-109">**BlockedResourceInfo**</span></span>
</dt> <dd>

<span data-ttu-id="56b7d-110">Type : **PMPRESOURCE \_ info**</span><span class="sxs-lookup"><span data-stu-id="56b7d-110">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="56b7d-111">Informations sur les ressources relatives à la ressource bloquée.</span><span class="sxs-lookup"><span data-stu-id="56b7d-111">Resource information about the resource being blocked.</span></span> <span data-ttu-id="56b7d-112">Par exemple, lorsque la progression est **MPNOTIFY \_ prévérifier la ressource est \_ \_ bloquée**.</span><span class="sxs-lookup"><span data-stu-id="56b7d-112">For example, when progress is **MPNOTIFY\_PRECHECK\_RESOURCE\_BLOCKED**.</span></span> <span data-ttu-id="56b7d-113">Consultez [**MPRESOURCE \_ info**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="56b7d-113">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="56b7d-114">**\_informations PMPRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="56b7d-114">**PMPRESOURCE\_INFO**</span></span>
</dt> <dd>

<span data-ttu-id="56b7d-115">Type : **BlockingResourceInfo**</span><span class="sxs-lookup"><span data-stu-id="56b7d-115">Type: **BlockingResourceInfo**</span></span>

</dd> <dd>

<span data-ttu-id="56b7d-116">Informations de ressource sur la ressource qui bloque.</span><span class="sxs-lookup"><span data-stu-id="56b7d-116">Resource information about the resource that is blocking.</span></span> <span data-ttu-id="56b7d-117">Par exemple, lorsque la progression est **MPNOTIFY \_ prévérifier la ressource est \_ \_ bloquée**.</span><span class="sxs-lookup"><span data-stu-id="56b7d-117">For example, when progress is **MPNOTIFY\_PRECHECK\_RESOURCE\_BLOCKED**.</span></span> <span data-ttu-id="56b7d-118">Consultez [**MPRESOURCE \_ info**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="56b7d-118">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56b7d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56b7d-119">Requirements</span></span>



| <span data-ttu-id="56b7d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56b7d-120">Requirement</span></span> | <span data-ttu-id="56b7d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="56b7d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56b7d-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56b7d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="56b7d-123">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56b7d-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="56b7d-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56b7d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="56b7d-125">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56b7d-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56b7d-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="56b7d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="56b7d-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="56b7d-127"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56b7d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56b7d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56b7d-129">**\_informations MPRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="56b7d-129">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> </dl>

 

 





