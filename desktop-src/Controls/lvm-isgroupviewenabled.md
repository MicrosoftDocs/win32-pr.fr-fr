---
title: Message LVM_ISGROUPVIEWENABLED (commctrl. h)
description: Vérifie si la vue de groupe est activée pour le contrôle d’affichage de liste.
ms.assetid: 7c6ffa1f-300c-4e5e-900f-93a41e06c951
keywords:
- LVM_ISGROUPVIEWENABLED les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_ISGROUPVIEWENABLED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f8f7af79a1b0594ba6ebb100c1c975f09898d35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942640"
---
# <a name="lvm_isgroupviewenabled-message"></a><span data-ttu-id="5058b-104">\_Message ISGROUPVIEWENABLED LVM</span><span class="sxs-lookup"><span data-stu-id="5058b-104">LVM\_ISGROUPVIEWENABLED message</span></span>

<span data-ttu-id="5058b-105">Vérifie si la vue de groupe est activée pour le contrôle d’affichage de liste.</span><span class="sxs-lookup"><span data-stu-id="5058b-105">Checks whether the list-view control has group view enabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="5058b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5058b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5058b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5058b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5058b-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="5058b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5058b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5058b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5058b-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="5058b-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5058b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5058b-111">Return value</span></span>

<span data-ttu-id="5058b-112">Retourne la **valeur true** si la vue de groupe est activée, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5058b-112">Returns **TRUE** if group view is enabled, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5058b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5058b-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5058b-114">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="5058b-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="5058b-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5058b-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5058b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5058b-116">Requirements</span></span>



| <span data-ttu-id="5058b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5058b-117">Requirement</span></span> | <span data-ttu-id="5058b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="5058b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5058b-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5058b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5058b-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5058b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5058b-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5058b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5058b-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5058b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5058b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="5058b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5058b-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5058b-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





