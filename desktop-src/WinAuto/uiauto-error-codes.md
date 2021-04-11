---
title: Codes d’erreur (UIAutomationCoreApi. h)
description: Cette rubrique décrit les codes d’erreur exposés par Microsoft UI Automation.
ms.assetid: f7820aa3-908e-426e-851c-84397019d735
topic_type:
- apiref
api_name:
- UIA_E_ELEMENTNOTAVAILABLE
- UIA_E_ELEMENTNOTENABLED
- UIA_E_INVALIDOPERATION
- UIA_E_NOCLICKABLEPOINT
- UIA_E_NOTSUPPORTED
- UIA_E_PROXYASSEMBLYNOTLOADED
- UIA_E_TIMEOUT
api_location:
- UIAutomationCoreApi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baaa03746bfb1a5e56fcac8b39d326581159f459
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032284"
---
# <a name="error-codes-uiautomationcoreapih"></a><span data-ttu-id="3e481-103">Codes d’erreur (UIAutomationCoreApi. h)</span><span class="sxs-lookup"><span data-stu-id="3e481-103">Error Codes (UIAutomationCoreApi.h)</span></span>

<span data-ttu-id="3e481-104">Cette rubrique décrit les codes d’erreur exposés par Microsoft UI Automation.</span><span class="sxs-lookup"><span data-stu-id="3e481-104">This topic describes the error codes exposed by Microsoft UI Automation.</span></span> <span data-ttu-id="3e481-105">La liste est triée par ordre alphabétique par nom.</span><span class="sxs-lookup"><span data-stu-id="3e481-105">The list is sorted alphabetically by name.</span></span>



