---
title: Message TB_ISBUTTONHIDDEN (commctrl. h)
description: Détermine si le bouton spécifié dans une barre d’outils est masqué.
ms.assetid: 3372a64f-8209-4e3f-a6a9-8fe2e7e87ff2
keywords:
- TB_ISBUTTONHIDDEN les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_ISBUTTONHIDDEN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db36f289a05fecfb2a0795965820324a9ce68057
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942908"
---
# <a name="tb_isbuttonhidden-message"></a><span data-ttu-id="b3f95-104">TO \_ ISBUTTONHIDDEN message</span><span class="sxs-lookup"><span data-stu-id="b3f95-104">TB\_ISBUTTONHIDDEN message</span></span>

<span data-ttu-id="b3f95-105">Détermine si le bouton spécifié dans une barre d’outils est masqué.</span><span class="sxs-lookup"><span data-stu-id="b3f95-105">Determines whether the specified button in a toolbar is hidden.</span></span>

## <a name="parameters"></a><span data-ttu-id="b3f95-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3f95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3f95-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b3f95-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b3f95-108">Identificateur de commande du bouton.</span><span class="sxs-lookup"><span data-stu-id="b3f95-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="b3f95-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b3f95-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b3f95-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="b3f95-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3f95-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b3f95-111">Return value</span></span>

<span data-ttu-id="b3f95-112">Retourne une valeur différente de zéro si le bouton est masqué, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b3f95-112">Returns nonzero if the button is hidden, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3f95-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3f95-113">Requirements</span></span>



| <span data-ttu-id="b3f95-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3f95-114">Requirement</span></span> | <span data-ttu-id="b3f95-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3f95-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b3f95-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3f95-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b3f95-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3f95-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b3f95-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3f95-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b3f95-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3f95-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b3f95-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="b3f95-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3f95-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3f95-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





