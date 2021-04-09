---
title: Message CQPM_HELP (cmnquery. h)
description: Envoyé à la fonction de rappel CQPageProc d’une page d’extension de formulaire de requête pour permettre à l’extension de page d’afficher l’aide contextuelle pour la page.
ms.assetid: 07f5bd24-bca2-4d87-8e1e-acce552a3bf2
ms.tgt_platform: multiple
keywords:
- Message de CQPM_HELP Active Directory
topic_type:
- apiref
api_name:
- CQPM_HELP
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7635b87a0ba489c63f87fb32742c37a9f7044860
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103065"
---
# <a name="cqpm_help-message"></a><span data-ttu-id="a78ff-104">\_Message d’aide CQPM</span><span class="sxs-lookup"><span data-stu-id="a78ff-104">CQPM\_HELP message</span></span>

<span data-ttu-id="a78ff-105">Le message d' **\_ aide CQPM** est envoyé à la fonction de rappel [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) d’une page d’extension de formulaire de requête pour permettre à l’extension de page d’afficher l’aide contextuelle pour la page.</span><span class="sxs-lookup"><span data-stu-id="a78ff-105">The **CQPM\_HELP** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to allow the page extension to display context-sensitive help for the page.</span></span> <span data-ttu-id="a78ff-106">Si possible, l’extension de la page de requête doit afficher l’aide contextuelle en réponse à cet événement.</span><span class="sxs-lookup"><span data-stu-id="a78ff-106">If possible, the query page extension should display context-sensitive help in response to this event.</span></span>

## <a name="parameters"></a><span data-ttu-id="a78ff-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a78ff-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a78ff-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a78ff-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a78ff-109">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="a78ff-109">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="a78ff-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a78ff-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a78ff-111">Pointeur vers une structure [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) qui contient des données supplémentaires sur l’élément de menu, le contrôle, la boîte de dialogue ou la fenêtre pour laquelle une aide contextuelle est demandée.</span><span class="sxs-lookup"><span data-stu-id="a78ff-111">Pointer to a [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure that contains additional data about the menu item, control, dialog box, or window for which context-sensitive help is requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a78ff-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a78ff-112">Return value</span></span>

<span data-ttu-id="a78ff-113">La valeur de retour de ce message est ignorée.</span><span class="sxs-lookup"><span data-stu-id="a78ff-113">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="a78ff-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a78ff-114">Requirements</span></span>



| <span data-ttu-id="a78ff-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a78ff-115">Requirement</span></span> | <span data-ttu-id="a78ff-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a78ff-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a78ff-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a78ff-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a78ff-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a78ff-118">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="a78ff-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a78ff-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a78ff-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a78ff-120">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="a78ff-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="a78ff-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a78ff-122"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="a78ff-122"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a78ff-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a78ff-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a78ff-124">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="a78ff-124">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="a78ff-125">**HELPINFO**</span><span class="sxs-lookup"><span data-stu-id="a78ff-125">**HELPINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-helpinfo)
</dt> </dl>

 