| <span data-ttu-id="3e481-106">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="3e481-106">Constant/value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="3e481-107">Description</span><span class="sxs-lookup"><span data-stu-id="3e481-107">Description</span></span>                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIA_E_ELEMENTNOTAVAILABLE"></span><span id="uia_e_elementnotavailable"></span><dl> <span data-ttu-id="3e481-108"><dt>**UIA \_ \_ELEMENTNOTAVAILABLE**</dt> <dt>0x80040201</dt></span><span class="sxs-lookup"><span data-stu-id="3e481-108"><dt>**UIA\_E\_ELEMENTNOTAVAILABLE**</dt> <dt>0x80040201</dt></span></span> </dl>          | <span data-ttu-id="3e481-109">Indique qu’une méthode a été appelée sur un élément virtualisé, ou sur un élément qui n’existe plus, généralement parce qu’elle a été détruite.</span><span class="sxs-lookup"><span data-stu-id="3e481-109">Indicates that a method was called on a virtualized element, or on an element that no longer exists, usually because it has been destroyed.</span></span> <br/>                                                                                                  |
| <span id="UIA_E_ELEMENTNOTENABLED"></span><span id="uia_e_elementnotenabled"></span><dl> <span data-ttu-id="3e481-110"><dt>**UIA \_ \_ELEMENTNOTENABLED**</dt> <dt>0x80040200</dt></span><span class="sxs-lookup"><span data-stu-id="3e481-110"><dt>**UIA\_E\_ELEMENTNOTENABLED**</dt> <dt>0x80040200</dt></span></span> </dl>                | <span data-ttu-id="3e481-111">Indique qu’une méthode qui requiert un élément activé, tel que [**Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select) ou [**expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand), a été appelée sur un élément qui a été désactivé.</span><span class="sxs-lookup"><span data-stu-id="3e481-111">Indicates that a method that requires an enabled element, such as [**Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select) or [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand), was called on an element that was disabled.</span></span> <br/>             |
| <span id="UIA_E_INVALIDOPERATION"></span><span id="uia_e_invalidoperation"></span><dl> <span data-ttu-id="3e481-112"><dt>**UIA \_ E \_ INVALIDOPERATION**</dt> <dt>0x80131509</dt></span><span class="sxs-lookup"><span data-stu-id="3e481-112"><dt>**UIA\_E\_INVALIDOPERATION**</dt> <dt>0x80131509</dt></span></span> </dl>                   | <span data-ttu-id="3e481-113">Indique que la méthode a tenté une opération qui n’était pas valide.</span><span class="sxs-lookup"><span data-stu-id="3e481-113">Indicates that the method attempted an operation that was not valid.</span></span><br/>                                                                                                                                                                          |
| <span id="UIA_E_NOCLICKABLEPOINT"></span><span id="uia_e_noclickablepoint"></span><dl> <span data-ttu-id="3e481-114"><dt>**UIA \_ \_NOCLICKABLEPOINT**</dt> <dt>0x80040202</dt></span><span class="sxs-lookup"><span data-stu-id="3e481-114"><dt>**UIA\_E\_NOCLICKABLEPOINT**</dt> <dt>0x80040202</dt></span></span> </dl>                   | <span data-ttu-id="3e481-115">Indique que la méthode [**GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint) a été appelée sur un élément qui n’a pas de point cliquable.</span><span class="sxs-lookup"><span data-stu-id="3e481-115">Indicates that the [**GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint) method was called on an element that has no clickable point.</span></span><br/>                                                                                    |
| <span id="UIA_E_NOTSUPPORTED"></span><span id="uia_e_notsupported"></span><dl> <span data-ttu-id="3e481-116"><dt>**UIA \_ \_NOTSUPPORTED**</dt> <dt>0x80040204</dt></span><span class="sxs-lookup"><span data-stu-id="3e481-116"><dt>**UIA\_E\_NOTSUPPORTED**</dt> <dt>0x80040204</dt></span></span> </dl>                               | <span data-ttu-id="3e481-117">Indique que le fournisseur ne prend pas en charge explicitement la propriété ou le modèle de contrôle spécifié.</span><span class="sxs-lookup"><span data-stu-id="3e481-117">Indicates that the provider explicitly does not support the specified property or control pattern.</span></span> <span data-ttu-id="3e481-118">UI Automation renverra ce code d’erreur à l’appelant sans tenter de fournir une valeur par défaut ou de revenir à un autre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3e481-118">UI Automation will return this error code to the caller without attempting to provide a default value or falling back to another provider.</span></span><br/> |
| <span id="UIA_E_PROXYASSEMBLYNOTLOADED"></span><span id="uia_e_proxyassemblynotloaded"></span><dl> <span data-ttu-id="3e481-119"><dt>**UIA \_ \_PROXYASSEMBLYNOTLOADED**</dt> <dt>0x80040203</dt></span><span class="sxs-lookup"><span data-stu-id="3e481-119"><dt>**UIA\_E\_PROXYASSEMBLYNOTLOADED**</dt> <dt>0x80040203</dt></span></span> </dl> | <span data-ttu-id="3e481-120">Indique qu’un problème s’est produit lors du chargement d’un assembly qui contient un fournisseur côté client (proxy).</span><span class="sxs-lookup"><span data-stu-id="3e481-120">Indicates that a problem occurred when loading an assembly that contains a client-side (proxy) provider.</span></span><br/>                                                                                                                                      |
| <span id="UIA_E_TIMEOUT"></span><span id="uia_e_timeout"></span><dl> <span data-ttu-id="3e481-121"><dt>**UIA \_ \_Délai d’expiration E**</dt> <dt>0x80131505</dt></span><span class="sxs-lookup"><span data-stu-id="3e481-121"><dt>**UIA\_E\_TIMEOUT**</dt> <dt>0x80131505</dt></span></span> </dl>                                                      | <span data-ttu-id="3e481-122">Indique que le temps alloué à un processus ou une opération a expiré.</span><span class="sxs-lookup"><span data-stu-id="3e481-122">Indicates that the time allotted for a process or operation has expired.</span></span><br/>                                                                                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="3e481-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e481-123">Requirements</span></span>



| <span data-ttu-id="3e481-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e481-124">Requirement</span></span> | <span data-ttu-id="3e481-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e481-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e481-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e481-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3e481-127">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e481-127">Windows XP \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3e481-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e481-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3e481-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e481-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3e481-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e481-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e481-131"><dt>UIAutomationCoreApi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e481-131"><dt>UIAutomationCoreApi.h</dt></span></span> </dl> |



 

 





