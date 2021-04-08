---
title: Message TB_REPLACEBITMAP (commctrl. h)
description: Remplace une image bitmap existante par une nouvelle image bitmap.
ms.assetid: abad5c7a-ebdd-46b5-a465-fe64ff8eb127
keywords:
- TB_REPLACEBITMAP les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_REPLACEBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0216d73f70f9bef8230d7e725834d63d60012798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843982"
---
# <a name="tb_replacebitmap-message"></a><span data-ttu-id="aba7d-104">TO \_ REPLACEBITMAP message</span><span class="sxs-lookup"><span data-stu-id="aba7d-104">TB\_REPLACEBITMAP message</span></span>

<span data-ttu-id="aba7d-105">Remplace une image bitmap existante par une nouvelle image bitmap.</span><span class="sxs-lookup"><span data-stu-id="aba7d-105">Replaces an existing bitmap with a new bitmap.</span></span>

## <a name="parameters"></a><span data-ttu-id="aba7d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aba7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aba7d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aba7d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="aba7d-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="aba7d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="aba7d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aba7d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aba7d-110">Pointeur vers une structure [**TBREPLACEBITMAP**](/windows/desktop/api/Commctrl/ns-commctrl-tbreplacebitmap) qui contient les informations de l’image bitmap à remplacer et la nouvelle bitmap.</span><span class="sxs-lookup"><span data-stu-id="aba7d-110">Pointer to a [**TBREPLACEBITMAP**](/windows/desktop/api/Commctrl/ns-commctrl-tbreplacebitmap) structure that contains the information of the bitmap to be replaced and the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aba7d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aba7d-111">Return value</span></span>

<span data-ttu-id="aba7d-112">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="aba7d-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="aba7d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aba7d-113">Requirements</span></span>



| <span data-ttu-id="aba7d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aba7d-114">Requirement</span></span> | <span data-ttu-id="aba7d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="aba7d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aba7d-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aba7d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="aba7d-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aba7d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aba7d-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aba7d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="aba7d-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aba7d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aba7d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="aba7d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="aba7d-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aba7d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





