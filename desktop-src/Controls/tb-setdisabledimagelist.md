---
title: Message TB_SETDISABLEDIMAGELIST (commctrl. h)
description: Définit la liste d’images que le contrôle ToolBar utilisera pour afficher les boutons désactivés.
ms.assetid: 1e76b3cf-2d06-48c8-8298-ef6caf3d85c3
keywords:
- TB_SETDISABLEDIMAGELIST les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETDISABLEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7cc8c9ec1fdc9658413da5991fa109e7bef27a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033093"
---
# <a name="tb_setdisabledimagelist-message"></a><span data-ttu-id="69b2c-104">TO \_ SETDISABLEDIMAGELIST message</span><span class="sxs-lookup"><span data-stu-id="69b2c-104">TB\_SETDISABLEDIMAGELIST message</span></span>

<span data-ttu-id="69b2c-105">Définit la liste d’images que le contrôle ToolBar utilisera pour afficher les boutons désactivés.</span><span class="sxs-lookup"><span data-stu-id="69b2c-105">Sets the image list that the toolbar control will use to display disabled buttons.</span></span>

## <a name="parameters"></a><span data-ttu-id="69b2c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69b2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69b2c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="69b2c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="69b2c-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="69b2c-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="69b2c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="69b2c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69b2c-110">Handle de la liste d’images qui sera définie.</span><span class="sxs-lookup"><span data-stu-id="69b2c-110">Handle to the image list that will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69b2c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="69b2c-111">Return value</span></span>

<span data-ttu-id="69b2c-112">Retourne le handle de la liste d’images utilisée précédemment pour afficher les boutons désactivés, ou **null** si aucune liste d’images n’a été définie précédemment.</span><span class="sxs-lookup"><span data-stu-id="69b2c-112">Returns the handle to the image list previously used to display disabled buttons, or **NULL** if no image list was previously set.</span></span>

## <a name="requirements"></a><span data-ttu-id="69b2c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69b2c-113">Requirements</span></span>



| <span data-ttu-id="69b2c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69b2c-114">Requirement</span></span> | <span data-ttu-id="69b2c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="69b2c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69b2c-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69b2c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="69b2c-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69b2c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="69b2c-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69b2c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="69b2c-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69b2c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="69b2c-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="69b2c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="69b2c-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="69b2c-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





