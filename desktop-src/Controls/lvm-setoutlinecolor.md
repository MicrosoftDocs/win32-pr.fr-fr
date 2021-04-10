---
title: Message LVM_SETOUTLINECOLOR (commctrl. h)
description: Définit la couleur de la bordure d’un contrôle d’affichage de liste si le \_ \_ style de fenêtre étendue LVS ex BORDERSELECT est défini.
ms.assetid: c2b606fa-8d47-4192-94b7-d01c3cfdc514
keywords:
- LVM_SETOUTLINECOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 776cb13479e4d091d394941844691c117a4ebbef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843090"
---
# <a name="lvm_setoutlinecolor-message"></a><span data-ttu-id="06e76-104">\_Message SETOUTLINECOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="06e76-104">LVM\_SETOUTLINECOLOR message</span></span>

<span data-ttu-id="06e76-105">Définit la couleur de la bordure d’un contrôle d’affichage de liste si le style de fenêtre étendue [**LVS \_ ex \_ BORDERSELECT**](extended-list-view-styles.md) est défini.</span><span class="sxs-lookup"><span data-stu-id="06e76-105">Sets the color of the border of a list-view control if the [**LVS\_EX\_BORDERSELECT**](extended-list-view-styles.md) extended window style is set.</span></span>

## <a name="parameters"></a><span data-ttu-id="06e76-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06e76-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06e76-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="06e76-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="06e76-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="06e76-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="06e76-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="06e76-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="06e76-110">**COLORREF** , structure qui spécifie la couleur de définition de la bordure.</span><span class="sxs-lookup"><span data-stu-id="06e76-110">**COLORREF** structure that specifies the color to set the border.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06e76-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="06e76-111">Return value</span></span>

<span data-ttu-id="06e76-112">Retourne la structure **COLORREF** qui contient la couleur de contour.</span><span class="sxs-lookup"><span data-stu-id="06e76-112">Returns **COLORREF** structure that contains the outline color.</span></span>

## <a name="remarks"></a><span data-ttu-id="06e76-113">Notes</span><span class="sxs-lookup"><span data-stu-id="06e76-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="06e76-114">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="06e76-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="06e76-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="06e76-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="06e76-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06e76-116">Requirements</span></span>



| <span data-ttu-id="06e76-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06e76-117">Requirement</span></span> | <span data-ttu-id="06e76-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="06e76-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06e76-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06e76-119">Minimum supported client</span></span><br/> | <span data-ttu-id="06e76-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06e76-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="06e76-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06e76-121">Minimum supported server</span></span><br/> | <span data-ttu-id="06e76-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06e76-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="06e76-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="06e76-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="06e76-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="06e76-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





