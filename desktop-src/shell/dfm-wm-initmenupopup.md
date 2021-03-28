---
description: Envoyé lorsqu’un menu déroulant ou un sous-menu est sur le paragraphe actif. Cela permet à une application de modifier le menu avant qu’il ne soit affiché, sans modifier le menu entier.
title: Message DFM_WM_INITMENUPOPUP (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 314e83f7-839d-4ca0-b5c1-842c5bf14923
api_name:
- DFM_WM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1c89731bdffc0e7d902e6c83b9a4f208134b7cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112335"
---
# <a name="dfm_wm_initmenupopup-message"></a><span data-ttu-id="6734f-104">\_Message DFM WM \_ INITMENUPOPUP</span><span class="sxs-lookup"><span data-stu-id="6734f-104">DFM\_WM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="6734f-105">Envoyé lorsqu’un menu déroulant ou un sous-menu est sur le paragraphe actif.</span><span class="sxs-lookup"><span data-stu-id="6734f-105">Sent when a drop-down menu or submenu is about to become active.</span></span> <span data-ttu-id="6734f-106">Cela permet à une application de modifier le menu avant qu’il ne soit affiché, sans modifier le menu entier.</span><span class="sxs-lookup"><span data-stu-id="6734f-106">This allows an application to modify the menu before it is displayed, without changing the entire menu.</span></span>


```C++
DFM_WM_INITMENUPOPUP 

    wParam = (WPARAM);

    lParam = (LPARAM);

            
```



## <a name="parameters"></a><span data-ttu-id="6734f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6734f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6734f-108">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6734f-108">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6734f-109">Handle vers le menu ou le sous-menu déroulant.</span><span class="sxs-lookup"><span data-stu-id="6734f-109">A handle to the drop-down menu or submenu.</span></span>

</dd> <dt>

<span data-ttu-id="6734f-110">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6734f-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6734f-111">Le mot de poids faible spécifie la position relative de base zéro de l’élément de menu qui ouvre le menu déroulant ou le sous-menu.</span><span class="sxs-lookup"><span data-stu-id="6734f-111">The low-order word specifies the zero-based relative position of the menu item that opens the drop-down menu or submenu.</span></span>

<span data-ttu-id="6734f-112">Le mot de poids fort indique si le menu déroulant est le menu fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6734f-112">The high-order word indicates whether the drop-down menu is the window menu.</span></span> <span data-ttu-id="6734f-113">Si le menu est le menu fenêtre, ce paramètre a la **valeur true**; Sinon, la **valeur est false**.</span><span class="sxs-lookup"><span data-stu-id="6734f-113">If the menu is the window menu, this parameter is **TRUE**; otherwise, it is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6734f-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6734f-114">Return value</span></span>

<span data-ttu-id="6734f-115">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="6734f-115">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="6734f-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6734f-116">Requirements</span></span>



| <span data-ttu-id="6734f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6734f-117">Requirement</span></span> | <span data-ttu-id="6734f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="6734f-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6734f-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6734f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6734f-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6734f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6734f-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6734f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6734f-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6734f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6734f-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="6734f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6734f-124"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="6734f-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




