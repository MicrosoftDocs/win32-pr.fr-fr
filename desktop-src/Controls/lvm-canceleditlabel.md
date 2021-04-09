---
title: Message LVM_CANCELEDITLABEL (commctrl. h)
description: Annule une opération de modification de texte d’un élément.
ms.assetid: 73e9c922-3223-4c49-a33c-df7c09443ccc
keywords:
- LVM_CANCELEDITLABEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_CANCELEDITLABEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edfed26fb3c38d91f7a5b07683079d29ecd4597d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102908"
---
# <a name="lvm_canceleditlabel-message"></a><span data-ttu-id="d2101-104">\_Message CANCELEDITLABEL LVM</span><span class="sxs-lookup"><span data-stu-id="d2101-104">LVM\_CANCELEDITLABEL message</span></span>

<span data-ttu-id="d2101-105">Annule une opération de modification de texte d’un élément.</span><span class="sxs-lookup"><span data-stu-id="d2101-105">Cancels an item text editing operation.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2101-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2101-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2101-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2101-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d2101-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="d2101-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d2101-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2101-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d2101-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="d2101-110">Must be zero.</span></span></dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2101-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d2101-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d2101-112">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="d2101-112">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="d2101-113">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d2101-113">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

<span data-ttu-id="d2101-114">Ce message entraîne l’envoi d’une notification [ \_ ENDLABELEDIT LVN](lvn-endlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="d2101-114">This message causes a an [LVN\_ENDLABELEDIT](lvn-endlabeledit.md) notification to be sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2101-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2101-115">Requirements</span></span>



| <span data-ttu-id="d2101-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2101-116">Requirement</span></span> | <span data-ttu-id="d2101-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2101-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2101-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2101-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d2101-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2101-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2101-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2101-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d2101-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2101-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2101-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="d2101-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2101-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2101-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





