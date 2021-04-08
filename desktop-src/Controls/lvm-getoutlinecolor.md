---
title: Message LVM_GETOUTLINECOLOR (commctrl. h)
description: Récupère la couleur de la bordure d’un contrôle List View si le \_ \_ style de fenêtre étendue LVS ex BORDERSELECT est défini.
ms.assetid: cc9d69d1-1470-4eaa-8d54-e31b796cf685
keywords:
- LVM_GETOUTLINECOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489f21f2f6d4dcca2c79d92a13a85d7718a85693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844094"
---
# <a name="lvm_getoutlinecolor-message"></a><span data-ttu-id="46137-104">\_Message GETOUTLINECOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="46137-104">LVM\_GETOUTLINECOLOR message</span></span>

<span data-ttu-id="46137-105">Récupère la couleur de la bordure d’un contrôle List View si le style de fenêtre étendue [**LVS \_ ex \_ BORDERSELECT**](extended-list-view-styles.md) est défini.</span><span class="sxs-lookup"><span data-stu-id="46137-105">Retrieves the color of the border of a list-view control if the [**LVS\_EX\_BORDERSELECT**](extended-list-view-styles.md) extended window style is set.</span></span>

## <a name="parameters"></a><span data-ttu-id="46137-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46137-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46137-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="46137-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="46137-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="46137-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="46137-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="46137-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="46137-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="46137-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46137-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="46137-111">Return value</span></span>

<span data-ttu-id="46137-112">Retourne une structure **COLORREF** qui contient la couleur de la bordure d’un contrôle List View.</span><span class="sxs-lookup"><span data-stu-id="46137-112">Returns a **COLORREF** structure that contains the color of the border of a list-view control.</span></span>

## <a name="remarks"></a><span data-ttu-id="46137-113">Notes</span><span class="sxs-lookup"><span data-stu-id="46137-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="46137-114">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="46137-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="46137-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="46137-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="46137-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46137-116">Requirements</span></span>



| <span data-ttu-id="46137-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46137-117">Requirement</span></span> | <span data-ttu-id="46137-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="46137-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46137-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46137-119">Minimum supported client</span></span><br/> | <span data-ttu-id="46137-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46137-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="46137-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46137-121">Minimum supported server</span></span><br/> | <span data-ttu-id="46137-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46137-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="46137-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="46137-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="46137-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="46137-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





