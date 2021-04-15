---
title: Message RB_SETBANDWIDTH (commctrl. h)
description: Définit la largeur d’une bande ancrée.
ms.assetid: dca9dfe9-3e5a-40bb-8de7-a296e6be7d06
keywords:
- RB_SETBANDWIDTH les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_SETBANDWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790f42ab977cfc0554c9a0eca737d541e001b6c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466071"
---
# <a name="rb_setbandwidth-message"></a><span data-ttu-id="d7255-104">\_Message SETBANDWIDTH RB</span><span class="sxs-lookup"><span data-stu-id="d7255-104">RB\_SETBANDWIDTH message</span></span>

<span data-ttu-id="d7255-105">Définit la largeur d’une bande ancrée.</span><span class="sxs-lookup"><span data-stu-id="d7255-105">Sets the width for a docked band.</span></span>

## <a name="parameters"></a><span data-ttu-id="d7255-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7255-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7255-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d7255-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7255-108">Index de la bande.</span><span class="sxs-lookup"><span data-stu-id="d7255-108">Index of the band.</span></span>

</dd> <dt>

<span data-ttu-id="d7255-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7255-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7255-110">Nouvelle largeur en pixels.</span><span class="sxs-lookup"><span data-stu-id="d7255-110">New width in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7255-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d7255-111">Return value</span></span>

<span data-ttu-id="d7255-112">Retourne la valeur **true** si la valeur a été définie et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d7255-112">Returns **TRUE** if the value was set and **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7255-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7255-113">Requirements</span></span>



| <span data-ttu-id="d7255-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7255-114">Requirement</span></span> | <span data-ttu-id="d7255-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7255-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7255-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7255-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d7255-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7255-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d7255-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7255-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d7255-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7255-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7255-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7255-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7255-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7255-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





