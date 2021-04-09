---
title: Message EM_GETTOUCHOPTIONS (RichEdit. h)
description: Récupère les options tactiles associées à un contrôle RichEdit.
ms.assetid: 1D367818-5625-4A5A-A7A1-330FED516990
keywords:
- EM_GETTOUCHOPTIONS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812d37de1972c6da205944d9913dc3fa046c205d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033099"
---
# <a name="em_gettouchoptions-message"></a><span data-ttu-id="6b577-104">\_Message GETTOUCHOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="6b577-104">EM\_GETTOUCHOPTIONS message</span></span>

<span data-ttu-id="6b577-105">Récupère les options tactiles associées à un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="6b577-105">Retrieves the touch options that are associated with a rich edit control.</span></span>


```C++
#define EM_GETTOUCHOPTIONS       (WM_USER + 310)
```



## <a name="parameters"></a><span data-ttu-id="6b577-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6b577-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b577-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b577-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b577-108">Options tactiles à récupérer.</span><span class="sxs-lookup"><span data-stu-id="6b577-108">The touch options to retrieve.</span></span> <span data-ttu-id="6b577-109">Il peut avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6b577-109">It can be one of the following values.</span></span>



| <span data-ttu-id="6b577-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b577-110">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="6b577-111">Signification</span><span class="sxs-lookup"><span data-stu-id="6b577-111">Meaning</span></span>                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <span data-ttu-id="6b577-112"><dt>**RTO \_ SHOWHANDLES**</dt></span><span class="sxs-lookup"><span data-stu-id="6b577-112"><dt>**RTO\_SHOWHANDLES**</dt></span></span> </dl>          | <span data-ttu-id="6b577-113">Récupère si les pinceaux tactiles sont visibles.</span><span class="sxs-lookup"><span data-stu-id="6b577-113">Retrieves whether the touch grippers are visible.</span></span><br/> |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <span data-ttu-id="6b577-114"><dt>**RTO \_ DISABLEHANDLES**</dt></span><span class="sxs-lookup"><span data-stu-id="6b577-114"><dt>**RTO\_DISABLEHANDLES**</dt></span></span> </dl> | <span data-ttu-id="6b577-115">La récupération de cet indicateur n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="6b577-115">Retrieving this flag is not implemented.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="6b577-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b577-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b577-117">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="6b577-117">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b577-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6b577-118">Return value</span></span>

<span data-ttu-id="6b577-119">Retourne la valeur de l’option spécifiée par le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="6b577-119">Returns the value of the option specified by the *wParam* parameter.</span></span> <span data-ttu-id="6b577-120">Il est différent de zéro si *wParam* est **RTO \_ SHOWHANDLES** et que les pinceaux tactiles sont visibles ; sinon,.</span><span class="sxs-lookup"><span data-stu-id="6b577-120">It is nonzero if *wParam* is **RTO\_SHOWHANDLES** and the touch grippers are visible; zero, otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b577-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b577-121">Requirements</span></span>



| <span data-ttu-id="6b577-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b577-122">Requirement</span></span> | <span data-ttu-id="6b577-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b577-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b577-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b577-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6b577-125">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b577-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6b577-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b577-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6b577-127">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b577-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b577-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="6b577-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b577-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b577-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b577-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b577-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b577-131">**\_SETTOUCHOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="6b577-131">**EM\_SETTOUCHOPTIONS**</span></span>](em-settouchoptions.md)
</dt> </dl>

 

 





