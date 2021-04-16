---
title: Message TB_ISBUTTONCHECKED (commctrl. h)
description: Détermine si le bouton spécifié dans une barre d’outils est activé.
ms.assetid: ce576951-8db6-4854-8457-211ece018ce8
keywords:
- TB_ISBUTTONCHECKED les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_ISBUTTONCHECKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb9bc573478ea55ce8e0bda48ff16679b135fc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508450"
---
# <a name="tb_isbuttonchecked-message"></a><span data-ttu-id="807ac-104">TO \_ ISBUTTONCHECKED message</span><span class="sxs-lookup"><span data-stu-id="807ac-104">TB\_ISBUTTONCHECKED message</span></span>

<span data-ttu-id="807ac-105">Détermine si le bouton spécifié dans une barre d’outils est activé.</span><span class="sxs-lookup"><span data-stu-id="807ac-105">Determines whether the specified button in a toolbar is checked.</span></span>

## <a name="parameters"></a><span data-ttu-id="807ac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="807ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="807ac-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="807ac-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="807ac-108">Identificateur de commande du bouton.</span><span class="sxs-lookup"><span data-stu-id="807ac-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="807ac-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="807ac-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="807ac-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="807ac-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="807ac-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="807ac-111">Return value</span></span>

<span data-ttu-id="807ac-112">Retourne une valeur différente de zéro si le bouton est activé, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="807ac-112">Returns nonzero if the button is checked, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="807ac-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="807ac-113">Requirements</span></span>



| <span data-ttu-id="807ac-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="807ac-114">Requirement</span></span> | <span data-ttu-id="807ac-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="807ac-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="807ac-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="807ac-116">Minimum supported client</span></span><br/> | <span data-ttu-id="807ac-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="807ac-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="807ac-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="807ac-118">Minimum supported server</span></span><br/> | <span data-ttu-id="807ac-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="807ac-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="807ac-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="807ac-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="807ac-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="807ac-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





