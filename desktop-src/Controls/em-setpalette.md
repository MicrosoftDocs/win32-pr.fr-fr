---
title: Message EM_SETPALETTE (RichEdit. h)
description: Modifie la palette utilisée par un contrôle RichEdit pour sa fenêtre d’affichage.
ms.assetid: c1dc0c24-eaf2-47a8-9bb1-59f37b206feb
keywords:
- EM_SETPALETTE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETPALETTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 026a0a85001818b6f69366e8dba80ef56a7a8f20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032760"
---
# <a name="em_setpalette-message"></a><span data-ttu-id="ce21f-104">\_Message SETPALETTE em</span><span class="sxs-lookup"><span data-stu-id="ce21f-104">EM\_SETPALETTE message</span></span>

<span data-ttu-id="ce21f-105">Modifie la palette utilisée par un contrôle RichEdit pour sa fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="ce21f-105">Changes the palette that a rich edit control uses for its display window.</span></span>

## <a name="parameters"></a><span data-ttu-id="ce21f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce21f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce21f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ce21f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce21f-108">Handle vers la nouvelle palette utilisée par le contrôle Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="ce21f-108">Handle to the new palette used by the rich edit control.</span></span>

</dd> <dt>

<span data-ttu-id="ce21f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce21f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce21f-110">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="ce21f-110">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce21f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ce21f-111">Return value</span></span>

<span data-ttu-id="ce21f-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ce21f-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce21f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ce21f-113">Remarks</span></span>

<span data-ttu-id="ce21f-114">Le contrôle Rich Edit ne vérifie pas si la nouvelle palette est valide.</span><span class="sxs-lookup"><span data-stu-id="ce21f-114">The rich edit control does not check whether the new palette is valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce21f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce21f-115">Requirements</span></span>



| <span data-ttu-id="ce21f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce21f-116">Requirement</span></span> | <span data-ttu-id="ce21f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce21f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce21f-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce21f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ce21f-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce21f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ce21f-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce21f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ce21f-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce21f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce21f-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce21f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce21f-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce21f-123"><dt>Richedit.h</dt></span></span> </dl> |



 

 





