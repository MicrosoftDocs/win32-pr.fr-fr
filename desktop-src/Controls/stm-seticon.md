---
title: Message STM_SETICON (winuser. h)
description: Une application envoie le \_ message STM SETICON pour associer une icône à un contrôle Icon.
ms.assetid: 105b0667-8e23-47ed-9fb1-0792a22d7100
keywords:
- STM_SETICON les contrôles de message Windows
topic_type:
- apiref
api_name:
- STM_SETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9c7e2a007c1f866a1c73b3a1c1a55b157add47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032412"
---
# <a name="stm_seticon-message"></a><span data-ttu-id="bdbcf-104">\_Message SETICON STM</span><span class="sxs-lookup"><span data-stu-id="bdbcf-104">STM\_SETICON message</span></span>

<span data-ttu-id="bdbcf-105">Une application envoie le message **STM \_ SETICON** pour associer une icône à un contrôle Icon.</span><span class="sxs-lookup"><span data-stu-id="bdbcf-105">An application sends the **STM\_SETICON** message to associate an icon with an icon control.</span></span>

## <a name="parameters"></a><span data-ttu-id="bdbcf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bdbcf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdbcf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bdbcf-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdbcf-108">Handle de l’icône à associer au contrôle Icon.</span><span class="sxs-lookup"><span data-stu-id="bdbcf-108">Handle to the icon to associate with the icon control.</span></span>

</dd> <dt>

<span data-ttu-id="bdbcf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bdbcf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdbcf-110">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="bdbcf-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdbcf-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bdbcf-111">Return value</span></span>

<span data-ttu-id="bdbcf-112">La valeur de retour est un handle de l’icône précédemment associée au contrôle Icon, ou zéro si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="bdbcf-112">The return value is a handle to the icon previously associated with the icon control, or zero if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdbcf-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bdbcf-113">Requirements</span></span>



| <span data-ttu-id="bdbcf-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bdbcf-114">Requirement</span></span> | <span data-ttu-id="bdbcf-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdbcf-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdbcf-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bdbcf-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bdbcf-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bdbcf-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bdbcf-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bdbcf-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bdbcf-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bdbcf-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bdbcf-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="bdbcf-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdbcf-121"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bdbcf-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdbcf-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bdbcf-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="bdbcf-123">**Référence**</span><span class="sxs-lookup"><span data-stu-id="bdbcf-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bdbcf-124">**\_GETICON STM**</span><span class="sxs-lookup"><span data-stu-id="bdbcf-124">**STM\_GETICON**</span></span>](stm-geticon.md)
</dt> <dt>

<span data-ttu-id="bdbcf-125">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="bdbcf-125">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="bdbcf-126">**LoadIcon**</span><span class="sxs-lookup"><span data-stu-id="bdbcf-126">**LoadIcon**</span></span>](/windows/desktop/api/winuser/nf-winuser-loadicona)
</dt> </dl>

 

