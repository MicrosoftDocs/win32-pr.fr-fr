---
title: Constantes TF_LBMENUF_ (Ctfutb. h)
description: Les \_ \_ constantes TF LBMENUF \ sont utilisées dans la méthode ITfMenu AddMenuItem pour spécifier les caractéristiques d’un élément de menu dans la barre de langue.
ms.assetid: f8f3f397-b84e-4635-b454-31369c679ce2
topic_type:
- apiref
api_name:
- TF_LBMENUF_CHECKED
- TF_LBMENUF_SUBMENU
- TF_LBMENUF_SEPARATOR
- TF_LBMENUF_RADIOCHECKED
- TF_LBMENUF_GRAYED
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a056e9a758419965341b4d508db083fc8f31b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942082"
---
# <a name="tf_lbmenuf_-constants"></a><span data-ttu-id="e0f9c-103">TF \_ LBMENUF, \_ \* constantes</span><span class="sxs-lookup"><span data-stu-id="e0f9c-103">TF\_LBMENUF\_\* Constants</span></span>

<span data-ttu-id="e0f9c-104">Les constantes \**tf \_ LBMENUF \_ \** _ sont utilisées dans la méthode [ITfMenu :: AddMenuItem](/windows/desktop/api/Ctfutb/nf-ctfutb-itfmenu-addmenuitem) pour spécifier les caractéristiques d’un élément de menu dans la barre de langue.</span><span class="sxs-lookup"><span data-stu-id="e0f9c-104">The \**TF\_LBMENUF\_\** _ constants are used in the [ITfMenu::AddMenuItem](/windows/desktop/api/Ctfutb/nf-ctfutb-itfmenu-addmenuitem) method to specify the characteristics of a menu item in the language bar.</span></span>



| <span data-ttu-id="e0f9c-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="e0f9c-105">Constant/value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="e0f9c-106">Description</span><span class="sxs-lookup"><span data-stu-id="e0f9c-106">Description</span></span>                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------|
| <span id="TF_LBMENUF_CHECKED"></span><span id="tf_lbmenuf_checked"></span><dl> <span data-ttu-id="e0f9c-107"><dt>_ \* TF \_ LBMENUF \_ activé \* \*</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="e0f9c-107"><dt>_\*TF\_LBMENUF\_CHECKED\*\*</dt> <dt>0x01</dt></span></span> </dl>                | <span data-ttu-id="e0f9c-108">L’élément de menu est activé.</span><span class="sxs-lookup"><span data-stu-id="e0f9c-108">The menu item is checked.</span></span><br/>            |
| <span id="TF_LBMENUF_SUBMENU"></span><span id="tf_lbmenuf_submenu"></span><dl> <span data-ttu-id="e0f9c-109"><dt>**Tf \_ \_Sous-menu LBMENUF**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="e0f9c-109"><dt>**TF\_LBMENUF\_SUBMENU**</dt> <dt>0x02</dt></span></span> </dl>                | <span data-ttu-id="e0f9c-110">L’élément de menu est un sous-menu.</span><span class="sxs-lookup"><span data-stu-id="e0f9c-110">The menu item is a submenu.</span></span><br/>          |
| <span id="TF_LBMENUF_SEPARATOR"></span><span id="tf_lbmenuf_separator"></span><dl> <span data-ttu-id="e0f9c-111"><dt>**Tf \_ LBMENUF \_ separator**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="e0f9c-111"><dt>**TF\_LBMENUF\_SEPARATOR**</dt> <dt>0x04</dt></span></span> </dl>          | <span data-ttu-id="e0f9c-112">L’élément de menu est un séparateur.</span><span class="sxs-lookup"><span data-stu-id="e0f9c-112">The menu item is a separator.</span></span><br/>        |
| <span id="TF_LBMENUF_RADIOCHECKED"></span><span id="tf_lbmenuf_radiochecked"></span><dl> <span data-ttu-id="e0f9c-113"><dt>**Tf \_ LBMENUF de \_ radiovérification**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="e0f9c-113"><dt>**TF\_LBMENUF\_RADIOCHECKED**</dt> <dt>0x08</dt></span></span> </dl> | <span data-ttu-id="e0f9c-114">L’élément de menu est une coche radio.</span><span class="sxs-lookup"><span data-stu-id="e0f9c-114">The menu item is a radio check mark.</span></span><br/> |
| <span id="TF_LBMENUF_GRAYED"></span><span id="tf_lbmenuf_grayed"></span><dl> <span data-ttu-id="e0f9c-115"><dt>**Tf \_ LBMENUF en \_ grisé**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e0f9c-115"><dt>**TF\_LBMENUF\_GRAYED**</dt> <dt>0x10</dt></span></span> </dl>                   | <span data-ttu-id="e0f9c-116">L’élément de menu est désactivé.</span><span class="sxs-lookup"><span data-stu-id="e0f9c-116">The menu item is disabled.</span></span><br/>           |



## <a name="requirements"></a><span data-ttu-id="e0f9c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0f9c-117">Requirements</span></span>



| <span data-ttu-id="e0f9c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0f9c-118">Requirement</span></span> | <span data-ttu-id="e0f9c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0f9c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0f9c-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0f9c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e0f9c-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0f9c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e0f9c-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0f9c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e0f9c-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0f9c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e0f9c-124">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="e0f9c-124">Redistributable</span></span><br/>          | <span data-ttu-id="e0f9c-125">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="e0f9c-125">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="e0f9c-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="e0f9c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0f9c-127"><dt>Ctfutb. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0f9c-127"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="e0f9c-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="e0f9c-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e0f9c-129"><dt>Ctfutb. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e0f9c-129"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0f9c-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0f9c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0f9c-131">ITfMenu::AddMenuItem</span><span class="sxs-lookup"><span data-stu-id="e0f9c-131">ITfMenu::AddMenuItem</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itfmenu-addmenuitem)
</dt> </dl>

 

 





