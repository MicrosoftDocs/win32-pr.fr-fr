---
title: Message RB_SHOWBAND (commctrl. h)
description: Affiche ou masque une bande donnée dans un contrôle rebar.
ms.assetid: 18097aca-e1b4-4359-9d08-4e62406f3f7f
keywords:
- RB_SHOWBAND les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_SHOWBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27c9cedeb42e7eeed9432af9c2a040ac4991810
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106249"
---
# <a name="rb_showband-message"></a><span data-ttu-id="63075-104">\_Message SHOWBAND RB</span><span class="sxs-lookup"><span data-stu-id="63075-104">RB\_SHOWBAND message</span></span>

<span data-ttu-id="63075-105">Affiche ou masque une bande donnée dans un contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="63075-105">Shows or hides a given band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="63075-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63075-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63075-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="63075-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63075-108">Index de base zéro d’une bande dans le contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="63075-108">Zero-based index of a band in the rebar control.</span></span>

</dd> <dt>

<span data-ttu-id="63075-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="63075-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63075-110">Valeur **booléenne** qui indique si la bande doit être affichée ou masquée.</span><span class="sxs-lookup"><span data-stu-id="63075-110">**BOOL** value that indicates if the band should be shown or hidden.</span></span> <span data-ttu-id="63075-111">Si cette valeur est différente de zéro, la bande est affichée.</span><span class="sxs-lookup"><span data-stu-id="63075-111">If this value is nonzero, the band will be shown.</span></span> <span data-ttu-id="63075-112">Dans le cas contraire, la bande sera masquée.</span><span class="sxs-lookup"><span data-stu-id="63075-112">Otherwise, the band will be hidden.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63075-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="63075-113">Return value</span></span>

<span data-ttu-id="63075-114">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="63075-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="63075-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63075-115">Requirements</span></span>



| <span data-ttu-id="63075-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63075-116">Requirement</span></span> | <span data-ttu-id="63075-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="63075-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63075-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63075-118">Minimum supported client</span></span><br/> | <span data-ttu-id="63075-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63075-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="63075-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63075-120">Minimum supported server</span></span><br/> | <span data-ttu-id="63075-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63075-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="63075-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="63075-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="63075-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="63075-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





