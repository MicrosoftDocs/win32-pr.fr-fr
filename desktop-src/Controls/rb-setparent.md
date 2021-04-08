---
title: Message RB_SETPARENT (commctrl. h)
description: Définit la fenêtre parente d’un contrôle rebar.
ms.assetid: bb8036d4-cab8-4887-86c6-66460bdbe64b
keywords:
- RB_SETPARENT les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_SETPARENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6fafd054d9438b6aedd268620097847b42f3d60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843918"
---
# <a name="rb_setparent-message"></a><span data-ttu-id="74068-104">\_Message SETPARENT, RB</span><span class="sxs-lookup"><span data-stu-id="74068-104">RB\_SETPARENT message</span></span>

<span data-ttu-id="74068-105">Définit la fenêtre parente d’un contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="74068-105">Sets a rebar control's parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="74068-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="74068-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74068-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74068-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74068-108">Handle de la fenêtre parente à définir.</span><span class="sxs-lookup"><span data-stu-id="74068-108">Handle to the parent window to be set.</span></span>

</dd> <dt>

<span data-ttu-id="74068-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74068-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="74068-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="74068-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74068-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="74068-111">Return value</span></span>

<span data-ttu-id="74068-112">Retourne le handle vers la fenêtre parente précédente, ou **null** s’il n’existe aucun parent précédent.</span><span class="sxs-lookup"><span data-stu-id="74068-112">Returns the handle to the previous parent window, or **NULL** if there is no previous parent.</span></span>

## <a name="remarks"></a><span data-ttu-id="74068-113">Notes</span><span class="sxs-lookup"><span data-stu-id="74068-113">Remarks</span></span>

<span data-ttu-id="74068-114">Le contrôle rebar envoie des messages de notification à la fenêtre que vous spécifiez avec ce message.</span><span class="sxs-lookup"><span data-stu-id="74068-114">The rebar control sends notification messages to the window you specify with this message.</span></span> <span data-ttu-id="74068-115">Ce message ne modifie pas réellement le parent du contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="74068-115">This message does not actually change the parent of the rebar control.</span></span>

## <a name="requirements"></a><span data-ttu-id="74068-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74068-116">Requirements</span></span>



| <span data-ttu-id="74068-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74068-117">Requirement</span></span> | <span data-ttu-id="74068-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="74068-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74068-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74068-119">Minimum supported client</span></span><br/> | <span data-ttu-id="74068-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74068-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="74068-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74068-121">Minimum supported server</span></span><br/> | <span data-ttu-id="74068-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74068-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="74068-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="74068-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="74068-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="74068-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





