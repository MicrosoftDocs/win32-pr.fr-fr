---
title: Message DM_POINTERHITTEST
description: Envoyé à une fenêtre, lorsque l’entrée de pointeur est détectée pour la première fois, afin de déterminer la cible d’entrée la plus probable pour la manipulation directe.
ms.assetid: E4CE60F0-0C2A-440A-8F64-B070867A1572
keywords:
- DM_POINTERHITTEST les messages d’entrée du message et les notifications
topic_type:
- apiref
api_name:
- DM_POINTERHITTEST
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 23efab4606f758acfffdd02fa4c53a729f1f4a99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104863"
---
# <a name="dm_pointerhittest-message"></a><span data-ttu-id="f1baf-104">Message DM_POINTERHITTEST</span><span class="sxs-lookup"><span data-stu-id="f1baf-104">DM_POINTERHITTEST message</span></span>

<span data-ttu-id="f1baf-105">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="f1baf-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f1baf-106">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="f1baf-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f1baf-107">Envoyé à une fenêtre, lorsque l’entrée de pointeur est détectée pour la première fois, afin de déterminer la cible d’entrée la plus probable pour la [manipulation directe](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal).</span><span class="sxs-lookup"><span data-stu-id="f1baf-107">Sent to a window, when pointer input is first detected, in order to determine the most probable input target for [Direct Manipulation](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal).</span></span>

> <span data-ttu-id="f1baf-108">\[! Précieuse\]</span><span class="sxs-lookup"><span data-stu-id="f1baf-108">\[!Important\]</span></span>  
> <span data-ttu-id="f1baf-109">Les applications de bureau doivent prendre en charge DPI.</span><span class="sxs-lookup"><span data-stu-id="f1baf-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="f1baf-110">Si votre application n’a pas de prise en charge DPI, les coordonnées d’écran contenues dans les messages de pointeur et les structures associées peuvent apparaître inexactes en raison de la virtualisation DPI.</span><span class="sxs-lookup"><span data-stu-id="f1baf-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="f1baf-111">La virtualisation PPP offre une prise en charge de la mise à l’échelle automatique aux applications qui ne prennent pas en charge la fonction PPP et est active par défaut (les utilisateurs peuvent la désactiver).</span><span class="sxs-lookup"><span data-stu-id="f1baf-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="f1baf-112">Pour plus d’informations, consultez [écriture d’applications Win32 à haute résolution](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f1baf-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define DM_POINTERHITTEST       0x0250
```



## <a name="parameters"></a><span data-ttu-id="f1baf-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1baf-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1baf-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f1baf-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1baf-115">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="f1baf-115">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="f1baf-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f1baf-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1baf-117">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="f1baf-117">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1baf-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f1baf-118">Return value</span></span>

<span data-ttu-id="f1baf-119">NULL</span><span class="sxs-lookup"><span data-stu-id="f1baf-119">NULL</span></span>

## <a name="requirements"></a><span data-ttu-id="f1baf-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1baf-120">Requirements</span></span>



| <span data-ttu-id="f1baf-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1baf-121">Requirement</span></span> | <span data-ttu-id="f1baf-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1baf-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1baf-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1baf-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f1baf-124">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1baf-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f1baf-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1baf-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f1baf-126">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1baf-126">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f1baf-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="f1baf-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1baf-128"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1baf-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1baf-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1baf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1baf-130">Messages</span><span class="sxs-lookup"><span data-stu-id="f1baf-130">Messages</span></span>](messages.md)
</dt> </dl>

 

