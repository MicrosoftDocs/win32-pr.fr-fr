---
title: Message EM_GETOLEINTERFACE (RichEdit. h)
description: Récupère un objet IRichEditOle qu’un client peut utiliser pour accéder à la fonctionnalité COM (Component Object Model) d’un contrôle RichEdit.
ms.assetid: fa462c7b-29b9-4694-b7ad-6068c69ffb76
keywords:
- EM_GETOLEINTERFACE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETOLEINTERFACE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d7557d40c6dcec38ce629d949a8db9915714821
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104818"
---
# <a name="em_getoleinterface-message"></a><span data-ttu-id="90b44-104">\_Message GETOLEINTERFACE em</span><span class="sxs-lookup"><span data-stu-id="90b44-104">EM\_GETOLEINTERFACE message</span></span>

<span data-ttu-id="90b44-105">Récupère un objet [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) qu’un client peut utiliser pour accéder à la fonctionnalité com (Component Object Model) d’un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="90b44-105">Retrieves an [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) object that a client can use to access a rich edit control's Component Object Model (COM) functionality.</span></span>

## <a name="parameters"></a><span data-ttu-id="90b44-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="90b44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90b44-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="90b44-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90b44-108">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="90b44-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="90b44-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="90b44-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90b44-110">Pointeur vers un pointeur qui reçoit l’objet [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) .</span><span class="sxs-lookup"><span data-stu-id="90b44-110">Pointer to a pointer that receives the [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) object.</span></span> <span data-ttu-id="90b44-111">Le contrôle appelle la méthode [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) pour l’objet avant de retourner, de sorte que l’application appelante doit appeler la méthode [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) lorsque l’objet est terminé.</span><span class="sxs-lookup"><span data-stu-id="90b44-111">The control calls the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) method for the object before returning, so the calling application must call the [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) method when it is done with the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90b44-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="90b44-112">Return value</span></span>

<span data-ttu-id="90b44-113">Si l’opération a échoué, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="90b44-113">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="90b44-114">Si l’opération échoue, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="90b44-114">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="90b44-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90b44-115">Requirements</span></span>



| <span data-ttu-id="90b44-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="90b44-116">Requirement</span></span> | <span data-ttu-id="90b44-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="90b44-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90b44-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90b44-118">Minimum supported client</span></span><br/> | <span data-ttu-id="90b44-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="90b44-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="90b44-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90b44-120">Minimum supported server</span></span><br/> | <span data-ttu-id="90b44-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="90b44-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="90b44-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="90b44-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="90b44-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="90b44-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90b44-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90b44-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90b44-125">**IRichEditOle**</span><span class="sxs-lookup"><span data-stu-id="90b44-125">**IRichEditOle**</span></span>](/windows/desktop/api/Richole/nn-richole-iricheditole)
</dt> </dl>

 

