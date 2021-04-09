---
title: Message CCM_SETVERSION (commctrl. h)
description: Ce message est utilisé pour informer le contrôle que vous attendez un comportement associé à une version particulière.
ms.assetid: f87b20bc-0139-4d0a-b38c-32c75743d6f6
keywords:
- CCM_SETVERSION les contrôles de message Windows
topic_type:
- apiref
api_name:
- CCM_SETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 349935173c41cd9c90a016ef3d2f3c77df8f159c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033022"
---
# <a name="ccm_setversion-message"></a><span data-ttu-id="f5173-104">\_Message CCM SETVERSION</span><span class="sxs-lookup"><span data-stu-id="f5173-104">CCM\_SETVERSION message</span></span>

<span data-ttu-id="f5173-105">Ce message est utilisé pour informer le contrôle que vous attendez un comportement associé à une version particulière.</span><span class="sxs-lookup"><span data-stu-id="f5173-105">This message is used to inform the control that you are expecting a behavior associated with a particular version.</span></span>

## <a name="parameters"></a><span data-ttu-id="f5173-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5173-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5173-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f5173-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5173-108">Numéro de version.</span><span class="sxs-lookup"><span data-stu-id="f5173-108">The version number.</span></span>

</dd> <dt>

<span data-ttu-id="f5173-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5173-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f5173-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="f5173-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5173-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f5173-111">Return value</span></span>

<span data-ttu-id="f5173-112">Retourne la version spécifiée dans le message **\_ SETVERSION CCM** précédent.</span><span class="sxs-lookup"><span data-stu-id="f5173-112">Returns the version specified in the previous **CCM\_SETVERSION** message.</span></span> <span data-ttu-id="f5173-113">Si *wParam* est défini sur une valeur supérieure à la version actuelle de la dll, la valeur-1 est retournée.</span><span class="sxs-lookup"><span data-stu-id="f5173-113">If *wParam* is set to a value greater than the current DLL version, it returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5173-114">Notes</span><span class="sxs-lookup"><span data-stu-id="f5173-114">Remarks</span></span>

<span data-ttu-id="f5173-115">Dans certains cas, un contrôle peut se comporter différemment, selon la version.</span><span class="sxs-lookup"><span data-stu-id="f5173-115">In a few cases, a control may behave differently, depending on the version.</span></span> <span data-ttu-id="f5173-116">Cela s’applique principalement aux bogues qui ont été résolus dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f5173-116">This primarily applies to bugs that were fixed in later versions.</span></span> <span data-ttu-id="f5173-117">Le message **CCM \_ SETVERSION** vous permet d’informer le contrôle du comportement attendu.</span><span class="sxs-lookup"><span data-stu-id="f5173-117">The **CCM\_SETVERSION** message enables you to inform the control which behavior is expected.</span></span> <span data-ttu-id="f5173-118">Vous pouvez déterminer la version que vous avez spécifiée en envoyant un message [**CCM \_ GETVERSION**](ccm-getversion.md) .</span><span class="sxs-lookup"><span data-stu-id="f5173-118">You can determine which version you have specified by sending a [**CCM\_GETVERSION**](ccm-getversion.md) message.</span></span> <span data-ttu-id="f5173-119">Pour obtenir un exemple d’utilisation de ce message, consultez [dessin personnalisé avec les contrôles List-View et Tree-View](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="f5173-119">For an example of how to use this message, see [Custom Draw With List-View and Tree-View Controls](custom-draw.md).</span></span>

<span data-ttu-id="f5173-120">Si vous avez ComCtl32.dll version 6 installée, quelle que soit la valeur que vous avez définie dans *wParam*, le message **CCM \_ SETVERSION** retourne la version 6.</span><span class="sxs-lookup"><span data-stu-id="f5173-120">If you have ComCtl32.dll version 6 installed, regardless of what value you set in *wParam*, the **CCM\_SETVERSION** message returns version 6.</span></span>

> [!Note]  
> <span data-ttu-id="f5173-121">Ce message définit uniquement le numéro de version du contrôle auquel il est envoyé.</span><span class="sxs-lookup"><span data-stu-id="f5173-121">This message only sets the version number for the control to which it is sent.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f5173-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5173-122">Requirements</span></span>



| <span data-ttu-id="f5173-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5173-123">Requirement</span></span> | <span data-ttu-id="f5173-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5173-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5173-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5173-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f5173-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5173-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f5173-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5173-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f5173-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5173-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f5173-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5173-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5173-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5173-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





