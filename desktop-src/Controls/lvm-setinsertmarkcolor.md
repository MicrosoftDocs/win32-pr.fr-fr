---
title: Message LVM_SETINSERTMARKCOLOR (commctrl. h)
description: Définit la couleur du point d’insertion.
ms.assetid: dce2c266-672b-4682-ba23-51d9a8e1102b
keywords:
- LVM_SETINSERTMARKCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260d21d083e2c70d8e82a27628e42596bd1b37eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941669"
---
# <a name="lvm_setinsertmarkcolor-message"></a><span data-ttu-id="a716c-104">\_Message SETINSERTMARKCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="a716c-104">LVM\_SETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="a716c-105">Définit la couleur du point d’insertion.</span><span class="sxs-lookup"><span data-stu-id="a716c-105">Sets the color of the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="a716c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a716c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a716c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a716c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a716c-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="a716c-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a716c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a716c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a716c-110">**COLORREF** , structure qui spécifie la couleur de définition du point d’insertion.</span><span class="sxs-lookup"><span data-stu-id="a716c-110">**COLORREF** structure that specifies the color to set the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a716c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a716c-111">Return value</span></span>

<span data-ttu-id="a716c-112">Retourne la structure **COLORREF** définie sur la couleur précédente.</span><span class="sxs-lookup"><span data-stu-id="a716c-112">Returns **COLORREF** structure set to the previous color.</span></span>

## <a name="remarks"></a><span data-ttu-id="a716c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a716c-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a716c-114">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="a716c-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="a716c-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a716c-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a716c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a716c-116">Requirements</span></span>



| <span data-ttu-id="a716c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a716c-117">Requirement</span></span> | <span data-ttu-id="a716c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a716c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a716c-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a716c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a716c-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a716c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a716c-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a716c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a716c-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a716c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a716c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="a716c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a716c-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a716c-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





