---
description: Envoyé à une procédure DLL d’extension du gestionnaire de fichiers lorsque l’utilisateur appuie sur la touche F1 sur un élément de commande de menu ou de barre d’outils. L’extension doit appeler WinHelp, avec le paramètre HWND de cette fonction défini sur la valeur du paramètre HWND de l’extension.
title: Message FMEVENT_HELPMENUITEM (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPMENUITEM
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 6298061d-7e24-45ab-8bc4-96b28e071080
ms.openlocfilehash: c20b5828a6e2362b9b9c13fc9b2986b0ea7b5fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971918"
---
# <a name="fmevent_helpmenuitem-message"></a><span data-ttu-id="3a34e-104">\_Message FMEVENT HELPMENUITEM</span><span class="sxs-lookup"><span data-stu-id="3a34e-104">FMEVENT\_HELPMENUITEM message</span></span>

<span data-ttu-id="3a34e-105">Envoyé à une procédure DLL d’extension du gestionnaire de fichiers lorsque l’utilisateur appuie sur la touche F1 sur un élément de commande de menu ou de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="3a34e-105">Sent to a File Manager extension DLL procedure when the user presses F1 on a menu or toolbar command item.</span></span> <span data-ttu-id="3a34e-106">L’extension doit appeler [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa), avec le paramètre *HWND* de cette fonction défini sur la valeur du paramètre *HWND* de l’extension.</span><span class="sxs-lookup"><span data-stu-id="3a34e-106">The extension should call [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa), with that function's *hwnd* parameter set to the value of the extension's *hwnd* parameter.</span></span>

## <a name="parameters"></a><span data-ttu-id="3a34e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a34e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a34e-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3a34e-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3a34e-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="3a34e-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3a34e-110">*uItem*</span><span class="sxs-lookup"><span data-stu-id="3a34e-110">*uItem*</span></span> 
</dt> <dd>

<span data-ttu-id="3a34e-111">Valeur qui identifie l’élément de commande de menu ou de barre d’outils pour lequel vous souhaitez obtenir de l’aide.</span><span class="sxs-lookup"><span data-stu-id="3a34e-111">A value that identifies the menu or toolbar command item for which Help is desired.</span></span> <span data-ttu-id="3a34e-112">La procédure d’extension utilise cette valeur pour déterminer la meilleure façon d’appeler [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa).</span><span class="sxs-lookup"><span data-stu-id="3a34e-112">The extension procedure uses this value to determine how best to call [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a34e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3a34e-113">Return value</span></span>

<span data-ttu-id="3a34e-114">Une procédure DLL d’extension doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="3a34e-114">An extension DLL procedure should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a34e-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3a34e-115">Requirements</span></span>



| <span data-ttu-id="3a34e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a34e-116">Requirement</span></span> | <span data-ttu-id="3a34e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a34e-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3a34e-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a34e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3a34e-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3a34e-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="3a34e-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a34e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3a34e-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3a34e-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3a34e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="3a34e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a34e-123"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a34e-123"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a34e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a34e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a34e-125">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="3a34e-125">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="3a34e-126">**\_HELPSTRING FMEVENT**</span><span class="sxs-lookup"><span data-stu-id="3a34e-126">**FMEVENT\_HELPSTRING**</span></span>](fmevent-helpstring.md)
</dt> </dl>

 

 




