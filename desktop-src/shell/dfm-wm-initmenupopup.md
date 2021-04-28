---
description: DFM_WM_INITMENUPOPUP message-envoyé quand un menu déroulant ou un sous-menu est sur le paragraphe actif. Cela permet à une application de modifier le menu avant qu’il ne soit affiché, sans modifier le menu entier.
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
ms.openlocfilehash: 9df2700403dcdc0ce00b6d90d9c3a87d373b0a34
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096997"
---
# <a name="dfm_wm_initmenupopup-message"></a><span data-ttu-id="01846-104">\_Message DFM WM \_ INITMENUPOPUP</span><span class="sxs-lookup"><span data-stu-id="01846-104">DFM\_WM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="01846-105">Envoyé lorsqu’un menu déroulant ou un sous-menu est sur le paragraphe actif.</span><span class="sxs-lookup"><span data-stu-id="01846-105">Sent when a drop-down menu or submenu is about to become active.</span></span> <span data-ttu-id="01846-106">Cela permet à une application de modifier le menu avant qu’il ne soit affiché, sans modifier le menu entier.</span><span class="sxs-lookup"><span data-stu-id="01846-106">This allows an application to modify the menu before it is displayed, without changing the entire menu.</span></span>


```C++
DFM_WM_INITMENUPOPUP 

    wParam = (WPARAM);

    lParam = (LPARAM);

            
```



## <a name="parameters"></a><span data-ttu-id="01846-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01846-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01846-108">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="01846-108">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01846-109">Handle vers le menu ou le sous-menu déroulant.</span><span class="sxs-lookup"><span data-stu-id="01846-109">A handle to the drop-down menu or submenu.</span></span>

</dd> <dt>

<span data-ttu-id="01846-110">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="01846-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01846-111">Le mot de poids faible spécifie la position relative de base zéro de l’élément de menu qui ouvre le menu déroulant ou le sous-menu.</span><span class="sxs-lookup"><span data-stu-id="01846-111">The low-order word specifies the zero-based relative position of the menu item that opens the drop-down menu or submenu.</span></span>

<span data-ttu-id="01846-112">Le mot de poids fort indique si le menu déroulant est le menu fenêtre.</span><span class="sxs-lookup"><span data-stu-id="01846-112">The high-order word indicates whether the drop-down menu is the window menu.</span></span> <span data-ttu-id="01846-113">Si le menu est le menu fenêtre, ce paramètre a la **valeur true**; Sinon, la **valeur est false**.</span><span class="sxs-lookup"><span data-stu-id="01846-113">If the menu is the window menu, this parameter is **TRUE**; otherwise, it is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01846-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="01846-114">Return value</span></span>

<span data-ttu-id="01846-115">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="01846-115">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="01846-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01846-116">Requirements</span></span>



| <span data-ttu-id="01846-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01846-117">Requirement</span></span> | <span data-ttu-id="01846-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="01846-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="01846-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01846-119">Minimum supported client</span></span><br/> | <span data-ttu-id="01846-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01846-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="01846-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01846-121">Minimum supported server</span></span><br/> | <span data-ttu-id="01846-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01846-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="01846-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="01846-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="01846-124"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="01846-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




