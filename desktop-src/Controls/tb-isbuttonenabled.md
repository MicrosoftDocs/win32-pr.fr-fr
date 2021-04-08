---
title: Message TB_ISBUTTONENABLED (commctrl. h)
description: Détermine si le bouton spécifié dans une barre d’outils est activé.
ms.assetid: 055ed89a-2f3a-4174-b249-c6e68afbad31
keywords:
- TB_ISBUTTONENABLED les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_ISBUTTONENABLED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1647d158f0e19ce9dc110a475990cfcc9deff770
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843349"
---
# <a name="tb_isbuttonenabled-message"></a><span data-ttu-id="151e3-104">TO \_ ISBUTTONENABLED message</span><span class="sxs-lookup"><span data-stu-id="151e3-104">TB\_ISBUTTONENABLED message</span></span>

<span data-ttu-id="151e3-105">Détermine si le bouton spécifié dans une barre d’outils est activé.</span><span class="sxs-lookup"><span data-stu-id="151e3-105">Determines whether the specified button in a toolbar is enabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="151e3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="151e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="151e3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="151e3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="151e3-108">Identificateur de commande du bouton.</span><span class="sxs-lookup"><span data-stu-id="151e3-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="151e3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="151e3-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="151e3-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="151e3-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="151e3-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="151e3-111">Return value</span></span>

<span data-ttu-id="151e3-112">Retourne une valeur différente de zéro si le bouton est activé, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="151e3-112">Returns nonzero if the button is enabled, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="151e3-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="151e3-113">Requirements</span></span>



| <span data-ttu-id="151e3-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="151e3-114">Requirement</span></span> | <span data-ttu-id="151e3-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="151e3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="151e3-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="151e3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="151e3-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="151e3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="151e3-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="151e3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="151e3-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="151e3-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="151e3-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="151e3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="151e3-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="151e3-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





