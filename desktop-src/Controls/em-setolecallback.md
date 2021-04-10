---
title: Message EM_SETOLECALLBACK (RichEdit. h)
description: Fournit un contrôle Rich Edit à un objet IRichEditOleCallback que le contrôle utilise pour obtenir des ressources et des informations liées à OLE à partir du client.
ms.assetid: bd1f8048-214c-4ac6-b826-bedabb1aaee5
keywords:
- EM_SETOLECALLBACK les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETOLECALLBACK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edfc54db112bba42fc3d51b2e328fc7641990c7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942297"
---
# <a name="em_setolecallback-message"></a><span data-ttu-id="3e48c-104">\_Message SETOLECALLBACK em</span><span class="sxs-lookup"><span data-stu-id="3e48c-104">EM\_SETOLECALLBACK message</span></span>

<span data-ttu-id="3e48c-105">Fournit un contrôle Rich Edit à un objet [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) que le contrôle utilise pour obtenir des ressources et des informations liées à OLE à partir du client.</span><span class="sxs-lookup"><span data-stu-id="3e48c-105">Gives a rich edit control an [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) object that the control uses to get OLE-related resources and information from the client.</span></span>

## <a name="parameters"></a><span data-ttu-id="3e48c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e48c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e48c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3e48c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e48c-108">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="3e48c-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3e48c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3e48c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e48c-110">Pointeur vers un objet [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) .</span><span class="sxs-lookup"><span data-stu-id="3e48c-110">Pointer to an [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) object.</span></span> <span data-ttu-id="3e48c-111">Le contrôle appelle la méthode [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) pour l’objet avant de retourner.</span><span class="sxs-lookup"><span data-stu-id="3e48c-111">The control calls the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) method for the object before returning.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e48c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3e48c-112">Return value</span></span>

<span data-ttu-id="3e48c-113">Si l’opération a échoué, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="3e48c-113">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="3e48c-114">Si l’opération échoue, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="3e48c-114">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e48c-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e48c-115">Requirements</span></span>



| <span data-ttu-id="3e48c-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e48c-116">Requirement</span></span> | <span data-ttu-id="3e48c-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e48c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e48c-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e48c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3e48c-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e48c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3e48c-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e48c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3e48c-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e48c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3e48c-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e48c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e48c-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e48c-123"><dt>Richedit.h</dt></span></span> </dl> |



 

