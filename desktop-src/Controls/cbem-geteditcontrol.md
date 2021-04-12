---
title: Message CBEM_GETEDITCONTROL (commctrl. h)
description: Obtient le handle vers la partie du contrôle d’édition d’un contrôle ComboBoxEx. Un contrôle ComboBoxEx utilise une zone d’édition quand il est défini sur le \_ style de liste déroulante CBS.
ms.assetid: def91949-cadc-4297-a504-0680d7d9b815
keywords:
- CBEM_GETEDITCONTROL les contrôles de message Windows
topic_type:
- apiref
api_name:
- CBEM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 412d1183b29c8c89b5977d5f7f2a1b962d54dc01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105598"
---
# <a name="cbem_geteditcontrol-message"></a><span data-ttu-id="1b4bd-105">\_Message CBEM GETEDITCONTROL</span><span class="sxs-lookup"><span data-stu-id="1b4bd-105">CBEM\_GETEDITCONTROL message</span></span>

<span data-ttu-id="1b4bd-106">Obtient le handle vers la partie du contrôle d’édition d’un contrôle ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="1b4bd-106">Gets the handle to the edit control portion of a ComboBoxEx control.</span></span> <span data-ttu-id="1b4bd-107">Un contrôle ComboBoxEx utilise une zone d’édition quand il est défini sur le style de [**\_ liste déroulante CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="1b4bd-107">A ComboBoxEx control uses an edit box when it is set to the [**CBS\_DROPDOWN**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="1b4bd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b4bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b4bd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b4bd-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1b4bd-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="1b4bd-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1b4bd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b4bd-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1b4bd-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="1b4bd-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b4bd-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1b4bd-113">Return value</span></span>

<span data-ttu-id="1b4bd-114">Retourne le handle du contrôle d’édition dans le contrôle ComboBoxEx s’il utilise le style de [**\_ liste déroulante CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="1b4bd-114">Returns the handle to the edit control within the ComboBoxEx control if it uses the [**CBS\_DROPDOWN**](combo-box-styles.md) style.</span></span> <span data-ttu-id="1b4bd-115">Dans le cas contraire, le message retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="1b4bd-115">Otherwise, the message returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b4bd-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b4bd-116">Requirements</span></span>



| <span data-ttu-id="1b4bd-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b4bd-117">Requirement</span></span> | <span data-ttu-id="1b4bd-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b4bd-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b4bd-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b4bd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1b4bd-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b4bd-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b4bd-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b4bd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1b4bd-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b4bd-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b4bd-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="1b4bd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b4bd-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b4bd-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





