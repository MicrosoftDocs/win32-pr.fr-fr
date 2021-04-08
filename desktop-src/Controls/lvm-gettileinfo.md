---
title: Message LVM_GETTILEINFO (commctrl. h)
description: Récupère des informations sur une vignette dans un contrôle List-View.
ms.assetid: e89a3eae-0970-488c-ba95-1072aa85bbf4
keywords:
- LVM_GETTILEINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETTILEINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db5bfd085cd5cbaced0bf90b17e8862a6c0e159b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033139"
---
# <a name="lvm_gettileinfo-message"></a><span data-ttu-id="90ba7-104">\_Message GETTILEINFO LVM</span><span class="sxs-lookup"><span data-stu-id="90ba7-104">LVM\_GETTILEINFO message</span></span>

<span data-ttu-id="90ba7-105">Récupère des informations sur une vignette dans un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="90ba7-105">Retrieves information about a tile in a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="90ba7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="90ba7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90ba7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="90ba7-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="90ba7-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="90ba7-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="90ba7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="90ba7-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="90ba7-110">Pointeur vers une structure <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a> qui reçoit les informations récupérées.</span><span class="sxs-lookup"><span data-stu-id="90ba7-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a> structure that receives the retrieved information.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90ba7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="90ba7-111">Return value</span></span>

<span data-ttu-id="90ba7-112">Valeur de retour non utilisée.</span><span class="sxs-lookup"><span data-stu-id="90ba7-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="90ba7-113">Notes</span><span class="sxs-lookup"><span data-stu-id="90ba7-113">Remarks</span></span>

<span data-ttu-id="90ba7-114">L’affichage en mosaïque est une nouvelle façon d’organiser et d’afficher des éléments dans un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="90ba7-114">Tile view is a new way of arranging and displaying items in a list-view control.</span></span> <span data-ttu-id="90ba7-115">Les autres vues sont icône, petite icône, détails et liste.</span><span class="sxs-lookup"><span data-stu-id="90ba7-115">The other views are icon, small icon, details, and list.</span></span>

> [!Note]  
> <span data-ttu-id="90ba7-116">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="90ba7-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="90ba7-117">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="90ba7-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="90ba7-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90ba7-118">Requirements</span></span>



| <span data-ttu-id="90ba7-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="90ba7-119">Requirement</span></span> | <span data-ttu-id="90ba7-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="90ba7-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90ba7-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90ba7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="90ba7-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="90ba7-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="90ba7-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90ba7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="90ba7-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="90ba7-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="90ba7-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="90ba7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="90ba7-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="90ba7-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





