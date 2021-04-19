---
title: Message RB_DELETEBAND (commctrl. h)
description: Supprime une bande d’un contrôle rebar.
ms.assetid: 15f2ea78-5c3f-4fe1-a020-025c33f00703
keywords:
- RB_DELETEBAND les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_DELETEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a15fd8593c816b64f0d7f82058b3779f256dd521
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510761"
---
# <a name="rb_deleteband-message"></a><span data-ttu-id="a8a78-104">\_Message DELETEBAND RB</span><span class="sxs-lookup"><span data-stu-id="a8a78-104">RB\_DELETEBAND message</span></span>

<span data-ttu-id="a8a78-105">Supprime une bande d’un contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="a8a78-105">Deletes a band from a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a8a78-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8a78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8a78-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8a78-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8a78-108">Index de base zéro de la bande à supprimer.</span><span class="sxs-lookup"><span data-stu-id="a8a78-108">Zero-based index of the band to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="a8a78-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8a78-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a8a78-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="a8a78-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8a78-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a8a78-111">Return value</span></span>

<span data-ttu-id="a8a78-112">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a8a78-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8a78-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8a78-113">Requirements</span></span>



| <span data-ttu-id="a8a78-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8a78-114">Requirement</span></span> | <span data-ttu-id="a8a78-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8a78-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8a78-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8a78-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a8a78-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8a78-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a8a78-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8a78-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a8a78-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8a78-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a8a78-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="a8a78-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8a78-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8a78-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





