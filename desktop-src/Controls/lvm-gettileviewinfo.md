---
title: Message LVM_GETTILEVIEWINFO (commctrl. h)
description: Récupère des informations sur un contrôle d’affichage de liste en mode mosaïque.
ms.assetid: 114990c0-a150-49d8-80e7-b084c648ac34
keywords:
- LVM_GETTILEVIEWINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETTILEVIEWINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe1f34da560d539a9ae12cc7a065b2bf37bc3c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742981"
---
# <a name="lvm_gettileviewinfo-message"></a><span data-ttu-id="198a6-104">\_Message GETTILEVIEWINFO LVM</span><span class="sxs-lookup"><span data-stu-id="198a6-104">LVM\_GETTILEVIEWINFO message</span></span>

<span data-ttu-id="198a6-105">Récupère des informations sur un contrôle d’affichage de liste en mode mosaïque.</span><span class="sxs-lookup"><span data-stu-id="198a6-105">Retrieves information about a list-view control in tile view.</span></span>

## <a name="parameters"></a><span data-ttu-id="198a6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="198a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="198a6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="198a6-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="198a6-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="198a6-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="198a6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="198a6-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="198a6-110">Pointeur vers une structure <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a> qui reçoit les informations récupérées.</span><span class="sxs-lookup"><span data-stu-id="198a6-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a> structure that receives the retrieved information.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="198a6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="198a6-111">Return value</span></span>

<span data-ttu-id="198a6-112">Valeur de retour non utilisée.</span><span class="sxs-lookup"><span data-stu-id="198a6-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="198a6-113">Notes</span><span class="sxs-lookup"><span data-stu-id="198a6-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="198a6-114">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="198a6-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="198a6-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="198a6-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="198a6-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="198a6-116">Requirements</span></span>



| <span data-ttu-id="198a6-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="198a6-117">Requirement</span></span> | <span data-ttu-id="198a6-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="198a6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="198a6-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="198a6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="198a6-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="198a6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="198a6-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="198a6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="198a6-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="198a6-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="198a6-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="198a6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="198a6-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="198a6-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





