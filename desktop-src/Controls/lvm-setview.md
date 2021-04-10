---
title: Message LVM_SETVIEW (commctrl. h)
description: Définit l’affichage d’un contrôle List-View.
ms.assetid: e6d3f16d-52ea-4863-a6c9-9a085d5f794a
keywords:
- LVM_SETVIEW les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a159710b3086bcba5298a5a88f9cab15f76e0d89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105463"
---
# <a name="lvm_setview-message"></a><span data-ttu-id="9ebff-104">\_Message SETVIEW LVM</span><span class="sxs-lookup"><span data-stu-id="9ebff-104">LVM\_SETVIEW message</span></span>

<span data-ttu-id="9ebff-105">Définit l’affichage d’un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="9ebff-105">Sets the view of a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9ebff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ebff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ebff-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9ebff-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9ebff-108">**Valeur DWORD** qui spécifie la vue.</span><span class="sxs-lookup"><span data-stu-id="9ebff-108">**DWORD** that specifies the view.</span></span></dd> <dt>

<span data-ttu-id="9ebff-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ebff-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9ebff-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="9ebff-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ebff-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9ebff-111">Return value</span></span>

<span data-ttu-id="9ebff-112">Retourne 1 en cas de réussite, ou-1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="9ebff-112">Returns 1 if successful, or -1 otherwise.</span></span> <span data-ttu-id="9ebff-113">Par exemple,-1 est retourné si la vue n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="9ebff-113">For example, -1 is returned if the view is invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ebff-114">Notes</span><span class="sxs-lookup"><span data-stu-id="9ebff-114">Remarks</span></span>

<span data-ttu-id="9ebff-115">Voici les valeurs des vues.</span><span class="sxs-lookup"><span data-stu-id="9ebff-115">Following are the values for views.</span></span>

-   <span data-ttu-id="9ebff-116">Détails de la \_ vue LV \_</span><span class="sxs-lookup"><span data-stu-id="9ebff-116">LV\_VIEW\_DETAILS</span></span>
-   <span data-ttu-id="9ebff-117">\_icône de vue LV \_</span><span class="sxs-lookup"><span data-stu-id="9ebff-117">LV\_VIEW\_ICON</span></span>
-   <span data-ttu-id="9ebff-118">\_liste d’affichages LV \_</span><span class="sxs-lookup"><span data-stu-id="9ebff-118">LV\_VIEW\_LIST</span></span>
-   <span data-ttu-id="9ebff-119">LV \_ vue \_ SmallIcon</span><span class="sxs-lookup"><span data-stu-id="9ebff-119">LV\_VIEW\_SMALLICON</span></span>
-   <span data-ttu-id="9ebff-120">vignette de la \_ vue LV \_</span><span class="sxs-lookup"><span data-stu-id="9ebff-120">LV\_VIEW\_TILE</span></span>

> [!Note]  
> <span data-ttu-id="9ebff-121">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comctl32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="9ebff-121">To use this message, you must provide a manifest specifying Comctl32.dll version 6.0.</span></span> <span data-ttu-id="9ebff-122">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9ebff-122">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9ebff-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ebff-123">Requirements</span></span>



| <span data-ttu-id="9ebff-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ebff-124">Requirement</span></span> | <span data-ttu-id="9ebff-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ebff-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ebff-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ebff-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9ebff-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9ebff-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9ebff-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ebff-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9ebff-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9ebff-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9ebff-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="9ebff-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ebff-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ebff-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





