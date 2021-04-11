---
title: Message LVM_GETVIEW (commctrl. h)
description: Récupère la vue actuelle d’un contrôle List-View.
ms.assetid: dd63e726-3a7f-40e7-8d46-4680816c02a3
keywords:
- LVM_GETVIEW les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2da295fa5a5b335de60169ce06b777d9e355121
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105484"
---
# <a name="lvm_getview-message"></a><span data-ttu-id="00a05-104">\_Message GETVIEW LVM</span><span class="sxs-lookup"><span data-stu-id="00a05-104">LVM\_GETVIEW message</span></span>

<span data-ttu-id="00a05-105">Récupère la vue actuelle d’un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="00a05-105">Retrieves the current view of a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="00a05-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00a05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00a05-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="00a05-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="00a05-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="00a05-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="00a05-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="00a05-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="00a05-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="00a05-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00a05-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="00a05-111">Return value</span></span>

<span data-ttu-id="00a05-112">Retourne une **valeur DWORD** qui spécifie la vue actuelle.</span><span class="sxs-lookup"><span data-stu-id="00a05-112">Returns a **DWORD** that specifies the current view.</span></span>

## <a name="remarks"></a><span data-ttu-id="00a05-113">Notes</span><span class="sxs-lookup"><span data-stu-id="00a05-113">Remarks</span></span>

<span data-ttu-id="00a05-114">Voici les valeurs des vues.</span><span class="sxs-lookup"><span data-stu-id="00a05-114">Following are the values for views.</span></span>

-   <span data-ttu-id="00a05-115">Détails de la \_ vue LV \_</span><span class="sxs-lookup"><span data-stu-id="00a05-115">LV\_VIEW\_DETAILS</span></span>
-   <span data-ttu-id="00a05-116">\_icône de vue LV \_</span><span class="sxs-lookup"><span data-stu-id="00a05-116">LV\_VIEW\_ICON</span></span>
-   <span data-ttu-id="00a05-117">\_liste d’affichages LV \_</span><span class="sxs-lookup"><span data-stu-id="00a05-117">LV\_VIEW\_LIST</span></span>
-   <span data-ttu-id="00a05-118">LV \_ vue \_ SmallIcon</span><span class="sxs-lookup"><span data-stu-id="00a05-118">LV\_VIEW\_SMALLICON</span></span>
-   <span data-ttu-id="00a05-119">vignette de la \_ vue LV \_</span><span class="sxs-lookup"><span data-stu-id="00a05-119">LV\_VIEW\_TILE</span></span>

> [!Note]  
> <span data-ttu-id="00a05-120">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="00a05-120">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="00a05-121">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="00a05-121">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="00a05-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00a05-122">Requirements</span></span>



| <span data-ttu-id="00a05-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00a05-123">Requirement</span></span> | <span data-ttu-id="00a05-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="00a05-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="00a05-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00a05-125">Minimum supported client</span></span><br/> | <span data-ttu-id="00a05-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="00a05-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="00a05-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00a05-127">Minimum supported server</span></span><br/> | <span data-ttu-id="00a05-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="00a05-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="00a05-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="00a05-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="00a05-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="00a05-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





